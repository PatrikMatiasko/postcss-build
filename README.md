#PostCSS build
A postcss cli build tool. Useful if you use npm as a build tool. As opposed to [postcss-cli](https://github.com/postcss/postcss-cli), PostCSS build can scan an entire directory and subdirectory for files.

## Usage
```
$ npm install -g postcss-build --save-dev

$ postcssbuild --src main.css --output main.min.css --plugins [ "autoprefixer", "cssnano" ]
```


### CLI options
-c or --config  
configuration file  

-d or --dir  
Source directory  

-h or --help  
Displays help text  

-s or --src  
Path to source file  

-t or --options  
Plugin options  

-o or --output  
Path to output file  

-p or --plugins  
Array of postcss plugins names

-n or --notify
Show system notifications


### Config
Instead of passing arguments via the cli they can be placed inside a JSON config file.

CLI arguments overrule config.

Example
```
{
  "dir": "src/styles/",

  "output" : dist/styles/main.css,

	"plugins": [ "autoprefixer", "cssnano" ],

	"options": {
		"autoprefixer": {
			"browsers": ["> 1%", "IE 7"],
			"cascade": false
		},

		"cssnano": { "safe": true }
	}
}
```

## TODO
- Tests

## Credits
[postcss]('https://github.com/postcss/postcss')

##License
MIT
