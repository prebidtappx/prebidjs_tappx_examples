# VIDEO INSTREAM EXAMPLE

## VIDEO AD UNIT DESCRIPTION

Paramater | Mandatory | Description | Example |
--- | --- | --- | --- |
code | Yes | References your ad slot name or div element id | video-ad-div |
mediaTypes | Yes | Object to specify the supported formats and their respective properties. More info in `Mediatypes object` reference | - |
bids | Yes | Array of bids objects and its parameters. More info on `Bids object` reference | - |

### MEDIA TYPES OBJECT
Paramater | Mandatory | Description | Example |
--- | --- | --- | --- |
mediaTypes.video | Yes | Array that defines properties of a video ad | - |
mediaTypes.video.context |Yes | Video ad type specification. | Options: instream, outstream
mediaTypes.video.mimes | Yes | Mimes suported | Must be: [ "video/mp4" ]
mediaTypes.video.playerSize | Yes | Is where you define the player size that will be passed | Should be one array of sizes: [[320, 50],[320, 250]]

### BIDS OBJECT
Paramater | Mandatory | Description | Example |
--- | --- | --- | --- |
bids.bidder | Yes | Bidder name | Must be: tappx 
bids.params | Yes | Array of parameters for the request | More info on `Params object` reference

#### Bids.params object
Paramater | Mandatory | Description | Example |
--- | --- | --- | --- |
bids.params.host | Yes | Tappx url | YOUR HOST
bids.params.tappxkey | Yes | Tappx Key | YOUR TAPPX KEY
bids.params.endpoint | Yes | Tappx Endpoint  | YOUR ENDPOINT
bids.params.bidfloor | Yes | Desired bifloor | 0.01
bids.params.mktag | No | Tappx Mktag | 1234abcd |
bids.params.domainUrl | No | Site domain | example.com |
bids.params.test | No | Set it to true for testing purposes | 1 |

### Ad Unit extra options
### Params.ext object
Paramater | Mandatory | Description | Example |
--- | --- | --- | --- |
bids.params.ext | No | External object for extra params | |
bids.params.ext.video_id | No | Video Id | |
bids.params.ext.foo | No | Example extra param | |

### Params.video object
Paramater | Mandatory | Description | Example |
--- | --- | --- | --- |
bids.params.video | No | Contains video options for outstream video requests | |
bids.params.video.skip | No | Indicates the number of seconds before the ad skip is enabled (0 disables skip)  | 0 |
bids.params.video.minduration | No | | |
bids.params.video.maxduration | No | | |
bids.params.video.startdelay | No | | |
bids.params.video.playbackmethod | No | | |
bids.params.video.api | No | | |
bids.params.video.protocols | No | | |
bids.params.video.battr | No | | |
bids.params.video.linearity | No | | |
bids.params.video.placement | No | | |
bids.params.video.minbitrate | No | | |
bids.params.video.maxbitrate | No | | |

### Basic required params Example
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
Instream example with Adplayer.pro | tappx-video-appro-test.html | /integrationExamples/gpt/tappx-video-appro-test.html?pbjs_debug=true | -
Outstream example | tappx-video-outstream-test.html | /integrationExamples/gpt/tappx-video-outstream-test.html?pbjs_debug=true | -

