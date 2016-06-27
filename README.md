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

## Dropdown
A dropdown allows a user to select a value from a series of options.

## Dependencies
* AngularJS

## Implementation
```
<ng-dropdown 
  ng-model="modelA" 
  ng-option="optionList">
</ng-dropdown>
```

## Option List
```
// Expected server response
[
  {"id": 1, "value": "Option 1"},
  {"id": 2, "value": "Option 2"}
]
```
OR

    In this case simply assign the parameter data-label as a "label"
```
// Expected server response
[
  {"id": 1, "label": "Option 1"},
  {"id": 2, "label": "Option 2"}
]
```
OR
```
// Expected server response
{
  "1": {"id": 1, "value": "Option 1"},
  "2": {"id": 2, "value": "Option 2"}
}
```

## Parameters

| Name         | Type    | Dinamic | Mandatory | Description                                                  |
| ------------ | ------- | ------- | --------- | ------------------------------------------------------------ |
| ng-model     | String  | True    | True      | Scope of the attribute that will be the model                |
| ng-option    | Array   | True    | True      | Combo Object List                                            |
| ng-additions | Boolean | false   | False     | It allows adding options that are not on the list            |
| data-url     | String  | false   | False     | URL that will be requested for consultations on the back-end |
| data-label   | String  | false   | False     | JSON attribute name to be used as label                      |

## Custom Label
```
<ng-dropdown 
  ng-model="modelA" 
  ng-option="optionList" 
  data-label="name">
</ng-dropdown>
```

## Additional values (Suggestion)
```
<ng-dropdown 
  ng-model="modelA" 
  ng-option="optionList"
  ng-additions="true">
</ng-dropdown>
```

## Remote API
```
<ng-dropdown 
  ng-model="modelA" 
  ng-option="optionList" 
  data-url="/api/search?={query}">
</ng-dropdown>
```

```
// Expected server response
{
    "success": true,
    "results": [
      {
        // name displayed in dropdown
        "name"  : "Choice 1",
         // selected value
        "value" : "value1",
         // name displayed after selection (optional)
        "text"  : "Choice 1"
         // whether field should be displayed as disabled (optional)
        "disabled"  : false
       },
      {
        "name"  : "Choice 2",
        "value" : "value2",
        "text"  : "Choice 2"
      },
      {
        "name"  : "Choice 3",
        "value" : "value3",
        "text"  : "Choice 3"
      },
      {
        "name"  : "Choice 4",
        "value" : "value4",
        "text"  : "Choice 4"
      },
      {
        "name"  : "Choice 5",
        "value" : "value5",
        "text"  : "Choice 5"
      }
    ]
}
```

## Bower install de dependency
```
$ bower install semanticUI.ngDropdown --save
```

## Module AngularJS include
```
angular.module('example', ["ngDropdown"]);
```
