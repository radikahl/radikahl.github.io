---
layout: post
title: Debugging Tip for the Feedback Service of the APNS
excerpt_separator: “”
---
Debugging Apple's Push Notification service is a pain. Only little feedback if the dispatched notification was malformed or in some other way erroneous. But even worse is the service's accompanying feedback service. The feedback service provides an iOS developer with a list of devices that have uninstalled your app. Debugging it is hell. Not only will Apple empty the list every time the feedback service is called. Hence, test cases have to be reconstructed strenuously by hand every time. But there is a **mean bug**. If the iOS device on which you deleted our application doesn't have another development app installed that uses Apple's sandbox environment for push notifications the feedback service will never tell you that your app was deleted.

Thus to properly debug the feedback service you need another app that is registered with the APNS. It doesn't need to be more than a barebone application. When testing if your server can handle the feedback service properly you must always send the device that has deleted your app one more notification so that the APNS learns that the app isn't there anymore.