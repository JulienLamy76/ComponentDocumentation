# Toast

<style>
#event-toast-container {
  position: fixed;
  top: 10px;
  right: 15px;
  z-index: 999;
  display: flex;
  flex-direction: column-reverse;
  max-width: 300px;
}
#event-toast-container .toast-box {
  -webkit-animation: toast-fadein 0.5s, toast-fadeout 1s 3s;
  animation: toast-fadein 0.5s, toast-fadeout 1s 3s;
}
#event-toast-container .toast-box.toast-clicked {
  -webkit-animation: toast-fadeout 1s 1s;
  animation: toast-fadeout 1s 1s;
}
#event-toast-container .toast-message {
  background: #0000CC;
  padding: 15px;
  opacity: 0.8;
  border-radius: 3px;
  width: 300px;
  color: #fff;
  box-shadow: 0 0 12px #999;
  word-break: break-word;
  font-size: 14px;
  font-weight: 500;
  cursor: pointer;
}
#event-toast-container > .toast-message:hover {
  opacity: 1;
  box-shadow: 0 0 12px #000;
}
#event-toast-container > .toast-box + .toast-box {
  margin-bottom: 10px;
}

@-webkit-keyframes toast-fadein {
  from {transform: translateY(-100px); opacity: 0;}
  to {transform: translateY(0); opacity: 1;}
}

@keyframes toast-fadein {
  from {transform: translateY(-100px); opacity: 0;}
  to {transform: translateY(0); opacity: 1;}
}

@-webkit-keyframes toast-fadeout {
  from {transform: translateX(0); opacity: 1;}
  to {transform: translateX(315px); opacity: 0;}
}

@keyframes toast-fadeout {
  from {transform: translateX(0); opacity: 1;}
  to {transform: translateX(315px); opacity: 0;}
}

#toast-input {
  margin: 0 10px;
}
.toast-button {
  padding: 5px 10px;
  background: linear-gradient(90deg, #0162c8, #55e7fc);
  border: none;
  outline: none;
  border-radius: 20px;
  color: white;
  font-weight: bold;
  cursor: pointer;
  margin-top: 10px;
  width: 100px;
  max-width: 100%;
}
.toast-wrapper {
  flex-direction: column;
}
</style>

<div class="demo-wrapper toast-wrapper">
  <div>
    <label for="toast-input">Message :</label>
    <input type="text" id="toast-input" />
  </div>
  <div>
    <button class="toast-button" onClick="displayToast()">Toast !</button>
  </div>
  <div id="event-toast-container"></div>
</div>

<script>
toast = (message) => {
  let toastContainer = document.getElementById("event-toast-container");
  let toastBox = document.createElement("div");
  toastBox.classList.add('toast-box');
  let toastMsg = document.createElement("div");
  toastMsg.classList.add('toast-message');
  toastMsg.append(message);
  toastBox.append(toastMsg);
  toastContainer.append(toastBox);
  const animEnd = (e) => { e.animationName === 'toast-fadeout' && toastContainer.removeChild(toastBox); };
  toastBox.addEventListener("webkitAnimationEnd", animEnd);
  toastBox.addEventListener("animationend", animEnd);
  toastBox.onclick = () => { toastBox.classList.add('toast-clicked'); };
}

displayToast = () => {
  let toastMessage = document.getElementById('toast-input').value;
  toast(toastMessage);
}
</script>

<!-- tabs:start -->

#### ** HTML **

```html
<div id="event-toast-container"></div>
```

#### ** CSS **

```css
#event-toast-container {
  position: fixed;
  top: 10px;
  right: 15px;
  z-index: 999;
  display: flex;
  flex-direction: column-reverse;
  max-width: 300px;
}
#event-toast-container .toast-box {
  -webkit-animation: toast-fadein 0.5s, toast-fadeout 1s 3s;
  animation: toast-fadein 0.5s, toast-fadeout 1s 3s;
}
#event-toast-container .toast-box.toast-clicked {
  -webkit-animation: toast-fadeout 1s 1s;
  animation: toast-fadeout 1s 1s;
}
#event-toast-container .toast-message {
  background: #0000CC;
  padding: 15px;
  opacity: 0.8;
  border-radius: 3px;
  width: 300px;
  color: #fff;
  box-shadow: 0 0 12px #999;
  word-break: break-word;
  font-size: 14px;
  font-weight: 500;
  cursor: pointer;
}
#event-toast-container > .toast-message:hover {
  opacity: 1;
  box-shadow: 0 0 12px #000;
}
#event-toast-container > .toast-box + .toast-box {
  margin-bottom: 10px;
}

@-webkit-keyframes toast-fadein {
  from {transform: translateY(-100px); opacity: 0;}
  to {transform: translateY(0); opacity: 1;}
}

@keyframes toast-fadein {
  from {transform: translateY(-100px); opacity: 0;}
  to {transform: translateY(0); opacity: 1;}
}

@-webkit-keyframes toast-fadeout {
  from {transform: translateX(0); opacity: 1;}
  to {transform: translateX(315px); opacity: 0;}
}

@keyframes toast-fadeout {
  from {transform: translateX(0); opacity: 1;}
  to {transform: translateX(315px); opacity: 0;}
}
```

#### ** JavaScript **

```javascript
toast = (message) => {
  let toastContainer = document.getElementById("event-toast-container");
  let toastBox = document.createElement("div");
  toastBox.classList.add('toast-box');
  let toastMsg = document.createElement("div");
  toastMsg.classList.add('toast-message');
  toastMsg.append(message);
  toastBox.append(toastMsg);
  toastContainer.append(toastBox);
  const animEnd = (e) => { e.animationName === 'toast-fadeout' && toastContainer.removeChild(toastBox); };
  toastBox.addEventListener("webkitAnimationEnd", animEnd);
  toastBox.addEventListener("animationend", animEnd);
  toastBox.onclick = () => { toastBox.classList.add('toast-clicked'); };
}
```
<!-- tabs:end -->
