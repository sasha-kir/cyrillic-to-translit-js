# cyrillic-to-translit-js

[![Codeship Status for greybax/cyrillic-to-translit-js](https://app.codeship.com/projects/9666e180-f1e1-0136-edda-0a4322211bb2/status?branch=master)](https://app.codeship.com/projects/320439)

[![NPM version][npm-image]][npm-url]
[![NPM Downloads/month][npm-downloads-image]][npm-downloads-url]
[![Build Status][travis-image]][travis-url]
[![Coveralls Status][coveralls-image]][coveralls-url]
[![Dependency Status][depstat-image]][depstat-url]
[![DevDependency Status][depstat-dev-image]][depstat-dev-url]

[npm-url]: https://npmjs.org/package/cyrillic-to-translit-js
[npm-image]: https://img.shields.io/npm/v/cyrillic-to-translit-js.svg

[npm-downloads-url]: https://npmjs.org/package/cyrillic-to-translit-js
[npm-downloads-image]: https://img.shields.io/npm/dm/cyrillic-to-translit-js.svg

[travis-url]: https://travis-ci.org/greybax/cyrillic-to-translit-js
[travis-image]: https://travis-ci.org/greybax/cyrillic-to-translit-js.svg

[coveralls-url]: https://coveralls.io/r/greybax/cyrillic-to-translit-js
[coveralls-image]: https://img.shields.io/coveralls/greybax/cyrillic-to-translit-js.svg

[depstat-url]: https://david-dm.org/greybax/cyrillic-to-translit-js
[depstat-image]: https://david-dm.org/greybax/cyrillic-to-translit-js.svg

[depstat-dev-url]: https://david-dm.org/greybax/cyrillic-to-translit-js
[depstat-dev-image]: https://david-dm.org/greybax/cyrillic-to-translit-js/dev-status.svg


Simple javascript function for converting Cyrillic symbols to Translit

[Demo page](https://greybax.github.io/cyrillic-to-translit-js)

[![Patreon](https://c5.patreon.com/external/logo/become_a_patron_button.png)](https://www.patreon.com/bePatron?u=14980891)

## Install

`npm install --save cyrillic-to-translit-js`

## Simple to use

### Constructor

* `{ preset: ru }` or _**empty**_ - transliteration preset for Russian language.
* `{ preset: uk }` - transliteration preset for Ukranian language (see [PR #27](https://github.com/greybax/cyrillic-to-translit-js/pull/27)). 
  * [Rules](https://pasport.org.ua/vazhlivo/transliteratsiya)
  * [Apostrophe](https://uk.wikipedia.org/wiki/%D0%90%D0%BF%D0%BE%D1%81%D1%82%D1%80%D0%BE%D1%84#.D0.A2.D0.B5.D1.85.D0.BD.D1.96.D1.87.D0.BD.D1.96_.D0.BE.D1.81.D0.BE.D0.B1.D0.BB.D0.B8.D0.B2.D0.BE.D1.81.D1.82.D1.96)

### transform()

`cyrillicToTranslit().transform(input, spaceReplacement);`

* `input` - string which should be transformed
* `spaceReplacement` - symbol for space replacement

## Examples

```javascript
  cyrillicToTranslit().transform('Привет Мир!');

  >Privet Mir!
```

```javascript
  cyrillicToTranslit().transform('привет мир!', "_")

  >privet_mir!
```

```javascript
  cyrillicToTranslit({ preset: "uk" }).transform('привіт світе!', "_")

  >pryvit_svite!
```

## Typescript

Typescript supports starting form v2.0.0. See definitions [here](./CyrillicToTranslit.d.ts)

## Credits

* [kunashir](https://github.com/kunashir)
* [Vasyl Gendzeliuk](https://github.com/vasergen)
* [Nikita Svesnikov](https://github.com/nitruxa)
* [Igor Deryabin](https://github.com/ideryabin)
* [makepost](https://github.com/makepost)
* [Aleksey Kislov](https://github.com/evenfrost)
* [Igor Kamyshev](https://github.com/igorkamyshev)


## License

MIT © Aleksandr Filatov [alfilatov.com](http://alfilatov.com)
