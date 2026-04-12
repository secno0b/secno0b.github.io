# Dependabot gave you an A. You’re still exposed

We recently looked at a portfolio of around 230 repositories.

On paper, everything looked fine.  
Dependabot grades were solid. Most repos were sitting at an A.

Then we actually looked at the dependencies.

Over 2,000 packages were more than 1,000 days stale.

That is not a small gap. That is years of drift.

## The problem with “green”

Tools like Dependabot are useful, but they optimize for visibility, not reality.

If alerts are resolved and PRs are managed, you get a good score.  
That does not mean your dependencies are current.

It just means nothing is actively screaming.

## What we found

When we broke it down:

- Thousands of packages were outdated beyond a year  
- Core libraries like typescript and eslint showed up across dozens of repos  
- Legacy packages were sitting untouched because they were “not breaking anything”  

From a dashboard perspective, everything looked healthy.

From a risk perspective, it was not.

## Why this happens

A few reasons:

- Teams prioritize feature work over dependency upgrades  
- Small upgrades get delayed until they become big upgrades  
- No one owns dependency health across the portfolio  
- Tooling gives a false sense of completion  

## What actually works

Instead of chasing alerts, we changed the approach:

1. Start with low effort updates  
   Dev tooling, minor version bumps, anything that doesn’t break builds  

2. Identify repeat offenders  
   Packages that show up across multiple repos and fix them in batches  

3. Track staleness, not just alerts  
   Time since last update is a better signal than open PR count  

4. Make ownership visible  
   Tie repos and packages to owners so it’s not “someone else’s problem”  

## The takeaway

A clean dashboard does not mean a secure system.

If you are not measuring how far behind you are, you are not measuring risk.

And if nobody owns it, it will stay that way.
