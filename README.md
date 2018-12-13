# Bolt

[![Version](https://img.shields.io/cocoapods/v/Bolt.svg?style=flat)](http://cocoapods.org/pods/Bolt)
[![License](https://img.shields.io/cocoapods/l/Bolt.svg?style=flat)](http://cocoapods.org/pods/Bolt)

This SDK enables paying with credit cards within an iOS app.

## Requirements:
- **iOS** 10.0+
- Swift 4.2+

## Installation

<details>
<summary>CocoaPods</summary>
</br>
<p>To integrate Bolt into your Xcode project using <a href="http://cocoapods.org">CocoaPods</a>, specify it in your <code>Podfile</code>:</p>

```ruby
pod "Bolt"
```
</details>


<details>
<summary>Manually</summary>
</br>
Clone the repo and drag the Bolt folder into your project.

</details>

## Usage

First of all **BLTPaymentViewConfiguration** should be created.

**BLTPaymentViewConfiguration** Specifies merchant-specific configuration options for the payment view.

These values can be configured programatically in a custom configuration initializer, or by including the keys in the app's info.plist and creating a configuration instance through the default initializer.

<details>
<summary>Programatically</summary>
</br>

```swift
let serverEnvironment: BLTServerEnvironment = .production // or .sandbox
let publishableKey = "YOUR PUBLISHABLE KEY"
let paymentViewConfiguration = BLTPaymentViewConfiguration(publishableKey: publishableKey, serverEnvironment: serverEnvironment)
```
</details>


<details>
<summary>Including the keys in the app's Info.plist</summary>
</br>
<p>Include the keys <b>BLTPublishableKey</b> and <b>BLTServerEnvironmentKey</b> in the app's info.plist.</p>

- For **BLTServerEnvironmentKey**, a value of **0** specifies the **sandbox** server environment, a value of **1** specifies the **production** environment.
- If **BLTServerEnvironmentKey** isn't present, production is assumed.

1. Right-click **info.plist**, and choose **Open As Source Code**.
2. Copy and paste the following XML snippet into the body of your file (`<dict>...</dict>`).

```XML
<key>BLTPublishableKey</key>
<string>Your Publishable Key</string>
<key>BLTServerEnvironment</key>
<integer>0</integer>
```

3. Create a configuration instance through the default initializer. Throws an exception if a default initializer is creating but the **BLTPublishableKey** isn't present in the Info.plist.

```swift
let paymentViewConfiguration = BLTPaymentViewConfiguration()
```

</details>

### Delegate


## Example 

To run the example project, clone the repo, and run `pod install` from the Example directory first.

## License

Bolt is released under the MIT license. See [LICENSE](https://github.com/BoltApp/bolt-ios/blob/master/LICENSE) for more information.
