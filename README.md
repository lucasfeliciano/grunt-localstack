grunt-localstack
=======================

A grunt plugin to start and stop BrowserStack's tunnel client. On first run this will download the appropriate binary for your platform from BrowserStack. On Windows this will be a Jar file and you will need to have Java already installed.

For BrowserStack documentation see: http://www.browserstack.com/

## Installation

```
npm install grunt-localstack
```

## Usage


### Load task

```javascript
grunt.loadNpmTasks('grunt-localstack');
```

### Task Options

Configure localstack in your Gruntfile.js

#### Basic config

```javascript
grunt.initConfig({
  localstack: {
    options: {
      key: YOUR_KEY,
      hosts: [{
        name: 'localhost',
        port: 8080,
        sslFlag: 0
      }]
    }
  }
});

```

#### Optional options
```javascript
// override the default bin directory for the OSX binary
osxBin: 'your_bin_dir',
// override the default bin directory for the Linux 32 bit binary
linux32Bin: 'your_bin_dir',
// override the default bin directory for the Linux 64 bit binary
linux64Bin: 'your_bin_dir',
// override the default bin directory for the win32 binary
win32Bin: 'your_bin_dir',
// set the -tunnelIdentifier option
tunnelIdentifier: 'my_tunnel',
// set the -skipCheck option
skipCheck: true,
// set the -v (verbose) option
v: true,
// set the -proxyUser option
proxyUser: PROXY_USER,
// set the -proxyPass option
proxyPass: PROXY_PASS,
// set the -proxyPort option
proxyPort: PROXY_PORT,
// set the -proxyHost option
proxyHost: PROXY_HOST,
// set the -force option
force: false
```

### Tasks

To start browserstack binary use:

```
localstack
```

To stop browserstack binary use:

```
localstack:stop
```



## License
Copyright &copy; 2014 Lucas Feliciano  
Licensed under the MIT license.
