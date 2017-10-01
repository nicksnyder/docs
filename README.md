# Style guide

An assortment of learnings for what I think it means to be a good engineer.

## Architecture

### Don't build something before you need it

If you try to anticipate the future too much, you will be wrong and will have wasted time building something that isn't what you actually needed.

### Build the simplest thing that works

Build something, launch, then iterate based on real usage/feedback/data.

Don't try to theorycraft the perfect architecture/product from the beginning.

### Use tech that you are familiar with

> Better the devil you know than the devil you don't

Don't incur a huge risk using an unproven tech unless you have a very very good reason. When faced with a choice, the boring option is frequently the correct one. Aspirational tech is rarely a good idea.

### API is more important than implementation

Implementation is easy to change. API's are not.

Good APIs are also easier to understand and use.

## Code review

### Review code because it helps you learn

Reviewing code is like traveling. It exposes you to new ideas that make you a well rounded engineer.

Reviewing good code will help you understand what makes code good.
Reviewing bad code will help you understand what makes code bad.

### Ask for your code to be reviewed because it helps you learn

Nobody writes perfect code. It is useful to get a second opinion to see which parts of your code are hard to understand.

### Ask, don't tell (be humble)

If you don't understand something, ask for clarification. Either you will learn something or the author will realize that they don't know the answer either. In the former case more documentation may be appropriate; in the latter case there is probably an improvement to the code that could be made.

If you would do something differently, propose an alternative and see what the author thinks. Maybe the author already considered your idea and had a reason to not prefer it, or maybe they didn't.

### Understand the code you are reviewing

You job as a code reviewer is to understand and to help improve the code.

### Leave the linting to linters

Don't do the job that an automated tool should do. It is a waste of everyone's time. If you are spending time making lint comments in code reviews, invest that time adding automated lint tools instead.

## Code style

### Compile your code

Type safety is worth it.

### Complicated type systems don't scale to teams

A simple type system is sufficient. Languages with more pedantic type systems may be appropriate in very specific situations, but sacrifice readability and accessibility in a team setting.

### Optimize for human readability

Make the purpose of your code obvious to the reader. Assume the reader is inexperienced.

Code that is readable is easier to update and easier to fix, especially by someone who was not the original author.

All else equal, fewer lines of code is better, up until a point. Past that point code becomes too dense to read fluently. Don't pass that point.

### Document your code for humans (not for machines)

Write documentation in prose. Explain WHAT (the end goal) and WHY. The code itself is the HOW.

Not everything needs to be documented, but many things do. If a function is short enough and well named it doesn't need to be documented.

### Format your code

It doesn't matter what the format it, just that the formatting is consistent.

If you don't have an autmatic formatter (you should), match the formatting of the codebase that you are contributing to.

### Be kind to your reviewer

Changes should be small and do one thing. If you need to do multiple things, split it up into multiple changes that can be reviewed independently.

### Test your code when it helps you

|  | Easy to test | Hard to test |
|--|--------------|--------------|
| **Worth testing** | Do it. | If you have time. |
| **Not worth testing** | Don't do it. | Don't do it. |

Code is worth testing if...
- Tests help you verify that your implementation is correct when you are writing it.
- The code keeps breaking and you are spending a lot of time maintaining it.
- The correctness of the code is of particular importance to your application.

### Write idiomatic code

Whatever language you are writing in, write it like everyone else writes it.

## Personal development

### Solve problems, don't create them

Your job is to solve problems. Pointing out a problem is just the first step. The second, and more important, step is to propose a solution.

Junior
- "Don't do X"
- "We can't do X because Y"

Senior
- "Don't to X, do Y instead"
- "If we do X we also need to do Z because Y"

The former is adversarial and exhausting. The latter is collaborative and productive.

### Learn new programming languages

Learning new programming languages increases your literacy and exposes you to more concepts that are useful in any programming language.

### Listen

You learn by listening, not by talking. Optimize for learning. 

Added bonus: if you talk infrequently, others will listen more when you do.

### Spend as much time as possible with people who you admire

Learn from the best. Observe their behavior. Emulate them.
