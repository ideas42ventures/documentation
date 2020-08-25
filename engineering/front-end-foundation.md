# Front-end Foundation

This is an outline of topics, ideas, and resources helpful in gaining a solid foundation of building web pages.

## Overall ideas

- Learn and understand what progressive enhancement is and isn't. We follow a progressive enhancement approach at The Studio as much as we possibly can.
  - https://alistapart.com/article/understandingprogressiveenhancement
  - https://adactio.com/journal/16404
  - https://adactio.com/journal/15050
  - Or basically any post from Jeremy on the topic https://adactio.com/journal/tags/progressive
- Learn and understand why accessibiilty is a requirement, not a feature
  - https://www.a11yproject.com/

## HTML

- Use HTML to describe content, not to present it visually
- Often when you have a CSS layout problem, you really have an HTML problem. Reconsider your HTML before adding more CSS.
- Don't use `div` for buttons. If it's a link, use an `a` if it's not a link, use a `button` https://css-tricks.com/use-button-element/
- Frameworks and libraries cannot give you anything more than browsers offer. At the end of the day, it all gets compiled to browser HTML.

#### Resources

- https://abookapart.com/products/responsive-web-design
- https://abookapart.com/products/html5-for-web-designers

## CSS

- Frameworks and libraries cannot give you anything more than browsers offer. At the end of the day, it all gets compiled to browser CSS.

### Layout
- Learn the differences and reasons for using; floats, positioning, flexbox, and grid. **They all have uses, none invalidate the others**
- Often when you have a CSS layout problem, you really have an HTML problem. Reconsider your HTML before adding more CSS.

### Responsiveness
- Sorry, I'm linking to my own commit here (Tyler), but this is how to approach breakpoints https://www.reddit.com/r/web_design/comments/111egj/responsive_webdesign_what_sizes_do_i_need_to/c6ih9qq/?context=3

#### Resources

- Flexbox
  - https://flexboxfroggy.com
  - https://philipwalton.github.io/solved-by-flexbox/
  
## JavaScript

- Frameworks and libraries cannot give you anything more than browsers offer. At the end of the day, it all gets compiled to browser JS.
- Learn and understand DOM Scripting https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction

#### Resources

- https://domscripting.com/book (This is old, but still very recommended)