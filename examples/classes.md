```fenix
"""
notes:
- It needed to use explicitly the `from/import` statement. It is not possible
  to use just the `import` statement (as used by Python).
- Built-in modules and functions should be imported explicitly from
  `__core__`.
- line caracters limit: 79
- class visibility is related to the module.

"""
from __core__.io import file

from package_a import lib_a.module_b as mod_b
from package_b import (
  lib_a,
  lib_b,
  lib_c,
  lib_d,
  lib_e2 as lib_e
)

# function default visibility: public
public function log(message: string):
  """
  title: Store a message into a log file.

  parameters:
    - message: A message text for the log
  """
  with file.open("/tmp/log.txt") as f:
    f.write(message)



class Base -> public:
  """
  title: The Base class aims to organize a simple and util set of attributes
    and methods to be reused for derived classes.

  notes:
    - Default visibility for attributes: public
    - Default access type for attributes: mutable
    - For private and protected attributes it is optional the usage
      of a `_` as prefix, e.g. `_attr1` or `_attr2`. Maybe it can
      help to improve the code readability.

  attributes:
    - _attr1: Attribute used as a first attribute
    - _attr2: Attribute used as a second attribute
    - attr3: Attribute used as a third attribute
  """

  attributes:
    _attr1: private Nullable[int]
    _attr2: protected mutable float
    attr3: public constant string = "default"

  methods:
    default visibility for methods: public
    __init__(
      attr1: Nullable[int],
      attr2: mutable float,
      attr3: constant string = "default2"
    ):
      """
      title: Initialize the Base instance.

      parameters:
        - attr1: The first parameter.
        - attr2: The second parameter.
        - attr3: The third parameter.

      notes:
        - if at the end of __init__, self.attr1 is not defined, it
          will assume `Null`
        - if at the end of __init__, self.attr2 is not defined, an
          error is raised.
        - if at the end of __init__, self.attr3 is not defined, it
          will assume `"default"` string.

      """
      self.arg1 = self.arg1
      self.arg2 = self.arg2
      self.arg3 = self.arg3

    public add(number1: int, number2: int) -> int:
      """
      title: Add two integer and return the result.

      parameters:
        - number1: The first number for the addition operation.
        - number1: The second number for the addition operation.

      return: The result of the addition between number1 and number2.
      """
      return number1 + number2


class Derived(Base) -> public:
  attributes:
    attr4: public datetime

  methods:
    __init__(
      attr1: Nullable[int],
      attr2: mutable float,
      attr3: constant string = "default2",
      attr4: datetime
    ):
      """
      title: Initialize the Derived class.

      parameters:
        - attr1: The first parameter.
        - attr2: The second parameter.
        - attr3: The third parameter.
        - attr4: The forth attribute
      """
      self.__base__[Base].__init__(attr1, attr2, attr3)
      self.attr4 = attr4

    public sub(number1: int, number2: int) -> int:
      """
      title: Subtract two integer and return the result.

      parameters:
        - number1: The first number for the subtraction operation.
        - number1: The second number for the subtraction operation.

      return: The result of the addition between number1 and number2.
      """
      return number1 + number2

    private _update_attr4():
      self.attr4 = datetime.now()

```
