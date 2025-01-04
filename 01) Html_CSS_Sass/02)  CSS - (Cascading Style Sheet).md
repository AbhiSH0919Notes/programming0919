# CSS :-
>[!INTRO]- CSS INTRO
>	- 1) CSS was first proposed by **Haakon Whim Lie** on **10 October 1994**.
>	- 2) CSS is used to Styling Webpage. **(CSS is the body of the Skeleton)**

>[!SUMMARY]- **1) We can write CSS in 3 Types:**
>  -
> 	1) Inline CSS :
> 		- Write in HTML Tag Using Style Attribute. `<img src="/path" style="width: 100%; height: auto;">`
> 	2) Internal CSS :
> 		- Write inside HTML head Tag Using style tag. `<style> css </style>`
> 	3) External CSS :
> 		- Write Another External file & link inside head tag. We can use that multiple time. `<link rel="stylesheet" href="/path">`

>[!SUMMARY]- **2) Responsive Design Ingredient:**
>   - 1) Fluid Layout :
>        - 1] Webpage adapt to the current viewport.
>        - 2] Use [ % ], [ vh ] & [ vw ] units.
>        - 3] Use max-width
>   - 2) Responsive Units :
>        - 1] Use rem unit (10px = 1rem)
>        - 2] make it easy to scale the entire layout
>        - 3] use % value in html
>   - 3) Flexible Images :
>        - 1] By default Images are don't scale auto
>        - 2] use % width for images
>   - 4) Media queries :
>        - 1] Only at the end of building a certain page or a certain components.



## Rare Useable Property & Pseudo Classes

| No. | ---Property & Pseudo - classes--- | ---------------------------Use---------------------------                                                                              | -----------Code Attributes-----------                                                                       |
| :-: | --------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------- | :---------------------------------------------------------------------------------------------------------- |
| 01) | ==clip-path-polygon==             | create polygon of object                                                                                                               | `clip-path : polygon(x% y%, x% y%, x% y%, x% y%);`                                                          |
| 02) | ==clip-path-circle==              | create circle of object                                                                                                                | `clip-path : circle(radius at x% y%);`                                                                      |
| 03) | ==box-decoration==                | when text is wrapped then give same gap left of right                                                                                  | `box-decoration-break : clone;`                                                                             |
| 04) | ==pointer-events==                | make some content inaccessible to the mouse & keyboard                                                                                 | `pointer-events : none;`                                                                                    |
| 05) | ==:not(hover)==                   | some content is not hovered then apply style                                                                                           | `img:not(hover) { width : 50% };`                                                                           |
| 06) | ==writting-mode==                 | change text visual style                                                                                                               | `writing-mode : vertical-rl/lr;`                                                                            |
| 07) | ==input:invalid==                 | inputted text are invalidate                                                                                                           | `input:focus : invalid { color : red; }`                                                                    |
| 08) | ==shape-outside==                 | wrap text from outside                                                                                                                 | `shap-outside : circle(50% at 50% 50%);`                                                                    |
| 09) | ==[class^= "classStartName"]==    | select element with class start name                                                                                                   | `div[class^="box-"]`                                                                                        |
| 10) | ==[class$="classEndName"]==       | select element with class end name                                                                                                     | `div[class$="-box"]`                                                                                        |
| 11) | ==flex : grow shrink basis==      | combine 3 property in one property.<br>( When we use overflow scroll on flexbox them must be use `flex-shrink : 0;` on child element ) | `flex : 1 0 19rem;`                                                                                         |
| 12) | ==-webkit-background-clip==       | make text like a gradient                                                                                                              | `background-image : linear-gradient(#999, #333);`<br>`-webkit-background-clip : text; color : transparent;` |
| 13) | ==perspective==                   | use for rotate cards / container                                                                                                       | `perspective : 10rem;`                                                                                      |
| 14) | ==calc width==                    | create auto column adapting width                                                                                                      | `width : calc(2 * ((100% - 2 * 6rem) / 3) + 6rem);`                                                         |
| 15) | ==(hover:none)==                  | use for mobile devices                                                                                                                 | `@media only screen and (hover:none)`                                                                       |
| 16) | ==clearfix==                      | fixing white gap                                                                                                                       | `content : "";` `clear : both;` `display : table;`                                                          |





### Typography System

