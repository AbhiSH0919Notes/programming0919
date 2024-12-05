### Box Gallery - HTML
```html
  <div class="gallery">

            <figure class="gallery-item">

              <img src="resourses/img/gallery/gallery-1.jpg" alt="gallery-meals-photo" />

            </figure>
  </div>
```


### Box Gallery - CSS
```css

.gallery {
	display: grid;
	grid-template-columns: repeat(3, 1fr);
	background-color: #ffa500;
	gap: 1rem;
	padding: 1rem;
	align-content: start;
}

.gallery-item {
	overflow: hidden;
}

.gallery-item img {
	display: block;
	width: 100%;
	height: auto;
	transition: all 0.4s;
	/* transform: scale(1.5); */
}

.gallery-item img:hover {
	transform: scale(1.2);
	/* opacity: 0.6; */
}
```






### grid gallery - HTML
```html
  <section class="gallery">

        <figure class="gallery__item gallery__item--1">

            <img src="resources/img/gallery/gal-1.jpeg" alt="gallery image 1" class="gallery__img" />

        </figure>

        <figure class="gallery__item gallery__item--2">

            <img src="resources/img/gallery/gal-2.jpeg" alt="gallery image 2" class="gallery__img" />

        </figure>

        <figure class="gallery__item gallery__item--3">

            <img src="resources/img/gallery/gal-3.jpeg" alt="gallery image 3" class="gallery__img" />

        </figure>

        <figure class="gallery__item gallery__item--4">

            <img src="resources/img/gallery/gal-4.jpeg" alt="gallery image 4" class="gallery__img" />

        </figure>

        <figure class="gallery__item gallery__item--5">

            <img src="resources/img/gallery/gal-5.jpeg" alt="gallery image 5" class="gallery__img" />

        </figure>

        <figure class="gallery__item gallery__item--6">

            <img src="resources/img/gallery/gal-6.jpeg" alt="gallery image 6" class="gallery__img" />

        </figure>

        <figure class="gallery__item gallery__item--7">

            <img src="resources/img/gallery/gal-7.jpeg" alt="gallery image 7" class="gallery__img" />

        </figure>

        <figure class="gallery__item gallery__item--8">

            <img src="resources/img/gallery/gal-8.jpeg" alt="gallery image 8" class="gallery__img" />

        </figure>

        <figure class="gallery__item gallery__item--9">

            <img src="resources/img/gallery/gal-9.jpeg" alt="gallery image 9" class="gallery__img" />

        </figure>

        <figure class="gallery__item gallery__item--10">

            <img src="resources/img/gallery/gal-10.jpeg" alt="gallery image 10" class="gallery__img" />

        </figure>

        <figure class="gallery__item gallery__item--11">

            <img src="resources/img/gallery/gal-11.jpeg" alt="gallery image 11" class="gallery__img" />

        </figure>

        <figure class="gallery__item gallery__item--12">

            <img src="resources/img/gallery/gal-12.jpeg" alt="gallery image 12" class="gallery__img" />

        </figure>

        <figure class="gallery__item gallery__item--13">

            <img src="resources/img/gallery/gal-13.jpeg" alt="gallery image 13" class="gallery__img" />

        </figure>

        <figure class="gallery__item gallery__item--14">

            <img src="resources/img/gallery/gal-14.jpeg" alt="gallery image 14" class="gallery__img" />

        </figure>

    </section>
```



### grid gallery - SCSS
```scss
.gallery {

    background-color: $color-grey-light-1;

    grid-column: full-start / full-end;

  

    display: grid;

    grid-template-rows: repeat(7, 5vw);

    grid-template-columns: repeat(8, 1fr);

    gap: 1.5rem;

    padding: 1.5rem;

  

    &__item {

        overflow: hidden;

        &--1 {

            grid-column: 1 / 3;

            grid-row: 1 / 3;

        }

  

        &--2 {

            grid-column: 3 / 6;

            grid-row: 1 / 4;

        }

  

        &--3 {

            grid-column: 6 / 7;

            grid-row: 1 / 3;

        }

  

        &--4 {

            grid-column: 7 / 9;

            grid-row: 1 / 3;

        }

  

        &--5 {

            grid-column: 1 / 3;

            grid-row: 3 / 6;

        }

  

        &--6 {

            grid-column: 3 / 5;

            grid-row: 4 / 6;

        }

  

        &--7 {

            grid-column: 5 / 6;

            grid-row: 4 / 5;

        }

  

        &--8 {

            grid-column: 6 / 8;

            grid-row: 3 / 5;

        }

  

        &--9 {

            grid-column: 8 / 9;

            grid-row: 3 / 6;

        }

  

        &--10 {

            grid-column: 1 / 2;

            grid-row: 6 / 8;

        }

  

        &--11 {

            grid-column: 2 / 4;

            grid-row: 6 / 8;

        }

  

        &--12 {

            grid-column: 4 / 5;

            grid-row: 6 / 8;

        }

  

        &--13 {

            grid-column: 5 / 8;

            grid-row: 5 / 8;

        }

  

        &--14 {

            grid-column: 8 / 9;

            grid-row: 6 / 8;

        }

    }

  

    &__img {

        width: 100%;

        height: 100%;

        object-fit: cover;

        display: block;

        transition: all 0.3s;

        &:hover {

            transform: scale(1.2);

        }

    }

  

    @media only screen and (max-width: $bp-small) {

        gap: 1rem;

    }

}
```
