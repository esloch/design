# Variables


This chapter will present how different languages implements variables (in high level), their rules and conventions.

Points of interesting:

- variable name
- type annotation/declaration
- constant/immutable and mutable variables
- ownership

Finally, a example is presented to illustrate how the variable should be created for each programming language.

**Extra references:**

- https://en.wikipedia.org/wiki/Immutable_object

## C++

### Variable name

In **C++**, the variable name should be a valid **C++** indentifier.

According to [cplusplus.com][cplusplus-variables]

> A valid identifier is a sequence of one or more letters, digits, or underscore characters (_). Spaces, punctuation marks, and symbols cannot be part of an identifier. In addition, identifiers shall always begin with a letter. They can also begin with an underline character (_), but such identifiers are -on most cases- considered reserved for compiler-specific keywords or external identifiers, as well as identifiers containing two successive underscore characters anywhere. In no case can they begin with a digit.
>
> C++ uses a number of keywords to identify operations and data descriptions; therefore, identifiers created by a programmer cannot match these keywords. The standard reserved keywords that cannot be used for programmer created identifiers are:
>
> alignas, alignof, and, and_eq, asm, auto, bitand, bitor, bool, break, case, catch, char, char16_t, char32_t, class, compl, const, constexpr, const_cast, continue, decltype, default, delete, do, double, dynamic_cast, else, enum, explicit, export, extern, false, float, for, friend, goto, if, inline, int, long, mutable, namespace, new, noexcept, not, not_eq, nullptr, operator, or, or_eq, private, protected, public, register, reinterpret_cast, return, short, signed, sizeof, static, static_assert, static_cast, struct, switch, template, this, thread_local, throw, true, try, typedef, typeid, typename, union, unsigned, using, virtual, void, volatile, wchar_t, while, xor, xor_eq

Another point important here is that C++ language is a "case sensitive" language, so an identifier written in capital letters is not equivalent to another one with the same name but written in small letters.

C++ doesn't have strict naming convention, instead there is some recomendations that can be checked at the [C++ Core Guidelines][isocpp-naming]. These are the current points mentioned by this guideline:

Naming and layout rules:

- NL.1: Don’t say in comments what can be clearly stated in code
- NL.2: State intent in comments
- NL.3: Keep comments crisp
- NL.4: Maintain a consistent indentation style
- NL.5: Avoid encoding type information in names
- NL.7: Make the length of a name roughly proportional to the length of its scope
- NL.8: Use a consistent naming style
- NL.9: Use ALL_CAPS for macro names only
- NL.10: Prefer underscore_style names
- NL.11: Make literals readable
- NL.15: Use spaces sparingly
- NL.16: Use a conventional class member declaration order
- NL.17: Use K&R-derived layout
- NL.18: Use C++-style declarator layout
- NL.19: Avoid names that are easily misread
- NL.20: Don’t place two statements on the same line
- NL.21: Declare one name (only) per declaration
- NL.25: Don’t use void as an argument type
- NL.26: Use conventional const notation

### Type Annotation/Declaration

...

### Constant and Mutable Variables

...

### Ownership

...

### Examples

...

### References

[cplusplus-variables]: http://www.cplusplus.com/doc/tutorial/variables/
- http://www.cplusplus.com/doc/tutorial/variables/

[isocpp-naming]: http://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines#S-naming
- http://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines#S-naming


## C-Sharp

### Variable Name

...

### Type Annotation/Declaration

...

### Constant and Mutable Variables

...

### Ownership

...

### Examples

...

### References

...

## Go

### Variable Name

...

### Type Annotation/Declaration

...

### Constant and Mutable Variables

...

### Ownership

...

### Examples

...

### References

...

## Godot

### Variable Name

...

### Type Annotation/Declaration

...

### Constant and Mutable Variables

...

### Ownership

...

### Examples

...

### References

...


## Java

### Variable Name

...

### Type Annotation/Declaration

...

### Constant and Mutable Variables

...

### Ownership

...

### Examples

...

### References

...


## JavaScript

### Variable Name

...

### Type Annotation/Declaration

...

### Constant and Mutable Variables

...

### Ownership

...

### Examples

...

### References

...


## Julia

### Variable Name

...

### Type Annotation/Declaration

...

### Constant and Mutable Variables

...

### Ownership

...

### Examples

...

### References

...


## PHP

### Variable Name

...

### Type Annotation/Declaration

...

### Constant and Mutable Variables

...

### Ownership

...

### Examples

...

### References

...


## Python

##### Object Identity
In Python, every object that is created is given a number that uniquely identifies it. It is guaranteed that no two objects will have the 
same identifier during any period in which their lifetimes overlap. Once an object’s reference count drops to zero and it is garbage collected, 
as happened to the 300 object above, then its identifying number becomes available and may be used again.

```
The built-in Python function id() returns an object’s integer identifier. Using the id() function, you can verify that two variables indeed point to the same object
```

### Variable Name

