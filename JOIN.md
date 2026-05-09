# How to join Microsoft SE Team

## TL;DR

1. Open an Issue on this repo with the `join-request` label
2. Operator (@kody-w) reviews + adds you as a collaborator on the private companion
3. You're in

## Detailed flow

### Step 1 — open the join request

[**Click here to open a new join-request Issue**](https://github.com/kody-w/microsoft-se-team-neighborhood/issues/new?labels=join-request&title=join-request:%20%3Cyour-handle%3E&body=Hi%20kody-w%20%E2%80%94%20I'd%20like%20to%20join%20the%20Microsoft%20SE%20Team%20neighborhood.%0A%0A**My%20GitHub%20handle:**%20@your-handle%0A**My%20role%20at%20MS:**%20...%0A**Why%20I'd%20like%20access:**%20...)

Provide:

- Your GitHub handle (so the operator knows whom to add)
- Your role at Microsoft (SE? PM? Eng? Customer-facing?)
- A sentence on why you want access (current customer engagement / shared project / general collab)

### Step 2 — operator approval

@kody-w reviews + runs:

```bash
gh api -X PUT /repos/kody-w/microsoft-se-team-neighborhood-private/collaborators/<your-handle> -f permission=push
```

You'll get a GitHub email inviting you to accept.

### Step 3 — accept + start working

Accept the invite, then clone the private companion:

```bash
gh repo clone kody-w/microsoft-se-team-neighborhood-private
```

Drop work-items, comment on others', open PRs. The workspace flow uses three labels:

- `workspace-todo` — open work, assignable
- `workspace-in-progress` — claimed by someone, durable assignment
- `workspace-done` — artifact landed, consumable by other members

## What if I'm not Microsoft SE?

Open an Issue anyway. The operator may add you as a guest contributor for a specific project, OR redirect you to a more appropriate neighborhood (public-art-collective, braintrust-template, etc.).