>[!NOTE]
> 1) font size ( px )
>	10 / 12 / 14 / 16 / 18 / 20 / 24 / 30 / 36 / 44 / 52 / 62 / 74 / 86 / 98
> 2) font weights
>	 default - 400
> 3) colors
>	 Primary / Secondary / Tertiary / Tints / Shades / Accents / Greys
> 4) shadow , border-radius
>	 Primary / Secondary
> 5) spacing system
>	 2 / 4 / 8 /12 /16 / 24 / 32 / 48 / 64 / 80 / 96 / 128

### root variables
```css
/* =====CSS-VARIABLES===== */
:root {
	--primary-color: #eb2f64;
	--primary-color-light: #ff3366;
	--primary-color-dark: #ba265d;

	--grey-color-light-1: #faf9f9;
	--grey-color-light-2: #f4f2f2;
	--grey-color-light-3: #f0eeee;
	--grey-color-light-4: #ccc;

	--grey-color-dark-1: #333;
	--grey-color-dark-2: #777;
	--grey-color-dark-3: #999;

	--shadow-dark: 0 2rem 6rem rgba(0, 0, 0, 0.3);
	--shadow-light: 0 2rem 5rem rgba(0, 0, 0, 0.06);

	--line: 1px solid var(--grey-color-light-2);
}


:root {
	--color-primary: #5ec576;
	--color-secondary: #ffcb03;
	--color-tertiary: #ff585f;
	--color-primary-darker: #4bbb7d;
	--color-secondary-darker: #ffbb00;
	--color-tertiary-darker: #fd424b;
	--color-primary-opacity: #5ec5763a;
	--color-secondary-opacity: #ffcd0331;
	--color-tertiary-opacity: #ff58602d;
	--gradient-primary: linear-gradient(to top left, #39b385, #9be15d);
	--gradient-secondary: linear-gradient(to top left, #ffb003, #ffcb03);
}
```


### General base
```CSS
@import url("https://fonts.googleapis.com/css2?family=Rubik:wght@400;500;600;700&display=swap");

* {
	padding: 0;
	margin: 0;
	box-sizing: border-box;
}

html {
	/* font-size: 10px; */
	/* Percentage is user's browser default font-size setting */
	/* 10 / 16 = 0.625 */
	font-size: 62.5%;
	scroll-behavior: smooth;
	overflow-x: hidden;
	::-webkit-scrollbar {
		width: 5px;
		height: 0px;
	}

	::-webkit-scrollbar-thumb {
		background-color: var(--primary-color);
		border-radius: 100px;
	}

	::-webkit-scrollbar-track {
		background-color: #333;
	}

	::-webkit-inner-spin-button,
	::-webkit-outer-spin-button {
		display: none;
	}

	::selection {
		background-color: transparent;
	}

}

body {
	font-family: "Rubik", sans-serif;
	line-height: 1.1;
	font-weight: 400;
	font-size: 1.8rem;
	color: #555;
	overflow-x: hidden;
	backface-visibility: hidden;
}
```



### Heading
```CSS

/* ===== HEADINGS ===== */

.heading-primary,
.heading-secondary,
.heading-tertiary {
	color: #333;
	font-weight: 700;
	letter-spacing: -0.5px;
}

.heading-primary {
	font-size: 5.2rem;
	font-size: 4.8rem;
	line-height: 1.05;
	margin-bottom: 3.2rem;
	/* word-spacing: 1px; */
}

.heading-secondary {
	font-size: 4.4rem;
	line-height: 1.2;
	margin-bottom: 9.6rem;
}

.subheading {
	display: block;
	font-weight: 500;
	color: #cf711f;
	text-transform: uppercase;
	margin-bottom: 1.6rem;
	letter-spacing: 0.75px;
}

.heading-tertiary {
	font-size: 3rem;
	line-height: 1.2;
	margin-bottom: 3.2rem;
}

```
### Button
```css

/* ===== BUTTONS ===== */

.btn,
.btn:link,
.btn:visited {
	display: inline-block;
	font-weight: 600;
	padding: 1.6rem 3.2rem;
	border-radius: 9px;
	text-decoration: none;

	transition: all 0.3s;

	/* This is neccesary for the btn in CTA form section */
	border: none;
	cursor: pointer;
	font-family: inherit;
	font-size: inherit;
}

.btn-full:link,
.btn-full:visited {
	background-color: #e67e22;
	color: #fff;
	/* font-family: serif; */
}

.btn-full:hover,
.btn-full:active {
	background-color: #cf711f;
	color: #fff;
}

.btn-outline:link,
.btn-outline:visited {
	background-color: #fff;
	color: #555;
}

.btn-outline:hover {
	background-color: #fdf2e9;
	box-shadow: inset 0 0 0 3px #fff;
}

```

