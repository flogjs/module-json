# module.json

Format description of `module.json` for the Flog JavaScript runtime.

*This repository does not contain any code. If you're looking for code, check
out [Flog core][core] or the [Flog standard library][std] repositories.*

### `author`

Author name and email in the format `name <email>`. The email used here must
correspond to the actual email used for publishing the module.

### `bin`

Relative path to the file executed when `flgx <module>` or `flog with <module>`
is used.

### `bugs`

Alias for `issues`.

### `depends`

Map of dependencies of this module and their versions.

### `dependencies`

Alias for `depends`.

### `description`

Module description.

### `exposes`

Map of filesystem paths exposed to this module and their permissions (any
combination of `r`, `w` and `x`).

### `issues`

Link to an issue tracker for this module.

### `license`

License.

### `loaders`

Map of custom extensions loaders (any file extension that is not `js`, `json`
or `so`).

### `name`

Name, composed of `namespace/modulename`. If namespace is missing, it is
assumed to be the same as `modulename`.

This field may only contain lowercase characters, hyphens and a forward slash.
If it contains a forward slash, it must be prefixed (the namespace part) and
suffixed (the module name part) by at least two characters.

This field is *not* compatible with the corresponding field in package.json;
for example, the character `@` is not allowed.

### `repository`

Link to a repository for this module.

### `version`

Version, containing either only a major version (`1`), a major and minor
(`1.2`) or a major, minor and patch (`1.2.3`).

This field is *not* compatible with the corresponding field in package.json.
For example, the character `^` or `~` is not allowed.

[core]: https://github.com/flogjs/flog
[std]: https://github.com/flogjs/std
