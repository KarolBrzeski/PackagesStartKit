# PackagesStartKit
Startup package for a new project.

## ⚙ Setup

### Install Node.js

- Direct download -> [click here](https://nodejs.org/en/)
```
If you have Windows system restart your computer
```
### Install GRUNT

- Using `npm`

    ```bash
      npm install -g grunt-cli
    ```
### Install plugins from package.json
  ```bash
      cd project_path
  ```
  ```bash
      npm install
  ```
  ### Plugins:
  
  - [x] grunt-autoprefixer [click here](https://www.npmjs.com/package/grunt-autoprefixer)
  - [x] grunt-contrib-clean [click here](https://www.npmjs.com/package/grunt-contrib-clean)
  - [x] grunt-contrib-concat [click here](https://www.npmjs.com/package/grunt-contrib-concat)
  - [x] grunt-contrib-csslint [click here](https://www.npmjs.com/package/grunt-contrib-csslint)
  - [x] grunt-contrib-cssmin [click here](https://www.npmjs.com/package/grunt-contrib-cssmin)
  - [x] grunt-contrib-htmlmin [click here](https://www.npmjs.com/package/grunt-contrib-htmlmin)
  - [x] grunt-contrib-imagemin [click here](https://www.npmjs.com/package/grunt-contrib-imagemin)
  - [x] grunt-contrib-jshint [click here](https://www.npmjs.com/package/grunt-contrib-jshint)
  - [x] grunt-contrib-less [click here](https://www.npmjs.com/package/grunt-contrib-less)
  - [x] grunt-contrib-uglify [click here](https://www.npmjs.com/package/grunt-contrib-uglify)
  - [x] grunt-contrib-watch [click here](https://www.npmjs.com/package/grunt-contrib-watch)
  - [x] grunt-sass [click here](https://www.npmjs.com/package/grunt-sass)
  
  ## 🤔 How to use it?
  
  ### SASS or LESS ?
  
  In the Gruntfile.js you must delete the preprocessor which you do not use "sass" or "less"
   ```js
     135   grunt.registerTask("dev", ["clean", "jshint", "sass", "less", "autoprefixer", "csslint"]);
  ```
  ### Plugin Watch
    you must install LiveReload (Chrome plugin) or create script into index.html:
  ```js
    <script src="//localhost:35729/livereload.js"></script>
  ```     
  Now you can use this task 
  ```bath
    grunt watch
  ``` 
  :exclamation: Remember that you must be in the project directory
  
  - Now the plugin keeps track of all changes in the project and automatically runs the task "dev" :sunglasses: </br>
    **Multitask dev:**
   - [x] Clean - Clean files and folders
   - [x] Jshint - Validate files with JSHint
   - [x] Sass - Compile Sass to CSS using node-sass **or** Less - Compile LESS files to CSS
   - [x] Autoprefixer - Parses CSS and adds vendor-prefixed CSS properties using the Can I Use database.
   - [x] Csslint - Lint CSS files
  
   ### Create a production version
   
- Using `npm`

    ```bash
      grunt build
    ``` 
    
  This multitask will perform the following tasks: 
  - [x] Multitask **dev**
  - [x] Concat - Concatenate files.
  - [x] UglifyJS - Minify JavaScript files
  - [x] Cssmin - Minify CSS
  - [x] Htmlmin - Minify HTML
  - [x] Imagemin - Minify images
  
  
  :mag:The production version will be in the catalog: **build/**
  
  
