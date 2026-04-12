# Azure Policy looks good on paper. Then reality hits

We started with a list of over 50 Azure policies.

On paper, it made sense.  
Strong controls. Aligned with security guidance. Covered all the right areas.

Then we tried to apply them to real systems.

We ended up with around 30.

## What changed

A big chunk of policies didn’t survive contact with reality.

Some would break existing architecture.  
Some were not enforceable at the platform level.  
Some overlapped or conflicted with each other.  
Some went beyond what was actually required.

This is the part most discussions skip.

## The enforcement problem

There is always pressure to move from audit to deny.

In theory, that makes sense.  
In practice, it can break production workloads.

Examples:

- Blocking public network access when integrations depend on it  
- Enforcing authentication patterns that upstream systems don’t support  
- Applying controls that assume a different architecture than what exists  

You end up choosing between compliance and functionality.

## What we actually did

We split policies into categories:

- Enforceable now  
- Audit only  
- Not applicable  

For some services, like API Management and Function Apps, certain controls stayed in audit mode because enforcing them would break integrations.

Not ideal, but realistic.

## The gap

Azure Policy is powerful, but it assumes your architecture aligns with the model it expects.

Real systems don’t always do that.

Especially when:
- You integrate with legacy systems  
- You depend on external partners  
- You inherit constraints you cannot change  

## The takeaway

Policies are not the goal.

Working, secure systems are.

If a policy breaks your system, the answer is not blindly enforcing it.

The answer is understanding why the gap exists and deciding what you are willing to accept.
