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
| **collapseMenu** | false | Boolean | `true`, `false` |
| **layoutType** | menu-dark | String | `menu-dark`, `menu-light`, `dark` |
| **headerBackColor** | default-header | String | `default-header`, `header-blue`, `header-red`, `header-purple`, `header-info`, `header-green`, `header-dark` |
| **fullWidthLayout** | false | Boolean | `true`, `false` |
| **navFixedLayout** | true | Boolean | `true`, `false` |
| **headerFixedLayout** | true | Boolean | `true`, `false` |

{% tabs %}
{% tab title="app-config.ts" %}
```javascript
export class NextConfig {
  public static config = {
    layout: 'vertical', // vertical, horizontal
    collapseMenu: false,
    layoutType: 'menu-light', // menu-dark, menu-light
    headerBackColor: 'default-header', // default-header, header-blue, header-red, header-purple, header-info, header-dark
    fullWidthLayout: false,
    navFixedLayout: true,
    headerFixedLayout: true
  };
}

```
{% endtab %}
{% endtabs %}

