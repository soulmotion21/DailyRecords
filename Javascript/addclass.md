# Vanilla Js addClass code snippet

- class 네임을 가졌는지를 판단 후 class add, remove 하는 code

```javascript
hasClass: function (el, className) {
  if (el.classList) {
    return el.classList.contains(className);
  } else {
    return !!el.className.match(new RegExp('(\\s|^)' + className + '(\\s|$)'));
  }
},
addClass: function (el, className) {
  if (el.classList) {
    el.classList.add(className);
  } else if (!this.hasClass(el, className)) {
    el.className += " " + className;
  }
},
removeClass: function (el, className) {
  if (el.classList) {
    el.classList.remove(className);
  } else if (this.hasClass(el, className)) {
    var reg = new RegExp('(\\s|^)' + className + '(\\s|$)');
    el.className = el.className.replace(reg, ' ');
  }
}
```


