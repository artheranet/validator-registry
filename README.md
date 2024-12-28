# Public validator registry

A validator can choose to display its information to the public by creating a public `.json` file and registering its URL in the Arthera validator info contract as explain below.

## How to publish your validator info

The first step is to create a `.json` file with the following format:

```json
{
  "name": "genesis",
  "logoUrl": "",
  "website": "https://arthera.net",
  "contact": "dev@arthera.net"
}
```

Once you have the file, create a Pull Request to this repository and commit your file here.

### Naming rules

- Only in lower case
- Starting with `genesis-` if it's genesis node
- Following your validator name

### Remix usage

- Get the Raw URL for the uploaded file (e.g. `https://github.com/artheranet/validator-registry/raw/main/genesis-validator.json`)
- Fire up [Remix](https://remix.ethereum.org/)
- Copy the [ABI](https://github.com/bertux/arthera-abi/blob/main/abi/ValidatorInfo.json) in a new file you have to name ValidatorInfo.abi
- In the left panel click on the Ethereum logo to reach `Deploy & run transactions`
- Open up your validator wallet
- In `Environment` list select `Injected provider`
- In `Account` list select your validator wallet and wait to see the expected balance amount
- In `Load contract from Address` paste `0x000000000000000000000000000000000000Aa05`
- Click `At Address` button at the left of the pasted address
- Click `OK` button to confirm
- Click `>` under `Deployed Contracts`
- At the right of `setInfo` button paste the Raw URL of the first step
- Click `setInfo` button to send the transaction

[Documentation](https://docs.arthera.net/build/developing-sc/system-contracts/ValidatorInfo#setinfo)
