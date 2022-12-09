# zepp-ts
Compile ZeppOS projects in TypeScript.

# How it works
We accomplish this by setting up the project such that we develop with TypeScript in `src`. This directory should have the necessary files for a `zeus` build (`app.json`, `assets`, etc.). The `package.json` and `node_modules` should remain top-level.

NOTE: JSON references to source files should still point to `*.js` files, **NOT** `*.ts`.

Then, we run `teus`, which simply compiles your TypeScript code into JavaScript, copies over the other source files into the `dist` directory.

# Steps

1. Set the `module` to `ES6`, `target` to `es6`, and `moduleResolution` to `Node`. This ensures that external libraries are compiled in properly.

# Example
* `teus; cd dist; zeus build`
