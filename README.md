# Mine Verus Coin on Raspberry Pi

## Install (For CCminer)
```
# Install
sudo apt-get install libcurl4-openssl-dev libssl-dev libjansson-dev automake autotools-dev build-essential
git clone --single-branch -b ARM https://github.com/monkins1010/ccminer.git
cd ccminer
chmod +x build.sh
chmod +x configure.sh
chmod +x autogen.sh
./build.sh

# Mine
./ccminer -a verus -o stratum+tcp://ap.luckpool.net:3960 -u RBhVHA2TQp2vcp7wUsabXDjAppfsqWorfM.RPi5 -p x -t 4
```


## Hashrate
| Device                          | Operating System         | Hashrate                             | CPU Speed | CCminer version               | User     |
| ------------------------------- | ------------------------ | ------------------------------------ | --------- | ----------------------------- | -------- |
| Raspberry Pi 5 Rev 1.0          | Raspberry Pi OS 64 Bit   | 3.56 MH/s (Now), 2.39 MH/s (Avg)     | 2.4GHz    | CCMiner v3.8.3                | [applerobloxgames](https://github.com/InikoMatthewPro)
| Raspberry Pi 5 Rev 1.0          | Raspberry Pi OS 64 Bit   | 5.86 MH/s (Peak), 4.02 MH/s (Avg)    | 2.4GHz    | CCMiner v3.8.3-4 (Optimized)  | [applerobloxgames](https://github.com/InikoMatthewPro)

if you want add to this list, please make issues in github.
