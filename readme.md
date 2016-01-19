MyBB template editor
=================================
Edit MyBB templates using your favourite text editor.

This script saves all templates from template group to files and watching changes.

## Installation:
1. Download .zip
2. Unpack and call in your folder
```shell
npm install
```

## Configuration:
1. Edit config/app.json and fill your data

#### Configuration options:
```shell
{
	"database": {
		"prefix": "mybb_" 		// MyBB table prefix
	},
	"mysql": { 					// Database configuration
		"host": "localhost",
		"username": "root",
		"password": "secret",
		"database": "mybb"
	},
	"theme": {
		"id": 2					// Template group id
	},
	"app": {
		"datadir": "templates",	// Dirname with templates
		"fileext": ".html"		// Extension for files
	}
}
```

## Usage:

1. Save templates to files ``` node index.js init ```
2. Watch changes ``` node index.js watch ```

#### Available commands:
```shell
Usage: index [options] [command]


  Commands:

    init         create template repository
    write-file   overwrite all files by templates from database
    write-db     overwrite all database templates by templates from files
    watch        watch templates
    clear        delete all file templates

  Options:

    -h, --help     output usage information
    -V, --version  output the version numbers
```
