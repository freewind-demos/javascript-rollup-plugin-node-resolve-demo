JavaScript Rollup "rollup-plugin-node-resolve" Demo
===================================================

在使用rollup打包时，如果需要把`node_modules/`目录下的文件包含进来，就需要使用`rollup-plugin-node-resolve`这个插件。

但是它的功能比较弱，仅能处理es module，也就是说，被包含的文件里面，应该使用了类似`export function`这样的语法，
而不是`module.exports`这样的commonjs语法，后者需要使用另一个叫`rollup-plugin-commonjs`的插件配合处理。

所以在这个Demo中，为了不引入`rollup-plugin-commonjs`，在`toUpper`中的`index.js`文件中使用了es module语法。
注意`toUpper`这个module已经被publish到npmjs上了。

```
npm install
npm run demo
```
