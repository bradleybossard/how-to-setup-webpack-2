# how-to-setup-webpack-2
Following along with this tutorial https://gokulkrishh.github.io/webpack/2017/02/03/how-to-setup-webpack-2.html


## Steps (some missing from tutorial)

1.  Initialize an package.json

```
    npm init --yes
```

2.  Install webpack and webpack-dev-server

```
    npm install --save-dev webpack webpack-dev-server
```

3.  Add basic config
```
		var webpack = require('webpack');

		var config = {
			context: __dirname + '/src', // `__dirname` is root of project and `src` is source
			entry: {
				app: './app.js',
			},
			output: {
				path: __dirname + '/dist', // `dist` is the destination
				filename: 'bundle.js',
			},
		};

		module.exports = config;
```

4.  Install lodash (or other libraries to be used)

```
    npm install --save lodash
```

5.  Add a basic src/app.js file

```
    var _ = require('lodash');

    var array = [1];
    var other = _.concat(array, 2, [3], [[4]]);

    alert(other); // [1, 2, 3, [4]]
```

6.  Compile with webpack

```
    webpack
```
