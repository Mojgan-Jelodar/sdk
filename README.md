
# UID

UID is a SDK for authentication process.

## Installation

Use the cocoa dependency manager [pod](https://pip.pypa.io/en/stable/) to install UID.

```bash
cd 'to your project'
pod init
open -a xcode Podfile 
```
add below line into your target :
```bash
pod 'UID_SDK' 
```

save and close the file...
go back to terminal and in your project folder run this command
add below line into your target :
```bash
pod install 
```

## Usage

```swift
 import UID_SDK
 let vc = AuthenticatorRouter.createModule(url : "put your address server",
                                                    userInfo: UserInfo(nationalCode: "national code",serialCode: "serial code"),
                                                    delegate: self)
 self.present(vc, animated: true, completion: nil)

```
