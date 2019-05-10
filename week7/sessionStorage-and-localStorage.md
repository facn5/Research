## sessionStorage and localStorage
sessionStorage property allows you to accesss a Storage object for the current browser session.

localStorage allows you to access a Storage object for the Document's origin, stored across browser sessions.

sessionStorage gets cleared when the page session ends, localStorage has no expiration time.

The keys and values are always strings


---




## Syntax

```
sessionStorage.setItem('key', 'value');
let data = sessionStorage.getItem('key');
sessionStorage.removeItem('key');
sessionStorage.clear();


myStorage = window.localStorage;
localStorage.setItem('myCat', 'Tom');
var cat = localStorage.getItem('myCat');
localStorage.removeItem('myCat');
localStorage.clear();
```
