#Find Files#

a simple search utility that will return any file whose name includes the provided search term

###Install With npm###

npm install findFiles

###require it in node###

var finder = require('findFiles');

###Use it###
finder(value, options, callback);

####where####
* value - string
  + your search term as a string, findFiles will convert your string to a regex for testing against file names so 'colou?r' would match any files that had either the English or American spelling of the word colour.

* options - Object 
```
   {
       root: 'string' // The root directory where you search will begin before walking through all folders below it in the tree
       requireExts: array // Optional - if included the search will only return files which also have a file extension contained in this array
       ignoreDirs: array // Optional - if included the search will not iterate through files if they are in a folder/subfolder contained in the ignoreDirs array
   }

```

* callback - Function - the callback is passed one argument which is an array of objects as below
```
   [{
       name: fileName,
       filepath: absolute path of the file including filename
   }]
```
