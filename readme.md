# is-wsl

> Check if the process is running inside [Windows Subsystem for Linux](https://msdn.microsoft.com/commandline/wsl/about) (Bash on Windows)

Can be useful if you need to work around unimplemented or buggy features in WSL. Supports both WSL 1 and WSL 2.

## Install

```sh
npm install is-wsl
```

## Usage

```js
import isWsl from 'is-wsl';

// When running inside Windows Subsystem for Linux
console.log(isWsl);
//=> true
```

### Disable `is-wsl`

Some tools break when trying to use binaries outside WSL.
In these cases you can disable `is-wsl` by setting the `DISABLE_IS_WSL`
environment variable.

```sh
DISABLE_IS_WSL=true
```

```js
import isWsl from 'is-wsl';

// When running inside Windows Subsystem for Linux
console.log(isWsl);
//=> false
```