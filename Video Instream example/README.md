# Video Instream Example

You should copy these files in /integrationexamples/gpt/

## Video Ad Unit description:

Paramater | Mandatory | Description | Example |
--- | --- | --- | --- |
code | Yes | References your video div id  | video-ad-div |
mediaTypes.video.context |Yes | Video ad type specification | instream
mediaTypes.video.mimes | Yes | Mimes suported | Must be: [ "video/mp4" ]
mediaTypes.video.playerSize | Yes | Is where you define the player size that will be passed | Should be one array of sizes: [[320, 50],[320, 250]]
bids.bidder | Yes | Bidder name | Must be: tappx
bids.params.host | Yes | Tappx url | testing.ssp.tappx.com/rtb/v2/
bids.params.tappxkey | Yes | Tappx Key | pub-1234-desktop-1234
bids.params.endpoint | Yes | Tappx Endpoint  | ABCD1234
bids.params.bidfloor | Yes | Desired bifloor | 0.01
bids.params.test | No | Set it to true for testing purposes |

### Example
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
                host: "testing.ssp.tappx.com/rtb/v2/",
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

Player | File | Description
---  | --- | --- |
Example with Adplayer.pro | tappx-video-appro-test.html | -

