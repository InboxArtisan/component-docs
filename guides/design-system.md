---
description: A restricted design system for mail components
---

# Design system

### Overview

A **design system** is a collection of principles and patterns that govern the appearance and behaviour of components. However, a design system like Material Design which is used by component libraries like MUI, cannot be implemented over mail clients. Here is a simple example that explains why:

Material Design uses a number of CSS properties that are not supported by most mail clients. For example, the `:hover` pseudo-class is not supported by many mail clients. This means that if you use Material Design to style a mail template, the hover effects will not be displayed in many mail clients.

As a result, it is important to choose a design system that is specifically designed for mail clients. This would ensure that your mail templates will look consistent across all major mail clients, as such a design system would take into account the limitations of mail clients.

### Interactivity

Interactive elements like buttons or links have various interaction states and properties associated with them. For example, a button can be in the following interaction states (as per Material Design 3 guidelines \[[1](design-system.md#references)]):

* Enabled
* Disabled
* Hover
* Focused
* Pressed
* Dragged

Each of these states is associated with style properties like `opacity` or `background-color`.

<figure><img src="https://lh3.googleusercontent.com/iTOnDTFkxnPSHW_IdlCmbVssCHpXTYfCqDeC-mJmnxiG7URuayxmAGnvoGq5MGXlSu6wYwognBESOp4EmH5Y14QP98Iu0viYcLI46d4_cF4=s0" alt=""><figcaption><p>Opacity for hover, focused, pressed &#x26; dragged states of a button from the <strong>Material Design 3</strong> guidelines [<a href="design-system.md#references">2</a>]</p></figcaption></figure>

But here's the primary issue: These states are either irrelevant in the context of a mail or cannot be implemented due to the lower adoption of CSS properties that enable them. For example,

1. **A "disabled" button or a link is irrelevant in the context of a mail.** What's even the point of a button (which is actually just a link that looks like a button, in the context of a mail) that a user cannot click? While building a user interface in web browsers, disabled buttons have various use cases, for example, a submit button stays in the disabled state when a form is in submission, but it has no utility in a mail template.
2. **Other states like "hover",  "pressed" & "focused" states cannot be implemented across the major mail clients**, because (as of August '23) only 63.41% of mail clients fully support the `:hover` pseudo-class \[[3](design-system.md#references)], only 56.1% of mail clients fully support the `:active` pseudo-class \[[4](design-system.md#references)] & only 51.22% of mail clients fully support the `:focus` pseudo-class \[[5](design-system.md#references)]. Major mail clients like Gmail & Outlook do not support them on certain devices, so using them will create inconsistencies in the design.

#### TL;DR

> Interactivity has no utility for mail components, nor can it be implemented consistently across most mail clients

### Colors

> [🚧](https://emojipedia.org/construction/) WIP

### Typography

> [🚧](https://emojipedia.org/construction/) WIP

### Icons

> [🚧](https://emojipedia.org/construction/) WIP

### Theme object

> [🚧](https://emojipedia.org/construction/) WIP

### References

\[1] Interaction states overview (Material design guidelines): [https://m3.material.io/foundations/interaction/states/overview](https://m3.material.io/foundations/interaction/states/overview)

\[2] Interaction states layers (Material design guidelines): [https://m3.material.io/foundations/interaction/states/state-layers](https://m3.material.io/foundations/interaction/states/state-layers)

\[3] `:hover` pseudo-class (caniemail.com): [https://www.caniemail.com/features/css-pseudo-class-hover/](https://www.caniemail.com/features/css-pseudo-class-hover/)

\[4] `:active` pseudo-class (caniemail.com): [https://www.caniemail.com/features/css-pseudo-class-active/](https://www.caniemail.com/features/css-pseudo-class-active/)

\[5] `:focus` pseudo-class (caniemail.com): [https://www.caniemail.com/features/css-pseudo-class-focus/](https://www.caniemail.com/features/css-pseudo-class-focus/)

###
