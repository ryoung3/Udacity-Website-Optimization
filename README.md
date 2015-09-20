## Website Performance Optimization portfolio project

Your challenge, if you wish to accept it (and we sure hope you will), is to optimize this online portfolio for speed! In particular, optimize the critical rendering path and make this page render as quickly as possible by applying the techniques you've picked up in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).


Page load speed optimization

Image compression: images were rescaled and resized to the final layout dimensions.
Inline critical CSS: critical above-the-fold content styles are inlined and applied to the document immediately vs. blocking loading. This was done using the methods prescribed by Google Developers (see references).
Defer alternative media CSS: print stylesheets, although small, were deliberately chosen not to be served inline in HTML documents due to at least three different pages using it. A media attribute was added to ensure that it would only be downloaded when printing.
Minifying CSS/JS: all CSS and JS files were minified--but not obfuscated--to ensure faster downloading. The formatted and indented files are still present in their respective directories, without the .min in their filenames.
Frame rate optimization

Loop optimization: unnecessary JS operations were pulled out of for loops where possible, in views/js/main.js.
Debouncing: scroll events were 'debounced' to decouple the animations and only reflow/repaint when needed.

 
