We've used `list` to see _all_ the [[Git Config]]uration values, but the `get` sub[[command]] is useful for getting a single value.

```sh
git config get <section>.<keyname>`
```

Keys are in the format `<section>.<keyname>`. For example:

- `user.name`
- `webflyx.ceo`

## Caso de uso

Use the `get` subcommand to get the value of the `webflyx.valuation` key from your local Git configuration.

en caso se desea tambien se puede [[Remove a Section]]