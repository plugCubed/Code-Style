## JavaScript Style Guide

 * [Spacing](#spacing)
  * [Objects](#objects)
  * [Array and Function calls](#array-and-function-calls)
  * [Multi-line Statements](#multi-line-statements)
  * [Chained Method Calls](#chained-method-calls)
  * [Full File Closures](#full-file-closures)
 * [Equality](#equality)
 * [Type Checks](#type-checks)
 * [Comments](#comments)
 * [Quotes](#quotes)
 * [Semicolons](#semicolons)
 * [Naming Conventions](#naming-conventions)
  * [AMD Modules](#amd-modules)
 * [Switch Statements](#switch-statements)

### Spacing

* Indentation with 4 spaces.
* No whitespace at the end of line or on blank lines.
* `if`/`else`/`for`/`while` do not need to have braces if it's scope content is on one line.
* `try` always have braces and go on multiple lines.
* The `?` and `:` in a ternary conditional must have space on both sides.

#### Objects

Objects declarations must be one property per line.
Property names only need to be quoted if they are reserved words or contain special characters.

#### Array and Function calls

Never include extra spaces around elements and arguments.

#### Multi-line Statements

When a statement is too long to fit on one line, line breaks must occur after an operator.

Lines should be broken into logical groups if it improves readability, such as splitting each expression of a ternary operator onto its own line even if both will fit on a single line.

#### Chained Method Calls

When a chain of method calls is too long to fit on one line, there must be one call per line, with the first call on a separate line from the object the methods are called on.
If the method changes the context, an extra level of indentation must be used.

#### Full File Closures

When a entire file is wrapped in a closure / AMD wrapper, the body of the closure is indented.

## Equality

Strict equality checks (`===`) must be used in favor of abstract equality checks (`==`).
The only exception is when checking for `undefined` and `null` by way of `null`.

## Type Checks

 * String ```typeof object === 'string'```
 * Number ```typeof object === 'number'```
 * Boolean ```typeof object === 'boolean'```
 * Object ```typeof object === 'object'```
 * Plain Object 
  * jQuery in browser ```$.isPlainObject(object)```
  * Node.JS ```a```
 * Function 
  * jQuery in browser ```$.isFunction(object)```
  * Node.JS ```typeof object === 'function'```
 * Array 
  * jQuery in browser ```$.isArray(object)```
  * Node.JS ```util.isArray(object)```
 * null ```object === null```
 * null or undefined ```object == null```
 * undefined
  * Global variables ```typeof object === 'undefined'```
  * Local variables ```object === undefined```
  * Properties ```object.prop === undefined```

## Comments

Comments are always preceded by a blank line.
Comments start with a capital first letter and don't require a period at the end.
There must be a single space between the comment token and the comment text.

Single line comments go over the line they refer to.

## Quotes

The plug³ Team uses single quotes.

## Semicolons

Always use semicolons.

## Naming Conventions

Variable and function names should be full words, using camel case with a lowercase first letter.
Names should be descriptive but not excessively so.
Exceptions are allowed for iterators, such as the use of `i` to represent the index in a loop.

### AMD Modules

All parts of the module name must be with lowercase first letter, except the last part which must be a uppercase first letter.

## Switch Statements

Only use `switch` statements if there are a large number of cases or when fall-through would give an advantage.

When using `switch` statements:
 * Use a `break` or `return` for each case other than `default`.
 * Indent `case` statements from the `switch` statement.

----------
A lot of the guidelines are inspired heavily from the [jQuery Javascript Style Guide](http://contribute.jquery.org/style-guide/js/)