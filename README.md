# gulp-highlight-files
Gulp plugin to highlight a set of files.

### Installation

`npm install gulp-highlight-files --save-dev`

```ts
const gulpHighlightFiles = require('gulp-highlight-files');

/* Custom options for the gulp plugin. */
const options = {
  languageMap: { ts: 'typescript' }
};

/* Inside of the gulp task. */
return gulp.src('**/*.html')
  .pipe(gulpHighlightFiles(options)
  .pipe(gulp.dest('dist'));
```

### Configuration

```ts
type Options = {
  language: string; // Force HighlightJS language
  languageMap: any; // Map to overwrite languages
  hljsOptions: any // Options for highlightjs
}
```
