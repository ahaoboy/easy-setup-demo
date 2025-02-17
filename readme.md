Demo for [easy-setup](https://github.com/easy-install/easy-setup)

## demo

cross-platform CI testing

```yml
strategy:
  matrix:
    os: [ubuntu-24.04, windows-latest, macos-14, macos-13]
runs-on: ${{ matrix.os }}
steps:
  - uses: ahaoboy/easy-setup@v1
    with:
      url: |-
        https://github.com/ahaoboy/txiki.js-build
        https://github.com/ahaoboy/easy-install/raw/refs/heads/main/dist-manifest/llrt.json
        https://github.com/ahaoboy/easy-install/raw/refs/heads/main/dist-manifest/quickjs-ng.json
  - name: test
    run: |
      which qjs
      which llrt
      which tjs
```