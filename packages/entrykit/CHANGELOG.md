# @latticexyz/entrykit

## 2.2.17

### Patch Changes

- d5f4e1e: Bumped react-error-boundary dependency.
- 7385948: Renamed `deploy-local-prereqs` bin to `entrykit-deploy`, which now accepts an RPC URL so that you can deploy the EntryKit prerequisites to your chain of choice.

  ```
  RPC_URL=http://rpc.garnetchain.com pnpm entrykit-deploy
  ```

  This bin supports specifying the RPC URL via `RPC_URL`, `RPC_HTTP_URL`, `FOUNDRY_ETH_RPC_URL` environment variables or `FOUNDRY_PROFILE` if using `eth_rpc_url` in `foundry.toml`.

- ffefc8f: `CallWithSignature` module has been moved out of `@latticexyz/world-modules` and into its own package at `@latticexyz/world-module-callwithsignature`. This module is now installed by default during deploy as its needed by EntryKit.

  If you previously had this module installed in your MUD config, you can now remove it.

  ```diff
   export default defineConfig({
     tables: {
       ...
     },
  -  modules: [
  -    {
  -      artifactPath:
  -        "@latticexyz/world-modules/out/Unstable_CallWithSignatureModule.sol/Unstable_CallWithSignatureModule.json",
  -      root: true,
  -    },
  -  ],
   });
  ```

- Updated dependencies [94d82cf]
- Updated dependencies [589fd3a]
- Updated dependencies [7c3df69]
- Updated dependencies [dead80e]
- Updated dependencies [56e65f6]
- Updated dependencies [ffefc8f]
- Updated dependencies [7385948]
  - @latticexyz/world@2.2.17
  - @latticexyz/common@2.2.17
  - @latticexyz/protocol-parser@2.2.17
  - @latticexyz/world-module-callwithsignature@2.2.17
  - @latticexyz/config@2.2.17
  - @latticexyz/store@2.2.17
  - @latticexyz/paymaster@2.2.17

## 2.2.16

### Patch Changes

- @latticexyz/common@2.2.16
- @latticexyz/config@2.2.16
- @latticexyz/paymaster@2.2.16
- @latticexyz/protocol-parser@2.2.16
- @latticexyz/store@2.2.16
- @latticexyz/world@2.2.16
- @latticexyz/world-modules@2.2.16

## 2.2.15

### Patch Changes

- 971ffed: Initial, experimental release of EntryKit.
- Updated dependencies [9580d29]
- Updated dependencies [653f378]
- Updated dependencies [2d2aa08]
- Updated dependencies [09e9bd5]
- Updated dependencies [ba5191c]
- Updated dependencies [1b477d4]
- Updated dependencies [b819749]
- Updated dependencies [22674ad]
- Updated dependencies [9d71887]
- Updated dependencies [509a3cc]
- Updated dependencies [09536b0]
- Updated dependencies [88b9daf]
- Updated dependencies [275c867]
- Updated dependencies [a7625b9]
  - @latticexyz/config@2.2.15
  - @latticexyz/world@2.2.15
  - @latticexyz/common@2.2.15
  - @latticexyz/protocol-parser@2.2.15
  - @latticexyz/store@2.2.15
  - @latticexyz/paymaster@2.2.15
  - @latticexyz/world-modules@2.2.15
