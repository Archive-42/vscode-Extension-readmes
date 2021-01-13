# gitignore extension for Visual Studio Code

A extension for Visual Studio Code that assists you in working with `.gitignore` files.


## Features

- Language support for `.gitignore` files
- Add local `.gitignore` by pulling file from the the [github/gitignore](https://github.com/github/gitignore) repository.


## Usage

Start command palette (with <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>P</kbd> or <kbd>F1</kbd>) and start typing `Add gitignore`


## Settings

```JavaScript
{
	// Number of seconds the list of `.gitignore` files retrieved from github will be cached
	"gitignore.cacheExpirationInterval": 3600
}
```


## Roadmap

### v0.1
- Basic implementation that allows to pull a single `.gitignore` file

### v0.2
- Add language support for `.gitignore` files

### v0.3
- Support reading `.gitignore` files from subdirectories in the github/gitignore repository

### v0.4
- Support adding multiple `.gitignore` files and merge it to a `.gitignore` file

### v0.5
- Support proxy

### v0.6
- Update extension to more recent vscode ecosystem
- Update dependencies

### v0.7
- Support multi-root workspaces (see contribution by @hangxingliu)

### v0.8
- Further improve proxy support

### v0.9
- Switch to async/await
- Migrate from `github` to `@octokit/rest`


## Changelog



## License

See LICENSE file


## Credits

Icon based on the Git logo by Jason Long

