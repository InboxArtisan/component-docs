---
description: >-
  InboxArtisan components are a collection of React components for building mail
  templates
cover: .gitbook/assets/@inboxartisan_components (5).png
coverY: 0
layout:
  cover:
    visible: true
    size: hero
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Introduction

### Overview

`@inboxartisan/components` is a collection of reusable, thematic & MUI-like components for building mail templates. It is built on top of [react.email](http://react.email), which offers a collection of unstyled components which works on multiple mail clients.&#x20;

[react.email](https://react.email) provides a render utility [\[1\]](./#references) which converts a react component stored in a JSX/TSX file into an HTML file, but there's a catch, not all CSS properties and HTML elements are supported by all major mail clients, and so, typical component libraries like [MUI](https://mui.com/) and [Chakra UI](https://chakra-ui.com/) cannot be used directly for creating mail templates, as it might create inconsistencies across various mail clients.&#x20;

So keeping this in mind `@inboxartisan/components` is offering mail components that can work across most (>=90%) of the mail clients.

### Mail Clients vs Web Browsers

> Think of mail clients like outdated web browsers, which only support a limited number of HTML elements and CSS properties.

Here's a simple example of a CSS property that works on most web browsers, but won't work on most mail clients: A common way to add elevation to a container component (e.g., `<div>`) is by using a CSS property called `box-shadow` . As of Jul'23, only 56.1% of all significant mail clients support this property [\[2\]](./#references). Another common example is `display: grid;`. It is widely supported by most browsers, but it is only supported by 58.54% of all significant mail clients [\[3\]](./#references).&#x20;

Keeping track of which CSS properties or HTML elements can be used while building mail templates can give you a migraine & this is a problem that we're trying to solve.&#x20;

<figure><img src=".gitbook/assets/image.png" alt=""><figcaption><p>Estimated support for <code>box-shadow</code> property in mail clients</p></figcaption></figure>



### Limited Components

`@inboxartisan/components` will be offering a collection of 18 components, which is not a lot, especially in comparison to modern component libraries like MUI or Chakra UI. There are two reasons why:

1. **Limited support:** As mentioned above, most mail clients only support a limited number of HTML elements and CSS properties. This means that it wouldn't be feasible to render many HTML elements with low support in several mail clients. For example, a form element  `<input type="text" />` is used in all web apps but its full support is estimated to be 43.9% [\[4\]](./#references).
2. **Intentional limitation:** Just because a particular HTML element is supported by a certain mail client doesn't mean that it should be used in a mail template. Emails are a medium of communication, not very different from SMS. Their primary purpose is to inform users to perform certain actions (e.g., verifying their account) or update them about certain events (e.g., login from a new location, updates to settings). Emails are simply supposed to convey information, and that's it.

### A Rant

If you believe that despite all the improvements in mail clients, the following mail template is "okay" just because it gets the job done, then you should also be okay with web 1.0 style web apps. The whole point of this is to make beautiful and modern mail templates.

<figure><img src=".gitbook/assets/Firebase Verification-1 (1).png" alt=""><figcaption><p>Default mail template for Firebase authentication</p></figcaption></figure>

### References

\[1] Render utility (react.email): [https://react.email/docs/utilities/render](https://react.email/docs/utilities/render)

\[2] `box-shadow` (caniemail.com): [https://www.caniemail.com/features/css-box-shadow/](https://www.caniemail.com/features/css-box-shadow/)

\[3] `display: grid;` (caniemail.com): [https://www.caniemail.com/features/css-display-grid/](https://www.caniemail.com/features/css-display-grid/)

\[4] `<input type="text"/>` (caniemail.com): [https://www.caniemail.com/features/html-input-text/](https://www.caniemail.com/features/html-input-text/)
