# Card

## Isometric

<style>
.isometric-card {
  position: relative;
  width: 300px;
  max-width: 100%;
  background: #fff;
  transition: 0.5s;
  margin: 50px;
}
.isometric-card:before {
  content: '';
  position: absolute;
  top: -15px;
  left: 0;
  width: 100%;
  height: 15px;
  background: #00c0f6;
  transform-origin: bottom;
  transform: skewX(45deg);
  transition: 0.5s;
}
.isometric-card:hover {
  transform: translateY(-40px);
}
.isometric-card .card-header {
  position: relative;
  width: 300px;
  max-width: 100%;
  height: 200px;
  background: #00c7ff;
  justify-content: center;
  display: flex;
  align-items: center;
  flex-direction: column;
}
.isometric-card .card-header:before {
  content: '';
  position: absolute;
  top: -15px;
  left: -15px;
  width: 15px;
  height: 100%;
  background: #00c0f6;
  transform-origin:left;
  transform: skewY(45deg);
  transition: 0.5s;
}
.isometric-card .card-header img {
  max-width: 100px;
}
.isometric-card .card-header h3 {
  position: relative;
  color: #fff;
  margin-top: 10px;
}
.isometric-card .card-body {
  position: relative;
  width: 100%;
  padding: 20px;
  color: #777;
  text-align: center;
  background: #fff;
}
.isometric-card .card-body:before {
  content: '';
  position: absolute;
  left: 0;
  bottom: 0;
  width: 100%;
  height: 400px;
  background: linear-gradient(transparent,transparent, rgba(0,0,0,.1));
  transform: skewX(45deg);
  transform-origin: bottom;
  transform: 0.5s;
  pointer-events: none;
  z-index: -1;
  transition: 0.5s;
}
.isometric-card .card-body:after {
  content: '';
  position: absolute;
  top: -15px;
  left: -15px;
  width: 15px;
  height: 100%;
  background: #d9d9d9;
  transform-origin:left;
  transform: skewY(45deg);
  transition: 0.5s;
}
.isometric-card:hover .card-body:before {
  transform: translateY(40px) skewX(45deg);
  filter: blur(5px);
  opacity: 0.5;
}
</style>
<div class="demo-wrapper">
  <div class="isometric-card">
    <div class="card-header">
      <img src="/images/design_icon.png" alt="design icon">
      <h3>Design</h3>
    </div>
    <div class="card-body">
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
    </div>
  </div>
</div>

<!-- tabs:start -->

#### ** HTML **

```html
<div class="card">
  <div class="card-header">
    <img src="/images/design_icon.png" alt="design icon">
    <h3>Design</h3>
  </div>
  <div class="card-body">
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
  </div>
</div>
```
#### ** CSS **

```css
.card {
  position: relative;
  width: 300px;
  max-width: 100%;
  background: #fff;
  transition: 0.5s;
  margin: 50px;
}
.card:before {
  content: '';
  position: absolute;
  top: -15px;
  left: 0;
  width: 100%;
  height: 15px;
  background: #00c0f6;
  transform-origin: bottom;
  transform: skewX(45deg);
  transition: 0.5s;
}
.card:hover {
  transform: translateY(-40px);
}
.card .card-header {
  position: relative;
  width: 300px;
  max-width: 100%;
  height: 200px;
  background: #00c7ff;
  justify-content: center;
  display: flex;
  align-items: center;
  flex-direction: column;
}
.card .card-header:before {
  content: '';
  position: absolute;
  top: -15px;
  left: -15px;
  width: 15px;
  height: 100%;
  background: #00c0f6;
  transform-origin:left;
  transform: skewY(45deg);
  transition: 0.5s;
}
.card .card-header img {
  max-width: 100px;
}
.card .card-header h3 {
  position: relative;
  color: #fff;
  margin-top: 10px;
}
.card .card-body {
  position: relative;
  width: 100%;
  padding: 20px;
  color: #777;
  text-align: center;
  background: #fff;
}
.card .card-body:before {
  content: '';
  position: absolute;
  left: 0;
  bottom: 0;
  width: 100%;
  height: 400px;
  background: linear-gradient(transparent,transparent, rgba(0,0,0,.1));
  transform: skewX(45deg);
  transform-origin: bottom;
  transform: 0.5s;
  pointer-events: none;
  z-index: -1;
  transition: 0.5s;
}
.card .card-body:after {
  content: '';
  position: absolute;
  top: -15px;
  left: -15px;
  width: 15px;
  height: 100%;
  background: #d9d9d9;
  transform-origin:left;
  transform: skewY(45deg);
  transition: 0.5s;
}
.card:hover .card-body:before {
  transform: translateY(40px) skewX(45deg);
  filter: blur(5px);
  opacity: 0.5;
}
```
<!-- tabs:end -->

