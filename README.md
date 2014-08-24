#burstah
```
 _______  __   __  ______    _______  _______  _______  __   __
|  _    ||  | |  ||    _ |  |       ||       ||   _   ||  | |  |
| |_|   ||  | |  ||   | ||  |  _____||_     _||  |_|  ||  |_|  |
|       ||  |_|  ||   |_||_ | |_____   |   |  |       ||       |
|  _   | |       ||    __  ||_____  |  |   |  |       ||       |
| |_|   ||       ||   |  | | _____| |  |   |  |   _   ||   _   |
|_______||_______||___|  |_||_______|  |___|  |__| |__||__| |__|
```

**burstah** is a build monitor for [Go](http://go.cd) based on [node.js](http://nodejs.org).
It is a refreshed implementation of [cidar](https://github.com/patforna/cidar).

###To run is just do following:

```
   git clone https://github.com/lplotni/burstah.git
   cd burstah
   npm install
   nohup npm start &
```
###To configure
Open config.js and add the url of your GO server as well as the stages you would
like to show. The stucture of the config.js is pretty straight-forrward:

```
var config = {
    hostname: '127.0.0.1', //IP or host the Go server is running on
    port: '8153',
    auth: '', //user:password if Go is using simple auth
    project: {
      name: 'QEN', // pipeline name
        stages: [ //array with all the stages you would like to show
        'xxx :: yyy', 'zzz :: aaa'
      ]
    }
  };
```
###To improve
If you're used to node.js and express.js than you should be able to quickly navigate, through the code. For testing, I use [jasmine-node](https://github.com/mhevery/jasmine-node). All the tests can be found in the spec folder. To run them just enter
```
jasmine-node spec/
```
