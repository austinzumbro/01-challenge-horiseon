# Marketing Website Refactor

## Description

This week's challenge is to get some experience reading and refactoring someone else's code.

| **Scenario** | *A fictional marketing company, Horiseon, has hired me to refactor their site's HTML and CSS to improve accessibility.* |
| :--- | :--- |

Let's get to it!

### My Approach
---

#### Semantic Elements

The initial codebase included a lot of non-semantic elements in the HTML, so I went ahead and updated those to semantic elements. As a style reference, I used the [W3Schools semantic elements article](https://www.w3schools.com/html/html5_semantic_elements.asp) in addition to some general Googling.

**Original code example**

```html
<div class="header">...</div>
<div class="hero"></div>
<div class="content">
  <div class="search-engine-optimization">...</div>
  <div id="online-reputation-management" class="online-reputation-management">...</div>
  <div id="social-media-marketing" class="social-media-marketing">...</div>
</div>
```

**Refactored code**

```html
<header>...</header>
<figure class="hero"></figure>
<section class="content">
  <article class="search-engine-optimization" id="search-engine-optimization">...</article>
  <article class="online-reputation-management" id="online-reputation-management">...</article>
  <article class="social-media-marketing" id="social-media-marketing">...</article>
</section>
```
---

#### CSS

The above changes required updates to the associated CSS selectors, but it also afforded an opportunity to remove some redundancies within the stylesheet. And while I was doing that, I discovered a few fonts and colors that could be applied more globally to further reduce repetition.

**Original code example**

```css
.benefit-lead {
  margin-bottom: 32px;
  color: #ffffff;
}

.benefit-brand {
  margin-bottom: 32px;
  color: #ffffff;
}

.benefit-cost {
  margin-bottom: 32px;
  color: #ffffff;
}

/* etc, etc. */

.search-engine-optimization {
  margin-bottom: 20px;
  padding: 50px;
  height: 300px;
  font-family: "Gill Sans", "Gill Sans MT", Calibri, "Trebuchet MS", sans-serif;
  background-color: #0072bb;
  color: #ffffff;
}

.online-reputation-management {
  margin-bottom: 20px;
  padding: 50px;
  height: 300px;
  font-family: "Gill Sans", "Gill Sans MT", Calibri, "Trebuchet MS", sans-serif;
  background-color: #0072bb;
  color: #ffffff;
}

.social-media-marketing {
  margin-bottom: 20px;
  padding: 50px;
  height: 300px;
  font-family: "Gill Sans", "Gill Sans MT", Calibri, "Trebuchet MS", sans-serif;
  background-color: #0072bb;
  color: #ffffff;
}
```

**Refactored code**

```css
body {
  background-color: #d9dcd6;
  color: #ffffff;
}

section,
aside,
nav {
  font-family: "Gill Sans", "Gill Sans MT", Calibri, "Trebuchet MS", sans-serif;
}

/* etc, etc. */

.content article {
  margin-bottom: 20px;
  padding: 50px;
  height: 300px;
  background-color: #0072bb;
}

.benefits article {
  margin-bottom: 32px;
}
```
---

#### Alt text

`<img>` elements in the initial codebase did not include any alt attributes. I added them in accordance with accessibility guidelines.

In my opinion, none of the images on the page provide "necessary information," so I have purposefully left the alt attributes empty.

> Side note: beyond including "necessary information," guidance around  alt text usage and inclusion appears to come down to personal preference. As someone who does not currently use a screen reader, I have questions about the experience of using one and would like to try it out to learn more. For example, if purely decorative images are meant to improve the visual experience of a site, does the inclusion of decorative alt text similarly improve the reading experience? In that vein, should alt properties of decorative images be more about tone and message rather than a literal description? For example, perhaps the hero image in this project should have alt text like, "Our team is working hard to meet your goals."

---

#### Odds and Ends

- I fixed a broken link in the navigation menu.
- I reordered some `class` and `id` attributes.

Generally, the refactoring should not have affected the appearance of the site or the user experience. 

For reference, the provided mockup (built from the initial codebase) is here:

![Mockup of the site with the initial codebase](./preview-images/horiseon-old.png "Horiseon Site Mockup")

And the updated site:

![Preview of site with updated codebase](./preview-images/horiseon-page-scroll.gif "Horiseon Site Updated Scroll")

## Credits

I referenced all of the following:    
https://www.w3schools.com/html/html5_semantic_elements.asp   
https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Organizing#tips_to_keep_your_css_tidy    
https://codeguide.co/    

## License

MIT License

Copyright (c) 2023 Austin Zumbro

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.