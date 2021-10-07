# protractor-bitbucket-pipeline
Example to run protractor headless with bitbucket pipelines

## Capabilities

In your .conf you will need to declare capabilities. Here are examples for Chrome and Firefox.

### Chrome
```
    capabilities: {
           'browserName': 'chrome',
           'chromeOptions': {
               binary: "/usr/bin/google-chrome",
               args: [ "--no-sandbox", "--headless", "--disable-gpu", "--window-size=1325,744", "--remote-debugging-port=9222"]
           }
    }
```

### Firefox
```
    capabilities: {
         'browserName': 'firefox',
         'moz:firefoxOptions': {
             args: ['--verbose', '--headless'],
             binary: "/opt/atlassian/pipelines/agent/build/node_modules/protractor/node_modules/webdriver-manager/selenium/geckodriver-v0.25.0"
         }
    }
```
