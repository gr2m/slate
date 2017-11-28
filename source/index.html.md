---
title: Octokit

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  - javascript

toc_footers:
  - <a href='https://github.com/lord/slate'>Documentation Powered by Slate</a>

includes:
  - repositories

search: true
---

# Octokit

Welcome to Octokit – home of the official libraries to build amazing experiences using the [GitHub API](https://developer.github.com/)

Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

# Initialization

All Octokit libraries work against all GitHub versions: [GitHub.com](https://github.com), [GitHub Enterprise](https://enterprise.github.com) and [GitHub Business](https://github.com/business).

Depending on which version you want to work against, you have to set different options

<!-- table generated with https://www.tablesgenerator.com/markdown_tables -->
| Parameter  | Type   | Default            | Description                  |
|------------|--------|--------------------|------------------------------|
| host       | String | `'api.github.com'` | Hostname or IP of GitHub API |
| pathPrefix | String | `''`               |                              |
| protocol   | String | `'https:'`         |                              |
| port       | Number | `443`              |                              |

```javascript
// node: const Octokit = require('octokit')
// browser: <script src="https://cdn.github.com/octokit/javascript/octokit-1.2.3.js"></script>
const github = new Octokit({
    // optional
  timeout: 5000,
  host: 'github.my-GHE-enabled-company.com', // should be api.github.com for GitHub
  pathPrefix: '/api/v3', // for some GHEs; none for GitHub
  protocol: 'https',
  port: 9898,
  proxy: '<proxyUrl>',
  ca: 'whatever',
  headers: {
    'accept': 'application/vnd.github.something-custom',
    'cookie': 'something custom',
    'user-agent': 'something custom'
  },
  requestMedia: 'application/vnd.github.something-custom',
  rejectUnauthorized: false, // default: true
  family: 6
})
```

These arguments are shared across all Octokit libraries. Other options depend on the language you are using.

# Authentication

There are three ways to authenticate through GitHub API v3. Requests that require authentication will return `404 Not Found`, instead of `403 Forbidden`, in some places. This is to prevent the accidental leakage of private repositories to unauthorized users.

## Basic Authentication

```shell
$ curl https://api.github.com/user \
    -u "octocat:secret"
```

```javascript
octokit.authenticate({
  type: 'basic',
  username: 'octocat',
  password: 'secret'
})

octokit.users.get()
```

Authenticate using username and password.

## OAuth2 Token

```shell
# send as haeder
$ curl https://api.github.com \
    -H "Authorization: token 0000000000000000000000000000000000000001"
# send as a parameter
$ curl https://api.github.com/user?access_token=OAUTH-TOKEN
```

```javascript
octokit.authenticate({
  type: 'token',
  token: '0000000000000000000000000000000000000001'
})

octokit.users.get()
```

Read [more about OAuth2](https://developer.github.com/apps/building-integrations/setting-up-and-registering-oauth-apps/). Note that OAuth2 tokens can be [acquired programmatically](https://developer.github.com/v3/oauth_authorizations/#create-a-new-authorization), for applications that are not websites.

## OAuth2 Key/Secret

```shell
$ curl 'https://api.github.com/users/whatever?client_id=xxxx&client_secret=yyyy'
```

This should only be used in server to server scenarios. Don't leak your OAuth application's client secret to your users.

Read [more about unauthenticated rate limiting](https://developer.github.com/v3/#increasing-the-unauthenticated-rate-limit-for-oauth-applications).

## Failed login limit

Authenticating with invalid credentials will return an `Unauthorized Error`

| Property          | Value                               |
|-------------------|-------------------------------------|
| name              | `'Unauthorized'`                    |
| code              | `401`                               |
| message           | `'Bad credentials'`                 |
| documentation_url | `'https://developer.github.com/v3'` |

After detecting several requests with invalid credentials within a short period, the API will temporarily reject all authentication attempts for that user (including ones with valid credentials) with a `Forbidden Error`:

| Property          | Value                               |
|-------------------|-------------------------------------|
| name              | `'Forbidden'`                       |
| code              | `404`                               |
| message           | `'Maximum number of login attempts exceeded. Please try again later.'` |
| documentation_url | `'https://developer.github.com/v3'` |


# v3 Rest API

[https://developer.github.com/v3/](https://developer.github.com/v3/)

Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
