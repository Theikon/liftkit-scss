# LiftKit SCSS

A fork of LiftKit CSS utilizing the power of the CSS preprocessors Sass to
address various issues with the code style and deployment.

Huge thanks to [@chainlift](https://www.github.com/chainlift) for designing
LiftKit, a framework utilizing the golden ratio to provide web pages with an
oddly-satisfying look and feel.

## Overview

The aim of the fork is not to provide a simple drag-and-drop replacement for
LiftKit, but to enhance the source where possible, focusing on consistency and
clarity. This means that LiftKit SCSS is *not* compatible with LiftKit CSS out
of the box.

LiftKit SCSS uses mixins in favor of non-semantic classes in order to achieve
a significantly smaller footprint and encourage semantic naming of classes in
the DOM. Due to this, the following utility classes of LiftKit CSS are only
available in LiftKit SCSS using the `@include`-at rule:

- Margins (such as `m-top__s`) and padding (such as `p-bottom__m`). Note the
  shortening of `pad` to just `p`.
- Shadows (such as `shadow__m`). Note the name change for consistency.
- Blocks (such as `h-block` or `v-block__s`). Note the name change for
  consistency.
- Font and background colors (such as `bg-light__scrim` or `color-dark__info`).
- Sizes for both width and height (such as `w__s` or `h__xl`). Note the name
  change for consistency.

Note that the step size variables such as `--wholestep` (equal to `$MAJOR`) or
`--wholestep-dec` (equal to `$MINOR`) are now only available at compile-time.

Containers and sections also adhere to the naming convention involving the size
suffix (`__xs`, `__s`, `__m`, `__l`, `__xl`) for consistency.

## Quickstart

Already familiar with LiftKit and Sass? Then download the latest release of
LitKit SCSS from
[GitHub](https://github.com/Theikon/liftkit-scss/archive/refs/heads/main.zip),
and import the `liftkit.scss` file for example as follows:

```SCSS
@use "liftkit";

nav {
  @include liftkit.h-block__m;

  align-items: center;
}

p {
  @include liftkit.m-bottom__s;
}
```
LiftKit SCSS uses [Inter](https://rsms.me/inter/) throughout its font styles by
default, which is freely available on Google Fonts. If you are new to LiftKit
in general, have a look at the official documentation behind the design
philosophy over [here](https://www.chainlift.io/liftkitdocs/overview).

Feel free to reach out about any questions or feature requests by mail.
