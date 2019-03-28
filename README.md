# Example Project for iOS app using Google OAuth API

## CocoaPods Dependencies

1. Run the following command to install the required
library pods.

```
$ pod install
```

2. Open the workspace in Xcode:

```
$ open Example-iOS.xcworkspace
```


## Configure the Example to Use Your Client

To try the example with your own client, changes need to be made in the following
three places:

1. In `GTMAppAuthExampleViewController.m` update `kClientID` with your new client
id.

2. In the same file, update `kRedirectURI` with the *reverse DNS notation* form
of the client ID. For example, if the client ID is
`YOUR_CLIENT.apps.googleusercontent.com`, the reverse DNS notation would be
`com.googleusercontent.apps.YOUR_CLIENT`. A path component is added resulting in
`com.googleusercontent.apps.YOUR_CLIENT:/oauthredirect`.

3. Finally, open `Info.plist` and fully expand "URL types" (a.k.a.
"CFBundleURLTypes") and replace `com.googleusercontent.apps.YOUR_CLIENT` with
the reverse DNS notation form of your client id (not including the
`:/oauthredirect` path component).

Once you have made those three changes, the sample should be ready to try with
your new OAuth client.
