# Pump Trading Assistant

- A Pumpfun Pvp trading tool based on Electron, supporting token creation, buying, selling, and pumping functionalities.
- Free API without pumpportal high fees: http://154.201.73.182:3456/api/trade-local
- Free API has been attacked and is currently unavailable.
# No reselling allowed!!!

## Screenshots
<img width="1280" alt="image" src="https://github.com/user-attachments/assets/00efb7f1-72a1-449d-800f-fb3ada5386bc">
<img width="1280" alt="image" src="https://github.com/user-attachments/assets/e6b21f84-90d2-45f1-a24b-7af983b957fd">

## Project Structure
```
Pumpfun_pvp_tools/
├── src/
│   ├── create.js      # Token creation related functionality
│   ├── sell.js        # Token selling related functionality
│   ├── lapan.js       # Pumping related functionality
│   ├── monitor.js     # Transaction monitoring functionality
│   ├── tradem.js      # Trade management functionality
│   ├── wallet.js      # Wallet management functionality
│   ├── electron.js    # Main Electron process
│   └── index.html     # Main interface
├── .env               # Environment variables configuration
├── .env.example       # Environment variables example
├── package.json       # Project configuration file
└── README.md          # Project documentation
```
### Main Modules Description
- **create.js**: Implements token creation and initial buying functionality
- **sell.js**: Implements bulk token selling functionality
- **lapan.js**: Implements automatic pumping strategy
- **monitor.js**: Implements real-time transaction monitoring
- **tradem.js**: Handles trade-related core logic
- **wallet.js**: Implements wallet management, fund distribution, and collection
- **electron.js**: Main process of Electron application
- **index.html**: HTML implementation of the application interface

## Main Features
### 1. Token Trading
- Create and buy tokens
- One-click token selling
- Automatic pumping feature
- Real-time transaction monitoring

### 2. Wallet Management
- Supports multi-wallet management (creating wallets 1-5 and pumping wallets 1-100)
- One-click wallet creation
- Bulk SOL distribution
- Bulk SOL collection

### 3. Real-time Monitoring
- Real-time display of transaction information
- Display of buy/sell data
- Supports automatic monitoring of new tokens
- Real-time display of trading progress

## Installation Instructions

1. Clone the project
2. Install dependencies
3. Configure .env file
4. Run the project

```bash
# Clone the project
git clone https://github.com/vnxfsc/Pumpfun_pvp_tools
# Navigate to the project directory
cd Pumpfun_pvp_tools

# Install dependencies
npm install

# Run the project
 npm start
```
## Environment Configuration
Create a `.env` file in the project root directory with the following necessary parameters:
```env
# RPC node configuration
HELIUS_RPC_URL=Your Helius RPC URL
# Main wallet configuration (for token creation)
WALLET_PRIVATE_KEY_1=Main wallet private key
# Buying wallet configuration (wallets 2-5 are auto-generated)
WALLET_PRIVATE_KEY_1_AMOUNT=0
WALLET_PRIVATE_KEY_2_AMOUNT=3.00
WALLET_PRIVATE_KEY_3_AMOUNT=3.50
WALLET_PRIVATE_KEY_4_AMOUNT=3.30
WALLET_PRIVATE_KEY_5_AMOUNT=3.00
# Pumping wallet configuration (wallets 1-100 are auto-generated)
WALLET_LAPAN_KEY_1=
...
WALLET_LAPAN_KEY_100=
```
## Usage Guide
### 1. Wallet Preparation
- In the wallet management page, use the "One-click generate" feature to create buying wallets (2-5) and pumping wallets (1-100)
- Use the "Distribute" feature to distribute an appropriate amount of SOL to each wallet

### 2. Create Tokens
- In the create configuration page, set the buying amounts for each buying wallet
- Return to the homepage and click the "Create and Buy" button
- Wait for the transaction to complete; the system will automatically record the token address

### 3. Pumping Operations
- Set the pumping parameters on the homepage:
   * Delay time: 2-3 seconds (adjustable)
   * Number of wallets used per operation: 1-3 (adjustable)
   * Amount per transaction: 0.1-0.3 SOL (adjustable)
- Click the "Pump" button to start automatic pumping
- You can stop pumping at any time by clicking the button again
### 4. Selling Operations
- Ensure the token address is correctly displayed
- Click the "Sell" button
- The system will automatically sell tokens from all wallets

### 5. Fund Recovery
- After the transaction, use the "Collect" feature on the wallet management page
- Collect all SOL from all wallets to the main wallet

## Notes
1. Security Recommendations
   - Keep the main wallet private key secure
   - Regularly back up generated wallet private keys
   - Do not disclose private keys to others

2. Operational Recommendations
   - Ensure the main wallet has enough SOL
   - Reserve enough gas fees when distributing SOL
   - Test with small transactions before using
   - Regularly check wallet balances
3. Network-related
   - Use a reliable RPC node
   - Maintain a stable network connection
   - Avoid frequent large transactions
## Technical Support
- If you encounter any issues, please submit an issue
- Contributions to improve the code are welcome via pull requests
- Community Group: [Buff Community](https://t.me/chainbuff)
- Community Group: [Utopia Community](https://t.me/xiaojiucaiPC)
## Donations
- Solana address: 8nMFEMb1MXE8BjTBuAYMuy1mYtwwKNQcm937Y9yy9eHu
## Disclaimer
  This tool is for learning and research purposes only. Any consequences resulting from the use of this tool are the sole responsibility of the user.
## License
  MIT License
