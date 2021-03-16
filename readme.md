![box-img-lg-template](https://user-images.githubusercontent.com/218949/63261050-6ce11600-c27a-11e9-9355-1ee226b4497c.png)

# Svelte Truffle Box
A Truffle box using [SvelteJS](https://svelte.technology/), [TailwindCSS](https://tailwindcss.com/), and [Rollup](https://rollupjs.org/).

This box contains everything you need to start building a DApp. However, you may want to replace the `svelte-web3` package due to unknown maintenance status (See [Web3](#web3)).

## Truffle Box

A [truffle box](http://truffleframework.com/boxes/) is a seed project for building a truffle DApp.

## Setting up

1. Install truffle and an ethereum client. For local development, try Ethereum TestRPC.
    ```javascript
    npm install -g truffle
    ```

2. Download box.
    ```bash
    truffle unbox maxwellfortney/svelte-tailwind-box
    ```

4. Run an Ethereum RPC. For simplicity and development we will be using [Ganache](https://www.trufflesuite.com/ganache).

7. Compile and migrate the contracts after authenticating your account on the blockchain (i.e. restoring from seed in MetaMask).
    ```bash
    truffle compile
    truffle migrate
    ```

You're ready to go!

## Usage

Truffle and Svelte files are in their usual place [according to the docs](https://github.com/trufflesuite/truffle-init-default)

Ensure your Ethereum testnet is running, then deploy your contracts:

```bash
truffle deploy
```

Log in to metamask by importing any of the Ganache Wallet's private keys. Then, run the dev task to have the code updated in realtime as you develop:
```bash
truffle compile
npm run dev
```

## Publishing

To produce your production dApp, run the build task:
```bash
npm run build
```

This will publish your completed DApp to the folder `./public/build`

## Testing
Be sure you've compiled your contracts before running the tests, or you'll get file not found errors.

```bash
truffle test
```

## Releasing
To build the application for production, use the build command. A production build will be in the `./dist` folder.

```javascript
npm run build
```

## Web3
This project is comes with `svelte-web3`, however I'm unsure of the maintainability of the package. If anyone would like to implement a better Web3  implementation please feel free to submit a PR!

## Contributions

Feel free to submit a PR, or an issue, and I will try my best to address it. 

## Credits
Inspiration, images, and most of the readme is from here [svelte-box](https://github.com/antony/svelte-box)

Basic svelte project [svelte-template](https://github.com/sveltejs/template)
