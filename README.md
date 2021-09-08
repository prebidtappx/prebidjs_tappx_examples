# PREBID.JS :tappx ADAPTER
## Version of Prebid.js that includes the last stable version of :tappx adapter
5.11.0
## INTRODUCTION AND EXAMPLES
If you need to check the operation of our adapter, you can run the test files from a web browser, before that, you need to replace your connection details in the adunits of the .html files. The parameters to replace are:
- host: "HOST"
- tappxkey: "YOUR_TAPPX_KEY"
- endpoint: "YOUR_ENDPOINT"

### Setting your site domain
You can add your site domain on the Ad unit definition, but also you can add the domain of your site on the pbjs set config definition on `pbjs.setConfig({ pageUrl: "example.com" })`. More info on: https://docs.prebid.org/dev-docs/publisher-api-reference/setConfig.html#setConfig-Page-URL

## ADVANDED BUILD
If you want to run Prebid.js in advanced way, your can build a development
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
gulp build --modules="tappxBidAdapter,consentManagement,consentManagementUsp,priceFloors,admixerIdSystem,britepoolIdSystem,criteoIdSystem,deepintentDpesIdSystem,fabrickIdSystem,flocIdSystem,haloIdSystem,id5IdSystem,identityLinkIdSystem,idxIdSystem,intentIqIdSystem,liveIntentIdSystem,lotamePanoramaIdSystem,mwOpenLinkIdSystem,merkleIdSystem,netIdSystem,nextrollIdSystem,novatiqIdSystem,parrableIdSystem,pubProvidedIdSystem,quantcastIdSystem,sharedIdSystem,tapadIdSystem,unifiedIdSystem,uid2IdSystem,verizonMediaIdSystem,zeotapIdPlusIdSystem"
```

This will create the `prebid.js` file under `./build/dev/`

This runs some code quality checks, starts a web server at http://localhost:9999 serving from the project root and generates the following files:

## Using the examples on your dev build Prebid.Js
If you need to use the examples on your build of Prebid.js, you can create your files under `/integrationExamples/gpt`
