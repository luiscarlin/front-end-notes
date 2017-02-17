# Gulp

- requires node and npm (comes with node)
- install `npm install --global gulp gulp-cli`
- 4 parts:
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
- Easier learning curve and (possibly) faster than Grunt because of async execution
- Grunt may be slower because write to temp files
- Grunt has been around for longer and has more plugins
