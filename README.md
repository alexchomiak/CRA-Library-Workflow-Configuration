# About this Project
This is just a basic create react app with a webpack configuration that compiles anything exposed in the src/lib.js file
into a javascript library that can be used anywhere

# React Workflow Meant for Library development
Export any variables/classes you want exposed in the library inside of lib.js,
then run the command
```
    npm run buildlib
```
A directory will be created in the root of the project with your library file. 
You can then import the library via any script tag / es6 import

Example when using script tag:
Lets say our LibraryName is Library, the filename is Library.js, and in src/lib.js
we export one method called hello(), the corresponding HTML would look like this:
```html
<html>
    <head>
        <!-- load library file !-->
        <script src="./Library.js"> </script>
    </head>

    <body>
        <script>
            // call library method
            Library.hello()
        </script>
    </body>
</html>
```


# Configure your library
In the root of the project you will notice a librarysettings.js file which contains a JSON
of various settings that you can change about your library. 
Settings in librarysettings.js:
* fileName (filename the library will be compiled and minified into)
* libraryName (name of the global library variable when imported)
* libraryBuildFolder (folder library will be built into)
