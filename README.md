# PREBID.JS :tappx ADAPTER
## INTRODUCTION AND EXAMPLES

## How to run Prebid.Js project
Clone and install the project from Prebid.Js Repository
```
git clone https://github.com/prebid/Prebid.js/
cd Prebid.js
npm install
```
## Build for Development

Note: If gulp is not installed on your system, you can install it by running: `npm install --global gulp-cli`

```
# Build for Development
gulp serve

# Build Optimization
gulp serve --modules=tappxBidAdapter

# Fast build
gulp serve-fast --modules=tappxBidAdapter
```

This will create the `prebid.js` file under `./build/dev/`

This runs some code quality checks, starts a web server at http://localhost:9999 serving from the project root and generates the following files:

## Using the examples
If you need to use the examples, you can create your files under `/integrationExamples/gpt`
