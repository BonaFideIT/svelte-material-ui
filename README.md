<div align="center">
  <img src="packages/site/static/header-transparent.png" alt="Svelte Material UI" />
</div>

A library of Svelte Material UI components, based on [Material Design Components - Web](https://github.com/material-components/material-components-web).

# Demos, Code Samples, and Guides

https://sveltematerialui.com

# Features

Here are some unique features that help SMUI stand out:

- Full TypeScript support, including HTML attributes.
- You can add arbitrary attributes to all of the components and many of the elements within them.
- You can add actions to the components with `use={[Action1, [Action2, action2Props], Action3]}`.
- You can add props to lower components and elements with "$" props, like `input$maxlength="15"`.
- SMUI [supports RTL languages](https://svelte.dev/repl/c2ff2d5dd5404eccb901ba04ef0161be).

# Installation

To get started, check out the [installation docs](INSTALL.md) or the [SvelteKit docs](SVELTEKIT.md).

# Need Help?

If you need help installing or using SMUI, join the [Discord server](https://discord.gg/aFzmkrmg9P).

# Svelte 5

SMUI v8 requires Svelte 5. This is the documentation for v8, which is still in development (and is currently in a prerelease state).

If you are using Svelte 4, you can use SMUI v7, which is the current stable version. Check out the [v7 branch](https://github.com/hperrin/svelte-material-ui/tree/v7) for the current docs.

# Migration

Upgrading from an old version? Be sure to read the [migration doc](MIGRATING.md).

Upgrading from v7? You need Svelte 5. Event listeners no longer to use the CustomEvent type. Check out the [upgrade instructions](MIGRATING.md#smui-7---smui-8).

Upgrading from v6? You need Svelte 4. No more elemental components; you can now use the "tag" prop to change the element. No more "ComponentDev" types; components can now be used as their type. Check out the [upgrade instructions](MIGRATING.md#smui-6---smui-7).

Upgrading from v5? If you're still using the advanced styling method, it's really time to switch to the easy styling method. '/styled' endpoints are no longer provided. Check out the [upgrade instructions](MIGRATING.md#smui-5---smui-6).

Upgrading from v4? SMUI v5 requires the [TypeScript preprocessor](https://github.com/sveltejs/svelte-preprocess). SMUI v6 does not though, so if you upgrade straight to v6, don't worry. Check out the [upgrade instructions](MIGRATING.md#smui-4---smui-5).

Upgrading from v3? SMUI's styling method has been simplified. Check out the [upgrade instructions](MIGRATING.md#smui-3---smui-4).

Upgrading from v2? There are **lots** of changes listed in the [upgrade instructions](MIGRATING.md#smui-2---smui-3).

# Old Docs

You can find older versions of the docs on their respective branch:

- [v7 docs](https://github.com/hperrin/svelte-material-ui/tree/v7#readme)
- [v6 docs](https://github.com/hperrin/svelte-material-ui/tree/v6#readme)
- [v5 docs](https://github.com/hperrin/svelte-material-ui/tree/v5#readme)
- [v4 docs](https://github.com/hperrin/svelte-material-ui/tree/v4#readme)

# Icons

You can include icons in a number of ways, but the easiest is the [Material Icon Font](https://developers.google.com/fonts/docs/material_icons). This will give you the standard set of Material Icons, available with the CSS class "material-icons".

```html
<link
  href="https://fonts.googleapis.com/icon?family=Material+Icons"
  rel="stylesheet"
/>
```

However, there are two downsides. First is that all icons are downloaded, no matter which ones you use, so the size over the wire will almost certainly be more than necessary. Second is that it _only_ includes the Material Icons from Google.

Another option is the [Material Design Icons library](https://pictogrammers.com/library/mdi/). See the "Using SVGs" demo on the [Icon Button demo page](https://sveltematerialui.com/demo/icon-button) for instructions to use icons from the `@mdi/js` package (or any other SVG icons).

You can even use them in data URLs. To get a data URL for the icon:

1. [Find your icon](https://pictogrammers.com/library/mdi/) and click "Copy SVG" button (it looks like `</>`).
2. [Base64 encode](https://www.base64encode.org/) the document.
3. Format the URL like this `data:image/svg+xml;base64,encodedcontent`, replacing "encodedcontent" with the Base64 results.
4. Now you have an image URL you can use in an "img" tag src attribute or anywhere else you put an image URL (like `background-image: url();`).

# Components

Click a component/package below to go to the documentation. (Note that this documentation is a work in progress. The demo code should be your main source of truth for how something works.)

- [Accordion](packages/accordion/README.md)‡
- Action Buttons
  - [Button](packages/button/README.md)
  - [Floating Action Button](packages/fab/README.md)
  - [Icon Button](packages/icon-button/README.md)
- App Bars
  - [Bottom App Bar](packages/bottom-app-bar/README.md)‡
  - [Top App Bar](packages/top-app-bar/README.md)
- [Badge](packages/badge/README.md)‡
- [Banner](packages/banner/README.md)
- [Card](packages/card/README.md)
- [Common](packages/common/README.md)
- [Data Table](packages/data-table/README.md)
- [Dialog](packages/dialog/README.md)
- [Drawer](packages/drawer/README.md)
- [Elevation](https://sveltematerialui.com/demo/elevation/)†
- [Image List](packages/image-list/README.md)
- Inputs and Controls
  - [Autocomplete](packages/autocomplete/README.md)‡
  - [Checkbox](packages/checkbox/README.md)
  - [Chips](packages/chips/README.md)
  - [Chip Input](packages/chip-input/README.md)‡
  - [Floating Label](packages/floating-label/README.md)
  - [Form Field](packages/form-field/README.md)
  - [Line Ripple](packages/line-ripple/README.md)
  - [Notched Outline](packages/notched-outline/README.md)
  - [Radio Button](packages/radio/README.md)
  - [Segmented Button](packages/segmented-button/README.md)
  - [Select Menu](packages/select/README.md)
    - [Select Helper Text](packages/select/helper-text/README.md)
    - [Select Icon](packages/select/icon/README.md)
  - [Slider](packages/slider/README.md)
  - [Switch](packages/switch/README.md)
  - [Text Field](packages/textfield/README.md)
    - [Text Field Character Counter](packages/textfield/character-counter/README.md)
    - [Text Field Helper Text](packages/textfield/helper-text/README.md)
    - [Text Field Icon](packages/textfield/icon/README.md)
- [Layout Grid](packages/layout-grid/README.md)
- [List](packages/list/README.md)
- [Menu Surface](packages/menu-surface/README.md)
- [Menu](packages/menu/README.md)
- [Paper](packages/paper/README.md)‡
- Progress Indicators
  - [Circular Progress](packages/circular-progress/README.md)
  - [Linear Progress](packages/linear-progress/README.md)
- [Ripple](packages/ripple/README.md)
- [Snackbar](packages/snackbar/README.md)
  - [Kitchen](packages/snackbar/kitchen/README.md)‡
- Tabs
  - [Tab](packages/tab/README.md)
  - [Tab Bar](packages/tab-bar/README.md)
- [Tooltip](packages/tooltip/README.md)
- [Touch Target](packages/touch-target/README.md)
- [Typography](https://sveltematerialui.com/demo/typography/)†

<sub>† This is Sass based, and therefore doesn't require Svelte components. I've included a demo showing how you can use it.</sub>

<sub>‡ This is not an MDC-Web component (upstream library). It is an addition that SMUI provides.</sub>

- Labels and icons are named exports in the components that use them, or you can use the 'Label' and 'Icon' exports from '@smui/common'. (Except for chips labels and icons, textfield icons, and select icons, because they are special snowflakes.)

# License

Copyright 2019-2024 Hunter Perrin

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
