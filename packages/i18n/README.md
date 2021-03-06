# Internationalization (i18n)

Internationalization utilities for client-side localization. See [How to Internationalize Your Plugin](https://developer.wordpress.org/plugins/internationalization/how-to-internationalize-your-plugin/) for server-side documentation.

## Installation

Install the module:

```bash
npm install @wordpress/i18n --save
```

_This package assumes that your code will run in an **ES2015+** environment. If you're using an environment that has limited or no support for ES2015+ such as lower versions of IE then using [core-js](https://github.com/zloirock/core-js) or [@babel/polyfill](https://babeljs.io/docs/en/next/babel-polyfill) will add support for these methods. Learn more about it in [Babel docs](https://babeljs.io/docs/en/next/caveats)._

## Usage

```js
import { sprintf, _n } from '@wordpress/i18n';

sprintf( _n( '%d hat', '%d hats', 4, 'text-domain' ), 4 );
// 4 hats
```

For a complete example, see the [Internationalization section of the Gutenberg Handbook](https://wordpress.org/gutenberg/handbook/designers-developers/developers/internationalization/).

## API

<!-- START TOKEN(Autogenerated API docs) -->

### setLocaleData

[src/index.js#L45-L58](src/index.js#L45-L58)

Merges locale data into the Tannin instance by domain. Accepts data in a
Jed-formatted JSON object shape.

**Related**

-   <http://messageformat.github.io/Jed/>

**Parameters**

-   **data** `?Object`: Locale data configuration.
-   **domain** `?string`: Domain for which configuration applies.

### sprintf

[src/index.js#L159-L167](src/index.js#L159-L167)

Returns a formatted string. If an error occurs in applying the format, the
original format string is returned.

**Related**

-   <http://www.diveintojavascript.com/projects/javascript-sprintf>

**Parameters**

-   **format** `string`: The format of the string to generate.
-   **args** `...string`: Arguments to apply to the format.

**Returns**

`string`: The formatted string.

### \_n

[src/index.js#L125-L127](src/index.js#L125-L127)

Translates and retrieves the singular or plural form based on the supplied
number.

**Related**

-   <https://developer.wordpress.org/reference/functions/_n/>

**Parameters**

-   **single** `string`: The text to be used if the number is singular.
-   **plural** `string`: The text to be used if the number is plural.
-   **number** `number`: The number to compare against to use either the singular or plural form.
-   **domain** `?string`: Domain to retrieve the translated text.

**Returns**

`string`: The translated singular or plural form.

### \_nx

[src/index.js#L144-L146](src/index.js#L144-L146)

Translates and retrieves the singular or plural form based on the supplied
number, with gettext context.

**Related**

-   <https://developer.wordpress.org/reference/functions/_nx/>

**Parameters**

-   **single** `string`: The text to be used if the number is singular.
-   **plural** `string`: The text to be used if the number is plural.
-   **number** `number`: The number to compare against to use either the singular or plural form.
-   **context** `string`: Context information for the translators.
-   **domain** `?string`: Domain to retrieve the translated text.

**Returns**

`string`: The translated singular or plural form.

### \_x

[src/index.js#L107-L109](src/index.js#L107-L109)

Retrieve translated string with gettext context.

**Related**

-   <https://developer.wordpress.org/reference/functions/_x/>

**Parameters**

-   **text** `string`: Text to translate.
-   **context** `string`: Context information for the translators.
-   **domain** `?string`: Domain to retrieve the translated text.

**Returns**

`string`: Translated context string without pipe.

### \_\_

[src/index.js#L92-L94](src/index.js#L92-L94)

Retrieve the translation of text.

**Related**

-   <https://developer.wordpress.org/reference/functions/__/>

**Parameters**

-   **text** `string`: Text to translate.
-   **domain** `?string`: Domain to retrieve the translated text.

**Returns**

`string`: Translated text.


<!-- END TOKEN(Autogenerated API docs) -->

<br/><br/><p align="center"><img src="https://s.w.org/style/images/codeispoetry.png?1" alt="Code is Poetry." /></p>
