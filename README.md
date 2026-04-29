# hero-design-tokens

This repository is the single source of truth for HERO colour tokens.

It defines the colour system used across product, design and brand documentation. The goal is to ensure consistency, accessibility and reuse across all touchpoints.

## Purpose

This repository exists to:

- define primitive colour values
- define semantic colour roles
- document accessibility and usage rules
- provide a shared foundation for product, Figma libraries and the Brand Hub

## Source of truth

GitHub is the authoritative source for HERO colour tokens.

Figma libraries, frontend code and brand documentation should consume tokens from this repository. They should not define colour values independently.

If there is any mismatch between Figma, product code and the Brand Hub, this repository is the reference used to resolve it.

## Structure

- `tokens/colour/primitives.json`  
  Base colour scales and fixed values, such as brand, neutral, success, warning and error.

- `tokens/colour/semantic.json`  
  Semantic token roles such as text, background, border, action and feedback.

- `tokens/colour/rules.json`  
  Accessibility and usage rules, including contrast requirements, allowed combinations and state-specific constraints.

## Principle

Primitive tokens define what a colour is.

Semantic tokens define what a colour is used for.

Design and product should use semantic tokens wherever possible. Primitive tokens should only be used when creating or maintaining the token system itself.

## Figma usage

Figma is the primary design consumption layer for colour tokens.

Published Figma variables and libraries should reflect the tokens defined in this repository.

Changes to colour values or semantic roles should begin in this repository and then be propagated to Figma.

## Accessibility

All production colour usage should meet WCAG 2.2 AA requirements unless a stricter rule is specified.

Accessibility rules should cover:

- text on background
- interactive elements
- feedback and status colours
- light and dark themes, if applicable

Accessibility validation should be part of every token change.

## Change management

Changes to tokens should be made through pull requests.

Any update to primitive or semantic colour tokens should include:

- the reason for the change
- impacted semantic roles
- accessibility validation
- confirmation of downstream updates, including Figma if relevant

## Outputs

This repository may generate or export tokens for:

- Figma variables
- JavaScript or TypeScript
- CSS custom properties
- Brand Hub documentation

## Naming principle

Use semantic naming for consumption, for example:

- `color.text.primary`
- `color.background.default`
- `color.action.primary`

Avoid using raw hex values directly in product and design work unless explicitly required.

## Scope

This repository currently covers colour tokens.

It may later expand to include other token categories such as typography, spacing, radius, elevation and motion.

## Ownership

Design owns visual intent and semantic suitability.

Design system and frontend own token structure, implementation and downstream distribution.

Changes to shared colour tokens should be reviewed cross-functionally when they affect both design and product.
