# channel

Channels bring external conversations in, for [Effect](https://effect.website). A channel
transport is how one external system, such as Slack, an email service, or a chat bridge, is
received from and replied to: it verifies and reads what the system sends, as events in the
system's conversations, and posts replies there.

| Package                                   | What it is                                      |
| ----------------------------------------- | ----------------------------------------------- |
| [`@amends-dev/channel`](packages/channel) | The contract every channel transport implements |

```sh
bun add @amends-dev/channel effect
```

The [contract's guide](packages/channel/README.md) describes its members and events, and how to
[write a transport](packages/channel/README.md#writing-a-transport).
[`@amends-dev/connection`](https://github.com/amends-dev/connection) installs transports as what an
integration gives its connections.

## Contributing

[CONTRIBUTING.md](CONTRIBUTING.md) covers setting up, the checks every change passes, and
releases. Report a vulnerability as [SECURITY.md](SECURITY.md) describes.

## License

[MIT](LICENSE)
