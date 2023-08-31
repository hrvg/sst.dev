---
layout: post
title: Set up Custom Fonts
date: 2017-01-08 00:00:00
lang: en
ref: set-up-custom-fonts
description: To use custom fonts in our React.js project we are going to use Google Fonts and include it in our public/index.html.
comments_id: set-up-custom-fonts/81
---

Custom Fonts are now an almost standard part of modern web applications. We'll be setting it up for our note taking app using [Google Fonts](https://fonts.google.com){:target="_blank"}.

This also gives us a chance to explore the structure of our newly created React.js app.

### Include Google Fonts

For our project we'll be using the combination of a Serif ([PT Serif](https://fonts.google.com/specimen/PT+Serif){:target="_blank"}) and Sans-Serif ([Open Sans](https://fonts.google.com/specimen/Open+Sans){:target="_blank"}) typeface. They will be served out through Google Fonts and can be used directly without having to host them on our end.

Let's first include them in the HTML. Our React.js app is using a single HTML file.

{%change%} Edit `public/index.html` and add the following line in the `<head>` section of the HTML to include the two typefaces.

``` html
<link
  rel="stylesheet"
  type="text/css"
  href="https://fonts.googleapis.com/css?family=PT+Serif|Open+Sans:300,400,600,700,800"
/>
```

Here we are referencing all the 5 different weights (300, 400, 600, 700, and 800) of the Open Sans typeface.

### Add the Fonts to the Styles

Now we are ready to add our newly added fonts to our stylesheets. Create React App helps separate the styles for our individual components and has a master stylesheet for the project located in `src/index.css`.

{%change%} Let's replace the current styles in `src/index.css` for the `body` tag to the following.

``` css
body {
  margin: 0;
  padding: 0;
  color: #333;
  font-size: 16px;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  font-family: "Open Sans", sans-serif;
}
```

{%change%} And let's change the fonts for the header tags to our new Serif font by adding this block to the css file.

``` css
h1, h2, h3, h4, h5, h6 {
  font-family: "PT Serif", serif;
}
```

Now if you just flip over to your browser with our new app, you should see the new fonts update automatically; thanks to the live reloading.

![Custom fonts updated screenshot](/assets/part2/custom-fonts-updated.png)

We'll stay on the theme of adding styles and set up our project with Bootstrap to ensure that we have a consistent UI Kit to work with while building our app.
