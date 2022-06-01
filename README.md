<!--

@license Apache-2.0

Copyright (c) 2018 The Stdlib Authors.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

-->

# Mean

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> [Uniform][uniform-distribution] distribution [expected value][expected-value].

<!-- Section to include introductory text. Make sure to keep an empty line after the intro `section` element and another before the `/section` close. -->

<section class="intro">

The [expected value][expected-value] for a [uniform][uniform-distribution] random variable is

<!-- <equation class="equation" label="eq:uniform_expectation" align="center" raw="\mathbb{E}\left[ X \right] = 0.5 \cdot ( a + b )" alt="Expected value for a uniform distribution."> -->

<div class="equation" align="center" data-raw-text="\mathbb{E}\left[ X \right] = 0.5 \cdot ( a + b )" data-equation="eq:uniform_expectation">
    <img src="https://cdn.jsdelivr.net/gh/stdlib-js/stdlib@51534079fef45e990850102147e8945fb023d1d0/lib/node_modules/@stdlib/stats/base/dists/uniform/mean/docs/img/equation_uniform_expectation.svg" alt="Expected value for a uniform distribution.">
    <br>
</div>

<!-- </equation> -->

where `a` is the minimum support and `b` the maximum support of the distribution.

</section>

<!-- /.intro -->

<!-- Package usage documentation. -->



<section class="usage">

## Usage

```javascript
import mean from 'https://cdn.jsdelivr.net/gh/stdlib-js/stats-base-dists-uniform-mean@esm/index.mjs';
```

#### mean( a, b )

Returns the [expected value][expected-value] of a [uniform][uniform-distribution] distribution with parameters `a` (minimum support) and `b` (maximum support).

```javascript
var v = mean( 0.0, 1.0 );
// returns 0.5

v = mean( 4.0, 12.0 );
// returns 8.0

v = mean( 2.0, 8.0 );
// returns 5.0
```

If provided `NaN` as any argument, the function returns `NaN`.

```javascript
var v = mean( NaN, 2.0 );
// returns NaN

v = mean( 2.0, NaN );
// returns NaN
```

If provided `a >= b`, the function returns `NaN`.

```javascript
var y = mean( 3.0, 2.0 );
// returns NaN

y = mean( 3.0, 3.0 );
// returns NaN
```

</section>

<!-- /.usage -->

<!-- Package usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

</section>

<!-- /.notes -->

<!-- Package usage examples. -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script type="module">

import randu from 'https://cdn.jsdelivr.net/gh/stdlib-js/random-base-randu@esm/index.mjs';
import mean from 'https://cdn.jsdelivr.net/gh/stdlib-js/stats-base-dists-uniform-mean@esm/index.mjs';

var a;
var b;
var v;
var i;

for ( i = 0; i < 10; i++ ) {
    a = ( randu()*10.0 );
    b = ( randu()*10.0 ) + a;
    v = mean( a, b );
    console.log( 'a: %d, b: %d, E(X;a,b): %d', a.toFixed( 4 ), b.toFixed( 4 ), v.toFixed( 4 ) );
}

</script>
</body>
</html>
```

</section>

<!-- /.examples -->

<!-- Section to include cited references. If references are included, add a horizontal rule *before* the section. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="references">

</section>

<!-- /.references -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2022. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/stats-base-dists-uniform-mean.svg
[npm-url]: https://npmjs.org/package/@stdlib/stats-base-dists-uniform-mean

[test-image]: https://github.com/stdlib-js/stats-base-dists-uniform-mean/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/stats-base-dists-uniform-mean/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/stats-base-dists-uniform-mean/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/stats-base-dists-uniform-mean?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/stats-base-dists-uniform-mean.svg
[dependencies-url]: https://david-dm.org/stdlib-js/stats-base-dists-uniform-mean/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://gitter.im/stdlib-js/stdlib/

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/stats-base-dists-uniform-mean/tree/deno
[umd-url]: https://github.com/stdlib-js/stats-base-dists-uniform-mean/tree/umd
[esm-url]: https://github.com/stdlib-js/stats-base-dists-uniform-mean/tree/esm
[branches-url]: https://github.com/stdlib-js/stats-base-dists-uniform-mean/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/stats-base-dists-uniform-mean/main/LICENSE

[uniform-distribution]: https://en.wikipedia.org/wiki/Uniform_distribution_%28continuous%29

[expected-value]: https://en.wikipedia.org/wiki/Expected_value

</section>

<!-- /.links -->
