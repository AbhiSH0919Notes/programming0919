### Rotating card - HTML
```html
   <div class="tours-card">
                    <!-- --card-one-- -->
                    <div class="card">

                        <div class="card-side card-front-side card-front-side-1">

                            <div class="card-picture card-picture-1">&nbsp;</div>

                            <h4 class="card-heading">

                                <span class="card-heading-span card-heading-span-1">The sea explorer</span>

                            </h4>

                            <div class="card-details">

                                <ul class="card-list">

                                    <li class="card-list-item">3 day tours</li>

                                    <li class="card-list-item">Up to 30 people</li>

                                    <li class="card-list-item">2 tour guides</li>

                                    <li class="card-list-item">Sleep in cozy hotels</li>

                                    <li class="card-list-item">Difficulty: easy</li>

                                </ul>

                            </div>

                        </div>

                        <div class="card-side card-back-side card-back-side-1">

                            <div class="card-cta">

                                <div class="card-price-box">

                                    <div class="card-price-only">Only</div>

                                    <div class="card-price-value">$297</div>

                                </div>

  

                                <a href="#popup" class="btn btn-white">Book now!</a>

                            </div>

                        </div>

                    </div>
    </div>
```

### Rotating card - CSS
```css

/* =====SECTION-TOURS===== */

.section-tours {
  padding: 25rem 0 15rem 0;
  margin-top: -10rem;
  background-color: #f7f7f7;
}

.tours-card {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 6rem;
}

.card {
  height: 52rem;
  perspective: 150rem;
  -ms-perspective: 150rem;
  position: relative;
  backface-visibility: hidden;
}

.card-side {
  width: 100%;
  height: 52rem;
  border-radius: 3px;
  overflow: hidden;
  box-shadow: 0 1.5rem 4rem rgba(0, 0, 0, 0.15);
  position: absolute;
  top: 0;
  left: 0;
  transition: all 0.8s ease;
  backface-visibility: hidden;
}

.card-front-side {
  background-color: #fff;
}

.card-back-side {
  transform: rotateY(180deg);
}

.card-back-side-1 {
  background-image: linear-gradient(to right bottom, #ffb900, #ff7730);
}

.card-back-side-2 {
  background-image: linear-gradient(to right bottom, #7ed56f, #28b485);
}

.card-back-side-3 {
  background-image: linear-gradient(to right bottom, #2998ff, #5643fa);
}

.card:hover .card-side {
  transform: rotateY(-180deg);
}

.card:hover .card-back-side {
  transform: rotateY(0);
}

/* ---card-picture--- */
.card-picture {
  height: 23rem;
  background-size: cover;
  clip-path: polygon(0 0, 100% 0, 100% 85%, 0 100%);
  -webkit-clip-path: polygon(0 0, 100% 0, 100% 85%, 0 100%);
  background-blend-mode: screen;
}

.card-picture-1 {
  background-image: linear-gradient(to right bottom, #ffb900, #ff7730),
    url("resource/img/nat-5.jpg");
}

.card-picture-2 {
  background-image: linear-gradient(to right bottom, #7ed56f, #28b485),
    url("resource/img/nat-6.jpg");
}

.card-picture-3 {
  background-image: linear-gradient(to right bottom, #2998ff, #5643fa),
    url("resource/img/nat-7.jpg");
}

/* ---card-heading--- */
.card-heading {
  font-size: 2.8rem;
  width: 75%;
  color: #fff;
  font-weight: 300;
  text-align: right;
  text-transform: uppercase;
  position: absolute;
  top: 12rem;
  right: 2rem;
}

.card-heading-span {
  padding: 1rem 1.5rem;
  box-decoration-break: clone;
  -webkit-box-decoration-break: clone;
}

.card-heading-span-1 {
  background-image: linear-gradient(
    to right bottom,
    rgba(255, 185, 0, 0.85),
    rgba(255, 119, 48, 0.85)
  );
}

.card-heading-span-2 {
  background-image: linear-gradient(
    to right bottom,
    rgba(126, 213, 111, 0.85),
    rgba(40, 180, 133, 0.85)
  );
}

.card-heading-span-3 {
  background-image: linear-gradient(
    to right bottom,
    rgba(41, 152, 255, 0.85),
    rgba(85, 67, 250, 0.85)
  );
}

/* ---card-details--- */
.card-details {
  padding: 3rem;
}

.card-list {
  list-style: none;
  width: 80%;
  margin: 0 auto;
}

.card-details ul li {
  font-size: 1.5rem;
  padding: 1rem;
  text-align: center;
}

.card-list-item:not(:last-child) {
  border-bottom: 1px solid #eee;
}

/* ---card-back-side--- */
.card-cta {
  width: 90%;
  text-align: center;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.card-price-box {
  color: #fff;
  margin-bottom: 8rem;
}

.card-price-only {
  font-size: 1.4rem;
  text-transform: uppercase;
}

.card-price-value {
  font-size: 6rem;
  font-weight: 100;
}
```

