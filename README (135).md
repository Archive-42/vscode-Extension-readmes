# Npm Intellisense

Visual Studio Code plugin that autocompletes npm modules in import statements.

![auto complete](https://github.com/ChristianKohler/NpmIntellisense/raw/master/images/auto_complete.gif)

## Sponsors

<p><a title="Try CodeStream" href="https://sponsorlink.codestream.com/?utm_source=vscmarket&amp;utm_campaign=npmintel&amp;utm_medium=banner"><img src="https://alt-images.codestream.com/codestream_logo_npmintel.png"></a></br>
Eliminate context switching and costly distractions. Create and merge PRs and perform code reviews from inside your IDE while using jump-to-definition, your favorite keybindings, and other IDE tools.<br> <a title="Try CodeStream" href="https://sponsorlink.codestream.com/?utm_source=vscmarket&amp;utm_campaign=npmintel&amp;utm_medium=banner">Learn more</a></p>

## Installation

In the command palette (cmd-shift-p) select Install Extension and choose npm Intellisense.

![install](https://github.com/ChristianKohler/NpmIntellisense/raw/master/images/npm_install.gif)

## Contributing

Something missing? Found a bug? - Create a pull request or an issue.
[Github](https://github.com/ChristianKohler/NpmIntellisense)

## Features

### Import command

![import command](https://github.com/ChristianKohler/NpmIntellisense/raw/master/images/importcommand.gif)

```javascript
{
	"npm-intellisense.importES6": true,
	"npm-intellisense.importQuotes": "'",
	"npm-intellisense.importLinebreak": ";\r\n",
	"npm-intellisense.importDeclarationType": "const",
}
```

### Import command (ES5)

![import command](https://github.com/ChristianKohler/NpmIntellisense/raw/master/images/require_withname.gif)

```javascript
{
	"npm-intellisense.importES6": false,
	"npm-intellisense.importQuotes": "'",
	"npm-intellisense.importLinebreak": ";\r\n",
	"npm-intellisense.importDeclarationType": "const",
}
```

### Scan devDependencies

Npm intellisense scans only dependencies by default. Set scanDevDependencies to true to enable it for devDependencies too.

```javascript
{
	"npm-intellisense.scanDevDependencies": true,
}
```

### Show build in (local) libs

Shows build in node modules like 'path' of 'fs'

```javascript
{
	"npm-intellisense.showBuildInLibs": true,
}
```

### Lookup package.json recursive

Look for package.json inside nearest directory instead of workspace root. It's enabled by default.

```javascript
{
	"npm-intellisense.recursivePackageJsonLookup": true,
}
```

### Experimental: Package Subfolder Intellisense

Open subfolders of a module.
This feature is work in progress and experimental.

```javascript
{
	"npm-intellisense.packageSubfoldersIntellisense": false,
}
```

## License

This software is released under [MIT License](http://www.opensource.org/licenses/mit-license.php)
