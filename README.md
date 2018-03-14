# vue-project-with-sass

> A Vue.js project with sass/scss.

## Sass Loader Setup
1. Install `sass-loader` and `node-sass`.
``` bash
npm i sass-loader node-sass --save-dev
```

2. Open `build/webpack.base.conf.js`
``` js
module.exports = {
    ...
    module: {
        rules: [
            ...,
            // add the object below into rules
            {
                test: /\.s[a|c]ss$/,
                use: [
                    'style-loader', 
                    'css-loader', 
                    'sass-loader'
                ]
            }
        ]
    },
    ...
}
```
3. Done.

4. Try it, Open `src/components/HelloWorld.vue`.

5. Add `lang="sass"` or `lang="scss"` in `<style>`.
### Sass

``` html
<style lang="sass" scoped>
ul
    li
        display: inline-block;
</style>
```
### Scss

``` html
<style lang="scss" scoped>
ul {
    li {
        display: inline-block;
    }
}
</style>
```

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev
```

## More
[sass-loader](https://github.com/webpack-contrib/sass-loader)
