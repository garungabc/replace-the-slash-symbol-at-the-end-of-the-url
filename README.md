# replace-the-slash-symbol-at-the-end-of-the-url
replace the slash symbol at the end of the url - with Javascript

```php
var cur_url = window.location.href;
var index_cur = cur_url.lastIndexOf("/");
if(cur_url[index_cur + 1] === undefined) {
    var stateObj = { foo: cur_url };
    var replace_result = cur_url.substring(0, index_cur);
    history.replaceState(stateObj, replace_result, replace_result);
}
```
> refer: <a href="https://developer.mozilla.org/en-US/docs/Web/API/History_API">https://developer.mozilla.org/en-US/docs/Web/API/History_API </a>
