```js
function $ (query, callback) {
    var elements = document.querySelectorAll(query);
    
    if (!callback) {
        return Array.prototype.slice.apply(elements);
    }

    for (var i = 0; i < elements.length; i++) {
        var element = elements[i];
        callback.apply(element, [element, i]);
    }
}
```