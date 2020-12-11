## AWS Greengrass Stream Manager SDK for JS

The **AWS Greengrass Stream Manager SDK for JS** enables javascript developers to manage data streams using [Stream
Manager](https://docs.aws.amazon.com/greengrass/latest/developerguide/stream-manager.html) on AWS IoT Greengrass core.

## Overview

This document provides instructions for preparing your JS code to manage Streams in Stream Manager using the JS SDK.

## Using Stream Manager Client to work with Streams

Follow the guide [here](https://docs.aws.amazon.com/greengrass/latest/developerguide/work-with-streams.html) to work
with Streams using the Stream Manager Client from the Stream Manager SDK.

## Compatibility

Stream Manager SDK provided by this repo is compatible with Stream Manager running on Greengrass Core 1.11 and above.

### StreamManager Usage

```javascript
const {
    StreamManagerClient
} = require('aws-greengrass-stream-manager-sdk');

const c = new StreamManagerClient({
    onConnectCb: async () => {
        try {
            // Let's start with something simple.
            // Just print out all the available stream names on the server 
            console.log(await c.listStreams());
        } finally {
            c.close(); // Always close the client when you're done
        }
    }
});
```
<div class="Section" id="1.1.0updates">

## 1.1.0 Updates[¶](#1.1.0updates "Permalink to this headline")

Stream manager supports automatic data export to AWS S3 and AWS IoT SiteWise, provides new API method to update existing streams, and pause or resume exporting.

</div>

## Getting Help

*   [Ask on a Greengrass forum](https://forums.aws.amazon.com/forum.jspa?forumID=254)

## License

Apache 2.0
