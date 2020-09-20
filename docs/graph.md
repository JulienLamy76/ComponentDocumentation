# Graph

## Bin Chart

<style>
.dark-background {
    background-color: #E9E9E9;
    color: #002321;
}
.gb-bin__wrapper {
    position: relative;
    height: 300px;
    width: 300px;
    margin: 0 auto;
}
.gb-bin {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    position: relative;
    overflow: hidden;
    background: white;
    position: absolute;
}
.gb-bin__name {
    position: relative;
    z-index: 1;
}
.gb-bin__percentage {
    position: relative;
    z-index: 1;
}
.gb-bin-1 {
    height: 80px;
    width: 175px;
    border-radius: 0% 0% 100% 100% / 0% 0% 150% 150%;
    clip-path: polygon(25% 0%, 75% 0%, 100% 100%, 0% 100%);
    bottom: 0;
    left: 50%;
    transform: translateX(-50%);
}
.gb-bin-2 {
    width: 80px;
    height: 160px;
    border-radius: 100% 0% 0% 100% / 150% 0% 0% 150%;
    clip-path: polygon(0% 0%, 100% 25%, 100% 75%, 0% 100%);
    left: 0;
    top: 70px;
}
.gb-bin-3 {
    height: 80px;
    width: 175px;
    border-radius: 100% 100% 0% 0% / 150% 150% 0% 0%;
    clip-path: polygon(0% 0%, 100% 0, 75% 100%, 25% 100%);
    top:0;
    left: 50%;
    transform: translateX(-50%);
}
.gb-bin-4 {
    width: 80px;
    height: 160px;
    border-radius: 0% 100% 100% 0% / 0% 150% 150% 0%;
    clip-path: polygon(0% 25%, 100% 0%, 100% 100%, 0% 75%);
    right: 0;
    top: 70px;
}
.gb-bin-5 {
     height: 75px;
    width: 75px;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}
.gb-bin__gauge {
    position: absolute;
    left:0;
    bottom:0;
    width: 100%;
}
.gb-bin__gauge-green {
    background-color: green;
}
.gb-bin__gauge-yellow {
    background-color: yellow;
}
.gb-bin__gauge-red {
    background-color: red;
}
</style>

<div class="demo-wrapper dark-background">
  <div class="gb-bin__wrapper">
    <div class="gb-bin gb-bin-1">
        <div class="gb-bin__name">Bin 1</div>
        <div class="gb-bin__percentage"></div>
        <div class="gb-bin__gauge"></div>
    </div>
    <div class="gb-bin gb-bin-2">
        <div class="gb-bin__name">Bin 2</div>
        <div class="gb-bin__percentage"></div>
        <div class="gb-bin__gauge"></div>
    </div>
    <div class="gb-bin gb-bin-3">
        <div class="gb-bin__name">Bin 3</div>
        <div class="gb-bin__percentage"></div>
        <div class="gb-bin__gauge"></div>
    </div>
    <div class="gb-bin gb-bin-4">
        <div class="gb-bin__name">Bin 4</div>
        <div class="gb-bin__percentage"></div>
        <div class="gb-bin__gauge"></div>
    </div>
    <div class="gb-bin gb-bin-5">
        <div class="gb-bin__name">Bin 5</div>
        <div class="gb-bin__percentage"></div>
        <div class="gb-bin__gauge"></div>
    </div>
  </div>
</div>

<script>
const bins = [
    {
      number: 1,
      bin: "10",
    },
    {
      number: 2,
      bin: "90",
    },
    {
      number: 3,
      bin: "40",
    },
    {
      number: 4,
      bin: "20",
    },
    {
      number: 5,
      bin: "70",
    },
];
const getBinChartGauge = (value) => {
    if (value < 20) {
        return 'gb-bin__gauge-green';
    } if (value < 80) {
        return 'gb-bin__gauge-yellow';
    }
    return 'gb-bin__gauge-red';
};
bins.forEach(o => {
    document.querySelector(`.gb-bin-${o.number} .gb-bin__percentage`).textContent = `${o.bin}%`;
    document.querySelector(`.gb-bin-${o.number} .gb-bin__gauge`).classList.add(getBinChartGauge(o.bin));
    document.querySelector(`.gb-bin-${o.number} .gb-bin__gauge`).style.height = `${o.bin}%`;
});
</script>

