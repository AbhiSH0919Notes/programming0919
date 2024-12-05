### header navigation bar - HTML
```Html
 <header class="header">

    <nav class="navigation">

      <a class="logo-link header-logo" href="#">

        <img class="logo-img" src="resourses/img/omnifood-logo.png" alt="Omnifood-logo" />

      </a>

      <nav class="main-nav">

        <ul class="main-nav-list">

          <li><a class="main-nav-link" href="#how">How it works</a></li>

          <li><a class="main-nav-link" href="#meals">Meals</a></li>

          <li>

            <a class="main-nav-link" href="#testimonials">Testimonials</a>

          </li>

          <li><a class="main-nav-link" href="#pricing">Pricing</a></li>

          <li><a class="main-nav-link nav-cta" href="#cta">Try for free</a></li>

        </ul>

      </nav>

      <button class="btn-mobile-nav">

        <ion-icon class="icon icon-mobile-nav" name="menu-outline"></ion-icon>

        <ion-icon class="icon icon-mobile-nav" name="close-outline"></ion-icon>

      </button>

    </nav>

  </header>
```

### header navigation bar - CSS
```css
/* ========= HEADER ========= */
.header {
    background-color: #fdf2e9;
    height: 9.6rem;
}

.navigation {
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 140rem;
    height: 100%;
    padding: 0 3.2rem;
    margin: 0 auto;
}  

.header-logo {
    z-index: 999;
}

.main-nav-list {
    display: flex;
    align-items: center;
    gap: 4.8rem;
    list-style: none;
}

.main-nav-link:link,
.main-nav-link:visited {
    display: inline-block;
    color: #333;
    text-decoration: none;
    /* padding: 1.2rem 2.4rem; */
    font-weight: 500;
    transition: all 0.3s;
}

.main-nav-link:hover,
.main-nav-link:active {
    color: #cf711f;
}

.main-nav-link.nav-cta:link,
.main-nav-link.nav-cta:visited {
    color: #fff;
    background-color: #e67e22;
    padding: 1.2rem 2.4rem;
    border-radius: 9px;
}

.main-nav-link.nav-cta:hover,
.main-nav-link.nav-cta:active {
    background-color: #cf711f;
}

/* ========= MOBILE NAVIGATION ========= */
.btn-mobile-nav {
    border: none;
    background: none;
    cursor: pointer;
    display: none;
}

.icon-mobile-nav {
    height: 4.8rem;
    width: 4.8rem;
    color: #333;
}

.icon-mobile-nav[name="close-outline"] {
    display: none;
}

/* ========= Sticky Navigation ========= */
.sticky .header {
    position: fixed;
    top: 0;
    left: 50%;
    transform: translateX(-50%);
    bottom: 0;
    width: 100%;
    height: 8rem;
    padding-top: 0;
    padding-bottom: 0;
    background-color: #fffffff7;
    box-shadow: 0 1.2rem 3.2rem #00000008;
    z-index: 999;
}  

.sticky .section-hero {
    padding-top: 14.4rem;
}

```

### header navigation bar - JS

```js

// Make mobile navigation work
const btnNavEl = document.querySelector(".btn-mobile-nav");
const headerEl = document.querySelector(".header");
btnNavEl.addEventListener("click", function () {
    headerEl.classList.toggle("nav-open");
});

///////////////////////////////////////////////////////////

// Smooth scrolling animation
document.addEventListener("click", function (e) {
    const link = e.target?.closest("a:link");
    if (!link) return;
    e.preventDefault();
    const href = link?.getAttribute("href");

    // Scroll back to top
    if (href === "#" || href === "") {
        window.scrollTo({
            top: 0,
            behavior: "smooth",
        });
    } else if (
        (link && e.target.classList.contains("btn")) ||
        e.target.classList.contains("main-nav-link")
    ) {
        // Scroll to other links
        const scrollToSec = document.querySelector(href);
        scrollToSec?.scrollIntoView({ behavior: "smooth" });

        // Close mobile naviagtion when target sectio
        if (headerEl.classList.contains("nav-open"))
            headerEl.classList.remove("nav-open");
    }
});

///////////////////////////////////////////////////////////

// Sticky navigation
const sectionHeroEl = document.querySelector(".section-hero");
const obs = new IntersectionObserver(
    function (entries) {
        const ent = entries[0];
        ent.isIntersecting
            ? document.body.classList.remove("sticky")
            : document.body.classList.add("sticky");
    },
    {
        // In the viewport
        root: null,
        threshold: 0,
        rootMargin: "-85px",
    }
);

obs.observe(sectionHeroEl);

```






