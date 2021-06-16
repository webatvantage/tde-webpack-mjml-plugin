# Webatvantage Webpack MJML Plugin 

Webpack plugin for converting MJML files to HTML.  
Forked from TDE Webpack MJML Plugin.

## Install

```bash
npm install --save-dev webatvantage-webpack-mjml-plugin
```

## Usage

In your `webpack.config.js`

```javascript
const MjmlPlugin = require('webatvantage-webpack-mjml-plugin');

module.exports = {
    // ...
    plugins: [
        new MjmlPlugin(paths.MJML, {
            extension: '.twig',
            outputPath: path.resolve(__dirname, 'path/to/mjml'),
        }),
    ]
};
```

## API:

```js
// webpack.config.js

module.exports = {
    plugins: [
        new MjmlPlugin(inputPath, {
            extension: options.extension,
            outputPath: options.outputPath,
            // MJML options (https://documentation.mjml.io/#inside-node-js)
            filePath: path.resolve(__dirname, 'path/to/file'),
            keepComments: false,
        }),
    ]
}
```

### `inputPath`

Type: `String`

The path where MJML files are located

### `options.extension`

Type: `String`<br>
Default: `".html"`

The default output extension

### `options.outputPath`

Type: `String`<br>
Default: `""`

The path where HTML files should be written to

### `MJML options`
Pass optional options to the mjml2html function  
List of available options: https://documentation.mjml.io/#inside-node-js


## License

MIT © [TDE](https://github.com/tdeNL)  
MIT © [Webatvantage](https://github.com/webatvantage)
