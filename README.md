# Sass boilerplate

This is a starting point for projects using Sass. The following features are included:

* Folder structure orientated on the [7-1 Pattern](http://sass-guidelin.es/#the-7-1-pattern)
* Reset (provided by [normalize.css](https://necolas.github.io/normalize.css/))
* Base styling and best practices
* Print styles (taken from [HTML5 boilerplate](https://html5boilerplate.com/))
* Useful mixins (mediaquery, font-size)
* Helper functions and classes
* Base variable template

Everything is included in the `main.scss` file. To get started compile everything using this as entry point. You should also use [`postcss/autoprefixer`](https://www.google.de/webhp?sourceid=chrome-instant&ion=1&espv=2&ie=UTF-8#q=autoprefixer) to handle browser specific prefixes.

## Best practices

* Use `px` values for fonts
* Use Flexbox it's adopted in all [current browsers](http://caniuse.com/#feat=flexbox)
* Let autoprefixer handle vendor prefixes
