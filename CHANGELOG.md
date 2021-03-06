# Change Log

## 1.7.2

*2018-05-20*

- Updated `options.onError` callback `url` argument so that it always returns an
  absolute URL.

- Updated README with `options.onError` fixes and a few other minor tweaks.

## 1.7.1

*2018-05-19*

- Fixed `options.onError` message sent to console so that a URL is included when
  the status code is `0`. Also added a hint that these errors are possibly
  related to CORS restrictions to assist debugging efforts.

- Updated README with performance tips and better examples for `options.include`
  and `options.exclude`.

## 1.7.0

*2018-05-18*

- Improved performance when processing `<link>` and `<style>` data that does not
  contain a CSS custom property declaration or function.

## 1.6.0

*2018-05-17*

- Added `options.updateURLs` for converting relative `url()` paths to absolute
  urls.

## 1.5.0

*2018-05-16*

- Added `options.onBeforeSend` callback.

- Changed `options.onSuccess` callback so that it is called after CSS data has
  been collected from each node before CSS custom properties have been
  transformed.

## 1.4.0

*2018-04-23*

- Updated `get-css-data` dependency to 1.2.0 to resolve a callback related bug.

- Updated logic for inserting generated `<style>` element. Element is now
  inserted after the last `<style>` or `<link>` node processed. This
  change, combined with the proceeding change, ensures that the original cascade
  order is maintained after the transformed styles are appended to the DOM.

- Updated `options.onlyVars` default value from `true` to `false`. This
  change, combined with the preceding change, ensures that the original cascade
  order is maintained after the transformed styles are appended to the DOM.

## 1.3.0

*2018-04-17*

- Added `fixNestedCalc` option to remove nested `calc` keywords for legacy
  browser compatibility.

## 1.2.2

*2018-03-24*

- Updated README Examples section.

## 1.2.1

*2018-03-20*

- Updated README Examples section.

## 1.2.0

*2018-03-20*

- Fixed "Cannot read property 'length' of undefined" bug triggered while
  filtering comments that are a direct descendant of an at-rule.

## 1.1.2

*2018-03-12*

- Updated README browser support table.

## 1.1.1

*2018-03-12*

- Updated README: Added TOC, added demo link, added browser support table,
  updated examples.

## 1.1.0

*2018-02-08*

- Fixed bug that prevented `options.onlyVars` from properly filtering
  declarations that do not contain a custom property value or function.

- Updated `options.preserve` default value from `true` to `false`. This aligns
  with other default values which assume a "legacy-only" configuration.

- Updated logic for inserting generated `<style>` element. Element is now
  inserted as first CSS source node rather than the last. This allows the
  cascade order to be maintained when `options.onlyVars` is `true`.

## 1.0.0

*2018-01-31*

- Initial release