## Hover expand vertical

<style>
.card-hover-expandy {
  cursor: pointer;
}
.card-hover-expandy .card-header {
  position: relative;
  background: #333;
  color: #fff;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 1;
  transform: translateY(100px);
  max-width: 300px;
  height: 200px;
  transition: 0.5s;
}
.card-hover-expandy:hover .card-header {
  background: #ff0057;
  transform: translateY(0);
}
.card-hover-expandy .card-header .card-header-content {
  opacity: 0.2;
  transition: 0.5s;
}
.card-hover-expandy:hover .card-header .card-header-content {
  opacity: 1;
}
.card-hover-expandy .card-header .card-header-content img {
  max-width: 100px;
}
.card-hover-expandy .card-header .card-header-content h3 {
  margin: 10px 0 0;
  padding: 0;
  text-align: center;
}
.card-hover-expandy .card-body {
  position: relative;
  background: #fff;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 20px;
  box-sizing: border-box;
  box-shadow: 0 10px 15px rgba(0, 0, 0, 0.8);
  transform: translateY(-100px);
  max-width: 300px;
  height: 200px;
  transition: 0.5s;
}
.card-hover-expandy:hover .card-body {
  transform: translateY(0);
}
</style>
<div class="demo-wrapper">
  <div class="card-hover-expandy">
    <div class="card-header">
      <div class="card-header-content">
        <img src="/images/design_icon.png" alt="design icon">
        <h3>Design</h3>
      </div>
    </div>
    <div class="card-body">
      <div class="card-body-content">
        <span>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quas cum cumque minus iste veritatis provident at.</span>
      </div>
    </div>
  </div>
</div>

<!-- tabs:start -->

#### ** HTML **

```html
<div class="card">
  <div class="card-header">
    <div class="card-header-content">
      <img src="/images/design_icon.png" alt="design icon">
      <h3>Design</h3>
    </div>
  </div>
  <div class="card-body">
    <div class="card-body-content">
      <span>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quas cum cumque minus iste veritatis provident at.</span>
    </div>
  </div>
</div>
```

#### ** CSS **

```css
.card {
  cursor: pointer;
}

.card .card-header {
  position: relative;
  background: #333;
  color: #fff;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 1;
  transform: translateY(100px);
  max-width: 300px;
  height: 200px;
  transition: 0.5s;
}

.card:hover .card-header {
  background: #ff0057;
  transform: translateY(0);
}

.card .card-header .card-header-content {
  opacity: 0.2;
  transition: 0.5s;
}

.card:hover .card-header .card-header-content {
  opacity: 1;
}

.card .card-header .card-header-content img {
  max-width: 100px;
}

.card .card-header .card-header-content h3 {
  margin: 10px 0 0;
  padding: 0;
  text-align: center;
}

.card .card-body {
  position: relative;
  background: #fff;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 20px;
  box-sizing: border-box;
  box-shadow: 0 10px 15px rgba(0, 0, 0, 0.8);
  transform: translateY(-100px);
  max-width: 300px;
  height: 200px;
  transition: 0.5s;
}

.card:hover .card-body {
  transform: translateY(0);
}
```
<!-- tabs:end -->

