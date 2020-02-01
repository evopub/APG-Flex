# APG-FLEX 

Only 662 Bytes to create a responsive Flex Layout: [check the Demo](http://gouillou.com/scripts/apg-flex-demo.html) and get the [snippets for VSCode](http://gouillou.com/scripts/apg-flex-snippets.html)! 

## Versions 

- v.1.1 (1 february 2020): Addition of `.acolfinal` (Total: 662 Bytes)  
- v.1.0 (2 november 2019): First public version (637 Bytes) 

## Code 

```css 

	/*APG-FLEX : v1.1 (2020-02-01) - ©Philippe Gouillou (www.gouillou.com) - LGPL 3*/ 

.acontainer 				{display: block; max-width: 1170px; margin: 0 auto !important;}  
.arow 						{display: flex; margin: 0; padding: 0;}  
.acolfinal					{padding:.5rem;} 

	@media(min-width: 576px)	{.arowsm{display: flex}}  
	@media(min-width: 768px)	{.arowmd{display: flex}}  
	@media(min-width: 992px)	{.arowlg{display: flex}}  
	@media(min-width: 1200px)	{.arowxl{display: flex}} 

.arow>div,  
.arowsm>div,  
.arowmd>div,  
.arowlg>div,  
.arowxl>div 				{flex:1} 

.flex2 						{flex:2 !important}  
.flex3 						{flex:3 !important}  
.flex4 						{flex:4 !important}  
.flex5 						{flex:5 !important}  
.flex6 						{flex:6 !important}  
.flex7 						{flex:7 !important}  
.flex8 						{flex:8 !important}  
.flex9 						{flex:9 !important}  
.flex10 					{flex:10 !important}  
.flex11 					{flex:11 !important}  
.flex12 					{flex:12 !important} 

``` 

### Minified Code (662 Bytes) 

```css  
.acontainer{display:block;max-width:1170px;margin:0 auto !important}.arow{display:flex;margin:0;padding:0}.acolfinal{padding:.5rem}@media(min-width:576px){.arowsm{display:flex}}@media(min-width:768px){.arowmd{display:flex}}@media(min-width:992px){.arowlg{display:flex}}@media(min-width:1200px){.arowxl{display:flex}}.arow>div,.arowsm>div,.arowmd>div,.arowlg>div,.arowxl>div{flex:1}.flex2{flex:2 !important}.flex3{flex:3 !important}.flex4{flex:4 !important}.flex5{flex:5 !important}.flex6{flex:6 !important}.flex7{flex:7 !important}.flex8{flex:8 !important}.flex9{flex:9 !important}.flex10{flex:10 !important}.flex11{flex:11 !important}.flex12{flex:12 !important}  
``` 

## Installation 

1. Just copy/paste the code above (regular or minified version) somewhere in your CSS file or download the regular (.css) or minified (.min.css) and link it in the header of your HTML file.  
2. Create your HTML according the following rules 

Rem: The names of the CSS classes have been choosen to allow a perfect compatibility with Bootstrap (you can mix both). 

## How to use 

**Beware: it works the opposite of Bootstrap: you modify the row, not the column!** 

1. For each row: indicate at which limit you want the columns to collapse. A row is created by a div with one of the followings classes (example : `<div class="arow">`) :  
	- `arow`: never collapses  
	- `arowsm`: collapses under 576px  
	- `arowmd`: collapses under 768px  
	- `arowlg`: collapses under 992px  
	- `arowxl`: collapses under 1200px  
2. Inside the row, add one `<div>` per column (as much as you want: they will be evenly distributed) 

3. If needed, add to the column div one of the classes `flex2` to `flex12` to define its respective size (default = `flex1`; example `<div class="flex2">`) 

### Notes 

1. For Container (*max\-width: 1070px and centered*), add the class "`acontainer`" to a row (ex: `<div class="arow acontainer">`) 

2. A `div` is considered as a Flex Column *if and only if* it is directly under a `arowXX`. You can change this behavior by using style (`<div style="display: block;">`):  
	- `arow` : row  
		- `div` : displayed as Flex (column)  
			- `div` : displayed as Block (default behavior)  
		- `div` : displayed as Flex (column)  
3. If you need to add a `div` 

4. For nesting, just remember that a column *must exist* in each row (*see example below*) 

5. Sizes are respective! (*see example below*) 

6. `flex2`...`flex12` are optionals: suppress or modify them as needed 

### Simple Example 

*See the [Demo](http://gouillou.com/scripts/apg-flex-demo.html)* 

4 columns, the second one twice the size of the others (so a total size of 5) and containing 4 nested columns: 

```html 

	<div class="arowsm">			<!-- Row collapsing at 576px -->  
		<div>flex: 1</div>		<!-- Column size 1/5 of the full width -->  
		<div class="flex2">		<!-- Column size 2/5 of the full width -->  
			<div class="arowlg">	<!-- Nested row collapsing at 992px-->  
				<div>flex: 1</div> <!-- Column size 1/4 of 2/5 = 1/10 of the full width -->  
				<div>			<!-- Column size 1/4 of 2/5 = 1/10 of the full width -->  
					<div>B</div>	<!-- Block (not a column!) -->  
				</div>  
				<div>flex: 1</div> <!-- Column size 1/4 of 2/5 = 1/10 of the full width -->  
				<div>flex: 1</div> <!-- Column size 1/4 of 2/5 = 1/10 of the full width -->  
			</div>  
		</div>  
		<div>flex: 1</div>		<!-- Column size 1/5 of the full width -->  
		<div>flex: 1</div>		<!-- Column size 1/5 of the full width -->  
	</div>  
```  
