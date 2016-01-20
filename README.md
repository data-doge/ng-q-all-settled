# ng-q-all-settled

adds [Q's allSettled method](https://github.com/kriskowal/q/wiki/API-Reference#promiseallsettled) to [Angular's $q](https://docs.angularjs.org/api/ng/service/$q), using code from [this gist](https://gist.github.com/Aaronius/46ae4a0f8ff052cd24f0) by @Aaronius

## install

`npm install ng-q-all-settled`

## usage

```js

require('angular')
require('ng-q-all-settled')

var exampleApp = angular.module('exampleApp', ['qAllSettled'])

exampleApp.controller('exampleController', ['$scope', '$q', function ($scope, $q) {

  $q.allSettled(promiseArray).then(function (settledPromiseArray) {
    // executed if all promises are resolved
  }).catch(function () {
    // executed if any promises are rejected
  }).finally(function () {
    // executed when all promises have settled
  })

}])

```
