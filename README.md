Keychain Plugin for Apache Cordova
=====================================
created by Shazron Abdullah

Updated by Max Lynch <max@ionic.io>

### Installation

```shell
cordova plugin add https://github.com/ionic-team/cordova-plugin-ios-keychain
```

### iCloud keychain enabled

iCloud keychain synchonizing is enabled, so the keychain will be mirrored across all devices *if* the user is signed in to iCloud (Settings > iCloud) and has iCloud keychain turned on (Settings > iCloud > Keychain)

### Usage
              
See the **example** folder for example usage.

```js
/*
 Retrieves a value for a key
 
 @param successCallback returns the value as the argument to the callback when successful
 @param failureCallback returns the error string as the argument to the callback, for a failure
 @param key the key to retrieve
 @param TouchIDMessage the message to show underneath the TouchID prompt (if any)
 */
Keychain.get(successCallback, failureCallback, 'key', 'TouchID Message');

/*
 Sets a value for a key
 
 @param successCallback returns when successful
 @param failureCallback returns the error string as the argument to the callback, for a failure
 @param key the key to set
 @param value the value to set
 @param useTouchID whether to store the value with security such that TouchID will be needed to grab it
 */
Keychain.set(successCallback, failureCallback, 'key', 'value', useTouchID);

/*
 Removes a value for a key
 
 @param successCallback returns when successful
 @param failureCallback returns the error string as the argument to the callback
 @param key the key to remove
 */
Keychain.remove(successCallback, failureCallback, 'key');

/*
 Sets a JSON value for a key 
 
 @param successCallback returns when successful
 @param failureCallback returns the error string as the argument to the callback, for a failure
 @param key the key to set
 @param value the value to set
 @param useTouchID whether to store the value with security such that TouchID will be needed to grab it
 */
Keychain.setJson(successCallback, failureCallback, 'key', 'value', useTouchID);

/*
 Gets a JSON value for a key 
 
 @param successCallback returns when successful
 @param failureCallback returns the error string as the argument to the callback, for a failure
 @param key the key to set
 @param useTouchID whether to store the value with security such that TouchID will be needed to grab it
 */
Keychain.getJson(successCallback, failureCallback, 'key', useTouchID);
```

### License 

[Apache 2.0 License](http://www.apache.org/licenses/LICENSE-2.0.html) except for the Auth0 SimpelKeychain code that is under MIT
