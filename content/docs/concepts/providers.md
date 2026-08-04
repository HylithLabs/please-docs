---
title: Providers
weight: 2
---

please works with three AI providers. You pick one during setup and can change your mind later.

<!--more-->

## Supported providers

Anthropic (Claude), Google (Gemini), and OpenAI (ChatGPT).

## Model selection

please auto picks the cheapest model your API key has access to, so there is no need to know model names or pricing tiers. You can decline the pick during setup and type a specific model id yourself if you would rather choose.

The model is selected once at setup, not re selected on every call, and it heals itself on failure rather than needing you to intervene.

## Saving keys

Keys are saved globally to `~/.please/config` and apply to every project on the machine, not per repository. You can save keys for more than one provider at once. Adding a second one never overwrites the first.

Switch the active provider, change a saved provider's model, or remove a saved key any time by running please setup again.

## Adding new providers

The tool calling conversation that powers agent mode is represented in provider neutral terms internally. Only a small adapter per provider translates that to and from its own wire format. This is what lets please add support for a new provider without touching the agent loop itself.

{{< cards >}}
  {{< card link="../../getting-started/setup" title="Setup" subtitle="Run please setup to connect a provider" icon="settings" />}}
{{< /cards >}}
