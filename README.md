## Show More/Less

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

JavaScript library that truncates text, list or table by chars, elements or row and shows/hides text blocks, elements or table row with Show More and Show Less.

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
<div class="your-class" data-type="text" data-number="80" data-after="30">
  Lorem ipsum, dolor ...
  ...
</div>
```

For list:
```html
<ul class="your-class" data-type="list" data-number="5" >
  <li>Import win</li>
  ...
</ul>
<!-- or -->
<ol class="your-class" data-type="list" data-number="5">
  <li>Import win</li>
  ...
</ol>
<!-- or -->
<div class="your-class" data-type="list" data-number="5">
  <a href="#">Administracja biur</a>
  ...
</div>
```

For table:
```html
<table class="your-class" data-type="table" data-number="2">
  ...
</table>
```
| element | description |
|--------------- |-------------|
| `data-type` | we have three type after which it will be hidden [text, list or table] |
| `data-number` | `text` after how many characters to hide the text and insert `show more/less`<br />`list` or `table` after how many elements/rows hide the rest and insert `show more/less` |
| `data-after` | this parameter allows you to set how much text should be after the `show more/less button`.<br />Let's say we have 20 records with text and we determine that the text is to be trimmed after 100<br />characters in each record, it may happen that in several records the text is very short and has<br />110 characters, so `show more/less` will appear after 100 characters and after clicking an<br />additional 10 characters, it will look funny. To prevent this, we add the `data-after="50"`<br />parameter, which means that the hidden text must be at least 50 characters. Otherwise,<br />`show more/less` will not appear. |

> Number of records counted in the table `tr` based on all `tr` of `thead`, `tbody` and `tfoot`

```javascript
document.addEventListener('DOMContentLoaded', function() {
  // text, table, list, elelemnts
  new ShowMore({
    class: 'your-class',
     show: {
        type: 'span', // [div, li, a, ...] parameter not required
        more: ' → show more', // text before expanding 
        less: ' ← less' // expanded text
     }
  });
});
```

| element | description |
|----------|-------------|
| `class` | name of the class after which we want to add support for showing/hiding text, list or table |
| `type` | on the parameter we will create an html element and put in the text `show more/less` |
| `more/less` | is the text and chars that appears after the text, list or table e.g. `> show more` and  `< show less` |


## Browsers support

| [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png" alt="IE / Edge" width="24px" height="24px" />](http://godban.github.io/browsers-support-badges/)<br/>IE / Edge | [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png" alt="Firefox" width="24px" height="24px" />](http://godban.github.io/browsers-support-badges/)<br/>Firefox | [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png" alt="Chrome" width="24px" height="24px" />](http://godban.github.io/browsers-support-badges/)<br/>Chrome | [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png" alt="Opera" width="24px" height="24px" />](http://godban.github.io/browsers-support-badges/)<br/>Opera | [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/vivaldi/vivaldi_48x48.png" alt="Vivaldi" width="24px" height="24px" />](http://godban.github.io/browsers-support-badges/)<br/>Vivaldi |
| --------- | --------- | --------- | --------- | --------- |
| IE10, IE11, Edge| last 2 versions| last 2 versions| last 2 versions| last 2 versions