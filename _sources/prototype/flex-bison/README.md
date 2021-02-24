The example code here was based on the article wrote by Evan Typanski, available at:
https://dev.to/evantypanski/writing-a-simple-programming-language-from-scratch-part-1-54a2

Here are some information extracted from the same article:

> Additional Resources
>
> If you happen to want more info on anything covered here, > I've linked some stuff to get started. I went right over a > lot, so this is my chance to show you how to dive into > those topics.
>
> Flex codebase: https://github.com/westes/flex - the lexical > analysis tool we used.
> Bison documentation: https://www.gnu.org/software/bison/ - > the parser generator we used. Awesome documentation here.
> LALR parsing: https://web.cs.dal.ca/~sjackson/lalr1.html - > a well made explanation on how LALR(1) parsers (like what > Bison generates!) work.
> Resolving parsing conflicts: http://www.cs.ecu.edu/karl/> 5220/spr16/Notes/Bottom-up/conflict.html - how to fix shift/> reduce or reduce/reduce conflicts, like the one we saw > before.
> Chomsky hierarchy: https://en.wikipedia.org/wiki/> Chomsky_hierarchy - didn't go much in detail about this, > but we were using a context-free grammar so Bison can > compile it. If you want context sensitivity, that's for > later phases.
> Symbol table: https://www.tutorialspoint.com/> compiler_design/compiler_design_symbol_table.htm - using > symbol tables, how compilers deal with variables.
>

Also, at the same article, an user (Harvey Thompson) add some comments there:

> * Programming Languages: An Interpret Based Approach - Samel N Kamin - this isn't a well known book, but it totally re-ignited my interest. This book goes through various languages and their features and builds interpreters for them (in Pascal, it's an old book).
> * LLVM: Writing a Simple Programming Language - a step by step C++ tutorial on how to build a compiled language (using LLVM). You should basically use LLVM for the back-end, since that will save you hundreds of man-years of work and is open source. It's a well solved problem that is totally applicable to anything anyone can build. Clang is the C/C++/ObjectiveC front-end.
> * Types and Programming Languages: Benjamin C Pierce - this is perhaps heavy mathematically, however you can skip those parts and still understand the concepts. If you want to properly understand type systems and do it properly, this book has it all. New languages like Scala, Kotlin, Swift (and others such as Typescript) are beginning to include things like set-theoretic type systems (optionals, unions, intersections). This book has been incredibly influential for myself, and will lead you down many good rabbit holes.
