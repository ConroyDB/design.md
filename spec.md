# DESIGN.md Format

The DESIGN.md file is a textual representation of a design system. The main
audience of DESIGN.md is design and coding agents, to help them understand the
visual differentiation of a product and avoid producing generic designs. All
parts of the file are human readable and understandable, so that the human can
create and modify it.

# Design Tokens

DESIGN.md may also embed structured design tokens. The system that we use to
describe design tokens is loosely based on the
[Design Token JSON spec](https://www.designtokens.org/tr/2025.10/format/#abstract).
As such, it's easily converted from / to tokens.json, Figma variables, and
Tailwind theme configs.

The yaml may be embedded into DESIGN.md as Front Matter, or be distributed
throughout the document as YAML code blocks.

Front Matter Example:

```yaml
---
name: Kindred Spirit
description: Describes the design system for a pet care assistant.
colors:
  primary: "#647D66"
typography:
  headline-lg:
    fontFamily: Google Sans Display
    fontSize: 42px
    fontWeight: 500
    lineHeight: 50px
    letterSpacing: 1.2px
---
```

YAML codeblock example:[^2]

```markdown
## Colors

‍```yaml
colors:
  primary: "#647D66"
‍```

The palette uses a deep "Evergreen" primary to establish authority and
health-sector credibility. Use for moments of highest authority and deep
contrast.

## Typography

‍```yaml
typography:
  headline-lg:
    fontFamily: Google Sans Display
    fontSize: 42px
    fontWeight: 500
    lineHeight: 50px
    letterSpacing: 1.2px
‍```

This design system utilizes a dual-font strategy to balance character with
functionality. **Google Sans Display** provides a friendly, slightly rounded
geometric feel for headlines.
```

### Schema

Here's the overall schema for the design tokens:

```yaml
name: <string>
description: <string>
colors:
  token-name: <Color>
typography:
  token-name: <Typography>
rounded:
  level: <Dimension>
spacing:
  level: <Dimension>
components:
  component-name:
    token-name: <string|token reference>
```

**Color**: A color value must start with "#" followed by a hex color code in the
SRGB color space.

**Typography**: A typography value is an object that maps the name of the type
token (e.g., headline-lg) to an object defining its properties. The object may
contain:

- fontFamily (string)
- fontSize (Dimension)
- fontWeight (number)
- lineHeight (Dimension)
- letterSpacing (Dimension)
- fontFeature: (string) - configures
  [font-feature-settings](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/font-feature-settings).
- fontVariation: (string) - configures
  [font-variation-settings](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/font-variation-settings).

**Dimension**: a dimension value is a string with a unit suffix. Valid units are:
px and rem.

**Token references**: a token reference must be wrapped in curly braces, and
contain an object path to another value in the YAML tree. The referenced object
must be a primitive value, e.g. colors.primary-60, rather than an object, e.g.
colors.

# File Format

## Overview

A holistic overview of the design system. This section explains the look and
feel that the design needs to convey, the brand personality it embodies, and how
it serves the user's goals.

## Colors

This section defines the key color palettes for the design system.

At least one color palette should be defined, and should be referred to as
"primary". If there are other color palettes, we follow the material color
naming convention of calling them "primary", "secondary", "tertiary" and
"neutral".

Example:

```markdown
## Colors

The palette uses a deep "Evergreen" primary to establish authority and
health-sector credibility. This is balanced by a "Sun-Kissed Orange" secondary
color used sparingly for calls to action and playful highlights.

- **Primary:** Represents health, growth, and vitality. Used for key
  navigation and primary actions.
- **Secondary:** Represents warmth and activity. Used for notifications,
  reminders, and "joy" moments.
```

### Design Tokens

```yaml
colors:
  primary: "#ff0000"
  secondary: "#00ff00"
```

The colors section defines the color design tokens. It is a
map\<string, Color\>, that maps the name of the color token to the value.

## Typography

Define typography levels.

Most design systems have 9 - 15 typography levels from headlines, body, to
labels. For each level, choose the font family, size, weight, line height, and
optionally letter spacing.

Example:

```markdown
## Typography

This design system utilizes a dual-font strategy to balance character with
functionality. **Plus Jakarta Sans** provides a friendly, slightly rounded
geometric feel for headlines, making the app feel welcoming at first glance.
**Be Vietnam Pro** is used for all functional text; its clean terminals and
generous x-height ensure that medical notes and pet schedules are legible even
on small mobile screens. Headlines use a tighter letter-spacing to feel more
"designed" and editorial.
```

### Design Tokens

```yaml
typography:
  headline-lg:
    fontFamily: Google Sans Display
    fontSize: 42px
    fontWeight: 500
    lineHeight: 50px
    letterSpacing: 1.2px
  body-lg:
    fontFamily: Roboto
    fontSize: 14px
    fontWeight: 400
    lineHeight: 20px
    letterSpacing: 1.2px
```

The typography section defines the typography design tokens. It is a
map\<string, Typography\>

## Layout

Describe the layout method.

Most design systems follow a grid-based layout. Others, like Liquid Glass, use
margins, safe areas, and dynamic padding. Explain the layout model and spacing
rhythm.

Example:

```markdown
## Layout

The layout follows a **Fluid Grid** model for mobile devices and a
**Fixed-Max-Width Grid** for desktop (max 1200px).

A strict 8px spacing scale (with a 4px half-step for micro-adjustments) is used
to maintain a consistent rhythm. Components are grouped using "containment"
principles, where related items are housed in cards with generous internal
padding (24px) to emphasize the soft, approachable nature of the brand.
```

### Design Tokens

You may provide spacing units that are useful for implementing the layout model.
For example, a fixed grid layout may have spacing units for column spans,
gutters, and margins.

```yaml
spacing:
  gutter-s: 8px
  gutter-l: 16px
```

The spacing section defines the spacing design tokens. It is a
map\<string, Dimension\> that maps the spacing scale identifier to a dimension
value.

## Elevation[^1]

Describe how visual hierarchy is conveyed based on the design style. If
elevation is used, it defines the required styling (spread, blur, color). For
flat designs, this section explains the rationale and any alternative methods
employed (e.g., borders, color contrast).

Example:

```markdown
## Elevation & Depth

Depth is achieved through **Tonal Layers** rather than heavy shadows. The
background uses a soft off-white or very light green, while primary content sits
on pure white cards.
```

## Shapes

Describe the shape language. In particular, describe the rounded corners used in
buttons, cards, and other rectangular shapes.

### Design Tokens

```yaml
rounded:
  regular: 4px
  lg: 8px
  xl: 12px
  full: 9999px
```

The rounded section defines the design tokens for rounded corners used in
buttons, cards, and other rectangular shapes.

## Components

Provides style guidance for component atoms within the design system, focusing
on those most relevant to the application.

- **Buttons**: Covers primary, secondary, and tertiary variants, including
  sizing, padding, and states.
- **Chips**: Covers selection chips, filter chips, and action chips.
- **Lists**: Covers styling for list items, dividers, and leading/trailing
  elements.
- **Tooltips**: Covers positioning, colors, and timing.
- **Checkboxes**: Covers checked, unchecked, and indeterminate states.
- **Radio buttons**: Covers selected and unselected states.
- **Input fields**: Covers text inputs, text areas, labels, helper text, and
  error states.

This section may also suggest additional components particularly relevant to the
app's context.

### Design Tokens

```yaml
components:
  button-primary:
    backgroundColor: "{colors.primary-60}"
    textColor: "{colors.primary-20}"
    typography: "{typography.label-md}"
    rounded: "{rounded.md}"
    padding: 12px
  button-primary-hover:
    backgroundColor: "{colors.primary-70}"
```

The components section defines a collection of design tokens used to ensure
consistent styling of common components. It's a
map\<string, map\<string, string\>\> that maps a component identifier to a group
of sub token names and values. The design token values may be literal values, or
references to previously defined design tokens.

**Variants**. A component may have a variant for different UI states such as
active, hover, pressed, etc. You may define those variant components under a
different but related key, for example, "button-primary",
"button-primary-hover", "button-primary-active". The agent will consider all
variants and make the appropriate styling decisions.

### Component Property Tokens

A component may have these sub tokens:

- backgroundColor: \<Color\>
- textColor: \<Color\>
- typography: \<Typography\>
- rounded: \<Dimension\>
- padding: \<Dimension\>

## Do's and Don'ts

# Use Cases

## Usage within Stitch

DESIGN.md allows the user to gain insight into how Stitch understands their
design request and enables Stitch agent and the user to collaborate on the
design system.

- **Enforcing Style:** The agent consumes the DESIGN.md to enforce systemic
  rules, generating UI code that strictly adheres to the included design tokens
  and guidelines.
- **Enhancing Consistency:** The file is used to enhance the prompt for
  generating and editing existing screens to ensure consistency across the
  project.
- **Decoupling Content and Style:** Stitch is designed to strictly decouple
  content from styling. The DESIGN.md provides the styling rulebook, which the
  agent combines with the context of previous screens to determine the actual
  content, preventing the model from inserting irrelevant content (like a map in
  a non-dog-walking app) based only on the design system contents.

## Usage outside of Stitch

We also envision usage of the DESIGN.md file in the broader design industry:

- **Viewing the System:** Users can view the generated design.md file. They can
  also view the design system of a selected screen in the UI panel (renamed from
  "theme" to "Design System" panel).
- **Setting Defaults:** Users can select an available design system to be used by
  default for all future generations within the same project.
- **Refinement:** The generated DESIGN.md can be used to enhance prompts,
  allowing users to guide the agent toward greater consistency and adherence to
  the defined look and feel.
- **Editing:** Users can make simple edits to the design system via the Design
  System panel in the UI.
- **Export:** When a user exports a project, the design.md file is intended to be
  included in the exported zip file.

# Creation

### Agent Generation

1. The agent interprets high-level aesthetic prompts from the user (e.g.,
   "playful and accessible").
2. The agent generates a valid design token specification and style guidelines
   from scratch, which is then summarized in the markdown format.
3. Agent creates a DESIGN.md file based on the design tokens and a DESIGN.md
   template.

### Direct Input

Advanced users may manually define or directly edit the design system. This
includes defining custom design personas and encoding detailed design
preferences to precisely guide the Stitch agent's UI generation.

### Derived from Branding Materials

The design system can be generated from external assets. The agent extracts
style and token information from sources such as user-provided images or a
specified URL containing branding profiles and design elements to create the
initial DESIGN.md file.

A DESIGN.md file has two faces:

- The prose describes the design system.
- The structured design tokens.

---

[^1]: May add tokens for border or box shadow later.
[^2]: Provincial format, exploring results.
