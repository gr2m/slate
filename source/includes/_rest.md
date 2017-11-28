# REST

[https://developer.github.com/v3/](https://developer.github.com/v3/)

Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

## Repositories

### List your repositories

```shell
$ curl -XGET https://api.github.com/user/repos \
    -H "Authorization: token 0000000000000000000000000000000000000001" \
    -d visibility=all \
    -d affiliation="owner,collaborator,organization_member" \
    -d type=all \
    -d sort=full_name \
    -d direction=asc
```

```javascript
const {data} = await octokit.repos.getAll({
  visibility: 'all',
  affiliation: 'owner,collaborator,organization_member',
  type: 'all',
  sort: 'full_name'
  direction: 'asc'
})
```

> Example Response

```json
[
  {
    "id": 1296269,
    "owner": {
      "login": "octocat",
      "id": 1,
      "avatar_url": "https://github.com/images/error/octocat_happy.gif",
      "gravatar_id": "",
      "url": "https://api.github.com/users/octocat",
      "html_url": "https://github.com/octocat",
      "followers_url": "https://api.github.com/users/octocat/followers",
      "following_url": "https://api.github.com/users/octocat/following{/other_user}",
      "gists_url": "https://api.github.com/users/octocat/gists{/gist_id}",
      "starred_url": "https://api.github.com/users/octocat/starred{/owner}{/repo}",
      "subscriptions_url": "https://api.github.com/users/octocat/subscriptions",
      "organizations_url": "https://api.github.com/users/octocat/orgs",
      "repos_url": "https://api.github.com/users/octocat/repos",
      "events_url": "https://api.github.com/users/octocat/events{/privacy}",
      "received_events_url": "https://api.github.com/users/octocat/received_events",
      "type": "User",
      "site_admin": false
    },
    "name": "Hello-World",
    "full_name": "octocat/Hello-World",
    "description": "This your first repo!",
    "private": false,
    "fork": false,
    "url": "https://api.github.com/repos/octocat/Hello-World",
    "html_url": "https://github.com/octocat/Hello-World",
    "archive_url": "http://api.github.com/repos/octocat/Hello-World/{archive_format}{/ref}",
    "assignees_url": "http://api.github.com/repos/octocat/Hello-World/assignees{/user}",
    "blobs_url": "http://api.github.com/repos/octocat/Hello-World/git/blobs{/sha}",
    "branches_url": "http://api.github.com/repos/octocat/Hello-World/branches{/branch}",
    "clone_url": "https://github.com/octocat/Hello-World.git",
    "collaborators_url": "http://api.github.com/repos/octocat/Hello-World/collaborators{/collaborator}",
    "comments_url": "http://api.github.com/repos/octocat/Hello-World/comments{/number}",
    "commits_url": "http://api.github.com/repos/octocat/Hello-World/commits{/sha}",
    "compare_url": "http://api.github.com/repos/octocat/Hello-World/compare/{base}...{head}",
    "contents_url": "http://api.github.com/repos/octocat/Hello-World/contents/{+path}",
    "contributors_url": "http://api.github.com/repos/octocat/Hello-World/contributors",
    "deployments_url": "http://api.github.com/repos/octocat/Hello-World/deployments",
    "downloads_url": "http://api.github.com/repos/octocat/Hello-World/downloads",
    "events_url": "http://api.github.com/repos/octocat/Hello-World/events",
    "forks_url": "http://api.github.com/repos/octocat/Hello-World/forks",
    "git_commits_url": "http://api.github.com/repos/octocat/Hello-World/git/commits{/sha}",
    "git_refs_url": "http://api.github.com/repos/octocat/Hello-World/git/refs{/sha}",
    "git_tags_url": "http://api.github.com/repos/octocat/Hello-World/git/tags{/sha}",
    "git_url": "git:github.com/octocat/Hello-World.git",
    "hooks_url": "http://api.github.com/repos/octocat/Hello-World/hooks",
    "issue_comment_url": "http://api.github.com/repos/octocat/Hello-World/issues/comments{/number}",
    "issue_events_url": "http://api.github.com/repos/octocat/Hello-World/issues/events{/number}",
    "issues_url": "http://api.github.com/repos/octocat/Hello-World/issues{/number}",
    "keys_url": "http://api.github.com/repos/octocat/Hello-World/keys{/key_id}",
    "labels_url": "http://api.github.com/repos/octocat/Hello-World/labels{/name}",
    "languages_url": "http://api.github.com/repos/octocat/Hello-World/languages",
    "merges_url": "http://api.github.com/repos/octocat/Hello-World/merges",
    "milestones_url": "http://api.github.com/repos/octocat/Hello-World/milestones{/number}",
    "mirror_url": "git:git.example.com/octocat/Hello-World",
    "notifications_url": "http://api.github.com/repos/octocat/Hello-World/notifications{?since, all, participating}",
    "pulls_url": "http://api.github.com/repos/octocat/Hello-World/pulls{/number}",
    "releases_url": "http://api.github.com/repos/octocat/Hello-World/releases{/id}",
    "ssh_url": "git@github.com:octocat/Hello-World.git",
    "stargazers_url": "http://api.github.com/repos/octocat/Hello-World/stargazers",
    "statuses_url": "http://api.github.com/repos/octocat/Hello-World/statuses/{sha}",
    "subscribers_url": "http://api.github.com/repos/octocat/Hello-World/subscribers",
    "subscription_url": "http://api.github.com/repos/octocat/Hello-World/subscription",
    "svn_url": "https://svn.github.com/octocat/Hello-World",
    "tags_url": "http://api.github.com/repos/octocat/Hello-World/tags",
    "teams_url": "http://api.github.com/repos/octocat/Hello-World/teams",
    "trees_url": "http://api.github.com/repos/octocat/Hello-World/git/trees{/sha}",
    "homepage": "https://github.com",
    "language": null,
    "forks_count": 9,
    "stargazers_count": 80,
    "watchers_count": 80,
    "size": 108,
    "default_branch": "master",
    "open_issues_count": 0,
    "topics": [
      "octocat",
      "atom",
      "electron",
      "API"
    ],
    "has_issues": true,
    "has_wiki": true,
    "has_pages": false,
    "has_downloads": true,
    "archived": false,
    "pushed_at": "2011-01-26T19:06:43Z",
    "created_at": "2011-01-26T19:01:12Z",
    "updated_at": "2011-01-26T19:14:43Z",
    "permissions": {
      "admin": false,
      "push": false,
      "pull": true
    },
    "allow_rebase_merge": true,
    "allow_squash_merge": true,
    "allow_merge_commit": true,
    "subscribers_count": 42,
    "network_count": 0
  }
]
```

List repositories that are accessible to the authenticated user.

This includes repositories owned by the authenticated user, repositories where the authenticated user is a collaborator, and repositories that the authenticated user has access to through an organization membership.

<aside class="notice">
  <p><strong>Note:</strong> The <code>topics</code> property for repositories on GitHub is currently available for developers to preview. To view the <code>topics</code> property in calls that return repository results, you must enable the <a href="#"><code>mercy</code> preview</a>.
</aside>

#### Parameters

<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Type</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>visibility</code></td>
      <td><code>string</code></td>
      <td>Can be one of <code>all</code>, <code>public</code>, or <code>private</code>. Default: <code>all</code></td>
    </tr>
    <tr>
      <td><code>affiliation</code></td>
      <td><code>string</code></td>
      <td>Comma-separated list of values. Can include:<br>* <code>owner</code>: Repositories that are owned by the authenticated user.<br>* <code>collaborator</code>: Repositories that the user has been added to as a collaborator.<br>* <code>organization_member</code>: Repositories that the user has access to through being a member of an organization. This includes every repository on every team that the user is on.<br><br>Default: <code>owner,collaborator,organization_member</code></td>
    </tr>
    <tr>
      <td><code>type</code></td>
      <td><code>string</code></td>
      <td>Can be one of <code>all</code>, <code>owner</code>, <code>public</code>, <code>private</code>, <code>member</code>. Default: <code>all</code><br><br>Will cause a <code>422</code> error if used in the same request as <strong>visibility</strong> or <strong>affiliation</strong>.</td>
    </tr>
    <tr>
      <td><code>sort</code></td>
      <td><code>string</code></td>
      <td>Can be one of <code>created</code>, <code>updated</code>, <code>pushed</code>, <code>full_name</code>. Default: <code>full_name</code></td>
    </tr>
    <tr>
      <td><code>direction</code></td>
      <td><code>string</code></td>
      <td>Can be one of <code>asc</code> or <code>desc</code>. Default: when using <code>full_name</code>: <code>asc</code>; otherwise <code>desc</code></td>
    </tr>
  </tbody>
</table>

### Create on your account

```shell
$ curl -XPOST https://api.github.com/user/repos \
    -H "Authorization: token 0000000000000000000000000000000000000001" \
    # optional \
    -d name="Hello-World" \
    -d description="My first repo created with Octokit" \
    -d homepage="https://github.com"
```

```javascript
const {data} = await octokit.repos.create({
  name: 'Hello-World',
  // optional
  description: 'My first repo created with Octokit',
  homepage: 'https://github.com'
})
```

> Example response

```json
{
  "id": 1296269,
  "owner": {
    "login": "octocat",
    "id": 1,
    "avatar_url": "https://github.com/images/error/octocat_happy.gif",
    "gravatar_id": "",
    "url": "https://api.github.com/users/octocat",
    "html_url": "https://github.com/octocat",
    "followers_url": "https://api.github.com/users/octocat/followers",
    "following_url": "https://api.github.com/users/octocat/following{/other_user}",
    "gists_url": "https://api.github.com/users/octocat/gists{/gist_id}",
    "starred_url": "https://api.github.com/users/octocat/starred{/owner}{/repo}",
    "subscriptions_url": "https://api.github.com/users/octocat/subscriptions",
    "organizations_url": "https://api.github.com/users/octocat/orgs",
    "repos_url": "https://api.github.com/users/octocat/repos",
    "events_url": "https://api.github.com/users/octocat/events{/privacy}",
    "received_events_url": "https://api.github.com/users/octocat/received_events",
    "type": "User",
    "site_admin": false
  },
  "name": "Hello-World",
  "full_name": "octocat/Hello-World",
  "description": "This your first repo!",
  "private": false,
  "fork": false,
  "url": "https://api.github.com/repos/octocat/Hello-World",
  "html_url": "https://github.com/octocat/Hello-World",
  "archive_url": "http://api.github.com/repos/octocat/Hello-World/{archive_format}{/ref}",
  "assignees_url": "http://api.github.com/repos/octocat/Hello-World/assignees{/user}",
  "blobs_url": "http://api.github.com/repos/octocat/Hello-World/git/blobs{/sha}",
  "branches_url": "http://api.github.com/repos/octocat/Hello-World/branches{/branch}",
  "clone_url": "https://github.com/octocat/Hello-World.git",
  "collaborators_url": "http://api.github.com/repos/octocat/Hello-World/collaborators{/collaborator}",
  "comments_url": "http://api.github.com/repos/octocat/Hello-World/comments{/number}",
  "commits_url": "http://api.github.com/repos/octocat/Hello-World/commits{/sha}",
  "compare_url": "http://api.github.com/repos/octocat/Hello-World/compare/{base}...{head}",
  "contents_url": "http://api.github.com/repos/octocat/Hello-World/contents/{+path}",
  "contributors_url": "http://api.github.com/repos/octocat/Hello-World/contributors",
  "deployments_url": "http://api.github.com/repos/octocat/Hello-World/deployments",
  "downloads_url": "http://api.github.com/repos/octocat/Hello-World/downloads",
  "events_url": "http://api.github.com/repos/octocat/Hello-World/events",
  "forks_url": "http://api.github.com/repos/octocat/Hello-World/forks",
  "git_commits_url": "http://api.github.com/repos/octocat/Hello-World/git/commits{/sha}",
  "git_refs_url": "http://api.github.com/repos/octocat/Hello-World/git/refs{/sha}",
  "git_tags_url": "http://api.github.com/repos/octocat/Hello-World/git/tags{/sha}",
  "git_url": "git:github.com/octocat/Hello-World.git",
  "hooks_url": "http://api.github.com/repos/octocat/Hello-World/hooks",
  "issue_comment_url": "http://api.github.com/repos/octocat/Hello-World/issues/comments{/number}",
  "issue_events_url": "http://api.github.com/repos/octocat/Hello-World/issues/events{/number}",
  "issues_url": "http://api.github.com/repos/octocat/Hello-World/issues{/number}",
  "keys_url": "http://api.github.com/repos/octocat/Hello-World/keys{/key_id}",
  "labels_url": "http://api.github.com/repos/octocat/Hello-World/labels{/name}",
  "languages_url": "http://api.github.com/repos/octocat/Hello-World/languages",
  "merges_url": "http://api.github.com/repos/octocat/Hello-World/merges",
  "milestones_url": "http://api.github.com/repos/octocat/Hello-World/milestones{/number}",
  "mirror_url": "git:git.example.com/octocat/Hello-World",
  "notifications_url": "http://api.github.com/repos/octocat/Hello-World/notifications{?since, all, participating}",
  "pulls_url": "http://api.github.com/repos/octocat/Hello-World/pulls{/number}",
  "releases_url": "http://api.github.com/repos/octocat/Hello-World/releases{/id}",
  "ssh_url": "git@github.com:octocat/Hello-World.git",
  "stargazers_url": "http://api.github.com/repos/octocat/Hello-World/stargazers",
  "statuses_url": "http://api.github.com/repos/octocat/Hello-World/statuses/{sha}",
  "subscribers_url": "http://api.github.com/repos/octocat/Hello-World/subscribers",
  "subscription_url": "http://api.github.com/repos/octocat/Hello-World/subscription",
  "svn_url": "https://svn.github.com/octocat/Hello-World",
  "tags_url": "http://api.github.com/repos/octocat/Hello-World/tags",
  "teams_url": "http://api.github.com/repos/octocat/Hello-World/teams",
  "trees_url": "http://api.github.com/repos/octocat/Hello-World/git/trees{/sha}",
  "homepage": "https://github.com",
  "language": null,
  "forks_count": 9,
  "stargazers_count": 80,
  "watchers_count": 80,
  "size": 108,
  "default_branch": "master",
  "open_issues_count": 0,
  "topics": [
    "octocat",
    "atom",
    "electron",
    "API"
  ],
  "has_issues": true,
  "has_wiki": true,
  "has_pages": false,
  "has_downloads": true,
  "archived": false,
  "pushed_at": "2011-01-26T19:06:43Z",
  "created_at": "2011-01-26T19:01:12Z",
  "updated_at": "2011-01-26T19:14:43Z",
  "permissions": {
    "admin": false,
    "push": false,
    "pull": true
  },
  "allow_rebase_merge": true,
  "allow_squash_merge": true,
  "allow_merge_commit": true,
  "subscribers_count": 42,
  "network_count": 0,
  "has_projects": true
}
```

Create a new repository for the authenticated user.

#### OAuth scope requirements

When using OAuth, authorizations must include:

- `public_repo` scope or `repo` scope to create a public repository
- `repo` scope to create a private repository

#### Parameters

<table>
    <thead>
        <tr>
            <th>Name</th>
            <th>Type</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><code>name</code></td>
            <td><code>string</code></td>
            <td>
                <strong>Required</strong>. The name of the repository.</td>
        </tr>
        <tr>
            <td><code>description</code></td>
            <td><code>string</code></td>
            <td>A short description of the repository.</td>
        </tr>
        <tr>
            <td><code>homepage</code></td>
            <td><code>string</code></td>
            <td>A URL with more information about the repository.</td>
        </tr>
        <tr>
            <td><code>private</code></td>
            <td><code>boolean</code></td>
            <td>Either <code>true</code> to create a private repository or <code>false</code> to create a public one. Creating private repositories requires a paid GitHub account. Default: <code>false</code>.</td>
        </tr>
        <tr>
            <td><code>has_issues</code></td>
            <td><code>boolean</code></td>
            <td>Either <code>true</code> to enable issues for this repository or <code>false</code> to disable them. Default: <code>true</code>.</td>
        </tr>
        <tr>
            <td><code>has_projects</code></td>
            <td><code>boolean</code></td>
            <td>Either <code>true</code> to enable projects for this repository or <code>false</code> to disable them. Default: <code>true</code>. <b>Note:</b> If you're creating a repository in an organization that has disabled repository projects, the default is <code>false</code>, and if you pass <code>true</code>, the API returns an error.</td>
        </tr>
        <tr>
            <td><code>has_wiki</code></td>
            <td><code>boolean</code></td>
            <td>Either <code>true</code> to enable the wiki for this repository or <code>false</code> to disable it. Default: <code>true</code>.</td>
        </tr>
        <tr>
            <td><code>team_id</code></td>
            <td><code>integer</code></td>
            <td>The id of the team that will be granted access to this repository. This is only valid when creating a repository in an organization.</td>
        </tr>
        <tr>
            <td><code>auto_init</code></td>
            <td><code>boolean</code></td>
            <td>Pass <code>true</code> to create an initial commit with empty README. Default: <code>false</code>.</td>
        </tr>
        <tr>
            <td><code>gitignore_template</code></td>
            <td><code>string</code></td>
            <td>Desired language or platform <a href="https://github.com/github/gitignore">.gitignore template</a> to apply. Use the name of the template without the extension. For example, "Haskell".</td>
        </tr>
        <tr>
            <td><code>license_template</code></td>
            <td><code>string</code></td>
            <td>Desired <a href="https://github.com/github/choosealicense.com">LICENSE template</a> to apply. Use the <a href="https://github.com/github/choosealicense.com/tree/gh-pages/_licenses">name of the template</a> without the extension. For example, "mit" or "mozilla".</td>
        </tr>
        <tr>
            <td><code>allow_squash_merge</code></td>
            <td><code>boolean</code></td>
            <td>Either <code>true</code> to allow squash-merging pull requests, or <code>false</code> to prevent squash-merging. Default: <code>true</code>
            </td>
        </tr>
        <tr>
            <td><code>allow_merge_commit</code></td>
            <td><code>boolean</code></td>
            <td>Either <code>true</code> to allow merging pull requests with a merge commit, or <code>false</code> to prevent merging pull requests with merge commits. Default: <code>true</code>
            </td>
        </tr>
        <tr>
            <td><code>allow_rebase_merge</code></td>
            <td><code>boolean</code></td>
            <td>Either <code>true</code> to allow rebase-merging pull requests, or <code>false</code> to prevent rebase-merging. Default: <code>true</code>
            </td>
        </tr>
    </tbody>
</table>
