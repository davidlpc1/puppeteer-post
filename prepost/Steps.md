# Installing puppeteer
```
    npm i puppeteer
    yarn add puppeteer
```
### Note: When you install Puppeteer, it downloads a recent version of Chromium (~170MB Mac, ~282MB Linux, ~280MB Win) that is guaranteed to work with the API

# Using puppeteer
## Create src/index.js
## Require puppeteer
```js
    const puppeteer = require('puppeteer')
```

## Create the function will screenshot a page(param)
```js
    async function screenshot(url){

    }
```

### Create a browser
```js
     const browser = await puppeteer.launch();
```

### Create a page and go to that page
```js
  const page = await browser.newPage();
  await page.goto(url);
```

### Screenshot and close the browser
```js
  await page.screenshot({ path:"screenshot.png" });

  await browser.close();
```

### Run the function
```js
    screenshot("https://google.com/")
```

### Run the code
```
    node src/index.js
```