# Semantic-UI.ngDropdown
Semantic UI - Dropdown AngularJS

<p>
  <a href="https://gitter.im/miamarti/semanticUI.ngDropdown" target="_blank"><img src="https://img.shields.io/gitter/room/nwjs/nw.js.svg"></a>
  <img src="https://img.shields.io/badge/semanticUI.ngDropdown-release-green.svg">
  <img src="https://img.shields.io/badge/version-1.0.0-blue.svg">
  <img src="https://img.shields.io/github/license/mashape/apistatus.svg">
  <a href="https://github.com/miamarti/Semantic-UI.ngDropdown/tarball/master"><img src="https://img.shields.io/github/downloads/atom/atom/latest/total.svg"></a>
  <img src="https://img.shields.io/bower/v/bootstrap.svg">
</p>



<h3>Dropdown</h3>
A dropdown allows a user to select a value from a series of options.

<h3>Dependencies</h3>
* AngularJS

<h3>Implementation</h3>
```
<ng-dropdown 
  ng-model="modelA" 
  ng-option="optionList"
  ng-additions="true" 
  data-url="/api/search?={query}" 
  data-label="name">
</ng-dropdown>
```

## Bower install de dependency
```
$ bower install semanticUI.ngDropdown --save
```

## Module AngularJS include
```
angular.module('example', ["ngDropdown"]);
```
