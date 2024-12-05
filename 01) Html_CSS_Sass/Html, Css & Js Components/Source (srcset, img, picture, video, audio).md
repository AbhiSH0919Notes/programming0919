### picture - HTML
```Html
  <div class="hero-img-box">
          <picture>
            <!-- some browser's are not rendering (.webp) extention -->
            <source srcset="resourses/img/hero.webp" type="image/webp" />
            <source srcset="resourses/img/hero-min.png" type="image/png" />
 
            <!-- replace img source when browser are not render img extention -->
            <img class="hero-img" src="resourses/img/hero-min.png" alt="women enjoying food" />
          </picture>
  </div>
```

### video - HTML
```html
 <div class="bg-video">
                <video class="bg-video-content" autoplay muted loop>
                    <source src="resource/img/video.mp4" type="video/mp4">
                    <source src="resource/img/video.webm" type="video/webm">
                    Your browser is not supported!
                </video>
 </div>
```

### video - CSS
```css
/* ===bg-video=== */
.bg-video {
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0;
  left: 0;
  /* opacity: 0.18; */
  opacity: 0.2;
  z-index: -1;
  overflow: hidden;
}

.bg-video-content {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
```
