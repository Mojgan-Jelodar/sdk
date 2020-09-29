
# UID_SEJAM_SDK

UID, a secure digital identity platform

UID is an application that allows you to login and register on websites without having a username and password. UID also has an electronic documents wallet that to stores you’re ID cards and lets you share it with the websites of the electronic service providers you wish.

By installing the UID app, registering on sites and filling forms becomes short & easy while giving you the option of accessing your identification documents anytime and anywhere.

Login with UID:

- Run the UID app and fill the required fields to complete your profile.

- A QR code will be displayed on the partner’s websites, just scan it with the UID app.

- Allow the partner access to your information and revoke it any time you want.

From now on, you need only to scan a QR code to login to your account on the UID partner’s website.


Advantages of using UID:

- Login to websites and apps with just a scan.

- Faster, shorter & easier signing and registering.

- No need for filling registration forms to receive online services.

- No need for physical copies to receive services anymore.

- Possible to store and maintain ID cards.

- Access your documents anytime, anywhere.


## Installation

```bash
cd 'to your project'
pod init
open -a xcode Podfile 
```
add below line into your target :
```bash
pod 'UID_SEJAM_SDK' 
```
save and close the file...

go back to terminal and in your project folder run this command
add below line into your target :
```bash
pod install 
```
if you encountered with the 
- `error Unable to find a specification for ...`
use the replacement commands
```bash
pod install --repo-update
```
### OR

```bash
pod repo update
```




## Usage

```swift
 import UID_SEJAM_SDK
 let vc = AuthenticatorRouter.createModule(url : "put your address server",
                                                    userInfo: UserInfo(nationalCode: "national code",serialCode: "serial code"),
                                                    delegate: self)
 self.present(vc, animated: true, completion: nil)

```
also you can catch up the result of authentication in 3 mode by a AuthenticatorDelegate
```swift
    func didFailure(error: Error) {
        print("Failed by error ::\(error.localizedDescription)")
    }
    
    func didCanceled() {
        print("Canceled by user!")
    }
    
    func didSuccess() {
        print("Authentication was successful!")
    }
```
