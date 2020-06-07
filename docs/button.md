# Button

## Ripple


<style>
.btn-ripple, .markdown-section .btn-ripple {
  position: relative;
  display: inline-block;
  padding: 12px 36px;
  margin: 10px 0;
  color: #fff;
  text-decoration: none;
  text-transform: uppercase;
  font-size: 18px;
  letter-spacing: 2px;
  border-radius: 40px;
  background: linear-gradient(90deg, #0162c8, #55e7fc);
  overflow: hidden;
  border: none;
  font-weight: bold;
  font-family: inherit;
  vertical-align: top;
  outline: none;
  cursor: pointer;
}
.btn-ripple .ripple-span {
  position: absolute;
  background: #fff;
  transform: translate(-50%, -50%);
  pointer-events: none;
  border-radius: 50%;
  animation: animation-ripple-effect 1s linear;
}
@keyframes animation-ripple-effect {
  0% {
    width: 0px;
    height: 0px;
    opacity: .5;
  }
  100% {
    width: 500px;
    height: 500px;
    opacity: 0;
  }
}
</style>

<div class="demo-wrapper">
  <div>
    <a class="btn-ripple" href="">Button</a>
    <button class="btn-ripple">Button</button>
  </div>
</div>

<script>
  const rippleButtons = document.querySelectorAll('.btn-ripple');
  rippleButtons.forEach(btn => {
    btn.addEventListener('click', e => {
      let x = e.layerX;
      let y = e.layerY;
      let ripple = document.createElement('span');
      ripple.classList.add('ripple-span');
      ripple.style.left = x + 'px'; 
      ripple.style.top = y + 'px';
      btn.append(ripple);
      ripple.addEventListener("webkitAnimationEnd", animation => animation.animationName === "animation-ripple-effect" && ripple.remove());
      ripple.addEventListener("animationend", animation => animation.animationName === "animation-ripple-effect" && ripple.remove());
      e.preventDefault();
    });
  });
</script>
<!-- tabs:start -->

#### ** HTML **

```html
<a class="btn-ripple" href="">Button</a>
<button class="btn-ripple">Button</button>
```
#### ** CSS **

```css
.btn-ripple {
  position: relative;
  display: inline-block;
  padding: 12px 36px;
  margin: 10px 0;
  color: #fff;
  text-decoration: none;
  text-transform: uppercase;
  font-size: 18px;
  letter-spacing: 2px;
  border-radius: 40px;
  background: linear-gradient(90deg, #0162c8, #55e7fc);
  overflow: hidden;
  border: none;
  font-weight: bold;
  font-family: inherit;
  vertical-align: top;
  outline: none;
  cursor: pointer;
}
.btn-ripple .ripple-span {
  position: absolute;
  background: #fff;
  transform: translate(-50%, -50%);
  pointer-events: none;
  border-radius: 50%;
  animation: animation-ripple-effect 1s linear;
}
@keyframes animation-ripple-effect {
  0% {
    width: 0px;
    height: 0px;
    opacity: .5;
  }
  100% {
    width: 500px;
    height: 500px;
    opacity: 0;
  }
}
```

#### ** JavaScript **

```javascript
const rippleButtons = document.querySelectorAll('.btn-ripple');
  rippleButtons.forEach(btn => {
    btn.addEventListener('click', e => {
      let x = e.layerX;
      let y = e.layerY;
      let ripple = document.createElement('span');
      ripple.classList.add('ripple-span');
      ripple.style.left = x + 'px'; 
      ripple.style.top = y + 'px';
      btn.append(ripple);
      ripple.addEventListener("webkitAnimationEnd", animation => animation.animationName === "animation-ripple-effect" && ripple.remove());
      ripple.addEventListener("animationend", animation => animation.animationName === "animation-ripple-effect" && ripple.remove());
    });
  });
```
<!-- tabs:end -->

