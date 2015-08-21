A patched version of [JaguarJS-JSDoc](https://github.com/davidshimjs/jaguarjs-jsdoc)
---
JaguarJS-JSDoc is by far the most beautiful JSDoc theme in existence, but unfortuantely it's no longer maintained.

This patched version is a hideous amalgam of every PR and every other patch I could find, all mashed together in the name of progress.  It seems to work.

Usage
---
1. Install from npm
```
$ npm install jaguarjs-jsdoc-patched --save-dev
```

2. Copy the `conf.json` file to your repo.  Edit as necessary.

3. Assuming you're using [grunt-jsdoc](https://github.com/krampstudio/grunt-jsdoc), set the template to `./node_modules/jaguarjs-jsdoc-patched`
``` javascript
  grunt.initConfig({
    jsdoc : {
      dist : {
        src: ['src/*.js'],
        options: {
          destination: 'docs',
          configure : "conf.json",
          template: './node_modules/jaguarjs-jsdoc-patched'
        }
      }
    }
  });
```
Other task runners should work similarly.

3. If you already have jsdoc system, you can use this project as jsdoc template.
```
$ jsdoc -t `project folder` -c `configuration file` `source files` `README.md file`
```

4. Again assuming you're using grunt-jsdoc, simply run `grunt jsdoc`!


License
---
This project under the MIT License.

