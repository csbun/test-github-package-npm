# test-github-package-npm

this is a test npm package publish to [github package](https://help.github.com/en/articles/about-github-package-registry).

## ❓ How

- [Creating a personal access token for the command line](https://help.github.com/en/articles/creating-a-personal-access-token-for-the-command-line)
- Log in with npm using your username and personal access token

```sh
npm login --registry=https://npm.pkg.github.com/OWNER
> Username: USERNAME
> Password: TOKEN
> Email: PUBLIC EMAIL ADDRESS
```

- Configuring package.json

GitHub Package Registry only supports scoped NPM packages. Scoped packages have names with the format of `@owner/name` with lower case. And add an a publishConfig entry wiht `https://npm.pkg.github.com/`.

```json
{
  "name": "@csbun/test-github-package-npm",
  "publishConfig": {
    "registry": "https://npm.pkg.github.com/"
  },
}
```

- Publish

```sh
npm publish
```
