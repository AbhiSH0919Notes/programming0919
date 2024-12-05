### story card - HTML
```html
 <div class="row u-margin-bottom-big">
                <div class="story">
                    <figure class="story-shape">
                        <img src="resource/img/nat-8.jpg" alt="Person on a tour" class="story-img">
                        <figcaption class="story-caption">Mary Smith</figcaption>
                    </figure>
                    <div class="story-text">
                        <h3 class="tertiary-heading">I had the best week ever with my family</h3>
                        <p>
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam, ipsum sapiente aspernatur
                            libero repellat quis consequatur ducimus quam nisi exercitationem omnis earum qui. Aperiam,
                            ipsum sapiente aspernatur libero repellat quis consequatur ducimus quam nisi exercitationem
                            omnis earum qui.
                        </p>
                    </div>
                </div>
 </div>
```

### story card - CSS
```css

/* =====SECTION-STORIES===== */
.section-stories {
  padding: 15rem 0;
  position: relative;
}

.story {
  width: 75%;
  padding: 6rem;
  padding-left: 9rem;
  margin: 0 auto;
  font-size: 1.6rem;
  background-color: rgba(255, 255, 255, 0.6);
  border-radius: 3px;
  box-shadow: 0 3rem 6rem rgba(0, 0, 0, 0.1);
  transform: skewX(-12deg);
}

.story-shape {
  width: 15rem;
  height: 15rem;
  float: left;
  -webkit-shape-outside: circle(50% at 50% 50%);
  shape-outside: circle(50% at 50% 50%);
  transform: skewX(12deg) translateX(-3rem);
  position: relative;
  overflow: hidden;
  border-radius: 50%;
}

@supports (-webkit-clip-path: circle(50% at 50% 50%)) or
  (clip-path: circle(50% at 50% 50%)) or
  (-webkit-shape-outside: circle(50% at 50% 50%)) or
  (shape-outside: circle(50% at 50% 50%)) {
  .story__shape {
    -webkit-clip-path: circle(50% at 50% 50%);
    clip-path: circle(50% at 50% 50%);
    shape-outside: circle(50% at 50% 50%);
    border-radius: none;
  }
}

.story-img {
  height: 100%;
  transform: translateX(-4rem) scale(1.4);
  transition: all 0.5s;
  backface-visibility: hidden;
}

.story-caption {
  font-size: 1.7rem;
  text-transform: uppercase;
  color: #fff;
  text-align: center;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, 20%);
  transition: all 0.5s;
  opacity: 0;
  backface-visibility: hidden;
}

.story-text {
  transform: skewX(12deg);
  backface-visibility: hidden;
}

.story:hover .story-img {
  transform: translateX(-4rem) scale(1);
  filter: blur(0.3rem) brightness(80%);
}

.story:hover .story-caption {
  transform: translate(-50%, -50%);
  opacity: 1;
}

```
