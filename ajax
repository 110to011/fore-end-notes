# ajax的js实现

```js
function ajax(url,callback) {
    var xhr = new XHLHttpRequest();
    
    xhr.open('GET',url,true);
    
    xhr.onreadystatechange = function() {
        if(xhr.readyState == 4 && xhr.status == 200) {
            callback(xhr.responseText);
        }
    }
    
    xhr.send();
}
```
