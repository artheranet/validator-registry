# Public validator registry

A validator can choose to display its information to the public by creating a public `.json` file and registering its URL in the Arthera validator info contract deployed at `0x000000000000000000000000000000000000Aa05`

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

Once you have the file, create a Pull Request to this repository and commit your file here. Give it any name you want.

Get the Raw URL for the uploaded file (e.g. `https://github.com/artheranet/validator-registry/raw/main/genesis-validator.json`), fire up the Arthera Wallet, open up your validator wallet and .... 
