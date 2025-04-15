# NxInvalidEslintTypescript

This project is meant to show an error that accours when using `(await import(@nx/eslint-plugin)).configs['flat/typescript']` inside an `extends` field of an eslint config entry, while using ESLint's `defineConfig` function.

See the issue in the NX repo: https://github.com/nrwl/nx/issues/30725

- [ESLint Config Entry of Interest](https://github.com/xDivisionByZerox/nx-invalid-eslint-typescript/blob/5bae30bc0decb15e1b091b89c2d9a4022205305f/eslint.config.mjs#L13)
- [Console Error](https://github.com/xDivisionByZerox/nx-invalid-eslint-typescript/actions/runs/14464536635/job/40563738315#step:5:1)
- [The Line in the Preset that is the reason](https://github.com/nrwl/nx/blob/bc685ce3c522ab12a3cfa075fd7c0e879117981f/packages/eslint-plugin/src/flat-configs/typescript.ts#L33)

```json
{
  "files": ["**/*.ts", "**/*.tsx", , "**/*.cts", "**/*.mts"],
  // ----------------------------^
  // ...
}
```
