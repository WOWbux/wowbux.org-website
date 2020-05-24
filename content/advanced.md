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
This is the command line wownero wallet. It needs to connect to a wownero
daemon to work correctly.

Wownero 'Hallucinogenic Hypnotoad' (v0.8.0.0-release)
Logging to ./wownero-wallet-cli.log
Specify wallet file name (e.g., MyWallet). If the wallet doesn't exist, it will be created.
Wallet file name (or Ctrl-C to quit): fluffydoge
No wallet found with that name. Confirm creation of new wallet named: fluffydoge
  (Y/Yes/N/No): Yes
Generating new wallet...
Enter a new password for the wallet: 
Confirm password: 
List of available languages for your wallet's seed:
If your display freezes, exit blind with ^C, then run again with --use-english-language-names
0 : Deutsch
1 : English
2 : Español
3 : Français
4 : Italiano
5 : Nederlands
6 : Português
7 : русский язык
8 : 日本語
9 : 简体中文 (中国)
10 : Esperanto
11 : Lojban
Enter the number corresponding to the language of your choice: 1
Generated new wallet: Wo534GxY9infzdbWYqkwMwXe4dbJiXMDmZM3Hne3kKYQ6uHNEfKN6euGHhMKLvdPKBe3TTvVn2bK8Rx2akym2gsG38cMK477x
View key: 0862e2836066ca7b56a1f4715e379598af485a18c9563671b893a4722a04c101
**********************************************************************
Your wallet has been generated!
To start synchronizing with the daemon, use the "refresh" command.
Use the "help" command to see a simplified list of available commands.
Use the "help_advanced" command to see an advanced list of available commands.
Use "help_advanced <command>" to see a command's documentation.
Always use the "exit" command when closing wownero-wallet-cli to save 
your current session's state. Otherwise, you might need to synchronize 
your wallet again (your wallet keys are NOT at risk in any case).


NOTE: the following 25 words can be used to recover access to your wallet. Write them down and store them somewhere safe and secure. Please do not store them in your email or on file storage services outside of your immediate control.

copy rays orders nirvana skew inundate inquest beer
lair likewise hills unjustly yoyo journal basin gourmet
ringing jabbed hacksaw juggled vats divers likewise muffin vats

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

To solo mine, follow these directions:

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



## Generate Wow with xmrig
How to mine wownero? You can use xmrig to mine wow on pools.

### Install xmrig
Get xmrig from [xmrig releases](https://github.com/xmrig/xmrig/releases)

### Run xmrig
Run xmrig with the following flags (don't forget to set your address!)
```
./xmrig -o pool.wowne.ro:7777 -u Wo3MWeKwtA918DU4c69hVSNgejdWFCRCuWjShRY66mJkU2Hv58eygJWDJS1MNa2Ge5M1WjUkGHuLqHkweDxwZZU42d16v94mP -p fluffydoge -a rx/wow --cpu-priority 0
```

