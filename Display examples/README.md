# DISPLAY EXAMPLE

## Display Ad Unit description:

Paramater | Mandatory | Description | Example |
--- | --- | --- | --- |
code | Yes | References your display div id  | display-ad-div |

### Mediatypes object
Paramater | Mandatory | Description | Example |
--- | --- | --- | --- |
mediaTypes.banner |Yes |  Object with the banner definition | 
mediaTypes.banner.sizes |Yes |  Is where you define the player size that will be passed | Should be one array of sizes: [[320, 50],[320, 250]]

### Bids object
Paramater | Mandatory | Description | Example |
--- | --- | --- | --- |
bids.bidder | Yes | Bidder name | Must be: tappx

### Bids.Params object
Paramater | Mandatory | Description | Example |
--- | --- | --- | --- |
bids.params.host | Yes | Tappx url | YOUR HOST
bids.params.tappxkey | Yes | Tappx Key | YOUR TAPPX KEY
bids.params.endpoint | Yes | Tappx Endpoint  | YOUR ENDPOINT
bids.params.bidfloor | Yes | Desired bifloor | 0.01
bids.params.mktag | No | Tappx Mktag | 1234abcd |
bids.params.domainUrl | No | Site domain | example.com |
bids.params.test | No | Set it to true for testing purposes | |


### Ad Unit extra options
### Bids.Params.ext object
Paramater | Mandatory | Description | Example |
--- | --- | --- | --- |
bids.params.ext | No | External object for extra params | |
bids.params.ext.foo | No | Example extra param | |

### Basic Example
```
var adUnits = [
    {
        code: 'video-ad-div',
        renderer: {
            options: {
                text: "Tappx instream Video"
                }
        },
        mediaTypes: {
            video: {
                context: "instream",
                mimes : [ "video/mp4" ],
                playerSize: [320, 250]
            }
        },
        bids: [{
            bidder: 'tappx',
            params: {
                host: "HOST",
                tappxkey: "YOUR_TAPPXKEY",
                endpoint: "YOUR_ENDPOINT",
                bidfloor: 0.005,
                test: true
            }
        }]
    }
];
```

# Files

Any of the files can be executed with the `pbjs_debug` parameter seted to true: `tappx-file.html?pbjs_debug=true`. This will enable debug mode of PrebidJs and you will be able to view more information on your browser console.

Player | File | Url | Description
---  | --- | --- | --- |
Example with gdpr file implemented | tappx-gdpr-banner-test.html | /integrationExamples/gpt/tappx-gdpr-banner-test.html?pbjs_debug=true | -

