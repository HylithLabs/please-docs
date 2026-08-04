---
title: Setup
weight: 2
---

Run setup once per machine to connect please to an AI provider.

<!--more-->

## Run setup

```bash
please setup
```

You pick a provider, Anthropic (Claude), Google (Gemini), or OpenAI (ChatGPT), and paste an API key.

## What happens during setup

please checks the key against the provider right away with a real, cheap call that lists available models. A typo gets caught immediately instead of failing confusingly on your first please commit. If the check fails, you get another try without restarting setup.

please then auto picks the cheapest model the key has access to, so you do not need to know model names or pricing tiers. You can decline the pick and type a specific model id yourself if you would rather choose.

Your choice is saved globally to `~/.please/config` and applies to every project on the machine.

## Multiple providers

You can save keys for more than one provider. Adding a second one never overwrites the first. You can switch which provider is active at any time, and change a saved provider's model later without entering its key again.

Run setup again and it shows what is already configured:

```text
Providers you have set up:
  * Anthropic (model: claude-haiku-4-5, key ending in ...ab12)
    Google (model: models/gemini-flash-lite-latest, key ending in ...hnxg)
  (* = active: this is what please uses right now)

What would you like to do?
  1) Add or update a provider
  2) Switch the active provider
  3) Change a provider's model
  4) Remove a saved provider
  5) Nothing, just checking
```

## Project context

On first use in a repo, please also generates a short project description cached at `.git/PLEASE.MD`, giving the AI context about the codebase.

{{< callout type="info" >}}
  Setup runs once per machine, not once per repo. The project description in `.git/PLEASE.MD` is the only thing generated per repository.
{{< /callout >}}
