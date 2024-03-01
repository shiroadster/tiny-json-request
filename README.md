> A tiny library for requesting and getting JSON resources.

## :cloud: Installation

```sh
# Using npm
npm install --save tiny-json-request

# Using yarn
yarn add jsonrequest
```
## :clipboard: Example

```js
// Dependencies
const request = require("jsonrequest");

request({
    url: "https://api.github.com/users/IonicaBizau",
    headers: {
        "User-Agent": "JsonRequest"
    }
}).then(data => {
    console.log(data);
    // => {
    //   "login": "IonicaBizau",
    //   "id": 2864371,
    //   "avatar_url": "https://avatars.githubusercontent.com/u/2864371?v=3",
    //   "gravatar_id": "",
    //   "url": "https://api.github.com/users/IonicaBizau",
    //   "html_url": "https://github.com/IonicaBizau",
    //   "followers_url": "https://api.github.com/users/IonicaBizau/followers",
    //   ...
    // }
}).catch(err => {
    console.error(err);
});

// Make a request to GitHub API
request("https://ionicabizau.net/api/articles", (err, data) => {
    console.log(err || data);
});
```

## :question: Get Help

There are few ways to get help:
 1. Please [post questions on Stack Overflow](https://stackoverflow.com/questions/ask). You can open issues with questions, as long you add a link to your Stack Overflow question.
 2. For bug reports and feature requests, open issues. :bug:
 3. For direct and quick help, you can [use Codementor](https://www.codementor.io/johnnyb). :rocket:

## :memo: Documentation

### `jsonRequest(options, data, callback)`
Creates the http(s) request and parses the response.

#### Params

- **String|Object** `options`: A string representing the request url or an object passed to the `tinyreq` function.
- **Object** `data`: The request data object.
- **Function** `callback`: The callback function.

#### Return
- **Object** The request object.

## :yum: How to contribute
Have an idea? Found a bug? See [how to contribute][contributing].

## :sparkling_heart: Support my projects
I open-source almost everything I can, and I try to reply to everyone needing help using these projects. Obviously,
this takes time. You can integrate and use these projects in your applications *for free*! You can even change the source code and redistribute (even resell it).

## :scroll: License