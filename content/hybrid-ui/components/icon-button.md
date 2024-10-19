---
title: Icon Buttons

cover:
  image: hybrid-ui/components/icon-button.png
  alt: Hybrid UI Cover
  relative: true

author: S. MohammadMahdi Zamanian
---

Creates a customizable icon button with various visual styles, optional toggle functionality, and detailed control over appearance and behavior.

<!--more-->

### Purpose

The `gecutIconButton` component offers a versatile way to build icon buttons within your Lit application. It provides a range of features to cater to different use cases, including:

* **Visual Styles:** Choose from several button types: filled, filledTonal, outlined, and normal (transparent background).
* **Toggle Functionality:** Create toggle buttons that switch states upon clicking.
* **Selected Icon:** Display a different icon when the button is in a selected state (for toggle buttons).
* **Loading Indicator:** Display a spinner icon to visually indicate an ongoing loading process.
* **Icon Support:** Add leading icons to enhance button clarity.
* **Accessibility:** Buttons automatically handle disabled states, tabindex, and toggle state management.
* **Customization:** Control button behavior and appearance through various options.

### Usage (Multiple Examples with TypeScript)

Here are various short examples demonstrating the usage of the `gecutIconButton` component for different scenarios:

#### 1. Basic Filled Button

```ts
import { gecutIconButton } from '@gecut/components';

const handleClick = () => {
  console.log('Button clicked!');
};

const buttonTemplate = html`
  ${gecutIconButton({
    type: 'filled',
    icon: { svg: '<svg>...</svg>' },
    events: { click: handleClick },
  })}
`;

render(buttonTemplate, document.body);
```

**2. Toggle Button (Unselected by Default):**

```ts
const buttonTemplate = html`
  ${gecutIconButton({
    type: 'toggle',
    icon: { svg: '<svg>...</svg>' },
    selectedIcon: { svg: '<svg>...</svg>' },
    checked: false,
  })}
`;

render(buttonTemplate, document.body);
```

#### 3. Normal (Transparent Background) Button with Disabled State

```ts
const buttonTemplate = html`
  ${gecutIconButton({
    type: 'normal',
    icon: { svg: '<svg>...</svg>' },
    disabled: true,
  })}
`;

render(buttonTemplate, document.body);
```

#### 4. Link-like Button with Custom Target

```ts
const buttonTemplate = html`
  ${gecutIconButton({
    href: '#',
    target: '_blank',
    icon: { svg: '<svg>...</svg>' },
  })}
`;

render(buttonTemplate, document.body);
```

#### 5. Button with Loading Indicator

```ts
const buttonTemplate = html`
  ${gecutIconButton({
    icon: { svg: '<svg>...</svg>' },
    loading: true,
  })}
`;

render(buttonTemplate, document.body);
```

### API Reference

The `gecutIconButton` directive accepts an object with the following optional properties:

- **type (string, default: 'normal')**: Specifies the visual style of the button:
    - `'filled'` (solid color background)
    - `'filledTonal'` (subtle color fill)
    - `'outlined'` (outlined border)
    - `'normal'` (transparent background)
- **href (string)**: If provided, the button is rendered as an anchor tag with the specified URL.
- **target (string)**: Sets the target attribute for a link-like button (e.g., `'_blank'`, `'_parent'`, `'_self'`, `'_top'`).
- **events (object)**: An object containing event handlers for specific events (e.g., `click`, `mouseover`). Handlers receive the DOM event object as an argument.
- **icon (object)**: An object containing an SVG string for the leading icon.
- **selectedIcon (object)**: An object containing an SVG string for the icon displayed when the button is in a selected state (applicable to toggle buttons).
- **name (string)**
  