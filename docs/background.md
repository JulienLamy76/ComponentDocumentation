# Background

## Blend mode

### Screen

<style>
.blend-mode-screen {
  width: 200px;
  height: 500px;
  background: url("/images/costume_noir.jpg"),
    url("/images/jungle.jpg");
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
  background: url("/images/costume_noir.jpg"),
    url("/images/jungle.jpg");
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
  background: url("/images/costume_noir.jpg"),
    url("/images/jungle.jpg");
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
  background: url("/images/costume_noir.jpg"),
    url("/images/jungle.jpg");
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
  background: url("/images/costume_noir.jpg"),
    url("/images/jungle.jpg");
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
  background: url("/images/costume_noir.jpg"),
    url("/images/jungle.jpg");
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
    <img class="blend-mode-multiply" src="/images/text_typography.jpg" alt="Text Image" />
  </div>
</div>

<!-- tabs:start -->

#### ** HTML **

```html
<div class="image-container">
    <img class="blend-mode-multiply" src="/images/text_typography.jpg" alt="Text Image" />
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