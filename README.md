# Angular Shim
ES6 compiled AMD wrapper for [Angular.js](https://angularjs.org/)


## How to use
1. Include your desired module script after the inclusion of `angular.js`
1. Import `angular` as a module in your script
1. Enjoy your importable use of angular


### Loaders
Extra libraries may be required for your project

|Module Type|Loader Name|Tested|
|-----------|-----------|------|
|amd|[loader.js](https://github.com/ember-cli/loader.js)|Passed|


### Examples

#### ES6
```js
import angular from 'angular'

angular.module('thing', []);
```


#### AMD
This may be an unnecessary library if you are using `requirejs`. Instead you can let it create the shim for you, optimized for your amd loader. More about that [here](http://requirejs.org/docs/api.html#config-shim).

```js
requirejs.config(
  paths: {
    // ...
  },
  shim: {
    'angular': {
      exports: 'angular'
    }
  }
)
```


```js
define('thing', ['angular'], function (angular) {
  angular.module('thing', []);
});
```


## Testing
Testing is limited to a quick `src` and `dist` check for linting: `npm test`
