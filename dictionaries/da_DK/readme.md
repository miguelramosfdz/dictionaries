# dictionary-da-dk

Danish (Denmark) spelling dictionary in UTF-8.

Useful with [hunspell][hunspell] ([node bindings][nodehun] or
[plain javascript][nspell]), Open Office, LibreOffice, FireFox and
Thunderbird, or [place them in `~/Library/Spelling`][osx] on OS X.

Generated by [**wooorm/dictionaries**][dictionaries], from [this
dictionary][source].

## Installation

[npm][npm]:

```bash
npm install dictionary-da-dk
```

## Usage

```js
var daDK = require('dictionary-da-dk');

daDK(function (err, result) {
  console.log(err || result);
});
```

Yields:

```js
{ dic: <Buffer>,
  aff: <Buffer> }
```

Where `dic` is a buffer for the dictionary file at `index.dic` (in UTF-8), and
`aff` is a buffer for the affix file at `index.aff` (in UTF-8).

Or directly load the files, using something like:

```js
var path = require('path');
var base = require.resolve('dictionary-da-dk');

// NEVER USE `readFileSync` IN PRODUCTION.
fs.readFileSync(path.join(base, 'index.dic'), 'utf-8');
fs.readFileSync(path.join(base, 'index.aff'), 'utf-8');
```

## License

Dictionary and affix file: [(GPL-2.0 OR LGPL-2.0 OR MPL-1.1)](https://github.com/wooorm/dictionaries/blob/master/dictionaries/da_DK/LICENSE).
Rest: MIT © [Titus Wormer][home].

[hunspell]: http://hunspell.sourceforge.net

[nodehun]: https://github.com/nathanjsweet/nodehun

[nspell]: https://github.com/wooorm/nspell

[osx]: https://github.com/wooorm/dictionaries#os-x

[source]: http://extensions.openoffice.org/en/project/danish-spellcheck-and-hyphenation-dictionaries

[npm]: https://docs.npmjs.com/cli/install

[dictionaries]: https://github.com/wooorm/dictionaries

[home]: https://wooorm.com
