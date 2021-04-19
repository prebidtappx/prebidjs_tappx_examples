# Video Instream Example

You should copy these files in /integrationexamples/gpt/

## Video Ad Unit description:

Paramater | Mandatory | Description | Example |
--- | --- | --- | --- |
code | Yes | References your video id  | video-ad-div |
mediaTypes.video.context |Yes | Video ad type specification | instream
mediaTypes.video.mimes | Yes |  | Must be: [ "video/mp4" ]
mediaTypes.video.playerSize | Yes | Is where you define the player size that will be passed | Should be one array ob sizes: [320, 250]
bids.bidder |  |  |
bids.params.host |  |  |
bids.params.tappxkey |  |  |
bids.params.endpoint |  |  |
bids.params.bidfloor |  |  |
bids.params.test |  |  |

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
tappx-video-test.html

Example with Adplayer.pro