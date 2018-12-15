# Coding Guide

## Practice

### YAGNI: You Arent Gonna Need It

#### Resources

[wiki.c2](http://wiki.c2.com/?YouArentGonnaNeedIt) 

@TODO fill in details

### Write it simple, dumb, plain, explicit the first time, then refactor

1. writing functions names very explicitly on what it's doing. if a function is doing four different things, write it out `doThisAndSendThatNotifcationAndCleanUpDataAndSave()`. Once it is done, then you can refactor. At this point, it is now very apparent what the function is doing. You can easily spot the responsibilities that should be split.

Iterative process. Follow simple guideline in each step. Write code -> refactor -> write code -> refactor. Then development becomes easy.

Focus on one thing at a time. Making it work vs Making it better.

We do it better when we focus on one thing at a time.

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

*explicitness* over *convenience*

### Code to make the intention clear

@TODO fill in details (encorporate quote at the bottom?)

### Careful with parameter default

In general, avoid having default for function parameters.
Having a parameter default needs to be an explicit decision, that provides actual value to the consumer of the function.
Defaults often lead to unexpected behavior, and is hard to debug, leaving the maintainer wondering "Why is this function working when it should not?" "From where am I getting this magical value?"

This ties to *Be explicit*.

Defaults can make sense in some cases. See more on [default-values-are-they-good-or-evil](https://softwareengineering.stackexchange.com/questions/63908/default-values-are-they-good-or-evil)

### On Testing

Always think about the value of the test. Be practical.

@TODO fill in details

### Avoid Double Negative

Avoid using double negative
If you don't have the function for the oppsite, create one.

`!isNil()` -> `exists()`

[Remove Double Negative](https://www.refactoring.com/catalog/removeDoubleNegative.html)

### If it's hard to do something, it usually means something is wrong

@TODO fill in details

examples include

naming

unit testing

### Quotes

> Bad code tries to do
too much, it has muddled intent and ambiguity of purpose. Clean code is focused. Each
function, each class, each module exposes a single-minded attitude that remains entirely
undistracted, and unpolluted, by the surrounding details.
>
> -- <cite>Robert C. Martin. *Clean Code: A Handbook of Agile Software Craftsmanship*</cite>

> I could list all of the qualities that I notice in
clean code, but there is one overarching quality
that leads to all of them. Clean code always
looks like it was written by someone who cares.
There is nothing obvious that you can do to
make it better. All of those things were thought
about by the code’s author, and if you try to
imagine improvements, you’re led back to
where you are, sitting in appreciation of the
code someone left for you—code left by someone
who cares deeply about the craft.
>
> Michael Feathers, author of *Working Effectively with Legacy Code*

> Duplication and expressiveness take me a very long way into what I consider clean
code, and improving dirty code with just these two things in mind can make a huge difference
>
> -- Ron Jeffries, author of *Extreme Programming Installed and Extreme Programming Adventures in C#*
