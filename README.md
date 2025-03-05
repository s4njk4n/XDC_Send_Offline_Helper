# Tool for sending XDC offline

Can be accessed here: [https://s4njk4n.github.io/XDC_Send_Offline_Helper/](https://s4njk4n.github.io/XDC_Send_Offline_Helper/)

Designed to work as the ONLINE half of the system for offline transactions. Simple to use via a mobile phone browser. You can save the bookmark on your mobile web browser or even "Save to Homescreen" on iPhones to save it as a webapp with is own desktop icon on your phone. It is set to use the XDC logo for the icon on your phone in this case.

General information on XDC Network send offline functionality can be found here: [https://medium.com/xinfin/send-offline-functionality-sof-a-secure-way-to-transact-xdc-coins-3734eaa81365
](https://medium.com/xinfin/send-offline-functionality-sof-a-secure-way-to-transact-xdc-coins-3734eaa81365)

## To use this send offline helper:
- Specify an RPC if you want to use a different one to the default Ankr one specified.
- Enter the XDC address you are sending from. Page accepts both 0x and xdc prefix formats. Then press "Get Transaction Parameters".
- You will then be presented with the "Gas Limit Suggestion", "Nonce", and "Suggested Gas Price". These are the numbers to use in your offline transaction builder (the OFFLINE half of the Send Offline Functionality).
- Build the transaction with your offline transaction builder.
- Once completed/signed on the OFFLINE device, you just need to get the signed transaction data into the "Broadcast Signed Transaction" box at the bottom of the Send Offline Helper page we created.
- One way to do this is to manually enter it.
- A simpler way, if your offline transaction builder presents a QR code, is to just point your camera at the QR code, THEN press the "Scan QR Code" button. If it has been scanned, you will see your same transaction populate the box in the Send Offline Helper.
- Then you just press the "Broadcast Transaction" button and you're done.

### Notes:
- If your QR scan did not work, you can manually turn off the scanner by pressing the red "Stop Scanner" button that has appeared at the bottom of the page.
