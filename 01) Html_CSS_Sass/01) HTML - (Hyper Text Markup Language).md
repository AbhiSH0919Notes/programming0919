
# Html -:
>[!INTRO]- HTML INTRO
 >  1) First version of HTML was written by **Tim Berners-Lee** in **1993**.
 >  2) HTML is used to **create structure of webpage.** **(HTML is the Skeleton of the body)**
 >  3) **HTML5 is standard version** of HTML from** 2014**.
 >  4) HTML HAVE 2 TYPES OF TAGS:
 > 	 1) **Paired Tags** :- We need open & close tag. - (`<div> </div>`)
 > 	 2) **Singular Tags** :- We don't need to close tag.  - (`<img src="./path" class="img">`)
 > - **Graphical overview of HTML Syntax**
 > ![600](HtmlSyntax.jpg)
 
 



| No. | -----Tag Name----- | --------Use cases-----------      | ------------------------------------------Syntax-code--------------------------------------                   |
| :-: | :----------------- | :-------------------------------- | :------------------------------------------------------------------------------------------------------------ |
| 01) | ==cite==           | Showing Author Name               | ` <cite> name </cite> `                                                                                       |
| 02) | ==article==        | Blog Post Article                 | ` <article> <> code </> </article> `                                                                          |
| 03) | ==aside==          | Article Related Post              | ` <aside> code </aside> `                                                                                     |
| 04) | ==details==        | Showing Inner Details             | ` <details> code </details> `                                                                                 |
| 05) | ==audio==          | Play Audio                        | ` <audio src="filename" autostart="true" hidden="false" loop="false" controls="" > <source src=""> </audio> ` |
| 06) | ==embed==          | Embedding content/code            | ` <embed src="filename" /> `                                                                                  |
| 07) | ==form==           | Get user data or send to server   | ` <form method="post/get" action="filename" target="_blank/_self/_parent/_top"> <code/> </form> `             |
| 08) | ==fieldset==       | Form fields                       | ` <fieldset> <legend> 1st field </legend> <input type="text" name="" id=""> </fieldset> `                     |
| 09) | ==hgroup==         | Wrap one or more heading elements | ` <hgroup> <h1>title</h1> <h2>subtitle</h2> </hgroup> `                                                       |
| 10) | ==comment==        | Commenting Content                | `<comment> xyz </comment>`                                                                                    |
| 11) | ==frameset==       | Add other website/webpage         | `<frameset width="" height=""> </frameset>`                                                                   |
| 12) | ==applet==         |                                   |                                                                                                               |
| 13) | ==object==         |                                   |                                                                                                               |
| 14) | ==acronym==        |                                   |                                                                                                               |
| 15) | ==var==            |                                   |                                                                                                               |
| 16) | ==legend==         |                                   |                                                                                                               |
| 17) | ==canvas==         |                                   |                                                                                                               |
| 18) | ==outut==          |                                   |                                                                                                               |
| 19) | ==ruby==           |                                   |                                                                                                               |
| 20) | ==time==           |                                   |                                                                                                               |
| 21) | ==mark==           |                                   |                                                                                                               |

### Density switching (*Images according to screen resolutions*)
```html
	   <!-- density-switching = small screen - low resolution & large screen - high resolution (300 is the image width for small screen & 1000 is the large screen width, & w is same as x : small or large screen) -->

             <!-- 300 and 1000 = proper image width in pixel -->
              <!-- sizes = 20vw or 30vw these value comes are proper image width(in media:900px) / 900px or 600px -->
            <img class="composition_photo composition_photo-p1 photo"
                srcset="resources/img/nat-1.jpg 300w, resources/img/nat-1-large.jpg 1000w"
                sizes="(max-width:56.25em) 20vw, (max-width:37.5em) 30vw, 300px" alt="photo-1" src="resources/img/nat-1-large.jpg">
```


### Art direction (*Different images for different viewport*)
```html
		<picture class="footer__logo">
                <!-- media=__Art Direction__ = Different images for different viewport (browser automatically choose required image) -->
                <!-- srcset="img-path orignal img width(w = 1x or 2x)" -->
                <source srcset="resources/img/logo-green-small-1x.png 1x, resources/img/logo-green-small-2x.png 2x" media="(max-width:37.5em)">

                <!-- srcset__Density Switching__ = Get the high resolution & low resolution images according to viewport (1x or 2x is density descripter) -->
                <img srcset="resources/img/logo-green-1x.png 1x, resources/img/logo-green-2x.png 2x" alt="Full-logo"
                    src="resources/img/logo-green-2x.png">
		</picture>
```





















