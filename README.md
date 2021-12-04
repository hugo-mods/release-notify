<!-- <a href=""><img alt="Logo" align="right" width="200" src="https://raw.githubusercontent.com/hugo-mods/icons/main/.github/logo.png"></a> -->

# hugo-mods: release-notify

> :warning: Work in progress! Use at own risk.

Notifies the user whenever a new module release is available.

## Use cases
- Notify user whenever a new major/minor/bugfix update is available (configurable)
- Parse and compare semantic versions
- Fetch and display release information

Preconditions:
- Use [Hugo module system](https://gohugo.io/hugo-modules/)
- Release via [GitHub releases](https://docs.github.com/en/repositories/releasing-projects-on-github/managing-releases-in-a-repository) and use [semantic versioning](https://go.dev/doc/modules/version-numbers)
- The go.mod dependencies must come directly from github.com

How does it work? 
In short: Parses `go.mod` file, fetches releases via GitHub API and compares local vs. upstream version.
Yes, this is all possible by using Hugo natively.


## Go get it <a href="quickstart"></a>

Initialize [Hugo's mod system](https://gohugo.io/hugo-modules/) on your site:

`hugo mod init github.com/<username>/<your-repo>`

Add module to site's config (e.g. `config.yaml`):

```yaml
module:
  imports:
  - path: github.com/hugo-mods/release-notify
```

## Configuration <a href="configuration"></a>

Take a look at the `exampleSite` for now.
