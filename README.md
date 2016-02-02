# [stringify-github-short-urls][author-www-url] [![npmjs.com][npmjs-img]][npmjs-url] [![The MIT License][license-img]][license-url] 

> Stringify array of `parse-github-short-url` objects to shorthand.

[![code climate][codeclimate-img]][codeclimate-url] [![standard code style][standard-img]][standard-url] [![travis build status][travis-img]][travis-url] [![coverage status][coveralls-img]][coveralls-url] [![dependency status][david-img]][david-url]


## Install
```
npm i stringify-github-short-urls --save
```


## Usage
> For more use-cases see the [tests](./test.js)

```js
const stringifyGithubShortUrls = require('stringify-github-short-urls')
```

### [stringifyGithubShortUrls](index.js#L49)
Stringify object or list of arguments to Github / npm shorthand.

**Params**

* `<owner>` **{Array|String|Object}**: user or org string, or object, array of objects    
* `[name]` **{String}**: repo name    
* `[branch]` **{String}**: branch name    
* `[npm]` **{String}**: pass `true` if you want to generate npm shorthand    
* `returns` **{String}**: generated shorthand  

**Example**

```js
const gh = require('stringify-github-short-urls')

// same as `stringify-github-short-url`
gh('jonschlinkert', 'micromatch')          // => ['jonschlinkert/micromatch']
gh('jonschlinkert', 'micromatch', 'dev')   // => ['jonschlinkert/micromatch#dev']
gh('gulpjs', 'gulp', 'v3.8.1', true)       // => ['gulpjs/gulp@v3.8.1']
gh({
  owner: 'tunnckoCore',
  name: 'parse-function'
}) // => ['tunnckoCore/parse-function']
gh({
  user: 'assemble',
  repo: 'assemble-core'
}) // => ['assemble/assemble-core']

// or accept arrays of objects that are passed to `stringify-github-short-url`
gh([
  {owner: 'assemble', name: 'assemble-core'},
  {owner: 'jonschlinkert', name: 'micromatch', branch: 'dev'}
]) // => ['assemble/assemble-core', 'jonschlinkert/micromatch#dev']
```


## Contributing
Pull requests and stars are always welcome. For bugs and feature requests, [please create an issue](https://github.com/tunnckoCore/stringify-github-short-urls/issues/new).  
But before doing anything, please read the [CONTRIBUTING.md](./CONTRIBUTING.md) guidelines.


## [Charlike Make Reagent](http://j.mp/1stW47C) [![new message to charlike][new-message-img]][new-message-url] [![freenode #charlike][freenode-img]][freenode-url]

[![tunnckocore.tk][author-www-img]][author-www-url] [![keybase tunnckocore][keybase-img]][keybase-url] [![tunnckoCore npm][author-npm-img]][author-npm-url] [![tunnckoCore twitter][author-twitter-img]][author-twitter-url] [![tunnckoCore github][author-github-img]][author-github-url]


[npmjs-url]: https://www.npmjs.com/package/stringify-github-short-urls
[npmjs-img]: https://img.shields.io/npm/v/stringify-github-short-urls.svg?label=stringify-github-short-urls

[license-url]: https://github.com/tunnckoCore/stringify-github-short-urls/blob/master/LICENSE
[license-img]: https://img.shields.io/badge/license-MIT-blue.svg


[codeclimate-url]: https://codeclimate.com/github/tunnckoCore/stringify-github-short-urls
[codeclimate-img]: https://img.shields.io/codeclimate/github/tunnckoCore/stringify-github-short-urls.svg

[travis-url]: https://travis-ci.org/tunnckoCore/stringify-github-short-urls
[travis-img]: https://img.shields.io/travis/tunnckoCore/stringify-github-short-urls.svg

[coveralls-url]: https://coveralls.io/r/tunnckoCore/stringify-github-short-urls
[coveralls-img]: https://img.shields.io/coveralls/tunnckoCore/stringify-github-short-urls.svg

[david-url]: https://david-dm.org/tunnckoCore/stringify-github-short-urls
[david-img]: https://img.shields.io/david/tunnckoCore/stringify-github-short-urls.svg

[standard-url]: https://github.com/feross/standard
[standard-img]: https://img.shields.io/badge/code%20style-standard-brightgreen.svg


[author-www-url]: http://www.tunnckocore.tk
[author-www-img]: https://img.shields.io/badge/www-tunnckocore.tk-fe7d37.svg

[keybase-url]: https://keybase.io/tunnckocore
[keybase-img]: https://img.shields.io/badge/keybase-tunnckocore-8a7967.svg

[author-npm-url]: https://www.npmjs.com/~tunnckocore
[author-npm-img]: https://img.shields.io/badge/npm-~tunnckocore-cb3837.svg

[author-twitter-url]: https://twitter.com/tunnckoCore
[author-twitter-img]: https://img.shields.io/badge/twitter-@tunnckoCore-55acee.svg

[author-github-url]: https://github.com/tunnckoCore
[author-github-img]: https://img.shields.io/badge/github-@tunnckoCore-4183c4.svg

[freenode-url]: http://webchat.freenode.net/?channels=charlike
[freenode-img]: https://img.shields.io/badge/freenode-%23charlike-5654a4.svg

[new-message-url]: https://github.com/tunnckoCore/ama
[new-message-img]: https://img.shields.io/badge/ask%20me-anything-green.svg