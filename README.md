PSL Mobile Foundation
===
## PushNotificationsSwift
A sample application demonstrating use of push notifications in iOS applications.

### Tutorials
https://pmf.persistentproducts.com/tutorials/en/foundation/9.0/notifications/


### Usage

1. From a **Command-line** window, navigate to the project's root folder and run the commands:
  - `pod update` followed by `pod install` to add the MobileFoundation SDK.
  - `mfpdev app register` to register the application in the MobileFoundation Server.
2. In the MobileFoundation console: 
  - Under **Applications** → **PushNotificationsSwift** → **Security** → **Map scope elements to security checks**, add a mapping for `push.mobileclient`.
  - Under **Applications** → **PushNotificationsSwift** → **Push** → **Push Settings**, upload your PKCS 12 (.p12) file and password.
3. Import the project to Xcode using the .xcworkspace file.
4. Configure the project with your bundleId (based on bundleId that you have created for your push notifications certificate .p12 file). 
5. Run the app by clicking the **Run** button.

**[Sending a notification](https://pmf.persistentproducts.com/tutorials/en/foundation/9.0/notifications//tutorials/en/foundation/9.0/notifications/sending-push-notifications):**

* Tag notification
    * Use the **MobileFoundation Operations Console → [your application] → Push → Send Push tab**.
* Authenticated notification:
    * Deploy the [**UserLogin** sample Security Check](https://pmf.persistentproducts.com/tutorials/en/foundation/9.0/notifications//tutorials/en/foundation/9.0/authentication-and-security/user-authentication/security-check).
    * In **MobileFoundation Operations Console → [your application] → Security tab**, map the **push.mobileclient** scope to the **UserLogin** Security Check.
    * Follow the instructions for [REST APIs](https://pmf.persistentproducts.com/tutorials/en/foundation/9.0/notifications//tutorials/en/foundation/8.0/notifications/sending-push-notifications#rest-apis) to send the notification.

**Notes:**

* Must be tested on physical devices.
* The BundleID must relate to an AppID configured with push notifications.
* The certificate must be uploaded via the MobileFoundation Operations Console.
* Must use Xcode 8.2.1 and above  and Swift 3.0

### Supported Levels
PSL MobileFoundation 9.0
