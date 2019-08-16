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
1. Issues should be broken down into samller problems that fit the contribution cadence resulting in child issues
1. Issues focus on defining the problem, not the solution
1. Each issue is fixed by a pull request
1. One issue, one feature branch, one pull request

## Commits

Commits should tell a story of the contributions made by the team. Anyone should be able to check the repository history and understand what is going on and what changes where introduced when. See Telling stories with your git history [post](https://about.futurelearn.com/blog/telling-stories-with-your-git-history) and [presentation](https://www.slideshare.net/joelchippindale/telling-stories-through-your-commits).

### Atomic commits

Large commits can be difficult to read, especially when they contain changes which are unrelated. **Atomic commits** are the smallest amount of code changed which delivers value.

### Commit messages

Explain why you’ve made the change in the first place. This is the perfect opportunity to reflect on what you’re doing and to provide context – whether it’s to satisfy a user requirement, to fix a bug or to make another change easier to make in the future.

```
Issue Reference - Short one line title.

Description of what the change does

An explanation of why the change is being made.

Optionally, a discussion of alternatives that were considered.
```

## Pull requests

1. Pull requests are used to track progress, discuss solutions and review code
1. Create the corresponding pull request for an issue as soon as possible and explicitly reference the issue in the pull request
1. Immediatly after creating the pull request, involve team members for reviewing even if there is yet nothing significant to review
1. With the pull request open and team members involved you can discuss solutions to the problem or request feedback as needed without waiting for the final solution
1. Pull requests with a lifespan bigger than the contribution cadence may indicate a problem (bad issue sizing, difficult problem, paralysis by analysis, ...)

## CI System

1. The minimum quality gate is proving the build does not break

