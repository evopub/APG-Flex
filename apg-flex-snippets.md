 # APG-FLEX SNIPPETS FOR VISUAL STUDIO CODE
 
## Explanation and Demo

See: <http://gouillou.com/scripts/apg-flex-snippets.html>

## Installation

Copy the code below and Paste it in HTML language found in *User Snippets under File > Preferences* (*Code > Preferences* on macOS), (on macOS the file is at: *~/Library/Application Support/Code/User/snippets/html.json*). 

VSCode Help is at: <https://code.visualstudio.com/docs/editor/userdefinedsnippets>

## Code

```JSON
"Div Arow 2 Cols": {
	"prefix": "arow2",
	"body": [
		"&ltdiv class=\"arow\">\n\t&ltdiv class=\"acolfinal\">\n\t\tA\n\t&lt/div>\n\t&ltdiv class=\"acolfinal\">\n\t\tB\n\t&lt/div>\n&lt/div>\n"
	],
	"description": "arow 2 columns"
},
"Div Arow 4 Cols": {
	"prefix": "arow4",
	"body": [
		"<div class=\"arowmd\">\n\t<div class=\"\">\n\t\t<div class=\"arow\">\n\t\t\t<div class=\"acolfinal\">\n\t\t\t\tA\n\t\t\t</div>\n\t\t\t<div class=\"acolfinal\">\n\t\t\t\tB\n\t\t\t</div>\n\t\t</div>\n\t</div>\n\t<div class=\"\">\n\t\t<div class=\"arow\">\n\t\t\t<div class=\"acolfinal\">\n\t\t\t\tC\n\t\t\t</div>\n\t\t\t<div class=\"acolfinal\">\n\t\t\t\tD\n\t\t\t</div>\n\t\t</div>\n\t</div>\n</div>\n"	
	],
	"description": "arow 4 columns break at the middle"
},
"Div ArowMD 4 Cols": {
	"prefix": "arowmd4",
	"body": [
		"<div class=\"arow\">\n\t<div class=\"\">\n\t\t<div class=\"arowmd\">\n\t\t\t<div class=\"acolfinal\">\n\t\t\t\tA\n\t\t\t</div>\n\t\t\t<div class=\"acolfinal\">\n\t\t\t\tB\n\t\t\t</div>\n\t\t</div>\n\t</div>\n\t<div class=\"\">\n\t\t<div class=\"arowmd\">\n\t\t\t<div class=\"acolfinal\">\n\t\t\t\tC\n\t\t\t</div>\n\t\t\t<div class=\"acolfinal\">\n\t\t\t\tD\n\t\t\t</div>\n\t\t</div>\n\t</div>\n</div>\n"	
	],
	"description": "arowmd 4 columns break in each half"
}
```