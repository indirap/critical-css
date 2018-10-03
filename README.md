# Critical CSS

Extract critical css (above the fold) from a specific site using puppeteer.

### Usage

1) `npm i critical-css-generator`
2) Run the following:
```
const critical = require('critical-css-generator');
critical.generate({
    url: 'https://www.vistaprint.com/business-cards',
    path: 'critical-business-cards.css',
    viewport: true
});
```
3) A `critical-business-cards.css` file will be generated. Add this into the page!

Options include:
* url: URL to get critical CSS for.
* path: Where to output critical CSS. Default is `critical.css`.
* deviceName: What device to run it on. Default is Pixel 2.
* waitFor: How long to wait after page navigation before generating critical CSS. Some pages have long load times, so specifying this may be helpful. Default is 20 seconds.
* viewport: Whether to generate critical CSS (only above the fold content) or generate used CSS for the whole page. Default is true.
* cssSelectorFilter: An array of CSS selectors (regex) to always include in the generated CSS. For example: [/mobile/]. Default is [].