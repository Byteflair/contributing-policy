# Byteflair code contribution policy

## Trunk based developement

We use [trunk based development](https://trunkbaseddevelopment.com/). This means, in summary:

1. One master repository with a single branch, the trunk, that is regularly deployed to production
1. Trunk is always releasable
1. Trunk contains work in progress
1. The team regularly contributes incremental code to the trunk in a contribution candence of no more than a couple of days
1. Developers work on forked repositories on feature branches whose life is determined by the contribution cadence
1. Code is shared with the team via pull requests
1. CI System ensures quality gates are met by the resulting merge of the trunk and a pull request
1. Pull requests that pass the quality gates are directly merged in the trunk in an automated way

## Issues

1. Issues define a problems to be solved
1. Issues should be split up into smaller problems that fit the contribution cadence resulting in child issues
1. Issues provide a discussion area to track the definition and break down of a problem, not its solution
1. Each issue is fixed by a pull request in a single purpose feature branch

By splitting up an issue, you not only reduce the pain of merging each branch, you also deliver value sooner and make your repository history more readable.

## Branches

We use single purpose feature branches. If a feature branch is delivering unrelated value or has multiple purposes, it indicates that the corresponding issue needs to be broken down.

## Commits

Commits should tell a story of the contributions made by the team. Anyone should be able to check the repository history and understand what is going on and what changes where introduced when. See Telling stories with your git history [post](https://about.futurelearn.com/blog/telling-stories-with-your-git-history) and [presentation](https://www.slideshare.net/joelchippindale/telling-stories-through-your-commits).

### Atomic commits

Large commits can be difficult to read, especially when they contain changes which are unrelated. **Atomic commits** are the smallest amount of code changed which delivers value.

### Commit messages

Explain why you’ve made the change in the first place. This is the perfect opportunity to reflect on what you’re doing and to provide context – whether it’s to satisfy a user requirement, to fix a bug or to make another change easier to make in the future.

Use the following template for commit messages.

```
Issue Reference - Short one line title.

Value delivered

Description of what the change does

An explanation of why the change is being made.

Optionally, a discussion of alternatives that were considered.
```

The first line should be used to explain the value of the changes, rather than focussing on the implementation details. It’s always useful to explain what you’ve changed and why you’ve changed it. In some cases, it also helps, to provide further context such as explaining alternative solutions you’ve ruled out or providing external references.

### Review history

When developing your code, you are bound to change direction or even make mistakes (most commonly introducing typos or bugs). 

Before you share your commit history, it’s important to think about what is useful information for someone else to read. You shouldn’t think of your Git history as a “truthful” log of what you worked on step-by-step. Just as we refactor code, we should refactor our commits before sharing them with others.

The power of Git makes it simple to re-order, reword and refactor your commits until they tell the clearest story possible.

Use `git rebase --interactive`.

## Pull requests

1. Pull requests are used to track progress, discuss solutions and review code
1. Pull requests reference the issue they provide a solution for
1. Create the corresponding pull request for an issue as you start working on the solution
1. Immediatly after creating the pull request, involve team members for reviewing even if there is yet nothing significant to review
1. With the pull request open and team members involved you can discuss solutions to the problem or request feedback as needed without waiting for the final solution
1. Pull requests with a lifespan bigger than the contribution cadence may indicate a problem (bad issue sizing, difficult problem, paralysis by analysis, ...)

## Code documentation

Avoid comments in code. The code documentation should be comprised of code meta data captured in the repository, issues and pull requests:

- From the code we can trace the commit that introduced that code which contains a reference to the issue and the value delivered by this contribution
- From the commit we can trace the issue to gather macro information about the problem it solves, giving further context to the commit
- From the issue we can trace the pull request to track the decisions made to come up with a specific solution completing the the context of the code

## CI System

The minimum quality gate is proving the build does not break

