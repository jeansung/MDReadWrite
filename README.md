## MDReadWrite
This project contains a web application for generating HTML that renders easy to interact with documents that facilitate model driven reading and writing. 

## Resources 
* [Project Website](jeansung.github.io/MDReadWrite/), the web application
* [DSL Research](https://github.com/jeansung/DSLResearch), a local version of the web app, with the recursive feature 
* [Project Documents](https://drive.google.com/drive/folders/0B9z84Or5GzOnazl4a25UZV9yTHc), the architecture and design notebook for this project, for independent study project, Spring 2016 

## How to run
### Pre requisites 
* Download these [files](https://github.com/jeansung/DSLResearch/tree/master/output/dependencies). Note that the there must already specified javascript file in the parent directory of the dependencies. The generated HTML file should be in said parent directory, and named the same STEM name as the javascript file. 

* For example, consider an example that has a javascript file named `ballot.js`. The directory structure looks like: 

```
parent_directory/dependencies/
parent_directory/ballot.js
parent_directory/ballot.html
```
Thus, when the file `ballot.html` generated, here is where it should be placed. When the file is generated, open the `html` file in a web browser. Has been tested on the latest version of Google Chrome. 


### Using the website
* When you start on the website, **Step 1** is to connect the Javascript into the HTML. The file name should be the name of the javascript file and will be the name of the generated html file. The example ID 
* **Step 2**, specify the text. Use () for constants, [] for independent variables, and {} for dependent variables. 
* **Step 3**, define all of the variables. After each definition, you have to click "SAVE" to save. 
* If you want to edit a variable, click on it, and it will reload the data that has been saved, and you can continue to edit it. 
* Finish by downloading the HTML file, a button will generated for you to download the HTML file when all variables have been defined. 

## Known limitations

### Future work (limitations on functionality) 
* The math interface is still defined through javascript and must be linked in. Ideas for remedying this is to use Google Spreadsheet. 
* The web version does not support recursively defined variables - that is variables whose values rotate through text values that may contain other. 


### Minor Fixes (limitations on usability) 

* If you have duplicate variable defined in the text, it is duplicated in the variable list (only have to define once, and it will show up as defined for both). 
* Constants need to be specified with (), which means parentheses cannot be used in the text - find a better way to do the markup. 
* For things that have options, you have to use "//" as the separator, a future improvement is to have the ability to dynamically add more options. 
* More robust error checking - for example, checking that data max is bigger than data min, etc (especially for numerical answers). 
* Right now, you must include certain libraries when you download, would be better to link those to CDN. 
* Right now, saving doesn't perform any action besides just save - better to have alert or a different button style. 
* Also the download HTML button only shows up after the variables have been defined, but there should be a better alert system. 
* The backing variable (for TKSwitch Positive Negative) should be generate from a list of already defined variable. 


### Aesthetic Fixes (limitations on beauty) 
* Sometimes the formatting of the lists for variables runs over the line and then the title of the next category is bumped up. 
* There is a persistent large font. 
* There could be a better more unified theme. 
* There is not super helpful messages for the various form components, could be set. 