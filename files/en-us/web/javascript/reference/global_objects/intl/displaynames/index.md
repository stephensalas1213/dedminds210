---
title: Intl.DisplayNames
slug: Web/JavaScript/Reference/Global_Objects/Intl/DisplayNames
page-type: javascript-class
tags:
  - Class
  - DisplayNames
  - Internationalization
  - Intl
  - JavaScript
  - Localization
  - Reference
browser-compat: javascript.builtins.Intl.DisplayNames
---

{{JSRef}}

The **`Intl.DisplayNames`** object enables the consistent translation of language, region and script display names.

{{EmbedInteractiveExample("pages/js/intl-displaynames.html")}}

<!-- The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone https://github.com/mdn/interactive-examples and send us a pull request. -->

## Constructor

- {{jsxref("Intl/DisplayNames/DisplayNames", "Intl.DisplayNames()")}}
  - : Creates a new `Intl.DisplayNames` object.

## Static methods

- {{jsxref("Intl/DisplayNames/supportedLocalesOf", "Intl.DisplayNames.supportedLocalesOf()")}}
  - : Returns an array containing those of the provided locales that are supported without having to fall back to the runtime's default locale.

## Instance methods

- {{jsxref("Intl/DisplayNames/of", "Intl.DisplayNames.prototype.of()")}}
  - : This method receives a `code` and returns a string based on the locale and options provided when instantiating `Intl.DisplayNames`.
- {{jsxref("Intl/DisplayNames/resolvedOptions", "Intl.DisplayNames.prototype.resolvedOptions()")}}
  - : Returns a new object with properties reflecting the locale and formatting options computed during initialization of the object.

## Examples

### Region Code Display Names

To create an `Intl.DisplayNames` for a locale and get the display name for a region code.

```js
// Get display names of region in English
let regionNames = new Intl.DisplayNames(['en'], {type: 'region'});
regionNames.of('419'); // "Latin America"
regionNames.of('BZ');  // "Belize"
regionNames.of('US');  // "United States"
regionNames.of('BA');  // "Bosnia & Herzegovina"
regionNames.of('MM');  // "Myanmar (Burma)"

// Get display names of region in Traditional Chinese
regionNames = new Intl.DisplayNames(['zh-Hant'], {type: 'region'});
regionNames.of('419'); // "????????????"
regionNames.of('BZ');  // "?????????"
regionNames.of('US');  // "??????"
regionNames.of('BA');  // "??????????????????????????????"
regionNames.of('MM');  // "??????"
```

### Language Display Names

To create an `Intl.DisplayNames` for a locale and get the display name for a language-script-region sequence.

```js
// Get display names of language in English
let languageNames = new Intl.DisplayNames(['en'], {type: 'language'});
languageNames.of('fr');      // "French"
languageNames.of('de');      // "German"
languageNames.of('fr-CA');   // "Canadian French"
languageNames.of('zh-Hant'); // "Traditional Chinese"
languageNames.of('en-US');   // "American English"
languageNames.of('zh-TW');   // "Chinese (Taiwan)"]

// Get display names of language in Traditional Chinese
languageNames = new Intl.DisplayNames(['zh-Hant'], {type: 'language'});
languageNames.of('fr'); // "??????"
languageNames.of('zh'); // "??????"
languageNames.of('de'); // "??????"
```

### Script Code Display Names

To create an `Intl.DisplayNames` for a locale and get the display name for a script code.

```js
// Get display names of script in English
let scriptNames = new Intl.DisplayNames(['en'], {type: 'script'});
// Get script names
scriptNames.of('Latn'); // "Latin"
scriptNames.of('Arab'); // "Arabic"
scriptNames.of('Kana'); // "Katakana"

// Get display names of script in Traditional Chinese
scriptNames = new Intl.DisplayNames(['zh-Hant'], {type: 'script'});
scriptNames.of('Latn'); // "?????????"
scriptNames.of('Arab'); // "????????????"
scriptNames.of('Kana'); // "?????????"
```

### Currency Code Display Names

To create an `Intl.DisplayNames` for a locale and get the display name for currency code.

```js
// Get display names of currency code in English
let currencyNames = new Intl.DisplayNames(['en'], {type: 'currency'});
// Get currency names
currencyNames.of('USD'); // "US Dollar"
currencyNames.of('EUR'); // "Euro"
currencyNames.of('TWD'); // "New Taiwan Dollar"
currencyNames.of('CNY'); // "Chinese Yuan"

// Get display names of currency code in Traditional Chinese
currencyNames = new Intl.DisplayNames(['zh-Hant'], {type: 'currency'});
currencyNames.of('USD'); // "??????"
currencyNames.of('EUR'); // "??????"
currencyNames.of('TWD'); // "?????????"
currencyNames.of('CNY'); // "?????????"
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- {{jsxref("Intl")}}