<!-- tabs:start -->

#### ** HTML **

```html
<div class="gb-bin__wrapper">
    <div class="gb-bin gb-bin-1">
        <div class="gb-bin__name">Bin 1</div>
        <div class="gb-bin__percentage"></div>
        <div class="gb-bin__gauge"></div>
    </div>
    <div class="gb-bin gb-bin-2">
        <div class="gb-bin__name">Bin 2</div>
        <div class="gb-bin__percentage"></div>
        <div class="gb-bin__gauge"></div>
    </div>
    <div class="gb-bin gb-bin-3">
        <div class="gb-bin__name">Bin 3</div>
        <div class="gb-bin__percentage"></div>
        <div class="gb-bin__gauge"></div>
    </div>
    <div class="gb-bin gb-bin-4">
        <div class="gb-bin__name">Bin 4</div>
        <div class="gb-bin__percentage"></div>
        <div class="gb-bin__gauge"></div>
    </div>
    <div class="gb-bin gb-bin-5">
        <div class="gb-bin__name">Bin 5</div>
        <div class="gb-bin__percentage"></div>
        <div class="gb-bin__gauge"></div>
    </div>
</div>
```

#### ** CSS **

```css
.gb-bin__wrapper {
    position: relative;
    height: 300px;
    width: 300px;
    margin: 0 auto;
}
.gb-bin {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    position: relative;
    overflow: hidden;
    background: white;
    position: absolute;
}
.gb-bin__name {
    position: relative;
    z-index: 1;
}
.gb-bin__percentage {
    position: relative;
    z-index: 1;
}
.gb-bin-1 {
    height: 80px;
    width: 175px;
    border-radius: 0% 0% 100% 100% / 0% 0% 150% 150%;
    clip-path: polygon(25% 0%, 75% 0%, 100% 100%, 0% 100%);
    bottom: 0;
    left: 50%;
    transform: translateX(-50%);
}
.gb-bin-2 {
    width: 80px;
    height: 160px;
    border-radius: 100% 0% 0% 100% / 150% 0% 0% 150%;
    clip-path: polygon(0% 0%, 100% 25%, 100% 75%, 0% 100%);
    left: 0;
    top: 70px;
}
.gb-bin-3 {
    height: 80px;
    width: 175px;
    border-radius: 100% 100% 0% 0% / 150% 150% 0% 0%;
    clip-path: polygon(0% 0%, 100% 0, 75% 100%, 25% 100%);
    top:0;
    left: 50%;
    transform: translateX(-50%);
}
.gb-bin-4 {
    width: 80px;
    height: 160px;
    border-radius: 0% 100% 100% 0% / 0% 150% 150% 0%;
    clip-path: polygon(0% 25%, 100% 0%, 100% 100%, 0% 75%);
    right: 0;
    top: 70px;
}
.gb-bin-5 {
     height: 75px;
    width: 75px;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}
.gb-bin__gauge {
    position: absolute;
    left:0;
    bottom:0;
    width: 100%;
}
.gb-bin__gauge-green {
    background-color: green;
}
.gb-bin__gauge-yellow {
    background-color: yellow;
}
.gb-bin__gauge-red {
    background-color: red;
}
```

#### ** JavaScript **

```javascript
const bins = [
    {
      number: 1,
      bin: "10",
    },
    {
      number: 2,
      bin: "90",
    },
    {
      number: 3,
      bin: "40",
    },
    {
      number: 4,
      bin: "20",
    },
    {
      number: 5,
      bin: "70",
    },
];
const getBinChartGauge = (value) => {
    if (value < 20) {
        return 'gb-bin__gauge-green';
    } if (value < 80) {
        return 'gb-bin__gauge-yellow';
    }
    return 'gb-bin__gauge-red';
};
bins.forEach(o => {
    document.querySelector(`.gb-bin-${o.number} .gb-bin__percentage`).textContent = `${o.bin}%`;
    document.querySelector(`.gb-bin-${o.number} .gb-bin__gauge`).classList.add(getBinChartGauge(o.bin));
    document.querySelector(`.gb-bin-${o.number} .gb-bin__gauge`).style.height = `${o.bin}%`;
});
```
<!-- tabs:end -->