## Hover photo

<style>
.dark-background {
  background-color: #212121;
}
.card-photo-container {
  padding: 40px 0;
  z-index: 0;
}
.card-photo {
  position: relative;
  width: 300px;
  height: 350px;
  background: #fff;
  margin: 0 auto;
  border-radius: 4px;
  box-shadow:0 2px 10px rgba(0,0,0,.2);
}
.card-photo:before,
.card-photo:after {
  content:"";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border-radius: 4px;
  background: #fff;
  transition: 0.5s;
  z-index:-1;
}
.card-photo:hover:before {
  transform: rotate(20deg);
  box-shadow: 0 2px 20px rgba(0,0,0,.2);
}
.card-photo:hover:after {
  transform: rotate(10deg);
  box-shadow: 0 2px 20px rgba(0,0,0,.2);
}
.card-photo .card-header {
  position: absolute;
  top: 10px;
  left: 10px;
  bottom: 10px;
  right: 10px;
  background: #222;
  transition: 0.5s;
  z-index: 1;
}
.card-photo:hover .card-header {
  bottom: 80px;
}
.card-photo .card-header img {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
}
.card-photo .card-body {
  position: absolute;
  left: 10px;
  right: 10px;
  bottom: 10px;
  height: 60px;
  text-align: center;
  text-transform: uppercase;
}
.card-photo .card-body h2 {
  margin: 0;
  padding: 0;
  font-size: 20px;
  color: #777;
}
.card-photo .card-body span {
  font-weight: 500;
  color: #f38695;
  display: block;
  margin-top: 5px;
}
</style>
<div class="demo-wrapper dark-background">
  <div class="card-photo-container">
    <div class="card-photo">
      <div class="card-header">
        <img src="/images/michel_dumas.jpg" alt="Michel Dumas">
      </div>
      <div class="card-body">
        <h2>Michel Dumas</h2>
        <span>Chef</span>
      </div>
    </div>
  </div>
</div>
<!-- tabs:start -->

#### ** HTML **

```html
<div class="card-photo-container">
  <div class="card-photo">
    <div class="card-header">
      <img src="/images/michel_dumas.jpg" alt="Michel Dumas">
    </div>
    <div class="card-body">
      <h2>Michel Dumas</h2>
      <span>Chef</span>
    </div>
  </div>
</div>
```
#### ** CSS **

```css
.card-photo-container {
  padding: 40px 0;
  z-index: 0;
}

.card-photo {
  position: relative;
  width: 300px;
  height: 350px;
  background: #fff;
  margin: 0 auto;
  border-radius: 4px;
  box-shadow:0 2px 10px rgba(0,0,0,.2);
}

.card-photo:before,
.card-photo:after {
  content:"";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border-radius: 4px;
  background: #fff;
  transition: 0.5s;
  z-index: -1;
}

.card-photo:hover:before {
  transform: rotate(20deg);
  box-shadow: 0 2px 20px rgba(0,0,0,.2);
}

.card-photo:hover:after {
  transform: rotate(10deg);
  box-shadow: 0 2px 20px rgba(0,0,0,.2);
}

.card-photo .card-header {
  position: absolute;
  top: 10px;
  left: 10px;
  bottom: 10px;
  right: 10px;
  background: #222;
  transition: 0.5s;
  z-index: 1;
}

.card-photo:hover .card-header {
  bottom: 80px;
}

.card-photo .card-header img {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.card-photo .card-body {
  position: absolute;
  left: 10px;
  right: 10px;
  bottom: 10px;
  height: 60px;
  text-align: center;
  text-transform: uppercase;
}

.card-photo .card-body h2 {
  margin: 0;
  padding: 0;
  font-size: 20px;
  color: #777;
}

.card-photo .card-body span {
  font-weight: 500;
  color: #f38695;
  display: block;
  margin-top: 5px;
}
```
<!-- tabs:end -->