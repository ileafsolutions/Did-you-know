# Did you Know?
Notification center widget with shared coredata.
Example project for sharing data between iOS Extension and container app through shared coredata.

<img src="./Asset/art.png?raw=true">

## Preview
<img src="./Asset/preview.png?raw=true">

## Installation

### Compatibility

- iOS 10.3+ 

- Xcode 8.0+

## Usage

1.CREATE AN APP GROUP

App Groups are the scheme iOS uses to allow different apps to share data. If the apps have the right entitlements and proper provisioning, they can access a shared directory outside of their normal iOS sandbox. To share data between widget extension and container app ,select the Target for your App and go to the Capabilities tab. There, enable App Groups. Do the same in the Target of your widget extension 

<img src="./Asset/appgroup.png?raw=true">

When you flip that switch, Xcode will talk to the developer center to configure your app ID for app groups.Next it'll ask you for a group name. Give it one and it'll create and download a new provisioning profile.Now, your app and its extension are ready to share the container, so it’s time to put the data in it.

2.PUT YOUR COREDATA IN SHARED CONTAINER

-Move SCDCoreDataWrapper.swift Class, the .xcdatamodeled and NSManagedObject Subclass to my SharedCode Framework.
-Get the URL of the group container with containerURL(forSecurityApplicationGroupIdentifier: of FileManager passing the container identifier.you need to point to the securitygroup as your store url so that they are both being stored to that. 

## Author
iLeaf Solutions
 [http://www.ileafsolutions.com](http://www.ileafsolutions.com)
