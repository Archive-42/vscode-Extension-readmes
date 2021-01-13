# vscode-journal README

Lightweight Extension for Visual Studio Code to take track of your daily notes.  

## What's this about?
This extension is only useful for people like me, who use simple text files for notes, task lists, and everything else which has to be remembered and searched for. Textfiles are easy to backup, sync and can be opened anywhere by everything. This extension has the following functions: 


## Features



## Settings

You have to set the base folder for notes folder structure before you start. Open your settings, search for 'journal' and copy the journal.base line into your personal settings. Adjust the value, for example: ` "journal.base": "C:/Users/FooBar/Documents/Journal"` (use forward slash!)

The default file format is Markdown (using `md` as extension), which is natively supported by Visual Studio Code. I use Asciidoc for my notes (with `.adoc` as extension), in this case you should also install an Asciidoc Syntax extension. 

Syntax highlighting is configured in your workspace settings. The options are stored automatically in the settings, you can then manually change them. Make sure to restart to apply the changes. The settings try to recognize if a dark or light theme is used. If you switch in between, you either have to delete the settings (to reload them from the extension) or adapt them for yourself. 


## Demo

![Screen Capture](https://github.com/pajoma/vscode-journal/raw/master/./docs/intro.gif)

The demo shows also the use of the [vscode-journal-view](https://marketplace.visualstudio.com/items?itemName=Gruntfuggly.vscode-journal-view) extension for browsing  for vscode-journal by [Gruntfuggly](https://github.com/Gruntfuggly/vscode-journal-view) 
