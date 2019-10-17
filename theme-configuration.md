---
description: Menu/Layout Customize Options
---

# Template Configuration

{% hint style="info" %}
You can edit this file at **`[ ../src/app/app-config.ts ]`**
{% endhint %}

| **Option** | **Default** | **Data Type** | **Description** |
| :--- | :--- | :--- | :--- |
| **layout** | vertical | String | `vertical`, `horizontal` |
| **subLayout** | - | String | `horizontal-2` \(only used for layout is horizontal\) |
| **collapseMenu** | false | Boolean | `true`, `false` |
| **layoutType** | menu-dark | String | `menu-dark`, `menu-light`, `dark` |
| **headerBackColor** | default-header | String | `default-header`, `header-blue`, `header-red`, `header-purple`, `header-info`, `header-green`, `header-dark` |
| **navBrandColor** | brand-default | string | `brand-blue`, `brand-red`,  `brand-purple`,  `brand-info`,   `brand-green`,  `brand-dark`,  |
| **rtlLayout** | false | Boolean | `true`, `false` |
| **navFixedLayout** | true | Boolean | `true`, `false` |
| **headerFixedLayout** | true | Boolean | `true`, `false` |
| **boxLayout** | false | Boolean | `true`, `false` |

{% code-tabs %}
{% code-tabs-item title="app-config.ts" %}
```javascript
export class NextConfig {
  public static config = {
    layout: 'vertical', // vertical, horizontal
    subLayout: '', // horizontal-2
    collapseMenu: false,
    layoutType: 'menu-dark', // menu-dark, menu-light, dark
    headerBackColor: 'default-header', // default-header, header-blue, header-red, header-purple, header-info, header-green, header-dark
    navBrandColor: 'brand-default', // brand-blue, brand-red, brand-purple, brand-info, brand-green, brand-dark
    rtlLayout: false,
    navFixedLayout: true,
    headerFixedLayout: true,
    boxLayout: false,
  };
}
```
{% endcode-tabs-item %}
{% endcode-tabs %}

