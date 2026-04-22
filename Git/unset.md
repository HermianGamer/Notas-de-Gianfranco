The `unset` sub[[command]] is used to _remove_ a [[Git Config]] value. For example:

```sh
git config unset <section>.<keyname>`
```

## Caso de uso

Remove the `webflyx.cto` key from your local Git configuration, and verify that it was removed.

Try using `unset` to remove the entire `webflyx` section. it cant be done, it need a key.