### @media query - Pixel Ratio & Min Resolution
```css
/* ========================Pixel ratio and Resolution======================== */

@media only screen and (-webkit-min-device-pixel-ratio: 2) and (min-width: 37.5em),
  only screen and (min-resolution: 192dpi) and (min-width: 37.5em),
  only screen and (min-width: 125em) {
  .header {
    background-image: linear-gradient(
        to right bottom,
        rgba(126, 213, 111, 0.8),
        rgba(40, 180, 133, 0.8)
      ),
      url("../img/hero.jpg");
    background-position: top;
    background-size: cover;
    background-repeat: no-repeat;
  }
}

@media (-webkit-min-device-pixel-ratio: 2) and (min-width: 37.5em),
  (min-resolution: 192dpi) and (min-width: 37.5em),
  (min-width: 125em) {
  .section-features {
    background: linear-gradient(
        to bottom right,
        rgba(126, 213, 111, 0.8),
        rgba(40, 180, 133, 0.8)
      ),
      url("../img/nat-4-large.jpg");
    background-size: cover;
    background-position: center;
  }
}
```

### @support browser code
```css
@supports (-webkit-clip-path: polygon(0 0)) or (clip-path: polygon(0 0)) {
  .header {
    -webkit-clip-path: polygon(0 0, 100% 0, 100% 75vh, 0 100%);
    clip-path: polygon(0 0, 100% 0, 100% 75vh, 0 100%);
    height: 95vh;
  }
}
```


### background mask image (icon)
```css
item::before {
		content: "";
		display: inline-block;
		width: 1rem;
		height: 1rem;
		margin-right: 0.7rem;

		/* OLDER BROWSER */
		background-image: url("../img/icons/chevron-thin-right.svg");
		background-size: cover;

		/* NEWER BROWSER MASK */
		/* __set background image or icons how's look-(mask-image) */
		@supports (-webkit-mask-image: url()) or (mask-image: url()) {
			background-color: var(--primary-color);
			-webkit-mask-image: url(../img/icons/chevron-thin-right.svg);
			-webkit-mask-size: cover;
			mask-image: url(../img/icons/chevron-thin-right.svg);
			mask-size: cover;
			background-image: none;
		}
	}
```





### grid systems
```css
<div class="container">
  <div class="header">header</div>
  <div class="box-0">box-0</div>
  <div class="box-1">box 1</div>
  <div class="box-2">box 2</div>
  <div class="side">side</div>
  <div class="main">main</div>
  <div class="foot">foot</div>
</div>

/* GRID AREA NAMEING SYSTEM========USE ONLY SMALL LAYOUTS============ */
.container {
display: grid;
grid-template-columns: repeat(3, 1fr) 200px;
grid-template-rows: 100px 200px 400px 100px;
gap: 30px;
grid-template-areas: "head head head head"
					"box-0 box-1 box-2 side"
					"main main main side"
					"foot foot foot foot";
}

/* GRID ROWS & COLUMNS = (LINES) NAMING SYSTEM======================= */
.container {
display: grid;
grid-template-columns: [grid-start] repeat(3, 1fr) [grid-side] 200px [grid-end];
grid-template-rows: [head-start] 100px [head-end box-start] 200px [box-end main-start] 400px [main-end foot-start] 100px [foot-end];
gap: 30px;
}

 /* =================MINMAX, AUTO-FILL & AUTO-FIT FUNCTION========================= */
  /* text overflow fixing with minmax function */
.container {
  display: grid;
  grid-template-rows: repeat(2, minmax(100px, min-content));
  grid-template-columns: minmax(150px, 2fr) repeat(3, 1fr);
  grid-template-columns: repeat(auto-fill, 100px);
  grid-template-columns: repeat(auto-fit, 100px);
  grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
  grid-template-columns: repeat(auto-fit, minmax(max-content, 1fr));
  grid-auto-rows: 150px;
}

```
