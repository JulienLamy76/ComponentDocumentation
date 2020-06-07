# Border

## Striped

https://stripesgenerator.com/

<style>
.striped-border {
  background-image: linear-gradient(135deg,
    #0375f4 16.67%,
    #42b983 16.67%,
    #42b983 50%,
    #0375f4 50%,
    #0375f4 66.67%,
    #42b983 66.67%,
    #42b983 100%);
  background-size: 15.00px 15.00px;
  padding: 5px;
}
.striped-content {
  background-color: white;
  padding: 5px;
}
</style>
<div class="demo-wrapper">
  <div class="striped-border">
    <div class="striped-content">
      <h3>Lorem Ipsum</h3>
    </div>
  </div>
</div>
<!-- tabs:start -->

#### ** HTML **

```html
<div class="striped-border">
  <div class="striped-content">
    <h3>Lorem Ipsum</h3>
  </div>
</div>
```
#### ** CSS **

```css
.striped-border {
  background-image: linear-gradient(135deg,
    #0375f4 16.67%,
    #42b983 16.67%,
    #42b983 50%,
    #0375f4 50%,
    #0375f4 66.67%,
    #42b983 66.67%,
    #42b983 100%);
  background-size: 15.00px 15.00px;
  padding: 5px;
}
.striped-content {
  background-color: white;
  padding: 5px;
}
```
<!-- tabs:end -->

## Skewed

<style>
.skewed-container {
  position: relative;
}
.skewed-border {
  width: 200px;
  height: 400px;
  background: white;
}
.skewed-border:before {
  content: '';
  position: absolute;
  top: -2px;
  left: -2px;
  right: -2px;
  bottom: -2px;
  z-index: -1;
  transform: skew(2deg, 2deg);
  background: linear-gradient(315deg, #0375f4, #7055bc);
}
</style>
<div class="demo-wrapper">
  <div class="skewed-container">
    <div class="skewed-border">
    </div>
  </div>
</div>

<!-- tabs:start -->

#### ** HTML **

```html
<div class="skewed-container">
  <div class="skewed-border">
  </div>
</div>
```

#### ** CSS **

```css
.skewed-container {
  position: relative;
}
.skewed-border {
  width: 200px;
  height: 400px;
  background: white;
}
.skewed-border:before {
  content: '';
  position: absolute;
  top: -2px;
  left: -2px;
  right: -2px;
  bottom: -2px;
  z-index: -1;
  transform: skew(2deg, 2deg);
  background: linear-gradient(315deg, #0375f4, #7055bc);
}
```
<!-- tabs:end -->
