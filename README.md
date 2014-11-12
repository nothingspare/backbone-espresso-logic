backbone-espresso-logic
=======================

## About : ##

backbone-espresso-logic provides a simple way to adapt your Backbone.Model to Espresso Logic API requests and responses
 by providing API Filter configuration and response data parsing.

Licence: MIT (see LICENCE file)
see https://github.com/EspressoLogicCafe/npm-espressologic for an SDK to read the meta model (@tables) and create generated resources for backbone developers. 

## API Filter usage : ##

```javascript
// Create the model and set the urlRoot for example
var MyModel = Backbone.EspressoLogic.Model.extend({
    myProp: 'myPropValue',
    urlRoot: 'https://api.com/my/resource'
});
//
var resourceId = 1;
var myModel = new MyModel(
    { some: "attribute" },
    { apiFilter: "?filter=id = '" + resourceId + "'" } // Passing apiFilter option to append to the url
},)
// myModel.url(); will result "https://api.com/my/resource?filter=id = '1'"
```
