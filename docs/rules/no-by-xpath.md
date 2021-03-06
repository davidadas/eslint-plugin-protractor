# Discourage the use of `by.xpath` locator (no-by-xpath)

Ensure `by.xpath` locator is not used.

## Rule details

According to the [Protractor's style guide](https://github.com/angular/protractor/blob/master/docs/style-guide.md#never-use-xpath), using `by.xpath` is considered a bad practice. 

The following patterns are considered warnings:

```js
element(by.xpath("//a[starts-with(@href, 'something')]"));
element.all(by.xpath("//a[starts-with(@href, 'something')]"));
```

The following patterns are not warnings:

```js
element(by.css("a[href^=something]"));
element.all(by.css("a[href^=something]"));
```
