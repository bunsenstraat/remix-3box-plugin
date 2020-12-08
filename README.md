# REMIX 3BOX PLUGIN
A Remix plugin to access 3Box spaces

This plugin provides an interface for remix plugins to interact with 3Box spaces.

3Box provides private key-value storage linked to your eth address. Read more about it <a target=_blank href='https://docs.3box.io/api/storage'>https://docs.3box.io/api/storage</a>

Your plugin can basically call these functions if the user has activated the 3BOX plugin.

## Installation

Use the plugin manager in Remix to activate the '3BOX SPACES' plugin.
Select the plugin in the sidebar and click 'Connect to metamax'. When it's connected you should see the logout button.

## Using it in your plugin

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



