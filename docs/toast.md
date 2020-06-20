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
  -webkit-animation: toast-fadeout 1s 0.5s;
  animation: toast-fadeout 1s 0.5s;
}
#event-toast-container .toast-message {
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
#event-toast-container .toast-success-message {
  background-color: var(--theme-color);
}
#event-toast-container .toast-warning-message {
  background-color: #de9d0c;
}
#event-toast-container .toast-error-message {
  background-color: #CC0000;
}
#event-toast-container .toast-message:hover {
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

.toast-button {
  padding: 5px 20px;
  margin: 0 5px;
  border: none;
  outline: none;
  border-radius: 20px;
  color: white;
  font-weight: bold;
  cursor: pointer;
  margin-top: 10px;
  max-width: 100%;
}
.toast-success-button {
  background-color: var(--theme-color);
}
.toast-warning-button {
  background-color: #de9d0c;
}
.toast-error-button {
  background-color: #cc0000;
}
</style>

<div class="demo-wrapper">
  <button class="toast-button toast-success-button" onClick="toast.success('Success !')">Success</button>
  <button class="toast-button toast-warning-button" onClick="toast.warning('Warning !')">Warning</button>
  <button class="toast-button toast-error-button" onClick="toast.error('Error !')">Error</button>
  <div id="event-toast-container"></div>
</div>

<script>
toast = {
  display: (message, type) => {
    let toastContainer = document.getElementById("event-toast-container");
    let toastBox = document.createElement("div");
    toastBox.classList.add('toast-box');
    let toastMsg = document.createElement("div");
    toastMsg.classList.add('toast-message');
    toastMsg.classList.add(`toast-${type}-message`);
    toastMsg.append(message);
    toastBox.append(toastMsg);
    toastContainer.append(toastBox);
    const animEnd = (e) => { e.animationName === 'toast-fadeout' && toastContainer.removeChild(toastBox); };
    toastBox.addEventListener("webkitAnimationEnd", animEnd);
    toastBox.addEventListener("animationend", animEnd);
    toastBox.onclick = () => { toastBox.classList.add('toast-clicked'); };
  },
  success: (message) => {
    toast.display(message, 'success');
  },
  warning: (message) => {
    toast.display(message, 'warning');
  },
  error: (message) => {
    toast.display(message, 'error');
  }
};
</script>

<!-- tabs:start -->

#### ** HTML **

```html
<button onClick="toast.success('Success !')">Success</button>
<button onClick="toast.warning('Warning !')">Warning</button>
<button onClick="toast.error('Error !')">Error</button>
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
  -webkit-animation: toast-fadeout 1s 0.5s;
  animation: toast-fadeout 1s 0.5s;
}
#event-toast-container .toast-message {
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
#event-toast-container .toast-success-message {
  background-color: var(--theme-color);
}
#event-toast-container .toast-warning-message {
  background-color: #de9d0c;
}
#event-toast-container .toast-error-message {
  background-color: #CC0000;
}
#event-toast-container .toast-message:hover {
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
toast = {
  display: (message, type) => {
    let toastContainer = document.getElementById("event-toast-container");
    let toastBox = document.createElement("div");
    toastBox.classList.add('toast-box');
    let toastMsg = document.createElement("div");
    toastMsg.classList.add('toast-message');
    toastMsg.classList.add(`toast-${type}-message`);
    toastMsg.append(message);
    toastBox.append(toastMsg);
    toastContainer.append(toastBox);
    const animEnd = (e) => { e.animationName === 'toast-fadeout' && toastContainer.removeChild(toastBox); };
    toastBox.addEventListener("webkitAnimationEnd", animEnd);
    toastBox.addEventListener("animationend", animEnd);
    toastBox.onclick = () => { toastBox.classList.add('toast-clicked'); };
  },
  success: (message) => {
    toast.display(message, 'success');
  },
  warning: (message) => {
    toast.display(message, 'warning');
  },
  error: (message) => {
    toast.display(message, 'error');
  }
};
```
<!-- tabs:end -->
