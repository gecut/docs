---
title: Buttons

cover:
  image: hybrid-ui/components/button.png
  alt: Hybrid UI Cover
  relative: true

author: S. MohammadMahdi Zamanian
---

Creates customizable buttons with various visual styles, loading states, icons, and event handling capabilities

<!--more-->

### Purpose

The `gecutButton` component enhances your Lit applications by providing versatile buttons. It offers features like:

- **Visual Styles:** Choose from several types: elevated, filled, filledTonal, outlined, or text.
- **Loading Indicator:** Visually indicate ongoing processes by displaying a spinner icon.
- **Icons:** Add leading and/or trailing icons to enhance button clarity.
- **Accessibility:** Buttons handle disabled states and tabindex for proper keyboard navigation.
- **Customization:** Control button behavior and appearance through various options.

### Usage

Here are multiple short examples showcasing different use cases of the `gecutButton` component:

#### 1. Basic Button:

```ts
import { gecutButton } from "@gecut/components";

const buttonTemplate = html` ${gecutButton({ label: "Click Me" })} `;

render(buttonTemplate, document.body);
```

#### 2. Button with Icon:

```ts
import { gecutButton } from "@gecut/components";

const iconSvg = "<svg>...</svg>"; // Replace with your icon SVG

const buttonTemplate = html`
  ${gecutButton({
    label: "Download",
    icon: { svg: iconSvg },
  })}
`;

render(buttonTemplate, document.body);
```

#### 3. Disabled Button:

```ts
import { gecutButton } from "@gecut/components";

const buttonTemplate = html`
  ${gecutButton({ label: "Processing...", disabled: true })}
`;

render(buttonTemplate, document.body);
```

#### 4. Link Button:

```ts
import { gecutButton } from "@gecut/components";

const buttonTemplate = html`
  ${gecutButton({ label: "Visit Website", href: "https://example.com" })}
`;

render(buttonTemplate, document.body);
```

#### 5. Button with Loading Indicator:

```ts
import { gecutButton } from "@gecut/components";

const buttonTemplate = html`
  ${gecutButton({ label: "Loading...", loading: true })}
`;

render(buttonTemplate, document.body);
```

### API Reference (Short Overview)

- **type (string, default: 'elevated')**: Button visual style (elevated, filled, filledTonal, outlined, text).
- **htmlType (string)**: Sets the HTML button type attribute (e.g., `'submit'`, `'button'`, `'reset'`).
- **disabled (boolean, default: false)**: Disables the button.
- **loading (boolean, default: false)**: Displays a loading indicator.
- **loader (object)**: Customizes the loading indicator SVG (optional).
- **icon (object)**: Object containing an SVG string for the leading icon.
- **trailingIcon (object)**: Object containing an SVG string for the trailing icon.
- **href (string)**: Makes the button behave like a link with the specified URL.
- **target (string)**: Sets the target attribute for a link-like button (e.g., `'_blank'`).
- **events (object)**: Event handlers for specific events (e.g., `click`, `mouseover`).
- **label (string)**: The button's text content.

#### Additional Considerations

- Ensure Lit is installed in your project for the `gecutButton` directive to function.
- Refer to the `gecut/lit-helper` documentation for more details on the `GecutDirective` base class (if applicable).
- Customize the default loading indicator SVG or create custom icons using the `icon` component (if available) in your project
