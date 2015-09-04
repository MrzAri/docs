---
title: subtraction
tags:
  - JS
  - Basic
readiness: 'Ready to Use'
summary: 'Subtracts the value of one expression from another or provides unary negation of a single expression.'
uri: javascript/operators/subtraction

---
# subtraction

## Summary

Subtracts the value of one expression from another or provides unary negation of a single expression.

## Syntax

    result = number1 - number2 ;

**result**
:   Any numeric variable.

**number1**
:   Any numeric expression.

**number2**
:   Any numeric expression.

## Examples

``` {.js}
var x = 5;
var y = 7;
var z;
z = y - x; // result: z = 2
```

## Remarks

In Syntax 1, the **-** operator is the arithmetic subtraction operator used to find the difference between two numbers. In Syntax 2, the **-** operator is used as the unary negation operator to indicate the negative value of an expression.

For Syntax 2, as for all unary operators, expressions are evaluated as follows:

-   If applied to undefined or null expressions, a run-time error is raised.
-   Objects are converted to strings.
-   Strings are converted to numbers if possible. If not, a run-time error is raised.
-   Boolean values are treated as numbers (0 if false, 1 if true).

The operator is applied to the resulting number. In Syntax 2, if the resulting number is nonzero, result is equal to the resulting number with its sign reversed. If the resulting number is zero, result is zero.

## See also

### Other articles

-   [Subtraction Assignment Operator (-=)](/javascript/operators/subtraction_assignment)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/9ty8kw3w(v=vs.94).aspx)

