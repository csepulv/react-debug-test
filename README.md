#Debugging tests in WebStorm and create-react-app

`npm install`

Open the project in WebStorm. 
* Browse to `App.test.js`. Set a breakpoint (line 6 or 7, for example)
* Run the `Tests` in Debug mode

If all goes well, your breakpoint should get hit. 

As a note: this has only been tested with Node.js 6.9 (and higher). I am not sure if it will work with an older version.

Generally, you 

Create a Run configuration with these settings
* set babel-node as node interpreter
* add `--presets=babel-preset-es2015` as a node parameter
* `node_modules/react-scripts/scripts/test.js` as JavaScript file to run
* add `--env=jsdom` as an application parameter
* add `CI=true` as an environment variable (so all tests will run instead of running in <em>watch</em> mode)