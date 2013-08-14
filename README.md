# irc-notify

Send a message to an IRC channel

## Options

### required

* `server` - The hostname or ip address of the IRC server.
* `port` - The port of the IRC server.
* `nickname` - The nickname of the user that sends the message.
* `channel` - The channel that the message will be send to. Do not include '#' sign.

### optional

* `passed-message` - Use this option to override the default passed message.
* `failed-message` -  Use this option to override the default failed message.
* `on` - Possible values: `always` and `failed`, default `always`
* `doublehashes` - Set this option to `true` for it to join the double hash version of the specified channel (##channel instead of #channel)

## Example


    build:
        after-steps:
         - wouter/irc-notify:
            server: irc.freenode.net
            port: 6667
            nickname: yournickname
            channel: yourchannel

