---
title: C# 10 in a Nutshell
bookauthor: Joseph Albahari
date: 2022-09-25
header:
  teaser: /images/c-sharp-10-nutshell.jpeg
quotes:
  - date: 2022-09-25
    chapter: 3. Creating Types in C#
    quote: "Boxing is the act of converting a value-type instance to a reference-type instance"
  - date: 2022-09-25
    chapter: 3. Creating Types in C#
    quote: "If a constructor in a subclass omits the base keyword, the base type’s parameterless constructor is implicitly called"
  - date: 2022-09-25
    chapter: 3. Creating Types in C#
    quote: "From C# 9, you can override a method (or property get accessor) such that it returns a more derived (subclassed) type. "
  - date: 2022-09-25
    chapter: 3. Creating Types in C#
    quote: "this approach makes versioning difficult, in that adding an optional parameter to the constructor at a later date breaks binary compatibility with consumers (whereas adding a new init-only property breaks nothing)."
  - date: 2022-09-24
    chapter: 3. Creating Types in C#
    quote: "A deconstructor (also called a deconstructing method) acts as an approximate opposite to a constructor&#58; whereas a constructor typically takes a set of values (as parameters) and assigns them to fields, a deconstructor does the reverse and assigns fields back to a set of variables."
  - date: 2022-09-24
    chapter: 3. Creating Types in C#
    quote: "Whether a parameter is pass-by-value or pass-by-reference is also part of the signature"
  - date: 2022-09-24
    chapter: 3. Creating Types in C#
    quote: "the following pairs of methods cannot coexist in the same type, because the return type and the params modifier are not part of a method’s signature"
  - date: 2022-09-24
    chapter: 3. Creating Types in C#
    quote: "A constant can serve a similar role to a static readonly field, but it is much more restrictive—both in the types you can use and in field initialization semantics. A constant also differs from a static readonly field in that the evaluation of the constant occurs at compile time"
  - date: 2022-09-24
    chapter: 2. C# Language Basics
    quote: "Extern aliases allow your program to reference two types with the same fully qualified name (i.e., the namespace and type name are identical). This is an unusual scenario and can occur only when the two types come from different assemblies. "
  - date: 2022-09-24
    chapter: 2. C# Language Basics
    quote: "From .NET 6, project files allow for implicit global using directives. If the Implici⁠t​Usings element is set to true in the project file (the default for new projects), the following namespaces are automatically imported&#58;
    System
    System.Collections.Generic
    System.IO
    System.Linq
    System.Net.Http
    System.Threading
    System.Threading.Tasks
    Additional namespaces are imported, based on the project SDK (Web, Windows Forms, WPF, and so on)"
  - date: 2022-09-24
    chapter: 2. C# Language Basics
    quote: "You can also switch on multiple values (the tuple pattern)&#58;"
  - date: 2022-06-12
    chapter: 2. C# Language Basics
    quote: "The ??= operator (introduced in C# 8) is the null-coalescing assignment operator. It says, “If the operand to the left is null, assign the right operand to the left operand.”"
  - date: 2022-06-01
    chapter: 2. C# Language Basics
    quote: "decrementing the minimum possible int value results in the maximum possible int value&#58;"
  - date: 2022-06-01
    chapter: 2. C# Language Basics
    quote: "You can insert an underscore anywhere within a numeric literal to make it more readable&#58;"
---
## *{{page.bookauthor}}*

<img width="300" src="{{ page.header.teaser }}"/>

{% for quote in page.quotes reversed %}
#### {{ quote.date | date: '%B %d, %Y' }} {{ quote.chapter}}
{{ quote.quote }}
{% endfor %}