Officially, variable names in Python can be any length and can consist of uppercase and lowercase letters (A-Z, a-z), digits (0-9), 
and the underscore character *(_)*. An additional restriction is that, although a variable name can contain digits, the first character 
of a variable name cannot be a digit.

```
Note: One of the additions to Python 3 was full Unicode support, which allows for Unicode characters in a variable name as well. You will learn about Unicode in greater depth in a future tutorial.

```
The most commonly used methods of constructing a multi-word variable name are the last three examples:

- Camel Case: Second and subsequent words are capitalized, to make word boundaries easier to see. 
(Presumably, it struck someone at some point that the capital letters strewn throughout the variable name vaguely resemble camel humps.)  
*Example: numberOfCollegeGraduates*  
- Pascal Case: Identical to Camel Case, except the first word is also capitalized.  
*Example: NumberOfCollegeGraduates*  
- Snake Case: Words are separated by underscores.  
*Example: number_of_college_graduates*  

The Style Guide for Python Code, also known as PEP 8, contains Naming Conventions that list 
suggested standards for names of different object types. PEP 8 includes the following recommendations:

*Snake Case* should be used for functions and variable names.
*Pascal Case* should be used for class names. (PEP 8 refers to this as the “CapWords” convention.)  
#### Reserved Keywords
Keywords are the reserved words in Python.

We cannot use a keyword as a variable name, function name or any other identifier. They are used to define the syntax and structure of the Python language.

In Python, keywords are case sensitive.

There are 33 keywords in Python 3.7. This number can vary slightly over the course of time.

All the keywords except True, False and None are in lowercase and they must be written as they are. The list of all the keywords is given below.
|   |   |   |   |
|---|---|---|---|
False | await | else | import | pass |
None | break | except | in | raise |
True | class | finally | is | return |
and | continue | for | lambda | try |
as | def | from | nonlocal | while |
assert | del | global | not | with |
async | elif | if | or | yield |

### Global Variable Names
(Let's hope that these variables are meant for use inside one module only.) The conventions are about the same as those for functions.

Modules that are designed for use via from M import * should use the *\__all__* mechanism to prevent exporting globals, or use the older convention of prefixing such globals with an underscore (which you might want to do to indicate these globals are "module non-public").

### Function and Variable Names
Function names should be lowercase, with words separated by underscores as necessary to improve readability.

Variable names follow the same convention as function names.

**mixedCase** is allowed only in contexts where that's already the prevailing style (e.g. threading.py), to retain backwards compatibility.

### Function and Method Arguments
Always use self for the first argument to instance methods.

Always use cls for the first argument to class methods.

If a function argument's name clashes with a reserved keyword, it is generally better to append a single trailing underscore 
rather than use an abbreviation or spelling corruption. Thus class_ is better than clss. (Perhaps better is to avoid such clashes by using a synonym.)

### Method Names and Instance Variables
Use the function naming rules: lowercase with words separated by underscores as necessary to improve readability.

Use one leading underscore only for non-public methods and instance variables.

To avoid name clashes with subclasses, use two leading underscores to invoke Python's name mangling rules.

Python mangles these names with the class name: if class Foo has an attribute named *\__a*, it cannot be accessed by *Foo.\__a.* 
(An insistent user could still gain access by calling *Foo._Foo__a.*) Generally, double leading underscores should be used only to avoid name 
conflicts with attributes in classes designed to be subclassed.

Note: there is some controversy about the use of *\__names*.

### Constants
Constants are usually defined on a module level and written in all capital letters with underscores separating words. 
Examples include MAX_OVERFLOW and TOTAL.

### Type Annotation/Declaration

2.21 *Type Annotated Code*
You can annotate Python 3 code with type hints according to [PEP-484](https://www.python.org/dev/peps/pep-0484/), and type-check the code at build time with a type checking tool like pytype.

Type annotations can be in the source or in a stub pyi file. Whenever possible, annotations should be in the source. Use pyi files for third-party or extension modules.

2.21.1 *Definition*
Type annotations (or “type hints”) are for function or method arguments and return values:

```def func(a: int) -> List[int]:```
You can also declare the type of a variable using similar PEP-526 syntax:

``` a: SomeType = some_func()```
Or by using a type comment in code that must support legacy Python versions.

```a = some_func()```  # type: SomeType


### Constant and Mutable Variables

...

### Ownership

...

### Examples

...

### References

https://google.github.io/styleguide/pyguide.html#316-naming  
https://realpython.com/python-variables/
https://www.programiz.com/python-programming/keywords-identifier
https://www.python.org/dev/peps/pep-0008/#naming-conventions  

## R

### Variable Name

...

### Type Annotation/Declaration

...

### Constant and Mutable Variables

...

### Ownership

...

### Examples

...

### References

...

## Rust

### Variable Name

...

### Type Annotation/Declaration

...

### Constant and Mutable Variables

...

### Ownership

...

### Examples

...

### References

...

## TypeScript

### Variable Name

...

### Type Annotation/Declaration

...

### Constant and Mutable Variables

...

### Ownership

...

### Examples

...

### References

...
