## Getting Started

To work with this project, you'll need to set up an Avalanche subnet, deploy smart contracts, and test your setup. Follow the steps below to get everything running smoothly.

### 1. Install `avalanche-cli`

`avalanche-cli` is a command-line tool for managing Avalanche blockchains.

#### Using npm (Node Package Manager)

1. **Ensure Node.js is Installed**:
   - Install Node.js from [nodejs.org](https://nodejs.org/). Check your installation with:
     ```sh
     node -v
     ```

2. **Install `avalanche-cli` Globally**:
   - Open your terminal and run:
     ```sh
     npm install -g avalanche-cli
     ```
   - This installs `avalanche-cli` globally, allowing access from any directory.

3. **Verify Installation**:
   - Check that `avalanche-cli` is installed correctly:
     ```sh
     avalanche-cli --version
     ```

### 2. Create a Subnet

A subnet is a customized blockchain network on Avalanche.

1. **Create the Subnet**:
   - Run the following command to create a new subnet:
     ```sh
     avalanche-cli subnet create <subnet_name>
     ```
   - Replace `<subnet_name>` with your desired name for the subnet.

2. **Confirm Creation**:
   - Ensure the subnet was created successfully by checking the command output or using:
     ```sh
     avalanche-cli subnet list
     ```

### 3. Deploy the Subnet

Deploy the newly created subnet to the Avalanche network.

1. **Deploy the Subnet**:
   - Execute:
     ```sh
     avalanche-cli subnet deploy <subnet_name>
     ```
   - Replace `<subnet_name>` with the name you used in the creation step.

2. **Verify Deployment**:
   - Check the deployment status by running:
     ```sh
     avalanche-cli subnet status <subnet_name>
     ```

### 4. Connect MetaMask to Your Custom Subnet

To interact with your custom subnet, connect MetaMask to it.

1. **Open MetaMask**:
   - Go to the MetaMask extension in your browser.

2. **Add a Custom Network**:
   - Navigate to `Settings` > `Networks` > `Add Network`.
   - Enter the details for your custom subnet (you'll need the RPC URL and Chain ID, which should be provided by the deployment process).

3. **Save and Switch**:
   - Save the network settings and switch to your new custom subnet.

### 5. Open and Deploy Smart Contracts

You’ll deploy ERC20 and Vault smart contracts to your subnet using Remix IDE.

1. **Open Remix IDE**:
   - Go to [Remix IDE](https://remix.ethereum.org/).

2. **Load Smart Contracts**:
   - Open `erc20.sol` and `vault.sol` files in Remix.

3. **Compile the Contracts**:
   - Use the Solidity compiler in Remix to compile both `erc20.sol` and `vault.sol`.

4. **Deploy the Contracts**:
   - Switch to the "Deploy & Run Transactions" tab.
   - Make sure you are connected to the custom subnet (MetaMask should handle this).
   - Deploy the compiled contracts to your subnet.

### 6. Test Your Setup

After deploying, it’s crucial to test everything to ensure it works as expected.

1. **Interact with Contracts**:
   - Use Remix or any other interface to interact with your deployed contracts.

2. **Verify Functionality**:
   - Check that the ERC20 token and vault functions operate correctly on your subnet.

3. **Debug as Needed**:
   - If you encounter issues, review the deployment logs, contract code, and MetaMask configurations.
