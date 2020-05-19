## Show More/Less

This plugin provide functionality to append show-more controls to DOM-elements that are either text or lists.

### Demo

[https://tomik23.github.io/show-more/](https://tomik23.github.io/show-more/)

## Clone the repo and install dependencies
```bash
git clone
cd show-more
yarn
# or
npm i
```
## Watch/Build the app
Watch the app, just call:

```bash
yarn dev
# or
npm run dev
```

Build app:

```bash
yarn prod
# or
npm run prod
```

## Configuration of the plugin

For text:
```html
<div class="show-more" data-type="text" data-number="80">
  ...
</div>
```

For list:
```html
<ul class="show-list" data-type="list" data-number="5">
  ...
</ul>
```

For table:
```html
<table class="show-table" data-type="table" data-number="2">
```
> Important, the table must contain the tbody element. [See example](https://tomik23.github.io/show-more/)

```javascript
document.addEventListener('DOMContentLoaded', function() {
  new ShowMore({
    class: 'show-more',
     show: {
        type: 'span',
        more: ' | Show more',
        less: ' | Show less'
     }
  });

  new ShowMore({
    class: 'show-list',
     show: {
        type: 'li',
        more: ' &#8681; show more',
        less: ' &#8679; show less'
     }
  })

});
```

`class` - name of the class after which we want to add support for showing / hiding text or list,
 `more` and `less` is the text that appears after the text or list.


## Browsers support

| [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png" alt="IE / Edge" width="24px" height="24px" />](http://godban.github.io/browsers-support-badges/)<br/>IE / Edge | [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png" alt="Firefox" width="24px" height="24px" />](http://godban.github.io/browsers-support-badges/)<br/>Firefox | [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png" alt="Chrome" width="24px" height="24px" />](http://godban.github.io/browsers-support-badges/)<br/>Chrome | [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png" alt="Opera" width="24px" height="24px" />](http://godban.github.io/browsers-support-badges/)<br/>Opera | [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/vivaldi/vivaldi_48x48.png" alt="Vivaldi" width="24px" height="24px" />](http://godban.github.io/browsers-support-badges/)<br/>Vivaldi |
| --------- | --------- | --------- | --------- | --------- |
| IE10, IE11, Edge| last 2 versions| last 2 versions| last 2 versions| last 2 versions