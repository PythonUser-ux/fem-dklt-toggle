# Functional Requirements and Notes

Light/Dark Mode toggle -- takes system pref by default, but can override with toggle

What HTML markup (accessible) -- https://scottaohara.github.io/a11y_styled_form_controls/src/radio-button--switch/

Use fieldset, legend, radio inputs

Switching between light/dark modes via JS and Prefers-color-scheme media query -- https://developer.mozilla.org/en-US/docs/Web/CSS/@media/prefers-color-scheme

https://piccalil.li/tutorial/create-a-user-controlled-dark-or-light-mode/

Three option toggle: light/dark/system pref -- https://codepen.io/renddrew/pen/bRomab?editors=1100

CSS Variables (custom properties) -- https://css-tricks.com/updating-a-css-variable-with-javascript/

Accessibility

- Use correct heading tags
- Screenreader-only text for card titles/username -- https://www.accessibility-developer-guide.com/examples/hiding-elements/visually/

NVDA hotkeys:
https://webaim.org/resources/shortcuts/nvda

- Ctrl will stop speech immediately
- Caps Lock is NVDA key
- NVDA + Q will quit NVDA
- NVDA + B will read entire page from top to bottom
- Press H to navigate through headline tags (other elements have hotkeys)
- D will navigate through region/landmark
  - Landmarks/region are recognized by <header> or <main> tags, role="rolename" or aria-label
  - When NVDA recognizes a landmark/region, if no role or aria-label, it will read the first content
- Press NVDA + down arrow to narrate rest of page from current position
- Pressing Shift + H will navigate backwards
- Go to Top?
- Skip to content?

Outline for video:

- Accessibility overview
- Install NVDA
  - basic controls, Ctrl, navigating headlines and regions and down
- SaraSoueidan.com website
- Try to read FEM site
- Add:
  - title, fill in "yout name here" in footer
  - role="contentinfo" to footer
  - aria-label="" for platform overview and platform details
  - Add screenreader-only h3 tags for card titles

--

Semantic HTML and accessibility -- https://www.youtube.com/watch?v=qSNUi7pRmWg
Inclusive cards -- https://inclusive-components.design/cards/

-------------------------------------------------------------------------------------------------
The Gulp workflow is useful for possible future mantainance-related issues with scss
install gulp using *npm install gulp-cli -g* -g ensures that the installation is global so that gulp can be used from any folder
for this project we run *npm install @babel/core @babel/preset-env postcss autoprefixer browsers-sync cssnano dart-sass gulp gulp-babel gulp-postcss gulp-sass gulp-terser sass*
where:
<br>
@babel/core: Core functionality for Babel, a JavaScript compiler that allows you to use next-generation JavaScript features in your code.<br>
@babel/preset-env: A Babel preset that enables the use of the latest ECMAScript features based on the environments you are targeting.<br>
postcss: A tool for transforming styles with JavaScript plugins, often used for tasks like autoprefixing and minification.<br>
autoprefixer: A PostCSS plugin that adds vendor prefixes to your CSS to ensure cross-browser compatibility.<br>
browser-sync: A tool for live-reloading and synchronizing browsers during development.<br>
cssnano: A PostCSS plugin that optimizes and minifies CSS.<br>
dart-sass: Dart Sass, the Dart implementation of Sass, which is a popular CSS preprocessor.<br>
gulp: A task runner that allows you to automate various tasks in your development workflow.<br>
gulp-babel: A Gulp plugin for transpiling JavaScript using Babel.<br>
gulp-postcss: A Gulp plugin for running PostCSS tasks.<br>
gulp-sass: a Gulp plugin that allows you to compile Sass or SCSS files into regular CSS.<br>
gulp-terser: to optimize and minify Javascript.<br>
sass: sass itself
<br>
"Transpiling"<br>
is a term that combines "transform" and "compile." It refers to the process of taking source code written in one programming language (often a newer or alternative version) and converting it into equivalent code in another language, typically an older version or a more widely supported format.
<br><br>
"Autoprefixing"<br>
The need for autoprefixing arises because different browsers may support a CSS property or feature, but they might require different vendor-specific prefixes to apply that feature. Some common vendor prefixes include -webkit-, -moz-, and -ms-. Autoprefixing simplifies the task of writing cross-browser-compatible CSS by automatically adding these prefixes based on the specified rules and the browsers you want to support.
For example, consider the CSS property display: flex;, which is used to enable Flexbox layout. Different browsers might require different prefixes for this property:<br>
WebKit-based browsers (Chrome, Safari): -webkit-<br>
Mozilla Firefox: -moz-<br>
Microsoft Edge: -ms-<br><br>

use *npm audit* to check for security vulnerabilities among the packages and *npm audit fix* to fix them unsless a manual review is needed.
