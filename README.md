# @inboxartisan/components docs

![IA components banner](https://1913075412-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2Fe6dBrizqX2znMBrdvk9k%2Fuploads%2F9tcdATlLUJhN6ULncwiH%2F%40inboxartisan_components%20(5).png?alt=media&token=3c7481c3-5bf4-4f8f-8f8f-561aafad0024)

> 📝 NOTE: This repository contains docs for `@inboxartisan/components` hosted on gitbook.com. You can access the docs [here](https://components.inboxartisan.com).

## Overview
`@inboxartisan/components` is a collection of reusable, thematic & MUI-like components for building mail templates. It is built on top of react.email, which offers a collection of unstyled components which works on multiple mail clients. 

react.email provides a render utility [[1](#References)], which converts a react component stored in a JSX/TSX file into an HTML file, but there's a catch, not all CSS properties and HTML elements are supported by all major mail clients, and so, typical component libraries like MUI and Chakra UI cannot be used directly for creating mail templates, as it might create inconsistencies across various mail clients. 
So keeping this in mind, @inboxartisan/components is offering mail components that can work across most (>=90%) of the mail clients.


## Avoiding the vanilla way
> Think of mail clients like outdated web browsers, which only support a limited number of HTML elements and CSS properties.

Here's a simple example of a CSS property that works on most web browsers, but won't work on most mail clients: A common way to add elevation to a container component (e.g., `<div>`) is by using a CSS property called `box-shadow` . As of Jul'23, only 56.1% of all major mail clients support this property [[2](#References)]. Another common example is `display: grid;`. It is widely supported by most browsers, but it is only supported by 58.54% of all major mail clients [[3](#References)]. 

Keeping track of which CSS properties or HTML elements can be used while building mail templates can give you migrane & this is a problem that we're trying to solve. 

![Estimated support of `box-shadow` CSS property in mail clients](https://1913075412-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2Fe6dBrizqX2znMBrdvk9k%2Fuploads%2FJphm4Xe5sPGxAhXDSCI7%2Fimage.png?alt=media&token=b3b11198-dfab-494f-9938-9c623f1f11a2) 


## Limited number of components
@inboxartisan/components will be offering a collection of 18 components, which is not a lot, especially in comparison to modern component libraries like MUI or Chakra UI. There are two reasons why:

1. **Limited support**: As mentioned above, most mail clients only support a limited number of HTML elements and CSS properties. This means that it wouldn't be feasible to render many HTML elements with low support in several mail clients. For example, a form element like `<input type="text" />` is used in all web apps but it's full support is estimated to be 43.9% [[4](#References)].

2. **Intentional limitation**: Just because a particular HTML element is supported by a certain mail client doesn't mean that it should be used in a mail template. We believe that the answer is no. Emails are a medium of communication, not very different from SMS. Their primary purpose is to inform users to perform certain actions (e.g., verifying their account) or update them about certain events (e.g., newsletters, updates to settings). Emails are simply supposed to convey information, and that's it.

## Finally ...
If you believe that despite all the improvements in mail clients, the following mail template is "okay" just because it gets the job done, then you should also be okay with web 1.0 style web apps. The whole point of this is to make beautiful and modern mail templates.

![Default mail template for Firebase authentication](https://1913075412-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2Fe6dBrizqX2znMBrdvk9k%2Fuploads%2FuyVWuVeAnNiOPChfbkS4%2FFirebase%20Verification-1%20(1).png?alt=media&token=6aea90a2-2354-4612-9d52-b155e4078246)

## References
[1] Render utility (react.email): https://react.email/docs/utilities/render

[2] box-shadow (caniemail.com): https://www.caniemail.com/features/css-box-shadow/

[3] display: grid; (caniemail.com): https://www.caniemail.com/features/css-display-grid/

[4] <input type="text"/> (caniemail.com): https://www.caniemail.com/features/html-input-text/
