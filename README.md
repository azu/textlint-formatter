# textlint-formatter [![Build Status](https://travis-ci.org/azu/textlint-formatter.svg)](https://travis-ci.org/azu/textlint-formatter)

[textlint](https://github.com/azu/textlint "azu/textlint") output formatter.

## Installation

```
npm install textlint-formatter
```

## Usage

See [formatters/](lib/formatters).

Currently, you can use "stylish" (defaults), "compact", "checkstyle", "jslint-xml", "junit", "tap", "pretty-error".

```js
var createFormatter = require("textlint-formatter")
var formatter = createFormatter({
    formatterName: "stylish"
});
var output = formatter([
    {
        filePath: "./myfile.js",
        messages: [
            {
                ruleId: "semi",
                line: 1,
                column: 23,
                message: "Expected a semicolon."
            }
        ]
    }
]);
console.log(output);
/*
./myfile.js
  1:23  warning  Expected a semicolon  semi

✖ 1 problem
*/
```

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## License

MIT