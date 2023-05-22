# VerusMineOnRaspberryPi
Verus Mine for Raspberry Pi (Unofficial)

## Setup & Install (Raspberry Pi 4 ONLY)
```
# Install box86
sudo apt update
sudo apt full-upgrade -y
sudo apt install git build-essential cmake -y
git clone https://github.com/ptitSeb/box86

# If you running this on a 64-bit Operating Systems then use the following command.
sudo dpkg --add-architecture armhf
sudo apt update
sudo apt install gcc-arm-linux-gnueabihf libc6:armhf libncurses5:armhf libstdc++6:armhf -y

# Now let's setup box86.
cd ~/box86
mkdir build
cd build

cmake .. -DRPI4=1 -DCMAKE_BUILD_TYPE=RelWithDebInfo // 32-bit Operating Systems only.
cmake .. -DRPI4ARM64=1 -DCMAKE_BUILD_TYPE=RelWithDebInfo // 64-bit Operating Systems only.

make -j$(nproc)
sudo make install
sudo systemctl restart systemd-binfmt

# If you experience an error when running this command, try restarting your Raspberry Pi.
sudo reboot

# Next, Install nheqminer
sudo apt install wget -y
wget https://github.com/VerusCoin/nheqminer/releases/download/v0.8.2/nheqminer-Linux-v0.8.2.tgz
tar -xvzf nheqminer-Linux-v0.8.2.tgz
tar -xvzf nheqminer-Linux-v0.8.2.tar.gz
cd nheqminer

# and then start mine.
./nheqminer -v -l ap.luckpool.net:3956 -u RMU2QggCN43G5CUUNDEqF2AnYwNc8NLVmu.rpi4 -p x -t 4

Enjoy you mine verus coin on Raspberry Pi 4!
```

## Hashrate
| Device                          | Operating System         | Hashrate | Box86 Version | CPU Speed |
| ------------------------------- | ------------------------ | -------- | ------------- | --------- |
| Raspberry Pi 4 Model B Rev 1.4  | Raspberry Pi OS 64 Bit   | ?        | v0.3.0        | 1.8GHz    |
| Raspberry Pi 4 Model B Rev 1.4  | Raspberry Pi OS 32 Bit   | ?        | ?             | ?         |

if you want add to this list, please make issues in github.
