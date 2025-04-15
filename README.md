# NxInvalidEslintTypescript

This project is meant to show an error that accours when using `(await import(@nx/eslint-plugin)).configs['flat/typescript']` inside an `extends` field of an eslint config entry, while using ESLint's `defineConfig` function.

- [ESLint Config Entry of Interest](TODO_ADD_PERMA_LINK)
- [Console Error](TODO_ADD_LINK_WORKFLOW_RUN)
- [The Line in the Preset that is the reason](https://github.com/nrwl/nx/blob/bc685ce3c522ab12a3cfa075fd7c0e879117981f/packages/eslint-plugin/src/flat-configs/typescript.ts#L33)

```json
{
  "files": ["**/*.ts", "**/*.tsx", , "**/*.cts", "**/*.mts"],
  // ----------------------------^
  // ...
}
```
