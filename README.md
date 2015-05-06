#Disclaimer
This is an unofficial Bower package that simply puts togeter the JavaScript and CSS files found at the [Fluig Style Guide](http://style.fluig.com/) page, where you can find more information and documentation.

#Using with Webpack
In your `webpack.config.js` include the following loaders:
```javascript
{
  test: /\.(png|jpg|gif)$/,
  loader: 'url-loader?limit=8192'
}, {
  test: /\.woff(2)?(\?v=[0-9]\.[0-9]\.[0-9])?$/,
  loader: 'url-loader?limit=10000&minetype=application/font-woff'
}, {
  test: /\.(ttf|eot|svg)(\?v=[0-9]\.[0-9]\.[0-9])?$/,
  loader: 'file-loader'
}
```
Also include the following plugin for loading jQuery:
```javascript
new webpack.ProvidePlugin({
  $: "jquery",
  jQuery: "jquery"
})
```
