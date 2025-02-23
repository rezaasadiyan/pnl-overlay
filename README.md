# Solana PnL Overlay

A sleek, futuristic overlay designed for streamers to display their Solana (SOL) wallet balance and profit/loss (PnL) in real-time. Built with HTML, CSS, and JavaScript, this overlay fetches data from the Solana blockchain using the Helius RPC API and updates every 5 seconds.

## Features
- Displays current wallet balance in SOL.
- Shows real-time PnL compared to the initial balance at page load.
- Color-coded PnL: green for profit, red for loss, white for neutral.
- Semi-transparent background with a customizable GIF overlay for a modern look.
- Signature watermark ("Made by @rezacoded") included.

## Prerequisites
- A Solana wallet address to monitor.
- An API key from [Helius](https://helius.xyz/) (or another Solana RPC provider).
- A web browser to run the overlay (e.g., Chrome, Firefox).
- (Optional) A streaming software like OBS Studio to integrate the overlay.

## Setup Instructions

1. **Clone the Repository**

2. **Open the Project**
- Open the `index.html` file in a text editor (e.g., VS Code).

3. **Configure Your Wallet Address and API Key**
- In the `<script>` section of `index.html`, locate the following lines:
  ```
  const walletAddress = "YOUR_WALLET_ADDRESS_HERE";
  const RPC_URL = "https://mainnet.helius-rpc.com/?api-key=YOUR_API_KEY_HERE";
  ```
- Replace `YOUR_WALLET_ADDRESS_HERE` with your Solana wallet address (e.g., `GfXQesPe3Zuwg8JhAt6Cg8euJDTVx751enp9EQQmhzPH`).
- Replace `YOUR_API_KEY_HERE` with your Helius API key. Sign up at [Helius](https://helius.xyz/) to get one if you don’t have it. (its free)

4. **Test the Overlay**
- Open `index.html` in a web browser to verify it works. You should see your wallet balance and PnL updating every 5 seconds.

5. **Integrate with Streaming Software**
- Open your streaming software (e.g., OBS Studio).
- Add a new "Browser" source.
- Set the URL to the local file path of `index.html` (e.g., `http://127.0.0.1:5500/pnl.html`).
- Adjust the size and position of the overlay as needed.

6. **Customize (Optional)**
- Replace `giphy.gif` in the `.overlay::before` CSS rule with your own GIF or image URL for a personalized background. (images and gifs both work, just make sure to change the url of the image/gif source)
- Modify the styles in the `<style>` section to tweak the design (e.g., colors, fonts, size).

## Usage
- Once configured, the overlay will automatically fetch and display your wallet balance and PnL.
- The PnL is calculated as the difference between the current balance and the initial balance when the page loads.
- Refresh the page to reset the initial balance and start tracking PnL from a new baseline.

## Troubleshooting
- **"Error" Displayed**: Check your wallet address and API key for typos. Ensure your API key is active and hasn’t exceeded its rate limit.
- **No Updates**: Verify your internet connection and that the RPC URL is correct.
- **Background Image Issue**: Ensure `giphy.gif` exists in the project folder or replace it with a valid URL.

## Contributing
Feel free to fork this repository, make improvements, and submit a pull request! Suggestions for additional features or bug fixes are welcome.

## Credits
- Made by [@rezacoded](https://twitter.com/rezacoded).
- Powered by [Helius RPC](https://helius.xyz/).

## License
This project is open-source and available under the [MIT License](LICENSE).
