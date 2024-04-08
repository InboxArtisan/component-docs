---
description: A restricted design system for mail components
---

# Design system

### Overview

A **design system** is a collection of principles and patterns that govern the appearance and behavior of components. However, popular design systems like Material Design cannot be directly implemented for email templates because they rely on features (e.g. CSS properties) that are not universally supported by email clients. Here's a simple example to illustrate this:

Material Design employs various CSS properties and techniques that many email clients do not support. For instance, the `:hover` pseudo-class, which is used to create hover effects, is not supported by \~40% of email clients (As of April 2024). This means that if you were to use Material Design styles in an email template, the hover effects would not work as intended across various email clients.

Consequently, when building email templates, it is crucial to choose a design system specifically tailored for email clients. Such a design system would take into account the limitations and constraints of email clients, ensuring consistent rendering and behavior of your email templates across major email platforms.

### Interactivity

Interactive elements like buttons or links have various interaction states and properties associated with them. For example, in the Material Design 3 guidelines, a button can have the following interaction states: \[[1](design-system.md#references)]):

* Enabled
* Disabled
* Hover
* Focused
* Pressed
* Dragged

Each of these states is associated with style properties like `opacity` or `background-color`.

<figure><img src="https://lh3.googleusercontent.com/iTOnDTFkxnPSHW_IdlCmbVssCHpXTYfCqDeC-mJmnxiG7URuayxmAGnvoGq5MGXlSu6wYwognBESOp4EmH5Y14QP98Iu0viYcLI46d4_cF4=s0" alt=""><figcaption><p>Opacity for hover, focused, pressed &#x26; dragged states of a button from the <strong>Material Design 3</strong> guidelines [<a href="design-system.md#references">2</a>]</p></figcaption></figure>

But here's the primary issue: These states cannot be implemented due to the lower adoption of the CSS properties that enable them. For example **states like "hover",  "pressed" & "focused" states cannot be implemented across the major mail clients**, because, as of April '24, only 60.98% of mail clients fully support the `:hover` pseudo-class , only 53.66% of mail clients fully support the `:active` pseudo-class  & only 48.78% of mail clients fully support the `:focus` pseudo-class . Major mail clients like Gmail & Outlook do not support them on certain devices, so using them will create inconsistencies in the design.

The primary challenge lies in the limited support for CSS properties required to implement these interaction states across email clients. For example, as of April 2024, states like "hover", "pressed", and "focused" cannot be consistently rendered across major email clients. This is due to the low adoption rates of the necessary CSS pseudo-classes:

* Only 60.98% of email clients fully support the `:hover` pseudo-class \[[3](design-system.md#references)], which is essential for creating hover effects.
* Only 53.66% of email clients fully support the `:active` pseudo-class \[[4](design-system.md#references)], which is used to style elements in their active/pressed state.
* Only 48.78% of email clients fully support the `:focus` pseudo-class \[[5](design-system.md#references)], which is crucial for styling, focused elements, such as those receiving keyboard input.

Popular email clients like Gmail and Outlook have varying levels of support for these pseudo-classes across different devices and platforms. Utilizing these interaction states indiscriminately can lead to inconsistencies in the design and user experience of email templates.\
\
Another issue is that even if a particular interaction state (e.g. disabled state) can be implemented for a button component within a mail template, it has limited utility within an email template.

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
