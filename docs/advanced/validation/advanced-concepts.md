# Validation - Advanced Concepts

This is a functional styled validation engine.  It is an attempt to create a functional, easy to use, validation library that has a very small implementation footprint.  It is the goal of this library to remove as much ceremony as possible and allow for rich validation operations.

Given the following customer object:

``` javascript
var cust = {
  name: 'john',
  age: 19,
  shirtSize: 'large',
};
```

Next, using the following schema validation:

``` javascript
var schema = {
  name: all([required(), minLen(4), maxLen(12)]),
  age: all([min(21), max(55)]),
  shirtSize: all([within(['small', 'medium', 'large'])])
};
```

Finally, you run the validation engine:

``` javascript
var val = validate(schema);
var result = val(cust);
console.log(result);
```

You would get the following in the result object:

``` javascript
{ name: { 
    name: 'name', 
    value: 'john', 
    result: [ ] 
  },
  age: { 
    name: 'age',
    value: 19,
    result: [ 'Age must be greater than 21' ] 
  },
  shirtSize: { 
    name: 'shirtSize', 
    value: 'large', 
    result: [ ] 
  } 
}
```

As you can see, the engine tries to create intelligent validation messages when a failure happens.  However, you can override this at any time.  Here is an example of a schema that overrides the age error message:

``` javascript
var schema = {
  name: all([required(), minLen(4), maxLen(12)]),
  age: all([min(21, "Sorry, you are not the legal age!"), max(55)]),
  shirtSize: all([within(['small', 'medium', 'large'])])
};

var val = validate(schema);
var result = val(cust);
console.log(result);
```

You now get the following error message:

``` javascript
{ name: { 
    name: 'name', 
    value: 'john', 
    result: [ ] 
  },
  age: { 
    name: 'age',
    value: 19,
    result: [ 'Sorry, you are not the legal age!' ] 
  },
  shirtSize: { 
    name: 'shirtSize', 
    value: 'large', 
    result: [ ] 
  } 
}
```

##Documentation
Please refer to the following documentation for more information:

- [API](../../reference/validation/readme.md)
  - [one](../../reference/validation/readme.md#onetarget-fail)
  - [all](../../reference/validation/readme.md#alltarget-fail)
  - [required](../../reference/validation/readme.md#requiredtarget-fail)
  - [eq](../../reference/validation/readme.md#eqtarget-fail)
  - [notEq](../../reference/validation/readme.md#noteqtarget-fail)
  - [min](../../reference/validation/readme.md#mintarget-fail)
  - [max](../../reference/validation/readme.md#maxtarget-fail)
  - [eqLen](../../reference/validation/readme.md#eqlentarget-fail)
  - [minLen](../../reference/validation/readme.md#minlentarget-fail)
  - [maxLen](../../reference/validation/readme.md#maxlentarget-fail)
  - [within](../../reference/validation/readme.md#withintarget-fail)
  - [regex](../../reference/validation/readme.md#regextarget-fail)
  - [isNotNil](../../reference/validation/readme.md#isnotniltarget-fail)
  - [isNotEmpty](../../reference/validation/readme.md#isnotemptytarget-fail)
  - [isNumber](../../reference/validation/readme.md#isnumbertarget-fail)
  - [isString](../../reference/validation/readme.md#isstringtarget-fail)
  - [isObject](../../reference/validation/readme.md#isobjecttarget-fail)
  - [isFunction](../../reference/validation/readme.md#isfunctiontarget-fail)
  - [isNumeric](../../reference/validation/readme.md#isnumerictarget-fail)
  - [phone](../../reference/validation/readme.md#phonetarget-fail)
  - [email](../../reference/validation/readme.md#emailtarget-fail)
  - [url](../../reference/validation/readme.md#urltarget-fail)

##Dependencies
The validator has a dependency on the following:

* [RamdaJS](http://ramdajs.com) - A practical functional library for Javascript programmers.

We use RamdaJS as our functional library to help us create our validation engine as well as our validation functions.  We are using BabelJS to allow for transpiling our ES6 code back to ES5 with a special emphasis on fat arrow (=>) syntax.  

##Limitations
This library does not try to support nested-validations.  In fact, it is recommended that you produce a schema for each level you wish to validate.
