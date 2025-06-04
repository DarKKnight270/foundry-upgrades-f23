# 🔁 Upgradeable Smart Contract Example (UUPS Proxy Pattern)

This repository demonstrates a simple implementation of **proxy-based upgradeable smart contracts** using the **UUPS pattern**, powered by **Foundry**.

It includes:
- ✅ Deployment of a logic contract (`BoxV1`)
- ✅ Deployment of an `ERC1967Proxy` pointing to `BoxV1`
- ✅ Upgrade to a new logic contract (`BoxV2`)
- ✅ Scripted deployment and upgrade via `broadcast`
- ✅ Integration with [Cyfrin/foundry-devops](https://github.com/Cyfrin/foundry-devops) for tracking deployments

---

## 📁 Structure

- `src/BoxV1.sol`: Initial logic contract (with state)
- `src/BoxV2.sol`: Upgraded logic contract (with extended logic)
- `script/DeployBox.s.sol`: Script to deploy `BoxV1` and proxy
- `script/UpgradeBox.s.sol`: Script to deploy `BoxV2` and upgrade the proxy
- `foundry.toml`: Foundry configuration with remappings and permissions

---

## 🚀 Deployment

Deploy the logic contract and proxy:
```bash
forge script script/DeployBox.s.sol:DeployBox --broadcast --rpc-url <YOUR_RPC_URL> --private-key <YOUR_PRIVATE_KEY> -vvvv
