# Marketing Website Refactor

## Description 

This week's challenge is to get some experience reading and refactoring someone else's code. 

A fictional company, Horiseon, has hired me to refactor their HTML and CSS code to improve their site's accessibility. 

The initial codebase included a lot of non-semantic elements in the HTML. These have now been updated to semantic elements. As a style reference, I used the [W3Schools semantic elements article](https://www.w3schools.com/html/html5_semantic_elements.asp) in addition to general Googling.

<img> elements in the initial codebase did not include any alt attributes. For accessibility reasons, these have been added. As none of the images provide necessary information, their alt attributes have intentionally been left empty.

Additionally, the CSS file contained a number of repetitious and/or redundant entries. I have cleaned these up and reorganized them to better match the semantic order of the HTML. To further avoid unnecessary repetition, I have also centralized font and color attributes.

Regarding the CSS, because the exercise was to emphasize readability of code, I opted to include what may be "overly specific" tags. Specifically I chose to use **figure.hero**, **section.content**, and **aside.benefits** when only the class names would have sufficed. I do not believe this is considered to be best practice, but I do think it made the code more pleasant to read. 

## Usage 

Simply navigate to the webpage to load the site. The refactoring should not have affected the appearance of the site or the user experience.

For your reference, the provided mockup (built from the initial codebase) is here:
![Mockup of the site with the initial codebase](https://ucb.bootcampcontent.com/UCB-Coding-Bootcamp/UCB-VIRT-FSF-FT-03-2023-U-LOLC/-/raw/main/course-content/01-html-git-css/challenge/Assets/01-html-css-git-homework-demo.png "Horiseon Site Mockup")


## Credits

I referenced all of the following:
https://www.w3schools.com/html/html5_semantic_elements.asp
https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Organizing#tips_to_keep_your_css_tidy
https://codeguide.co/


## License

The last section of a good README is a license. This lets other developers know what they can and cannot do with your project. If you need help choosing a license, use [https://choosealicense.com/](https://choosealicense.com/)


---

🏆 The sections listed above are the minimum for a good README, but your project will ultimately determine the content of this document. You might also want to consider adding the following sections.

## Badges

![badmath](https://img.shields.io/github/languages/top/nielsenjared/badmath)

Badges aren't _necessary_, per se, but they demonstrate street cred. Badges let other developers know that you know what you're doing. Check out the badges hosted by [shields.io](https://shields.io/). You may not understand what they all represent now, but you will in time.

## Features

If your project has a lot of features, consider adding a heading called "Features" and listing them there.

## Contributing

If you created an application or package and would like other developers to contribute it, you will want to add guidelines for how to do so. The [Contributor Covenant](https://www.contributor-covenant.org/) is an industry standard, but you can always write your own.

## Tests

Go the extra mile and write tests for your application. Then provide examples on how to run them.

---

© 2022 Trilogy Education Services, LLC, a 2U, Inc. brand. Confidential and Proprietary. All Rights Reserved.
