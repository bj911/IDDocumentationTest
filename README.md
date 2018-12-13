# Bolt

[![Version](https://img.shields.io/cocoapods/v/Bolt.svg?style=flat)](http://cocoapods.org/pods/Bolt)
[![License](https://img.shields.io/cocoapods/l/Bolt.svg?style=flat)](http://cocoapods.org/pods/Bolt)

This SDK enables paying with credit cards within an iOS app.

## Requirements:
- **iOS** 10.0+
- Swift 4.2+

## Installation

Bolt is available through [CocoaPods](http://cocoapods.org). To install
it, simply add the following line to your Podfile:

To run the example project, clone the repo, and run `pod install` from the Example directory first.

<details>
<summary>CocoaPods</summary>
</br>
<p>To integrate SwifterSwift into your Xcode project using <a href="http://cocoapods.org">CocoaPods</a>, specify it in your <code>Podfile</code>:</p>

```ruby
pod "Bolt"
```
</details>

## Usage

### Create Payment View Configuration

Specifies merchant-specific configuration options for the payment view.

#### 1. Programatically

### Initialization

Объявить переменную класса **BLTPaymentManager** 

```swift
var paymentManager: BLTPaymentManager?
```
Инициализазия перемменной класса **BLTPaymentManager**

```swift
        do {
            paymentManager = try BLTPaymentManager()
        } catch {
            // error handling
        }
```


## Example 

To run the example project, clone the repo, and run `pod install` from the Example directory first.

## License

Bolt is available under the MIT license. See the LICENSE file for more info.
