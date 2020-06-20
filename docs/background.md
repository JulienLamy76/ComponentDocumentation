# Background

## Clip Path

https://bennettfeely.com/clippy/

### Screen


<style>
.clip-path-container {
  position: relative;
  width: 600px;
  height: 400px;
}
.clip-path-container .clip-path-image {
  position: absolute;
  width: 100%;
  height: 100%;
}
.clip-path-container .clip-path-image:nth-of-type(1) {
  background: url("images/jungle.jpg");
  background-size: cover;
}
.clip-path-container .clip-path-image:nth-of-type(2) {
  background: url("images/cloud.jpg");
  background-size: cover;
  z-index: 2;
  transition: 0.5s;
  clip-path: polygon(0 0, 100% 0, 100% 0, 0 100%);
}
.clip-path-container .clip-path-image:nth-of-type(2):hover {
  clip-path: polygon(0 0, 100% 0, 100% 100%, 0% 100%);
}
.clip-path-container .clip-path-image:nth-of-type(1):hover ~ .clip-path-image:nth-of-type(2) {
  clip-path: polygon(0 0, 100% 0, 100% 0, 0 0);
}
</style>


<div class="demo-wrapper">
  <div class="clip-path-container">
    <div class="clip-path-image"></div>
    <div class="clip-path-image"></div>
  </div>
</div>

<!-- tabs:start -->

#### ** HTML **

```html
<div class="clip-path-container">
  <div class="clip-path-image"></div>
  <div class="clip-path-image"></div>
</div>
```

#### ** CSS **

```css
.clip-path-container {
  position: relative;
  width: 600px;
  height: 400px;
}
.clip-path-container .clip-path-image {
  position: absolute;
  width: 100%;
  height: 100%;
}
.clip-path-container .clip-path-image:nth-of-type(1) {
  background: url("images/jungle.jpg");
  background-size: cover;
}
.clip-path-container .clip-path-image:nth-of-type(2) {
  background: url("images/cloud.jpg");
  background-size: cover;
  z-index: 2;
  transition: 0.5s;
  clip-path: polygon(0 0, 100% 0, 100% 0, 0 100%);
}
.clip-path-container .clip-path-image:nth-of-type(2):hover {
  clip-path: polygon(0 0, 100% 0, 100% 100%, 0% 100%);
}
.clip-path-container .clip-path-image:nth-of-type(1):hover ~ .clip-path-image:nth-of-type(2) {
  clip-path: polygon(0 0, 100% 0, 100% 0, 0 0);
}
```
<!-- tabs:end -->

## Blend mode

### Screen

<style>
.blend-mode-screen {
  width: 200px;
  height: 500px;
  background: url("images/costume_noir.jpg"),
    url("images/jungle.jpg");
  background-position: center;
  background-size: cover;
  background-blend-mode: screen;
}
</style>

<div class="demo-wrapper">
  <div class="blend-mode-screen"></div>
</div>

<!-- tabs:start -->

#### ** HTML **

```html
<div class="blend-mode-screen"></div>
```

#### ** CSS **

```css
.blend-mode-screen {
  width: 200px;
  height: 500px;
  background: url("images/costume_noir.jpg"),
    url("images/jungle.jpg");
  background-position: center;
  background-size: cover;
  background-blend-mode: screen;
}
```
<!-- tabs:end -->

### Lighten

<style>
.blend-mode-lighten {
  width: 200px;
  height: 500px;
  background: url("images/costume_noir.jpg"),
    url("images/jungle.jpg");
  background-position: center;
  background-size: cover;
  background-blend-mode: lighten;
}
</style>
<div class="demo-wrapper">
  <div class="blend-mode-lighten"></div>
</div>

<!-- tabs:start -->

#### ** HTML **

```html
<div class="blend-mode-lighten"></div>
```

#### ** CSS **

```css
.blend-mode-lighten {
  width: 200px;
  height: 500px;
  background: url("images/costume_noir.jpg"),
    url("images/jungle.jpg");
  background-position: center;
  background-size: cover;
  background-blend-mode: lighten;
}
```
<!-- tabs:end -->

### Darken

<style>
.blend-mode-darken {
  width: 200px;
  height: 500px;
  background: url("images/costume_noir.jpg"),
    url("images/jungle.jpg");
  background-position: center;
  background-size: cover;
  background-blend-mode: darken;
}
</style>
<div class="demo-wrapper">
  <div class="blend-mode-darken"></div>
</div>

<!-- tabs:start -->

#### ** HTML **

```html
<div class="blend-mode-darken"></div>
```

#### ** CSS **

```css
.blend-mode-darken {
  width: 200px;
  height: 500px;
  background: url("images/costume_noir.jpg"),
    url("images/jungle.jpg");
  background-position: center;
  background-size: cover;
  background-blend-mode: darken;
}
```
<!-- tabs:end -->

### Multiply

<style>
.image-multiply-container {
  background: linear-gradient(315deg, #0375f4, #7055bc);
}
.blend-mode-multiply {
  mix-blend-mode: multiply;
}
</style>
<div class="demo-wrapper">
  <div class="image-multiply-container">
    <img class="blend-mode-multiply" src="images/text_typography.jpg" alt="Text Image" />
  </div>
</div>

<!-- tabs:start -->

#### ** HTML **

```html
<div class="image-container">
  <img class="blend-mode-multiply" src="images/text_typography.jpg" alt="Text Image" />
</div>
```

#### ** CSS **

```css
.image-container {
  background: linear-gradient(315deg, #0375f4, #7055bc);
}
.blend-mode-multiply {
  mix-blend-mode: multiply;
}
```
<!-- tabs:end -->