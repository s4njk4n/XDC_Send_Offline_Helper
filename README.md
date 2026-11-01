# XDC Send Offline Helper

The online half of XDC's **Send Offline** method: look up what your offline wallet needs, then scan and broadcast the transaction it signs. Your private key never comes near this page. It's designed for phones.

**[Open the Send Offline Helper →](https://xdcoutpost.xyz/XDC_Send_Offline_Helper/?utm_source=github)**

Part of [XDC Outpost](https://xdcoutpost.xyz/?utm_source=github-send-offline) · Free, runs in your browser · ⭐ Star the repo if it helps you.

New to sending offline? XinFin's [guide to Send Offline Functionality](https://medium.com/xinfin/send-offline-functionality-sof-a-secure-way-to-transact-xdc-coins-3734eaa81365) explains the whole method.

## How it works

| Step | Where | What happens |
|---|---|---|
| 1. Get transaction details | This page | Tap **Scan** to read the sending address from your offline wallet's QR code (plain addresses and payment links both work), or type it in. You get the **nonce**, **gas price** (in Gwei and wei) and a **gas limit** suggestion, each with a Copy button, plus the address's **balance**. |
| 2. Build and sign | Your offline device | Build the transaction with those values and sign it. Most offline builders show the result as a QR code. |
| 3. Scan and broadcast | This page | Tap **Scan QR code** and point your camera at the offline device, or paste the signed transaction. **Check the summary**, then tap **Broadcast transaction**. |

### Check before you broadcast
Broadcasting can't be undone, so after you scan or paste, the page reads the signed transaction itself and shows:
- the **recipient** and **amount** (XDC transfers and XRC-20 token transfers)
- the **maximum fee**
- the **nonce**, and whether it matches step 1
- the **network** it was signed for

It warns you if:
- the nonce is already used, or too high
- it was signed for testnet
- the gas price is below the current network price
- the amount plus fee is more than the balance
- you scanned an address instead of a transaction

After broadcasting you get the transaction hash, a Copy button and a link to XDCScan.

### Gas limit
- **21,000** for a plain XDC transfer (25,000 if that fails)
- **60,000** for an XRC-20 token transfer

The nonce already allows for transactions you've sent that haven't been confirmed yet.

## Tips

- **Add it to your home screen.** On iPhone, tap Share → **Add to Home Screen**. On Android, open the browser menu → **Add to Home screen**. It opens like an app with the XDC icon.
- **Camera not working?** Allow camera access for the site (on iPhone: Settings → Safari → Camera). You can always paste the signed transaction instead.
- **Nothing secret is entered here.** Your address and signed transaction become public on chain anyway. The private key stays on your offline device.
- **Network settings:** the default RPC is `https://rpc.plugin.global/xdcmainnet`. To use another, open **Network settings** on the page. Other public XDC RPCs are listed on [Chainlist](https://chainlist.org/chain/50).

## How it's built

Plain HTML and JavaScript. The QR decoder ([jsQR](https://github.com/cozmo/jsQR) 1.4.0) is stored in this repo at a fixed version (`vendor/`), not loaded from a CDN. Amounts are calculated exactly, with no rounding.

## Contact

Questions, bugs or ideas: open a [GitHub issue](https://github.com/s4njk4n/XDC_Send_Offline_Helper/issues), or message me on [Telegram](https://t.me/s4njk4n) or [X](https://x.com/s4njk4n).

[MIT License](LICENSE). Provided as-is, without warranty. Always check a transaction's details before broadcasting it.
