# Ribbon.css

*A CSS library for displaying unobtrusive ribbons on your html elements*

---

Ribbon CSS is a standalone CSS resource which allows you to add various small, unobtrusive ribbon-like-banners to any HTML element with minimal additional markup. Instead of using JavaScript, ribbon.css relies on **CSS3 2D transformations** and **pseudo elements** for creating and positioning the ribbons. 

These ribbons are suitable to use on both desktop and mobile web applications to display counts, show date/time information, highlight a certain element, and much more. 

####Example Usage
```html
<div class="ribbon--corner--ne">
	<div class="ribbon">Ribbon Text</div>
</div>
```

## Get Started
####Download
Download one of the 2 library version:

- [unminified] : https://raw.github.com/ejaffe/ribbon.css/master/ribbon.css
- [minified] : https://raw.github.com/ejaffe/ribbon.css/master/ribbon.min.css

####Include
Download ribbon.css and include it in the `<head>` of your webpage:

```html
<link rel="stylesheet" href="ribbon.css"></link>
```
or
```html
<link rel="stylesheet" href="ribbon.min.css"></link>
```
####Use
Each ribbon banner must adhere to the following html structure...

```html
<div class="[ribbon--location--class]">
	<div class="ribbon">Ribbon Text</div>
</div>
```

...where *[ribbon--location--class]* is one of the following:

- `ribbon--corner--nw` <sub><sup>Top Left Corner</sup></sub>
- `ribbon--corner--ne` <sub><sup>Top Right Corner</sup></sub>
- `ribbon--corner--se` <sub><sup>Bottom Right Corner</sup></sub>
- `ribbon--corner--sw` <sub><sup>Bottom Left Corner</sup></sub>
- `ribbon--edge--n` <sub><sup>Top</sup></sub>
- `ribbon--edge--e` <sub><sup>Right</sup></sub>
- `ribbon--edge--s` <sub><sup>Bottom</sup></sub>
- `ribbon--edge--w` <sub><sup>Left</sup></sub>
- `ribbon--full--n` <sub><sup>Full Width Across Top</sup></sub>
- `ribbont--full--s` <sub><sup>Full Width Across Bottom</sup></sub>

####HTML Requirements
The parent in which the ribbon appears needs to have a CSS declaration of either `position:relative` or `position:absolute`, and **cannot** have a CSS declaration of `overflow:hidden`.

##Detailed Usage
####Tweak Position
The ribbons are positioned relative to the parent element. To change positing of all non `ribbon--corner` ribbons, a `top`, `right`, `bottom`, or `left` CSS value can be applied directly to the ribbon:

```html
<div class="ribbon--edge--n" style="left:200px">
	<div class="ribbon">Ribbon Text</div>
</div>
```

```html
<div class="ribbon--edge--w" style="top:100px">
	<div class="ribbon">Ribbon Text</div>
</div>
```

```html
<div class="ribbon--full--n" style="top:50px">
	<div class="ribbon">Ribbon Text</div>
</div>
```

####Add some color

In addition to position and location, ribbon.css also has some built in color options. Simply add any of these class names after the ribbon location class:

- `ribbon--turquoise`
- `ribbon--blue`
- `ribbon--green`
- `ribbon--purple`
- `ribbon--gray`
- `ribbon--ltgray`
- `ribbon--dkgray`
- `ribbon--yellow`
- `ribbon--orange`
- `ribbon--red`
- `ribbon--white`

```html
<div class="ribbon--edge--w ribbon--green" style="top:100px">
	<div class="ribbon">Ribbon Text</div>
</div>
```

If you would prefer to define a custom color, you can do so by adding a css declaration.

per-ribbon: 
```html
<link rel="stylesheet" href="ribbon.min.css"></link>
<style type="text/css">
#my-ribbon .ribbon{
	background-color:#000;
	border-color:#000;
	color:#fff;
}
</style>
<div class="ribbon--corner--ne" id="my-ribbon">
	<div class="ribbon">Ribbon Text</div>
</div>
```
globally:
```html
<link rel="stylesheet" href="ribbon.min.css"></link>
<style type="text/css">
.ribbon{
	background-color:#000;
	border-color:#000;
	color:#fff;
}
</style>
```

Remember that the border color should be the same as the background color because ribbon.css will automatically darken the color of the fold for the 3D effect.

## License
Copyright (c) 2013 Evan Jaffe
Licensed under the [MIT license](http://opensource.org/licenses/MIT).

## Credits
- [Kushagra Gour](https://github.com/chinchang) for his awesome css library, [Hint.css](https://github.com/chinchang/hint.css), that gave me inspiration to write my own CSS library. 
- My employer, [Four Winds Interactive](http://www.fourwindsinteractive.com), for providing the project which drove the conception of this library.
- [Flat UI](http://designmodo.github.io/Flat-UI/) for the hex color scheme.