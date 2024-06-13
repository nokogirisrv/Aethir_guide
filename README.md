# Running on the Aethir Node Testnet (Using the Ubuntu CLI)

## Specifications for Installing/Running a Node
- 64MB RAM
- 1 X86 CPU Core @ 2.1GHz
- 10 GB Disk Space
- 10Mbps Internet Connection

### Download in One of Two Ways

#### 1-1 Go to the Homepage to Download the CLI File, or Use:
Go to the client download site.

#### 1-2 You Can Also Download It from the VPS Terminal:
Note that the address and version may change or disappear. How to find a new URL:
```bash
wget https://aethir-checker-client-new.s3.ap-southeast-1.amazonaws.com/na/AethirCheckerCLI-linux-1.0.1.8-na.tar.gz
```
Download it from the homepage and upload it to your VPS directly (SFTP, etc.). Alternatively, you can find the address on the homepage and download it using `wget` as shown above.

### After That, Unzip It:
```bash
tar -xvf AethirCheckerCLI-linux-1.0.1.8.tar.gz
```
### Install the Screen:
```bash
sudo apt update
sudo apt install screen
```
### Create a Screen:
```bash
screen -S Aethir
```
### Navigate to the Folder:
```bash
cd AethirCheckerCLI-linux-1.0.1.8-na
```
**Notifications:** Aethir downloads seem to be downloaded close to where you are (AWS), so if you get an error that the end of the folder name may be different, check the actual folder name and enter the command. – Thanks to yaboi for the report.

### This is a New Command Since 1.0.1.7:
```bash
sudo ./install.sh
```
### Run:
```bash
sudo ./AethirCheckerCLI-1.0.1.8
```
Please accept the Terms of Service before continuing. Press `y` to continue, `n` to exit. Press `v` to read the Terms of Service.

### Do You Agree to the Terms?
Enter `Y`.

### Create a Wallet by Entering the Following:
```bash
aethir wallet create
```
Check your current private key and current public key and enter them in a safe place.

### To Import an Existing Wallet:
```bash
aethir wallet import
```
Enter your existing private key.

### Go to the Homepage and Connect/Sign Your Wallet
If the node exists, you will be taken to the dashboard.

### In the License Dashboard, Tap the Delegate Button
Enter your current public key in the address field and press Delegate. The wallet that appears will authorize the transaction.

### Return to the Terminal and Type the Following:
```bash
aethir license list --pending
```
The wallets with NFTs will be listed.

### Select All Licenses for the Wallet by Entering:
```bash
aethir license approve --all
```
License operation approve success. Approved. You have 1 delegated license, 0 pending.

When prompted, it is successfully selected.

### You Should See “Working” Appear in Your Dashboard

You can also check the running status in the terminal with the following command:
```bash
aethir license list --working
```
### License Summary Commands:
```bash
aethir license summary
```
### Before Exiting the Terminal, Press the Following Keyboard Key to Minimize the Screen:
`Ctrl+A+D`

Is the node working but giving 0 rewards? You’ll start earning around 24-48 hours after working.

## Find the URL When It’s Updated
When a new update is posted and I want to find the address, you go to [https://app.aethir.com](https://app.aethir.com).

Just hover over the CLI for Linux and copy the right-click link address! The folder may have been renamed, so check the actual folder and enter the command.

## Server Error Occurs, Client Close. If Prompted?
If you get an error like the image above Press `Ctrl+C` to stop. Go back here and restart the server, then the client, and the pending should start again.
```
