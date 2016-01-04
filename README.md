# ndarray-unsqueeze [![Build Status](https://travis-ci.org/scijs/ndarray-unsqueeze.svg)](https://travis-ci.org/scijs/ndarray-unsqueeze) [![npm version](https://badge.fury.io/js/ndarray-unsqueeze.svg)](https://badge.fury.io/js/ndarray-unsqueeze) [![js-standard-style](https://img.shields.io/badge/code%20style-standard-brightgreen.svg)](http://standardjs.com/)

> Add singleton dimensions to an ndarray

## Introduction

This module takes an input ndarray and either appends a singleton dimension of length one or inserts it before a specific dimension.

## Examples

```javascript
var ndarray = require('ndarray')

unsqueeze(ndarray([1, 2, 3, 4], [2, 2]))
// => ndarray([1, 2, 3, 4], [2, 2, 1])

unsqueeze(ndarray([1, 2, 3, 4], [2, 2]), 0)
// => ndarray([1, 2, 3, 4], [1, 2, 2])
``

## Installation

```javascript
$ npm install ndarray-unsqueeze
```

## API

#### `require('ndarray-unsqueeze')(input[, axis])`

Arguments:
- `input`: The input ndarray to be unsqueeze
- `axes` (optional):  An integer index of the dimension at which to insert the singleton dimension. If unspecified, singleton dimension is appended to the shape.

Returns:
A new array view of the unsqueezed ndarray (i.e. a new ndarray object with the same underlying data).


## License
&copy; 2016 Ricky Reusser. MIT License.
