---
title: Math.asin()
slug: Web/JavaScript/Reference/Global_Objects/Math/asin
page-type: javascript-static-method
tags:
  - JavaScript
  - Math
  - Method
  - Reference
browser-compat: javascript.builtins.Math.asin
---

{{JSRef}}

The **`Math.asin()`** static method returns the inverse sine (in radians) of a number. That is,

<math display="block" xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mo>β</mo><mi>x</mi><mo>β</mo><mo stretchy="false">[</mo><mrow><mo>β</mo><mn>1</mn></mrow><mo>,</mo><mn>1</mn><mo stretchy="false">]</mo><mo>,</mo><mspace width="0.2777777777777778em"></mspace><mrow><mo lspace="0em" rspace="0.16666666666666666em">πΌπππ.ππππ</mo><mo stretchy="false">(</mo><mi>π‘</mi><mo stretchy="false">)</mo></mrow><mo>=</mo><mo lspace="0em" rspace="0em">arcsin</mo><mo stretchy="false">(</mo><mi>x</mi><mo stretchy="false">)</mo><mo>=</mo><mtext>the unique&nbsp;</mtext><mi>y</mi><mo>β</mo><mrow><mo>[</mo><mrow><mo>β</mo><mfrac><mi>Ο</mi><mn>2</mn></mfrac><mo>,</mo><mfrac><mi>Ο</mi><mn>2</mn></mfrac></mrow><mo>]</mo></mrow><mtext>&nbsp;such that&nbsp;</mtext><mo lspace="0em" rspace="0em">sin</mo><mo stretchy="false">(</mo><mi>y</mi><mo stretchy="false">)</mo><mo>=</mo><mi>x</mi></mrow><annotation encoding="TeX">\forall x \in [{-1}, 1],\;\mathtt{\operatorname{Math.asin}(x)} = \arcsin(x) = \text{the unique } y \in \left[-\frac{\pi}{2}, \frac{\pi}{2}\right] \text{ such that } \sin(y) = x</annotation></semantics></math>

{{EmbedInteractiveExample("pages/js/math-asin.html")}}

## Syntax

```js-nolint
Math.asin(x)
```

### Parameters

- `x`
  - : A number between -1 and 1, inclusive, representing the angle's sine value.

### Return value

The inverse sine (angle in radians between <math><semantics><mrow><mo>-</mo><mfrac><mi>Ο</mi><mn>2</mn></mfrac></mrow><annotation encoding="TeX">-\frac{\pi}{2}</annotation></semantics></math> and <math><semantics><mfrac><mi>Ο</mi><mn>2</mn></mfrac><annotation encoding="TeX">\frac{\pi}{2}</annotation></semantics></math>, inclusive) of `x`. If `x` is less than -1 or greater than 1, returns {{jsxref("NaN")}}.

## Description

Because `asin()` is a static method of `Math`, you always use it as `Math.asin()`, rather than as a method of a `Math` object you created (`Math` is not a constructor).

## Examples

### Using Math.asin()

```js
Math.asin(-2); // NaN
Math.asin(-1); // -1.5707963267948966 (-Ο/2)
Math.asin(-0); // -0
Math.asin(0); // 0
Math.asin(0.5); // 0.5235987755982989 (Ο/6)
Math.asin(1); // 1.5707963267948966 (Ο/2)
Math.asin(2); // NaN
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- {{jsxref("Math.acos()")}}
- {{jsxref("Math.atan()")}}
- {{jsxref("Math.atan2()")}}
- {{jsxref("Math.cos()")}}
- {{jsxref("Math.sin()")}}
- {{jsxref("Math.tan()")}}
