# coding-guideline-checklist

This is a short checklist for you. Please check it once before you start to code and once again before you submit your work to us.

1. Only for `Nuxt.js` projects: `Bootstrap-vue` is **not** imported repeatedly in multiple `Vue.js components`. [Details](https://github.com/Webhikers-Docs/nuxt-bootstrap-doc)

2. Each page's `content` (everything between `header` and `footer`) is split into single `Vue.js components` for each `section` of the page, if there is more than one `section` on the page. [Details](https://github.com/Webhikers-Docs/code-architecture#modular-components)

3. **Every** single `style` tag in **each** `component` ever is `scoped`. [Details](https://github.com/Webhikers-Docs/code-architecture#scoped-style)

4. Global `scss` rules and `css resets` are wrapped into a layout wrapper. Something like `.my-layout{ p { margin:0; } }`. [Details](https://github.com/Webhikers-Docs/code-architecture#global-css)

5. `header`, `footer` and other **recurring** `components` are always placed outside a layout wrapper. [Details](https://github.com/Webhikers-Docs/code-architecture#recurring-components)

6. No css rules have been set for `body` or `html` tag (exeption is `font-family`). [Details](https://github.com/Webhikers-Docs/code-architecture#html-root)
