# Navbar

## Sliding Indicator

<style>
nav {
  position: relative;
}
nav a {
  position: relative;
  margin: 0 20px;
  font-size: 2em;
  color: var(--theme-color);
  text-decoration: none;
}
nav #marker {
  position: absolute;
  height: 4px;
  width: 0;
  background: var(--theme-color);
  bottom: -8px;
  transition: 0.5s;
  border-radius: 4px;
}
</style>
<div class="demo-wrapper">
  <nav>
    <div id="marker"></div>
    <a href="#/navbar">Home</a>
    <a href="#/navbar">About</a>
    <a href="#/navbar">Services</a>
    <a href="#/navbar">Portfolio</a>
    <a href="#/navbar">Team</a>
  </nav>
</div>
<script>
  let marker = document.querySelector('#marker');
  let items = document.querySelectorAll('nav a');
  function indicator(e) {
    marker.style.left = e.offsetLeft + "px";
    marker.style.width = e.offsetWidth + "px";
  }
  items.forEach(item => {
    item.addEventListener('click', (e) => {
      indicator(e.target);
    });
  });
</script>
<!-- tabs:start -->

#### ** HTML **

```html
<nav>
  <div id="marker"></div>
  <a href="#">Home</a>
  <a href="#">About</a>
  <a href="#">Services</a>
  <a href="#">Portfolio</a>
  <a href="#">Team</a>
</nav>
```

#### ** CSS **

```css
nav {
  position: relative;
}
nav a {
  position: relative;
  margin: 0 20px;
  font-size: 2em;
  color: var(--theme-color);
  text-decoration: none;
}
nav #marker {
  position: absolute;
  height: 4px;
  width: 0;
  background: var(--theme-color);
  bottom: -8px;
  transition: 0.5s;
  border-radius: 4px;
}
```

#### ** JavaScript **

```javascript
let marker = document.querySelector('#marker');
let items = document.querySelectorAll('nav a');
function indicator(e) {
  marker.style.left = e.offsetLeft + "px";
  marker.style.width = e.offsetWidth + "px";
}
items.forEach(item => {
  item.addEventListener('click', (e) => {
    indicator(e.target);
  });
});
```

<!-- tabs:end -->