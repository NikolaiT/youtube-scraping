# A Node library to scrape youtube videos

### Installation

```$xslt
git clone https://github.com/NikolaiT/youtube-scraping
```

Then install dependencies:

```$xslt
npm install
```

### Usage

Create a source file in the directory you downloaded the package and
add the following code.

```javascript
const puppeteer = require('puppeteer');
const youtube = require('./youtube');

try {
    (async () => {

        let keywords = [
            'scrapeulous.com',
            'scraping youtube',
            'stupid prank',
        ];

        const browser = await puppeteer.launch();
        let results = await youtube.scrape_youtube(browser, keywords);
        console.dir(results, {depth: null, colors: true});

        await browser.close();

    })()
} catch (err) {
    console.error(err)
}
```
