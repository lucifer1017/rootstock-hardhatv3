# rootstock-hardhatv3

This repository provides a minimal, no-frills workflow to deploy smart contracts to Rootstock using **Hardhat Ignition**.

---

## Quick steps

1. **Clone the repo**

```bash
git clone https://github.com/lucifer1017/rootstock-hardhatv3.git
cd rootstock-hardhatv3
```

2. **Install dependencies**

```bash
npm install
```

3. **Add your smart contracts**

Put your contract files inside the `contracts/` folder (e.g., `MyToken.sol`).

4. **Create the Ignition deployment module**

Inside `ignition/modules/` create a TypeScript deployment file with the **same base name** as your deployment (for example `MyToken.ts`). Use the existing `ignition/modules/Counter.ts` as a reference/example.

> The deployment file **must** have a `.ts` extension and live in `ignition/modules/`.

5. **Fill `.env`**

Populate the `.env` file with the correct parameters for your network and keys.

6. **Save everything, then run the deploy**

Assuming your deployment file is `Token.ts`, run:

* For testnet:

```bash
npx hardhat ignition deploy ignition/modules/Token.ts --network rskTestnet
```

* For mainnet:

```bash
npx hardhat ignition deploy ignition/modules/Token.ts --network rskMainnet
```

---


