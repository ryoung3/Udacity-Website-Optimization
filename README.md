## Website Performance Optimization portfolio project

Your challenge, if you wish to accept it (and we sure hope you will), is to optimize this online portfolio for speed! In particular, optimize the critical rendering path and make this page render as quickly as possible by applying the techniques you've picked up in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).


Page load speed optimization

* The images were rescaled and resized to the final layout dimensions.
* For the critical above-the-fold content styles, I inlined them and applied them to the document immediately vs. blocking loading. Below I've included the site to where I found the Google Developer suggested method.
* Defer alternative media CSS: Although the print stylesheets are small, they were deliberately chosen not to be served inline in HTML documents due to at least three different pages using it. A media attribute was added to ensure that it would only be downloaded when printing.
*All CSS and JS files were minified to ensure faster downloading. The original files are still present in their respective directories, without the .min in their filenames.
Frame rate optimization

* Unnecessary JS operations were pulled out of for loops where possible, in views/js/main.js.
* The scroll events were 'debounced' to split the animations and only reflow/repaint when needed.
References
 https://developers.google.com/speed/pagespeed/insights/
 https://developers.google.com/speed/docs/insights/OptimizeCSSDelivery
 http://www.html5rocks.com/en/tutorials/speed/animations/
