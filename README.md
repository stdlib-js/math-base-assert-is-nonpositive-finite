<!--

@license Apache-2.0

Copyright (c) 2022 The Stdlib Authors.

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


<details>
  <summary>
    About stdlib...
  </summary>
  <p>We believe in a future in which the web is a preferred environment for numerical computation. To help realize this future, we've built stdlib. stdlib is a standard library, with an emphasis on numerical and scientific computation, written in JavaScript (and C) for execution in browsers and in Node.js.</p>
  <p>The library is fully decomposable, being architected in such a way that you can swap out and mix and match APIs and functionality to cater to your exact preferences and use cases.</p>
  <p>When you use stdlib, you can be absolutely certain that you are using the most thorough, rigorous, well-written, studied, documented, tested, measured, and high-quality code out there.</p>
  <p>To join us in bringing numerical computing to the web, get started by checking us out on <a href="https://github.com/stdlib-js/stdlib">GitHub</a>, and please consider <a href="https://opencollective.com/stdlib">financially supporting stdlib</a>. We greatly appreciate your continued support!</p>
</details>

# isNonPositiveFinite

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Test if a numeric value is a nonpositive finite number.

<section class="installation">

## Installation

```bash
npm install @stdlib/math-base-assert-is-nonpositive-finite
```

Alternatively,

-   To load the package in a website via a `script` tag without installation and bundlers, use the [ES Module][es-module] available on the [`esm`][esm-url] branch (see [README][esm-readme]).
-   If you are using Deno, visit the [`deno`][deno-url] branch (see [README][deno-readme] for usage intructions).
-   For use in Observable, or in browser/node environments, use the [Universal Module Definition (UMD)][umd] build available on the [`umd`][umd-url] branch (see [README][umd-readme]).

The [branches.md][branches-url] file summarizes the available branches and displays a diagram illustrating their relationships.

To view installation and usage instructions specific to each branch build, be sure to explicitly navigate to the respective README files on each branch, as linked to above.

</section>

<section class="usage">

## Usage

```javascript
var isNonPositiveFinite = require( '@stdlib/math-base-assert-is-nonpositive-finite' );
```

#### isNonPositiveFinite( x )

Tests if a `numeric` value is a nonpositive finite number.

```javascript
var bool = isNonPositiveFinite( -3.14 );
// returns true

bool = isNonPositiveFinite( 2.0 );
// returns false
```

</section>

<!-- /.usage -->

<section class="notes">

</section>

<!-- /.notes -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```javascript
var isNonPositiveFinite = require( '@stdlib/math-base-assert-is-nonpositive-finite' );

var bool = isNonPositiveFinite( -3.14 );
// returns true

bool = isNonPositiveFinite( 0.0 );
// returns true

bool = isNonPositiveFinite( 2.0 );
// returns false

bool = isNonPositiveFinite( Infinity );
// returns false

bool = isNonPositiveFinite( NaN );
// returns false
```

</section>

<!-- /.examples -->

<!-- C interface documentation. -->

* * *

<section class="c">

## C APIs

<!-- Section to include introductory text. Make sure to keep an empty line after the intro `section` element and another before the `/section` close. -->

<section class="intro">

</section>

<!-- /.intro -->

<!-- C usage documentation. -->

<section class="usage">

### Usage

```c
#include "stdlib/math/base/assert/is_nonpositive_finite.h"
```

#### stdlib_base_is_nonpositive_finite( x )

Tests if a numeric value is a nonpositive finite number.

```c
#include <stdbool.h>

bool out = stdlib_base_is_nonpositive_finite( -3.14 );
// returns true

out = stdlib_base_is_nonpositive_finite( 2.0 );
// returns false
```

The function accepts the following arguments:

-   **x**: `[in] double` input value.

```c
bool stdlib_base_is_nonpositive_finite( const double x );
```

</section>

<!-- /.usage -->

<!-- C API usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

</section>

<!-- /.notes -->

<!-- C API usage examples. -->

<section class="examples">

### Examples

```c
#include "stdlib/math/base/assert/is_nonpositive_finite.h"
#include <stdbool.h>
#include <stdio.h>

int main( void ) {
    const double x[] = { 5.0, -5.0, 3.14, -3.14, 0.0, 0.0/0.0 };

    bool b;
    int i;
    for ( i = 0; i < 6; i++ ) {
        b = stdlib_base_is_nonpositive_finite( x[ i ] );
        printf( "Value: %lf. Is NonPositive Finite? %s.\n", x[ i ], ( b ) ? "True" : "False" );
    }
}
```

</section>

<!-- /.examples -->

</section>

<!-- /.c -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

* * *

## See Also

-   <span class="package-name">[`@stdlib/math-base/assert/is-negative-finite`][@stdlib/math/base/assert/is-negative-finite]</span><span class="delimiter">: </span><span class="description">test if a double-precision floating-point numeric value is a negative finite number.</span>
-   <span class="package-name">[`@stdlib/math-base/assert/is-positive-finite`][@stdlib/math/base/assert/is-positive-finite]</span><span class="delimiter">: </span><span class="description">test if a double-precision floating-point numeric value is a positive finite number.</span>
-   <span class="package-name">[`@stdlib/math-base/assert/is-nonnegative-finite`][@stdlib/math/base/assert/is-nonnegative-finite]</span><span class="delimiter">: </span><span class="description">test if a numeric value is a nonnegative finite number.</span>

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2025. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/math-base-assert-is-nonpositive-finite.svg
[npm-url]: https://npmjs.org/package/@stdlib/math-base-assert-is-nonpositive-finite

[test-image]: https://github.com/stdlib-js/math-base-assert-is-nonpositive-finite/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/math-base-assert-is-nonpositive-finite/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/math-base-assert-is-nonpositive-finite/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/math-base-assert-is-nonpositive-finite?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/math-base-assert-is-nonpositive-finite.svg
[dependencies-url]: https://david-dm.org/stdlib-js/math-base-assert-is-nonpositive-finite/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/math-base-assert-is-nonpositive-finite/tree/deno
[deno-readme]: https://github.com/stdlib-js/math-base-assert-is-nonpositive-finite/blob/deno/README.md
[umd-url]: https://github.com/stdlib-js/math-base-assert-is-nonpositive-finite/tree/umd
[umd-readme]: https://github.com/stdlib-js/math-base-assert-is-nonpositive-finite/blob/umd/README.md
[esm-url]: https://github.com/stdlib-js/math-base-assert-is-nonpositive-finite/tree/esm
[esm-readme]: https://github.com/stdlib-js/math-base-assert-is-nonpositive-finite/blob/esm/README.md
[branches-url]: https://github.com/stdlib-js/math-base-assert-is-nonpositive-finite/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/math-base-assert-is-nonpositive-finite/main/LICENSE

<!-- <related-links> -->

[@stdlib/math/base/assert/is-negative-finite]: https://github.com/stdlib-js/math-base-assert-is-negative-finite

[@stdlib/math/base/assert/is-positive-finite]: https://github.com/stdlib-js/math-base-assert-is-positive-finite

[@stdlib/math/base/assert/is-nonnegative-finite]: https://github.com/stdlib-js/math-base-assert-is-nonnegative-finite

<!-- </related-links> -->

</section>

<!-- /.links -->
