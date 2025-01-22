## SASS Features
| No. | -------------Feature-Name-------------                                                                            | ------------------------------Use------------------------------ | ----------------------Code---------------------- |
| :-: | ----------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------- | ------------------------------------------------ |
| 1)  | ==**Variables**==                                                                                                 | Declare value in variables (Reusable values)                    | `$primary_color: #fff;`                          |
| 2)  | ==**Nesting**==                                                                                                   | Style child element inside Parent selector/element.             | `&__classname { color: $primary_color; }`        |
| 3)  | ==**@extend**==                                                                                                   | Inherit style from one selector to other selector.              | `@extend selectorName;`                          |
| 4)  | ==**@import**==                                                                                                   | Import multiple files in one file.                              | `@import "filepath";`                            |
| 5)  | ==**Mixins**==                                                                                                    | Create style component/block & reuse them as they want.         | `@include mixinName;`                            |
| 6)  | ==**Operators**==<br>*- 1) Number Operator*<br>*- 2) Logical Operator*<br>*- 3) Control directives & expressions* | For mathematical operations right inside of CSS.                |                                                  |
| 7)  | ==Functions==                                                                                                     | Similar to mixins : produce a value                             |                                                  |
| 8)  | ==Control directives==                                                                                            | For writing complex code using conditionals & loops             |                                                  |



### Variables
```SCSS
// COLORS

$primary-color: #55c57a;
$primary-color-light: #7ed56f;
$primary-color-dark: #28b485;

$secondary-color-light: #ffb900;
$secondary-color-dark: #ff7730;

$tertiary-color-light: #2998ff;
$tertiary-color-dark: #5643fa;

$color-gray-light-1: #f7f7f7;
$color-gray-light-2: #eee;
$grey-light-1: #faf9f9;
$grey-light-2: #f4f2f2;
$grey-light-3: #f0eeee;
$grey-light-4: #ccc;

$grey-dark-1: #333;
$grey-dark-2: #777;
$grey-dark-3: #999;

$color-white: #fff;
$color-black: #000;

// SHADOW
$shadow-primary: 0 1.5rem 4rem rgba($color-black, 0.15);

// GRID
$grid-width: 120rem;
$gutter-horizontal: 3rem; // (==column-gap==)
$gutter-vertical: 8rem; // (==row-gap==)
$gutter-vertical-small: 6rem; // (==row-gap==)

```



### @mixin Media query
```SCSS
/*
  // =====MEDIA-QUERY-MANAGER=====$BREAKPOINT-ARGUMENT-CHOISES=====
	  - 0-420PX			:	SMALL-PHONE
      - 420-600PX    	:   PHONE
      - 600-900PX    	:   TAB-PORT
      - 900-1200PX   	:   TAB-LAND
      - 1200-1800PX  	:   NORMAL STYLE
      - 1800PX+      	:   BIG-DESK
*/

// ===========ITS THE REGULAR @MIXIN TRICK=================
@mixin respond-phone {
	@media only screen and (max-width: 600px) {
		@content;
	}
}

// ===========@MIXIN FUNCTINALITY QUERY CREATE=================
@mixin respond($breakpoint) {
	@if $breakpoint == small-phone {
		// WIDTH < 420PX
		@media only screen and (max-width: 26.25em) {
			@content;
		}
	}

	@if $breakpoint == phone {
		// WIDTH < 600PX
		@media only screen and (max-width: 37.5em) {
			@content;
		}
	}

	@if $breakpoint == tab-port {
		// WIDTH < 900PX
		@media only screen and (max-width: 56.25em) {
			@content;
		}
	}

	@if $breakpoint == tab-land {
		// WIDTH < 1200PX
		@media only screen and (max-width: 75em) {
			@content;
		}
	}

	@if $breakpoint == big-desk {
		// WIDTH > 1800PX
		@media only screen and (min-width: 112.5em) {
			@content;
		}
	}
}

// ===========@MIXIN FUNCTINALITY QUERY USE=================
@include respond(tab-land) {
	// WIDTH < 1200PX = 75em
	font-size: 56.25%; // 1rem = 9px; 9/16 = 56.25%;
}

```

### responsive grid columns
```SCSS
.container {
	max-width: 160rem;

	display: grid;
	grid-template-rows:
		90vh min-content minmax(min-content, 40vw)
		repeat(3, min-content);

	grid-auto-rows: min-content;

	grid-template-columns:
		[sidebar-start] 8rem [sidebar-end full-start]
		minmax(6rem, 1fr) [center-start]
		repeat(8, [col-start] minmax(min-content, 14rem) [col-end])
		[center-end] minmax(6rem, 1fr) [full-end];

	//===MEDIA-QUERY-FOR-1000PX===
	@media only screen and (max-width: $bp-large) {
		grid-template-rows:
			6rem minmax(50rem, 80vh) min-content minmax(min-content, 40vw)
			repeat(3, min-content);

		grid-template-columns:
			[full-start]
			minmax(6rem, 1fr) [center-start]
			repeat(8, [col-start] minmax(min-content, 14rem) [col-end])
			[center-end] minmax(6rem, 1fr) [full-end];
	}

	@media only screen and (max-width: $bp-medium) {
		grid-template-rows: 6rem minmax(55rem, calc(100vh - 6rem));
	}

	@media only screen and (max-width: $bp-micro) {
		grid-template-columns:
			[full-start]
			minmax(2rem, 1fr) [center-start]
			repeat(6, [col-start] minmax(min-content, 14rem) [col-end])
			[center-end] minmax(2rem, 1fr) [full-end];
	}
}
```
