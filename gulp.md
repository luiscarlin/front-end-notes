# Gulp

- requires node and npm (comes with node)
- easier learning curve and (possibly) faster than Grunt because of async execution
- Grunt may be slower because write to temp files
- Grunt has been around for longer and has more plugins

```bash
# install
npm install -g gulp

# in $ROOT_PROJ/
touch gulpfile.js
```

- 4 parts in gulpfile.js:
  - required modules

    ```js
    var uglify = require('gulp-uglify');
    ```
  - named tasks

    ```js
    // run as gulp <task-name>
    gulp.task('scripts', function() {
      // do some task or build something
    });
    ```
  - watch (optional)

    ```js
    // watch other tasks/ files for changes and run a task if they do
    gulp.task('watch', function() {
      gulp.watch('app/js/**/.*.js', ['scripts']);
    });
    ```
  - default tasks (optional)

    ```js
    // task(s) that run by default when calling 'gulp' wihtout task name
    // tasks are run asynchronously, but you can set sequence
    gulp.task('default', ['scripts', 'watch']);
    ```
