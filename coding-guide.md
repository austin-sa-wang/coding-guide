# Coding Guide

## Practice

### YAGNI: You Arent Gonna Need It

#### Resources

[wiki.c2](http://wiki.c2.com/?YouArentGonnaNeedIt) 

@TODO fill in details

### Keep the code simple

Unnecessary complexity is a form of technical debt.
  - more code means more poossible bugs
  - more things to maintain
  - more codes to read for the maintainer

@TODO fill in details

### Code is meant to be read by another human

@TODO fill in details

### Be explicit

@TODO fill in details

### Careful with parameter default

In general, avoid having default for function parameters.
Having a parameter default needs to be an explicit decision, that provides actual value to the consumer of the function.
Defaults often lead to unexpected behavior, and is hard to debug, leaving the maintainer wondering "Why is this function working when it should not?" "From where am I getting this magical value?"

In general, explicitness over convenience.

Defaults can make sense in some cases. See more on [default-values-are-they-good-or-evil](https://softwareengineering.stackexchange.com/questions/63908/default-values-are-they-good-or-evil)

### On Testing

Always think about the value of the test. Be practical.

@TODO fill in details

### Avoid Double Negative

Avoid using double negative
If you don't have the function for the oppsite, create one.

`!isNil()` -> `exists()`

[Remove Double Negative](https://www.refactoring.com/catalog/removeDoubleNegative.html)
