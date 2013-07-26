## Changelog

### 0.9.11
 * Fix undefined 'path' variable when forge returns an error
 * Reduce the number of API calls to the Forge
 * Forge versions were processed in the wrong order
 * Reduce calls to the Forge API
 * Don't sort versions as strings. Rely on the forge returning them ordered
 * When a git transitive dependency has no version the version is set to nil and fails later
 * Read deps from Puppetfiles in git repos
 * Pass --module_repository to `puppet module install` to install from other forges
 * Fail on conflict instead of error
 * Cache forge responses and print an error if returns an invalid response
 * Add a User-Agent header to all requests to the GitHub API
 * Convert puppet version requirements to rubygems, pessimistic and ranges
 * Use librarian gem
 * Ignore invalid versions in git repos, ie. 0.5.0-rc1

### 0.9.10

 * Catch GitHub API rate limit exceeded
 * Make Librarian::Manifest Semver 2.0.0 compatible

### 0.9.1
 * Proper error message when a module that is sourced from the forge does not
   exist.
 * Added support for annotated tags as git references.
 * `librarian-puppet init` adds `.tmp/` to gitignore instead of `tmp/`.
 * Fixed syntax error in the template Puppetfile created by `librarian-puppet
   init`.
 * Checks for `lib/puppet` as well as `manifests/` when checking if the git
   repository is a valid module.
 * When a user specifies `<foo>/<bar>` as the name of a module sources from a
   git repository, assume the module name is actually `<bar>`.
 * Fixed gem description and summary in gemspec.

### 0.9.0
 * Initial release
