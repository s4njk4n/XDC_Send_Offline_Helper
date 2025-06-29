# Tool for sending XDC offline

Can be accessed here: <a href="https://s4njk4n.github.io/XDC_Send_Offline_Helper/" target="_blank">https://s4njk4n.github.io/XDC_Send_Offline_Helper/</a>

Designed to work as the ONLINE half of the system for offline transactions. Simple to use via a mobile phone browser. You can save the bookmark on your mobile web browser or even "Save to Homescreen" on iPhones to save it as a webapp with its own desktop icon on your phone. It is set to use the XDC logo for the icon on your phone in this case.

General information on XDC Network Send-Offline-Functionality can be found here: <a href="https://medium.com/xinfin/send-offline-functionality-sof-a-secure-way-to-transact-xdc-coins-3734eaa81365" target="_blank">https://medium.com/xinfin/send-offline-functionality-sof-a-secure-way-to-transact-xdc-coins-3734eaa81365</a>

## To use this send offline helper:
- Specify an RPC (if you want to use a different one to the default Ankr one specified). You can find a list of current public XDC RPCs at <a href="https://chainlist.org/chain/50" target="_blank">https://chainlist.org/chain/50</a>
- Enter the XDC address you are sending from. Page accepts both 0x and xdc prefix formats. Then press "Get Transaction Parameters".
- You will then be presented with the "Gas Limit Suggestion", "Nonce", and "Suggested Gas Price". These are the numbers to use in your offline transaction builder (the OFFLINE half of the Send Offline Functionality).
- For ease-of-use it will also show the "XDC Balance" of the address so you dont need to separately look it up on a block explorer.
- Build the transaction with your offline transaction builder.
- Once completed/signed on the OFFLINE device, you just need to get the signed transaction data into the "Broadcast Signed Transaction" box at the bottom of the Send Offline Helper page we created.
- One way to do this is to manually enter it.
- A simpler way, if your offline transaction builder presents a QR code, is to just point your camera at the QR code, THEN press the "Scan QR Code" button. If it has been scanned, you will see your same transaction populate the box in the Send Offline Helper.
- Then you just press the "Broadcast Transaction" button and you're done.
- After sending your transaction, you will see a confirmation show up at the bottom of the screen, along with a URL linking directly to the block-explorer page for the transaction you have just done. This once again just simplifies the process by not needing to navigate the explorer to find it.

### Notes:
- If your QR scan did not work, you can manually turn off the scanner by pressing the red "Stop Scanner" button that has appeared at the bottom of the page.
