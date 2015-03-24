# grunt-dts-concat

> Combines TypeScript .d.ts files into a single .d.ts file for distributing CommonJS modules.

This project is under development and should not be used.


## Getting Started
This plugin requires Grunt `~0.4.5`

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install grunt-dts-concat --save-dev
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-dts-concat');
```

## The "dts_concat" task

### Overview
In your project's Gruntfile, add a section named `dts_concat` to the data object passed into `grunt.initConfig()`.

```js
grunt.initConfig({
  dts_concat: {
    options: {
      name: 'my-module',
      main: 'build/index.d.ts'
    }
  }
});
```

### Options

#### name
Type: `String`

The name of the module specified in package.json. Used to generate ambient external module declaration.

#### main
Type: `String`

The path to the .d.ts file generated by TypeScript for the main module.

#### outDir
Type: `String`
Default value: `'<baseDir>'`

Optional. The output directory.

#### out
Type: `String`
Default value: `'<baseDir>/<name>.d.ts'`

Optional. Full path to the output file. If `out` is specified then `outDir` is ignored.

#### indent
Type: `String`

Optional. Character sequence to use for indent. Default is four spaces.
