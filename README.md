# Marketing Website Refactor

## Description

This week's challenge is to get some experience reading and refactoring someone else's code.

| Scenario | A fictional company, Horiseon, has hired me to refactor their HTML and CSS code to improve their site's accessibility. |
| -------- | --- |

### Scenario:

A fictional company, Horiseon, has hired me to refactor their HTML and CSS code to improve their site's accessibility.

### How I approached the problem:

#### Semantic Elements

The initial codebase included a lot of non-semantic elements in the HTML, so I went ahead and updated those to semantic elements. As a style reference, I used the [W3Schools semantic elements article](https://www.w3schools.com/html/html5_semantic_elements.asp) in addition to some general Googling.

Original code example

```html
<div class="header">...</div>
<div class="hero"></div>
<div class="content">
  <div class="search-engine-optimization">...</div>
  <div id="online-reputation-management" class="online-reputation-management">...</div>
  <div id="social-media-marketing" class="social-media-marketing">...</div>
</div>
```

Refactored code

```html
<header>...</header>
<figure class="hero"></figure>
<section class="content">
  <article class="search-engine-optimization" id="search-engine-optimization">...</article>
  <article class="online-reputation-management" id="online-reputation-management">...</article>
  <article class="social-media-marketing" id="social-media-marketing">...</article>
</section>
```

This change naturally required updates to the associated CSS selectors, but it also afforded an opportunity to remove some redundancies within the stylesheet.

Original code example

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

Refactored code

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

#### Alt text

`<img>` elements in the initial codebase did not include any alt attributes. I added them in accordance with accessibility guidelines.

In my opinion, none of the images on the page provide "necessary information," so I have purposefully left the alt attributes empty.

> Beyond including "necessary information," the discussion around how best to use alt text seems to largely come down to personal preference. As a person who does not currently use a screen reader, I have questions about the experience of using one and would like to try it out. For example, given that purely decorative image is meant to improve the visual experience, does the inclusion of decorative alt text similarly improve a reading experience? In that vein, should alt properties of decorative images be about tone and message rather than a literal description? Should the hero image in this project have an alt text along the lines of "our team is working hard to meet your goals."

The refactoring should not have affected the appearance of the site or the user experience. For reference, the provided mockup (built from the initial codebase) is here:

![Mockup of the site with the initial codebase](https://ucb.bootcampcontent.com/UCB-Coding-Bootcamp/UCB-VIRT-FSF-FT-03-2023-U-LOLC/-/raw/main/course-content/01-html-git-css/challenge/Assets/01-html-css-git-homework-demo.png "Horiseon Site Mockup")

## Credits

I referenced all of the following:
https://www.w3schools.com/html/html5_semantic_elements.asp
https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Organizing#tips_to_keep_your_css_tidy
https://codeguide.co/

## License

The last section of a good README is a license.
This lets other developers know what they can and cannot do with your project.
If you need help choosing a license, use
[https://choosealicense.com/](https://choosealicense.com/) --- 🏆 The sections
listed above are the minimum for a good README, but your project will ultimately
determine the content of this document. You might also want to consider adding
the following sections.
