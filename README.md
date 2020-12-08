# REMIX 3BOX PLUGIN
A Remix plugin to access 3Box spaces

This plugin provides an interface for remix plugins to interact with 3Box spaces.

3Box itself provides private key-value storage linked to your eth address. Read more about it <a target=_blank href='https://docs.3box.io/api/storage'>https://docs.3box.io/api/storage</a>

Your plugin can basically call these functions if the user has activated the 3BOX plugin.

## Installation

Use the plugin manager in Remix to activate the '3BOX SPACES' plugin.

## Using it in your plugin

_Examples_

Get the 3BOX plugin to login to Metamask and 3BOX

```
await client.call('box', 'login')
```

Open a 3BOX space

```
await client.call('box', 'openSpace')
```

Store a private key value pair

```
await this.client.call("box","setSpacePrivateValue","testkey","testvalue")
```

Get a private key value pair

```
await this.client.call("box","getSpacePrivateValue","testkey")
```


Where client is your remix client.
<a href='https://github.com/ethereum/remix-plugin/tree/master/packages/plugin/webview' target=_blank>https://github.com/ethereum/remix-plugin/tree/master/packages/plugin/webview</a>


The API:

|Type     |Name                   |Parameters  |Returns     |Description                                      |
|---------|-----------------------|------------|------------|-------------------------------------------------|
|_event_  |`enabled`            |            |            | Metamask is connected
|_event_  |`loggedIn`            |            |            | 3Box is connected
|_event_  |`loggedOut`            |            |            | Logged out of 3Box
|_event_  |`spaceOpened`            |            |            | 3Box space is opened
|_event_  |`spaceClosed`            |            |            | 3Box space is closed
|_event_  |`spaceClosed`            |            |            | 3Box space is closed
|_method_  |`login`            |            | bool           | connect metamask to this plugin, then login to 3box
|_method_  |`openSpace`            |            | bool           | Open the 3box space
|_method_  |`closeSpace`            |            | bool           | Open the 3box space
|_method_  |`isEnabled`            |            | bool           | metamask AND 3box are connected/logged to this plugin
|_method_  |`isSpaceOpened`            |            | bool           | return true if the calling plugin has already an opened space
|_method_  |`getSpaceName`            |            | string           | Gives the name of the space currently used
|_method_  |`getSpacePrivateValue`            | key:string           | string           | 
|_method_  |`setSpacePrivateValue`            | key:string,value:string           | bool           | 
|_method_  |`getSpacePublicValue`            | key:string           | string           | 
|_method_  |`setSpacePublicValue`            | key:string,value:string           | bool           | 
|_method_  |`getSpaceName`            |            | string           | Gives the name of the space currently used


