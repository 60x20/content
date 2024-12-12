---
title: "DOMMatrixReadOnly: multiply() method"
short-title: multiply()
slug: Web/API/DOMMatrixReadOnly/multiply
page-type: web-api-instance-method
browser-compat: api.DOMMatrixReadOnly.multiply
---

{{APIRef("Geometry Interfaces")}}{{AvailableInWorkers}}

The **`multiply()`** method of the {{domxref("DOMMatrixReadOnly")}} interface creates a new matrix being the result of the multiplication of the original matrix. The method returns a new {{domxref("DOMMatrix")}} created by computing the dot product of the source matrix and the specified matrix: `A⋅B`. If no matrix is specified as the multiplier, the matrix is multiplied by a matrix in which every element is `0` _except_ the bottom-right corner and the element immediately above and to its left: `m33` and `m34`. These have the default value of `1`. The original matrix is not modified.

To mutate the matrix as you multiply it, see {{domxref("DOMMatrix.multiplySelf()")}}

## Syntax

```js-nolint
  DOMMatrixReadOnly.multiply( )
  DOMMatrixReadOnly.multiply( otherMatrix )
```

### Parameters

- `otherMatrix`
  - : The [`DOMMatrix`](/en-US/docs/Web/API/DOMMatrix) multiplier.

### Return value

A {{domxref("DOMMatrix")}}.

## Examples

```js
const matrix = new DOMMatrixReadOnly().translate(13, 21);
const multipliedMatrix = matrix.multiply(matrix);
console.log(matrix.toString()); // output: matrix(1, 0, 0, 1, 13, 21)
console.log(multipliedMatrix.toString()); // output: matrix(1, 0, 0, 1, 26, 42)
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- {{domxref("DOMMatrix.multiplySelf()")}}
- {{domxref("DOMMatrixReadOnly.preMultiply()")}}
- CSS {{CSSxRef("transform-function/matrix", "matrix()")}} function
- CSS {{CSSxRef("transform-function/matrix3d", "matrix3d()")}} function
