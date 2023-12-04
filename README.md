# Mine Verus Coin on ARM
- Raspberry Pi
- Orange Pi
- Nano Pi
- Others Pi/ARM
## Donate
Verus Coin: **RBhVHA2TQp2vcp7wUsabXDjAppfsqWorfM**

# Linux
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
./ccminer -a verus -o stratum+tcp://sg.vipor.net:5040 -u RBhVHA2TQp2vcp7wUsabXDjAppfsqWorfM -p x -t 4
```

## Install (For CCminer Optimized)
```
sudo apt-get install libcurl4-openssl-dev libssl-dev libjansson-dev automake autotools-dev build-essential libomp5 git -y
cd /usr/src
sudo git clone https://github.com/Oink70/CCminer-ARM-optimized
cd /usr/src/CCminer-ARM-optimized/

# Mine
./ccminer -a verus -o stratum+tcp://sg.vipor.net:5040 -u RBhVHA2TQp2vcp7wUsabXDjAppfsqWorfM -p x -t 4
```

## Hashrate
| Device                          | Operating System                           | Hashrate                             | CPU, Speed & Cores/Threads  | CCminer version               | User                                                   |
| ------------------------------- | ------------------------------------------ | ------------------------------------ | --------------------------- | ----------------------------- | ------------------------------------------------------ |
| Raspberry Pi 5 Rev 1.0          | Raspberry Pi OS Desktop 64 Bit (Bookworm)  | 3.56 MH/s (Now), 2.39 MH/s (Avg)     | BCM2712 & 2.4GHz (4/4)      | CCMiner v3.8.3                | [applerobloxgames](https://github.com/InikoMatthewPro) |
| Raspberry Pi 5 Rev 1.0          | Raspberry Pi OS Desktop 64 Bit (Bookworm)  | 5.86 MH/s (Peak), 4.02 MH/s (Avg)    | BCM2712 & 2.4GHz (4/4)      | CCMiner v3.8.3-4 (Optimized)  | [applerobloxgames](https://github.com/InikoMatthewPro) |
| Nano Pi R2S                     | Debian 11 (Bullseye)                       | 1.31 MH/s (Avg), 3.13 MH/s (Max)     | RK3328 & 1.296GHz (4/4)     | CCMiner v3.8.3                | [applerobloxgames](https://github.com/InikoMatthewPro) |

if you want add to this list, please make issues in github.
