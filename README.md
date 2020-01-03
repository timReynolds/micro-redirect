_**Micro Redirect -**_

A redirect function for Zeit's [micro](https://github.com/zeit/micro)

[![Build Status](https://travis-ci.org/timReynolds/micro-redirect.svg?branch=master)](https://travis-ci.org/timreynolds/micro-redirect)
[![Maintainability](https://api.codeclimate.com/v1/badges/0d5e4eb0820d66791e2d/maintainability)](https://codeclimate.com/github/timReynolds/micro-redirect/maintainability)
[![Test Coverage](https://api.codeclimate.com/v1/badges/0d5e4eb0820d66791e2d/test_coverage)](https://codeclimate.com/github/timReynolds/micro-redirect/test_coverage)
[![XO code style](https://img.shields.io/badge/code_style-XO-5ed9c7.svg)](https://github.com/sindresorhus/xo)

## Usage

Firstly, install it:

```bash
npm install --save micro-redirect
```

Then import it like this:

```js
const redirect = require("micro-redirect");
```

And use it the same you'd use Zeit's send:

```js
module.exports = async (req, res) => {
  const statusCode = 302;
  const location = "http://github.com";

  redirect(res, statusCode, location);
};
```

#### API

**`redirect(res, statusCode, location)`**

- `statusCode` is a `Number` with the HTTP redirect code, and must always be supplied.
- `location` is a `String` used to set the res header location, and must always be supplied.
