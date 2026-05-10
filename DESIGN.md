---
version: alpha
name: Alvento Genesis
description: Editorial precision identity for Alvento, the umbrella brand for narrow intelligence products, with SIA Watch as the first live product.
colors:
  primary: "#5B5CF0"
  primary-hover: "#4F46E5"
  secondary: "#20970B"
  neutral: "#8A8A96"
  background: "#FAFAFA"
  surface: "#FFFFFF"
  surface-alt: "#F5F5F8"
  surface-accent: "#F3F3FF"
  text-primary: "#0A0A0A"
  text-secondary: "#61616D"
  border: "#E8E8EC"
  success: "#10B981"
  warning: "#F59E0B"
  error: "#EF4444"
typography:
  h1:
    fontFamily: Inter
    fontSize: 4.25rem
    fontWeight: 800
    lineHeight: 1.01
    letterSpacing: "-0.05em"
  h2:
    fontFamily: Inter
    fontSize: 2.25rem
    fontWeight: 750
    lineHeight: 1.08
    letterSpacing: "-0.04em"
  body-md:
    fontFamily: Inter
    fontSize: 1rem
    fontWeight: 400
    lineHeight: 1.6
  body-lg:
    fontFamily: Inter
    fontSize: 1.14rem
    fontWeight: 400
    lineHeight: 1.65
  label-sm:
    fontFamily: Inter
    fontSize: 0.82rem
    fontWeight: 700
    lineHeight: 1.2
    letterSpacing: "0.02em"
rounded:
  sm: 8px
  md: 12px
  lg: 16px
spacing:
  xs: 4px
  sm: 8px
  md: 12px
  lg: 16px
  xl: 24px
  xxl: 32px
  xxxl: 48px
elevation:
  card: "0 6px 18px rgba(10,10,10,0.04)"
  feature: "0 18px 48px rgba(10,10,10,0.07)"
components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "#FFFFFF"
    rounded: "{rounded.sm}"
    padding: 12px
  button-primary-hover:
    backgroundColor: "{colors.primary-hover}"
    textColor: "#FFFFFF"
    rounded: "{rounded.sm}"
    padding: 12px
  button-secondary:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.text-primary}"
    rounded: "{rounded.sm}"
    padding: 12px
  card-default:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.text-primary}"
    rounded: "{rounded.lg}"
    padding: 20px
  badge-accent:
    backgroundColor: "{colors.surface-accent}"
    textColor: "{colors.primary}"
    rounded: "999px"
    padding: 8px
  pill-neutral:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.text-secondary}"
    rounded: "999px"
    padding: 8px
---

## Overview

Alvento is the umbrella identity for narrow intelligence products. SIA Watch is the first public product inside that family and focuses on UK private security compliance monitoring. The interface should feel clean, calm and systematic, with the same editorial precision found in Genesis: strong typography, generous spacing, soft cards and a restrained indigo accent.

## Colors

- **Primary (#5B5CF0):** Main interaction color for buttons, active states, links and selection.
- **Primary Hover (#4F46E5):** Darker indigo for hover states on primary actions.
- **Secondary (#20970B):** Used sparingly for live status and positive operational states.
- **Background (#FAFAFA):** Main page background. Keep it bright and lightly cool.
- **Surface (#FFFFFF):** Default card, panel and nav surface.
- **Surface Alt (#F5F5F8):** Alternate containers, inline panels and alert cards.
- **Surface Accent (#F3F3FF):** Subtle accent-tinted surface for badges and icon backplates.
- **Text Primary (#0A0A0A):** Main heading and body color.
- **Text Secondary (#61616D):** Supporting copy and metadata.
- **Border (#E8E8EC):** Quiet dividers, card borders and input outlines.
- **Success / Warning / Error:** Reserved for operational state, not decoration.

## Typography

Use Inter or a similar modern grotesk throughout. Headlines should feel decisive and slightly editorial. Body copy should stay plain, operational and low-drama.

- H1 is large and compact, with tight negative tracking.
- H2 is strong but quieter than the hero.
- Body text should stay readable and neutral.
- Small labels and chips can use slight tracking, but avoid making the whole interface shout.

## Layout

Use a content-plus-sidebar layout on larger screens. The main content tells the product story; the sidebar handles umbrella framing, coverage and delivery metadata.

- Max width: 1180px
- Base spacing rhythm: 4px scale
- Typical card padding: 20px to 24px
- Typical section spacing: 30px to 48px
- Keep major sections airy and modular rather than dense.

## Elevation & Depth

Depth is soft and sparse.

- Regular cards use the lighter card shadow.
- Highlight panels and CTAs can use the feature shadow.
- Avoid heavy shadow stacks or dramatic glow effects.
- Prefer tonal separation, borders and spacing over visual noise.

## Shapes

- Buttons and inputs: 8px radius
- Standard cards: 12px radius
- Large panels and hero/sidebar cards: 16px radius
- Metadata chips and pills: full pill radius

## Components

- Primary buttons use indigo fill and white text.
- Secondary buttons stay white with a soft border.
- Cards remain white or near-white with light borders.
- Badge surfaces can use a pale accent wash.
- Keep icon blocks simple and geometric, not illustrative.

## Do's and Don'ts

### Do

- Use indigo for interaction, not decoration.
- Keep the Alvento umbrella visible but subordinate to the product copy.
- Write product language in plain English.
- Use cards and chips consistently across the site.
- Let spacing and typography do most of the visual work.

### Don't

- Mix in dark gradients from the old version.
- Overload the page with multiple accent colors.
- Turn the umbrella brand into the headline at the expense of the product.
- Use generic AI-product language when a practical service phrase will do.
- Add decorative effects that break the calm, systemized feel.
