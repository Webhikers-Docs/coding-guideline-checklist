# coding-guideline-checklist

This is a short checklist for you. Please check it once before you start to code and once again before you submit your work to us.

**Please make sure that:**

1. Each page's `content` (everything between `header` and `footer`) is split into single `Vue.js components` for each `section` of the page, if there is more than one `section` on the page. A section can be defined visually, with a `section` tag, a bootstrap `.row` or by content. [Details](https://github.com/Webhikers-Docs/code-architecture#modular-components).

2. Your `.Vue` files dont have more than 100 lines of code. Otherwise you need to split it into more sub-components.

3. **Every** single `style` tag in **each** `component` ever is `scoped`. [Details](https://github.com/Webhikers-Docs/code-architecture#scoped-style)  

4. Global `scss` rules and `css resets` are wrapped into a layout wrapper. Something like `.my-layout{ p { margin:0; } }`. [Details](https://github.com/Webhikers-Docs/code-architecture#global-css)  

5. `header`, `footer` and other **recurring** `components` are **never** placed inside a layout wrapper (don't do this: `<div class=".my-layout"><header></header></div>`) . [Details](https://github.com/Webhikers-Docs/code-architecture#recurring-components)  

6. No css rules have been set for `body` or `html` tag (exeption is `font-family`). [Details](https://github.com/Webhikers-Docs/code-architecture#html-root)  

7. Only for `Nuxt.js` projects: `Bootstrap-vue` is **not** imported repeatedly in multiple `Vue.js components`. [Details](https://github.com/Webhikers-Docs/nuxt-bootstrap-doc)  

8. The app *never* uses `<a></a>` tags. Instead, **always** use `<nuxt-link></nuxt-link>`, `<router-link></router-link>`, or `<b-link></b-link>`.
    
9. You always use [native nuxt transitions](https://nuxtjs.org/docs/2.x/features/transitions) and no external `Vue.js` transition plugins. Such as `<transition name="fade"><div v-if="true"></div></transition>`
        
10. All clickable elements and other elements with any kind of interaction have `css transitions` for better UX
11. You use `nuxt layouts` for pages with different layouts. For example, pages with a transparent `navbar` could use a `transparent-layout` file and pages with a non-transparent navbar could use a `non-transparent-layout` file in `nuxt/layouts/`.

12. You use a `<div class="container"></div>` for the content of all legal pages (`impressum`, `privacy`, `terms`, `cookies`)

13. The page's content is always fetched in `asyncData` and not in 'fetch' hook.

14. All `legal` pages, such as (`impressum`, `privacy`, `terms`, `cookies`) have a fully functional layout with `footer` and `header`.
