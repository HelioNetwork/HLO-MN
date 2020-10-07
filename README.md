# Helio Coin Masternode Setup (Ubuntu 16.04 / 18.04)
This guide will assist you in setting up a Heliocoin Masternode on a Linux Server running Ubuntu 16.04 / 18.04

- [Heliocoin Masternode Setup](#heliocoin-masternode-setup)  
  	* [Requirements](#requirements) 
  * [Connecting to the VPS and installing the masternode script](#Connecting-to-the-VPS-and-installing-the-masternode-script)  
         [1. Log into the VPS with **root**](#1-log-into-the-vps-with-root)  
         [2. Git Installation](#2-git-installation)  
         [3. Clone MN setup script](#3-clone-mn-setup-script)  
         [4. Start MN setup script](#4-start-mn-setup-script)  
         [5. Copy Masternode Private Key](#5-copy-masternode-private-key-from-vps-console-window-and-pres-enter)
  * [Setup QT wallet](#setup-qt-wallet)  
         [1. Create new receiving address and copy it](#1-create-new-receiving-address-and-copy-it)  
	 [2. Send Collateral amount of Helio to copied address](#2-send-collateral-amount-of-helio-to-copied-address)  
	 [3. Get MN output and Set Masternode Configuration File](#3-open-console-get-mn-output-and-set-masternode-configuration-file-and-save-it)  
	 [4. Wait at least 15 confirmation of transaction](#4-wait-at-least-15-confirmation-of-transaction)  
         [5. Restart QT wallet](#5-restart-qt-wallet)  
         [6. Start MN in QT wallet console](#6-start-mn-in-qt-wallet-console)  
	 [7. Check Masternode Status in VPS](#7-check-masternode-status-in-vps)  

## Requirements
- MN Collateral amount of HLO coins.
- A VPS running Linux Ubuntu 16.04 or 18.04 with 1 CPU & 1GB Memory minimum (2gb Recommended) from [Vultr](https://www.vultr.com/?ref=8622028) or any other providers.
- Helio Coin Wallet (Local Wallet)
- An SSH Client (<a href="https://www.putty.org/" target="_blank">Putty</a> or <a href="https://dl.bitvise.com/BvSshClient-Inst.exe" target="_blank">Bitvise</a>)


## Connecting to the VPS and installing the masternode script

##### 1. Log into the VPS with **root**  

##### 2. Git Installation:  
- ```sudo apt-get install -y git-core```  

##### 3. Clone MN setup script: 
- ```git clone https://github.com/HelioNetwork/HLO-MN.git```  

##### 4. Start MN setup script: 
- ```cd HLO-MN && chmod +x ./Helio-MN.sh && ./Helio-MN.sh```
   
**Now ask for VPS Public IP Address** 

**Now you need to wait some time, while script preparing the VPS to setup**  
##### 5. Copy masternode private key from VPS console window and pres "Enter":


- to check VPS daemon status, type: ```helio-cli getinfo```

**Don't close this window!** 	

## Setup QT wallet
##### 1. Create new receiving address and copy it

##### 2. Send Collateral amount of Helio to copied address

##### 3. Open console Get MN output and set masternode configuration file and save it
- ```mn1 VPS_IP:14920 masternode_genkey masternode_output output_index```:

##### 4. Wait at least 15 confirmation of transaction

##### 5. Restart QT wallet  
- **it's important**

##### 6. Start MN in QT wallet console:
- ```startmasternode alias false MN-TEST```

##### 7. Check Masternode Status in VPS:
- ```helio-cli startmasternode local false``` 
- ```helio-cli getmasternodestatus```  

**Сongratulations you did it!**
