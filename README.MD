#Content handler plugin for punch site generation tool
*This plugin is no longer meant to be generic. It is used in a special project and does very individual things.*
This plugin allows you to put file folders into your content directory, in order for those files to be deployed
to your output directory.

Install via

	npm install punch-files-handler

In order to use this, you must add these things to your punch config:

	"files_dir": ["images", "videos"],
	
	"plugins": {
		"content_handler":  "punch-files-handler"
	}

`files_dir` is an array, that contains folder names, which you define as folders that contain files,
which should be copied into the resulting output directory. These folders can also be subfolders somewhere in your
content directory hierarchy. So "images" will be found in "\images" as well as in "\somesection\subsection\images".
So please only provide simple folder names in the files_dir array, not paths.

*Note: Everything within such folders will be simply copied into the output directory and NOT be processed any further
by punch*

Also note, that this content handler plugin is used INSTEAD the original content handler, if you include it as the
`content_handler` plugin.

This plugin is based on the original content handler of punch (version 0.5.44) and I added the file folder functionality.