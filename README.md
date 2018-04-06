# Easy-Walton-Miner
Batch file setup for running the Walton miner through the command prompt. Allows the user to bypass the thread limit and reach 100% CPU usage on high power machines. Automates the startup process to be a one click solution.

Created by [scavicchio](https://github.com/scavicchio) and [LeifEricson](https://github.com/EBLeifEricson).

## Installation ("Full" Version)
This is the version you want if you want a lot of customization options, logging features, and other future improvements. Runs in Python which may or may not have a slight impact on performance depending on your machine.
1) Run the ```EasyWaltonMiner-v1.3-Setup.exe``` file and choose the directory you wish to install it to.
2) Click your new "EasyWaltonMiner" shortcut and copy/past in your WTC Wallet address.
3) You should now be mining!

## Installation ("Lite" Version)
If you are worried about performance, or don't trust an executable file, you can download the lite version. It is entirely containted in two batch files, but it is very simplistic and will only recieve minor bug fixes going forward.
1) Run the ```EasyWaltonMinerLite-v1.3-Setup.exe``` file and choose the WTC wallet directory as the destination.
2) Click your new "EasyWaltonMinerLite" shortcut and copy/paste in your WTC Wallet address. 
3) You now should be mining!

## Configuration ("Full" Version Only)
There are a few command line configuration options available. The easiest way to use them is to right click your EasyWaltonMiner shorcut, click "Properties," and edit the "Target" so that the flags are placed at the end of the command, before the close quote. Example:

```
"C:\Program Files (x86)\EasyWaltonMiner\easyWaltonMiner.exe -t 16 -nolog -pkp address.txt"
```

Available options:
```
-wp or --walletpath [path] : Path to the WTC Walton Wallet folder. Defaults to C:/Program Files/WTC
-pkp or --publickeypath [path] : Path to public key text file. Defaults to pubaddr.txt
-m or --mode [mode] : Mode to launch in. Valid values are address, mine, and config.
-nl or --nolog : Disables hashrate logging. Logging is on by default and logs to EasyWaltonMiner/hashlog.csv
-t or --threads [value] : Number of threads to use. Defaults to 8
```

## Building from Source
For the lite version, simply copy the ```easy-miner.bat``` and ```start_automated.bat``` to the WTC directory.

For the full version, either run ```build.bat```, or run ```pyinstaller easyWaltonMiner.py``` (both require python and pyinstaller.) Output will be generated in dist/ folder.

#### [Youtube Channel](https://www.youtube.com/channel/UCfP0gt7jVOvb4SzkihderHQ?view_as=subscriber)
#### [Medium Page](https://medium.com/@salvycavicchio)
