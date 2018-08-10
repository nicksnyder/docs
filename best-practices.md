# Best practices

An assortment of what I consider to be engineering best practices.

## Architecture

### Don't build something before you need it

If you try to anticipate the future too much, you will be wrong and will have wasted time building something that isn't what you actually needed.

### Build the simplest thing that works

Build something, launch, then iterate based on real usage/feedback/data.

Understand how your system might need to evolve in the future, but don't try to theorycraft the perfect architecture/product from the beginning.

### Use tech that you are familiar with

> Better the devil you know than the devil you don't

Don't incur a huge risk using an unproven tech unless you have a very very good reason. When faced with a choice, the boring option is frequently the correct one. Aspirational tech is rarely a good idea.

### API is more important than implementation

Implementation is easy to change. API's are not.

Good APIs are also easier to understand and use.

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

### Test your code when it helps you

Code is worth testing if...
- Tests help you verify that your implementation is correct when you are writing it.
- The code keeps breaking and you are spending a lot of time maintaining it.
- The correctness of the code is of particular importance to your application or business (e.g. security).
- You are writing code on a team.

### Write idiomatic code

Whatever language you are writing in, write it like everyone else writes it.

## Code review

### Get your code reviewed because it helps you and it helps your team

Getting feedback on your code helps you learn how to write better code. It also helps your team fix and extend your code in the future without breaking it.

### Code reviews should be an appropriate size

Code reviews should be the smallest possible diff that makes sense (sometimes this can still be fairly large). If you need to do multiple things, split it up into multiple changes that can be reviewed independently.

### Review code because it helps you and it helps your team

Reviewing code is like traveling. It exposes you to new ideas that make you a well rounded engineer.

Reviewing good code will help you understand what makes code good.
Reviewing bad code will help you understand what makes code bad.

A good code review evaluates
* Correctness
  * Is this the right solution to the problem?
  * Are there any defects?
* Readability
  * Is the code easy to understand?

### Be humble

If you don't understand something, ask for clarification. Either you will learn something or the author will realize that they don't know the answer either. In the former case more documentation may be appropriate; in the latter case there is probably an improvement to the code that could be made.

If you would do something differently, propose an alternative and see what the author thinks. Maybe the author already considered your idea and had a reason to not prefer it, or maybe they didn't.

### Be helpful

You job is to understand and to help improve the code.

### Don't be a gatekeeper

Your job is not to ensure that the code is perfect.
Your job is not to ensure that the code is the way you would write it.

### Don't be a tool

Don't do the job that an automated tool should do. It is a waste of everyone's time. If you are spending time making lint comments in code reviews, invest that time adding automated lint tools instead.

### Don't spend more time discussing something than it would take to fix

Instead of suggesting a fix to code, just make the change yourself.

If there are two ways to do something, and it is easy to switch between them, then it doesn't matter what you choose the first time (you can switch later).

### Small incremental improvements are good

Don't fault the author for not fixing things with code they might be touching. Sometimes untangling code quickly snowballs into a large change which would derail the author from their original intent. If you notice an unrelated problem during code review, politely ask the author to add a TODO for the problem you identified.

### Trust the author by default

As a reviewer, you don't know all the tradeoffs that author took into account when making their change. Assume there are reasons. It is ok to ask what those reasons are. If you disagree with those reasons, remember to [choose your battles](#Choose-your-battles) and [don't spend too much time disagreeing](Don't-spend-more-time-discussing-something-than-it-would-take-to-fix).

### Choose your battles

Code is never perfect, and code someone else writes will usually be different than how you would write it. If you comment on everything you would do differently you are going to burn a lot of time and relationships. Focus on what is important.

## Personal development

### Solve problems, don't create them

Your job is to solve problems. Pointing out a problem is just the first step. The second, and more important, step is to propose a solution.

Adversarial and exhausting:
- "Don't do X"
- "We can't do X because Y"

Collaborative and productive:
- "Y would be better than X because Z"
- "If we do X we also need to do Z because Y"

### Learn new programming languages

Learning new programming languages increases your literacy and exposes you to more concepts that are useful in any programming language.

### Listen

You learn by listening, not by talking. Optimize for learning. 

Added bonus: if you talk infrequently, others will listen more when you do.

### Spend as much time as possible with people who you admire

Learn from the best. Observe their behavior. Emulate them.
