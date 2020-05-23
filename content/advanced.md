+++
title = "Advanced"
description = "Hugo, the world’s fastest framework for building websites"
date = "2019-02-28"
aliases = ["about-us","about-hugo","contact"]
author = "Hugo Authors"
+++


## Getting the CLI Wallet

### LINUX
Download the Linux 64-bit command line client and extract it
```
wget https://github.com/wownero/wownero/releases/download/v0.8.0.0/wownero_Linux_v0.8.tar.xz
tar -xf wownero_Linux_v0.8.tar.xz
cd wownero_Linux_v0.8
```

### MACOS
Download the Mac command line client and extract it
```
wget hhttps://github.com/wownero/wownero/releases/download/v0.8.0.0/wownero_macOS_v0.8.dmg
double-click wownero_macOS_v0.8.dmg and drag folder to desired destination
open wownero folder
```

### WINDOWS
Download the Mac command line client and extract it
```
wget https://github.com/wownero/wownero/releases/download/v0.8.0.0/wownero_win64_v0.8.zip
unzip wownero_win64_v0.8.zip
cd wownero_win64_v0.8
```

## Run the Wownero daemon
It will sync with the network and display the message "You are now synchronized with the network. You may now start wownero-wallet-cli" when it is completely up to date with the network

### LINUX/MAC
```
./wownerod
```
### WINDOWS
```
wownerod.exe
```


## Run the CLI Wallet
The job of the Wownero daemon is to monitor the network for new transactions. You now need to open a new terminal window and run the Wownero command line wallet, which will communicate with the Wownero daemon that you've just stared.

### LINUX/MAC
```
./wownero-wallet-cli
```
### WINDOWS
```
wownero-wallet-cli.exe
```
Follow the instructions displayed to create a new wallet. When told the 25 word SEED, write this down on paper and keep it in a very safe place. Even if you forget your passwords, the 25 word SEED can be used to recreate your wallet from any machine and have complete control over your Wownero funds. Sample output from the Wownero wallet is below:

```
Specify wallet file name (e.g., MyWallet). If the wallet doesn't exist, it will be created.
Wallet file name (or Ctrl-C to quit): testwallet
No wallet found with that name. Confirm creation of new wallet named: testwallet
(Y/Yes/N/No): Y
Generating new wallet...
Enter a password for your new wallet:  ********
Confirm Password: ********
List of available languages for your wallet's seed:
0 : English
1 : Spanish
2 : German
3 : Italian
4 : Portuguese
5 : Russian
6 : Japanese
Enter the number corresponding to the language of your choice: 0
Generated new wallet: Wo3MWeKwtA918DU4c69hVSNgejdWFCRCuWjShRY66mJkU2Hv58eygJWDJS1MNa2Ge5M1WjUkGHuLqHkweDxwZZU42d16v94mP
View key: 005c98c3db115140289bd0dfad97f910e6eeb5e8e12d02fdd4ab2373fbe9110a
**********************************************************************
Your wallet has been generated!
To start synchronizing with the daemon, use "refresh" command.
Use "help" command to see the list of available commands.
Always use "exit" command when closing wownero-wallet-cli to save your
current session's state. Otherwise, you might need to synchronize
your wallet again (your wallet keys are NOT at risk in any case).


PLEASE NOTE: the following 25 words can be used to recover access to your wallet. Please write them down and store them somewhere safe and secure. Please do not store them in your email or on file storage services outside of your immediate control.

locker welders womanly lodge gumball selfish altitude dewdrop
terminal nagged exit acquire hookup ashtray wobbly nineteen
duration duties javelin patio baffles ambush bamboo bite nineteen
**********************************************************************
Starting refresh...
Refresh done, blocks received: 0
Balance: 0.000000000000, unlocked balance: 0.000000000000
Background refresh thread started
```

Type "address" to see your public wallet address. You can give this address to anyone, and they will be able to send you Wownero. However, NEVER give anyone your 25 word SEED.
```
[wallet Wo3MWe]: address
Wo3MWeKwtA918DU4c69hVSNgejdWFCRCuWjShRY66mJkU2Hv58eygJWDJS1MNa2Ge5M1WjUkGHuLqHkweDxwZZU42d16v94mP
```

## Generate Wow with CLI

There will be no support for pools or mining software in the upcoming fork. 

To solo generate, follow these directions:

### Windows 10

1. Download `wownero_win64_v0.X.X.X.zip` archive file from [release page](https://github.com/wownero/wownero/releases/latest) and [extract files](https://support.microsoft.com/en-us/help/4028088/windows-zip-and-unzip-files).
2. Open [Command Prompt](https://www.howtogeek.com/235101/10-ways-to-open-the-command-prompt-in-windows-10/) and [change directory](https://www.digitalcitizen.life/command-prompt-how-use-basic-commands) to location of extracted files.
3. Run `wownerod.exe`and wait a few minutes until there is **SYNCHRONIZED OK** message.
4. Open new tab with `Ctrl + t`, run `wownero-wallet-cli.exe`, name your new wallet, enter a password, select a language,  write down and save the 25-word [Mnemonic Seed](https://web.getmonero.org/resources/moneropedia/mnemonicseed.html) somewhere safe.
5. To enable background mining while computer is idle and not on battery, type `yes`.
6. Copy your wallet's address, type `exit` and `exit` to close tab.
7. To start mining, in `wownerod.exe`, type and paste `start_mining YOUR_ADDRESS 2`. The number "2" is for two threads and the value could be increased or decreased depending on the number of cores in your CPU.
8. To see mining hash rate, type `status`. This will show you height, mining, and network information.
9. To stop mining, enter command `stop_mining`.
10. To exit Wownero, type `save` and `exit` and then `exit` again to close window.

### Linux
1. Download `wownero_Linux_v0.X.X.X.tar.bz2` archive file from [release page](https://github.com/wownero/wownero/releases/latest) and [untar files](https://www.howtogeek.com/50093/unzip-bunzip2-and-untar-those-tar-gz-or-tar-bz2-files-in-one-step/).
2. Open [Terminal](https://www.howtogeek.com/140679/beginner-geek-how-to-start-using-the-linux-terminal/) and [change directory](https://help.ubuntu.com/community/UsingTheTerminal#File_.26_Directory_Commands) to location of untared files.
3. Run `./wownerod`and wait a few minutes until there is **SYNCHRONIZED OK** message.
4. Open new tab with `Shift + Ctrl + t`, run `./wownero-wallet-cli`, name your new wallet, enter a password, select a language,  write down and save the 25-word [Mnemonic Seed](https://web.getmonero.org/resources/moneropedia/mnemonicseed.html) somewhere safe.
5. To enable background mining while computer is idle and not on battery, type `yes`.
6. Copy your wallet's address, type `exit` and `exit` to close tab.
7. To start mining, in `wownerod`, type and paste `start_mining YOUR_ADDRESS 2`. The number "2" is for two threads and the value could be increased or decreased depending on the number of cores in your CPU.
8. To see mining hash rate, type `status`. This will show you height, mining, and network information.
9. To stop mining, enter command `stop_mining`.
10. To exit Wownero, type `save` and `exit` and then `exit` again to close terminal.

### MacOS

Same as Linux
