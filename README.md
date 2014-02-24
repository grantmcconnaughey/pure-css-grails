# Grails Pure CSS Plugin

## Description

This plugin provides an easy way to include Pure CSS in your Grails application. Pure CSS is "A set of small, responsive CSS modules that you can use in every web project." Documentation on Pure CSS can be found at http://purecss.io.

## Usage

There are currently three ways to use the plugin:

1. Run `grails copy-pure-css` to copy the CSS files over to your application
2. Use the Resources plugin to add the CSS to your GSPs ( `<r:require module="pure-all" />` )
3. Include the files yourself via a style tag ( `<g:resource plugin="pure-css" dir="css" file="pure.css" />` )

## Modules

There are several modules you can include in your GSPs. Any module with "-nr" is the "non-responsive" version. They are:
* `pure-all`: The main `pure.css` file with all modules include.
* `pure-all-nr`: The non-responsive version of `pure-all`
* `pure-base`: The base pure functionality without any modules. All of the modules below will include this module.
* `pure-buttons`
* `pure-forms`
* `pure-forms-nr`
* `pure-grids`
* `pure-grids-nr`
* `pure-menus`
* `pure-menus-nr`
* `pure-tables`

## Usage with the Resources Plugin

To include modules using the Resources plugin, add any of the modules in an <r:require /> tag. For example, to include all of Pure CSS add the following to the head of your page:

```html
<r:require module="pure-all" />
```

To add just the Pure Grids and Pure Tables CSS, add this to your page:

```html
<r:require modules="['pure-grids', 'pure-tables']" />
```

This will add the Pure Grids, Pure Tables, and Pure Base CSS to your view. They will be bundled together into one file.