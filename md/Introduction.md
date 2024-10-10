# Introduction

Responsive design isn't the first approach to designing websites. In the years before responsive design, web designers and developers tried many different techniques.

## Early design choices

Developers built websites that were either [fixed-width](https://web.dev/learn/design/intro?continue=https%3A%2F%2Fweb.dev%2Flearn%2Fdesign%2F%23article-https%3A%2F%2Fweb.dev%2Flearn%2Fdesign%2Fintro#fixed-width_design) or [liquid layouts](https://web.dev/learn/design/intro?continue=https%3A%2F%2Fweb.dev%2Flearn%2Fdesign%2F%23article-https%3A%2F%2Fweb.dev%2Flearn%2Fdesign%2Fintro#liquid_layouts).

## Fixed-width design

In the early 1990s, when the web was first becoming popular, most monitors had screen dimensions of 640 pixels wide by 480 pixels tall.
In the formative days of early web design, it was a safe bet to design web pages with a width of 640 pixels.

## [Liquid layouts](https://web.dev/learn/design/intro?continue=https%3A%2F%2Fweb.dev%2Flearn%2Fdesign%2F%23article-https%3A%2F%2Fweb.dev%2Flearn%2Fdesign%2Fintro#liquid_layouts)

While the majority of designers used fixed-width layouts, some chose to make their layouts flexible. Instead of using fixed widths for your layouts you could make a flexible layout using percentages for your column widths. These designs work in more situations than a fixed-width layout that only looks right at one specific size.

## [Separate sites](https://web.dev/learn/design/intro?continue=https%3A%2F%2Fweb.dev%2Flearn%2Fdesign%2F%23article-https%3A%2F%2Fweb.dev%2Flearn%2Fdesign%2Fintro#separate_sites)

One option is to make a separate subdomain for mobile visitors. But then you have to maintain two separate codebases and designs.

## [Adaptive layouts](https://web.dev/learn/design/intro?continue=https%3A%2F%2Fweb.dev%2Flearn%2Fdesign%2F%23article-https%3A%2F%2Fweb.dev%2Flearn%2Fdesign%2Fintro#adaptive_layouts)

Instead of having separate sites on different subdomains, you could have a single site with two or three fixed-width layouts.

Adaptive design allowed designers to provide layouts that looked good at a few different sizes, but the design never looked quite right when viewed between those sizes. The problem of excess space persisted although it wasn't as bad as in a fixed-width layout.

## [Responsive web design](https://web.dev/learn/design/intro?continue=https%3A%2F%2Fweb.dev%2Flearn%2Fdesign%2F%23article-https%3A%2F%2Fweb.dev%2Flearn%2Fdesign%2Fintro#responsive_web_design)

If adaptive layouts are a mashup of media queries and fixed-width layouts, responsive web design is a mashup of media queries and liquid layouts.
The term was coined by [Ethan Marcotte](https://ethanmarcotte.com/) in [an article in A List Apart](https://alistapart.com/article/responsive-web-design/) in 2010.

Ethan defined three criteria for responsive design:

1. Fluid grids
2. Fluid media
3. Media queries

The layout and images of a responsive site would look good on any device. But there was one problem.

## [A meta element for viewport](https://web.dev/learn/design/intro?continue=https%3A%2F%2Fweb.dev%2Flearn%2Fdesign%2F%23article-https%3A%2F%2Fweb.dev%2Flearn%2Fdesign%2Fintro#a_meta_element_for_viewport)

Browsers on mobile phones had to deal with websites that were designed with fixed-width layouts for wider screens. By default mobile browsers assumed that 980 pixels was the width that people were designing for (and they weren't wrong). So even if you used a liquid layout, the browser would apply a width of 980 pixels and then scale the rendered web page down to the actual width of the screen.

If you use responsive design, you need to tell the browser not to do that scaling. You can do that with a meta element in the head of the web page:

<meta name="viewport" content="width=device-width, initial-scale=1">

There are two values, separated by commas. The first one is width=device-width. This tells the browser to assume the width of the website is the same as the width of the device (instead of assuming the width of the website is 980 pixels). The second value is initial-scale=1. This tells the browser how much or how little scaling to do. With a responsive design, you don't want the browser to do any scaling at all.

### [Modern responsive design](https://web.dev/learn/design/intro?continue=https%3A%2F%2Fweb.dev%2Flearn%2Fdesign%2F%23article-https%3A%2F%2Fweb.dev%2Flearn%2Fdesign%2Fintro#modern_responsive_design)

Now, we can make websites that are responsive in ways far beyond viewport sizes. Media features give developers access to user preferences and enable customized experiences. Container queries enable components to own their own responsive information. The picture element empowers designers to make art-direction decisions based on screen ratios.

## [Check your understanding](https://web.dev/learn/design/intro?continue=https%3A%2F%2Fweb.dev%2Flearn%2Fdesign%2F%23article-https%3A%2F%2Fweb.dev%2Flearn%2Fdesign%2Fintro#check_your_understanding)

Test your knowledge of responsive web design
