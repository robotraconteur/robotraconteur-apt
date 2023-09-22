# Robot Raconteur Apt Repository

This repository contains binary packages for Debian Buster and Bullseye for amd64, arm64, and armhf architectures. It also contains Raspbian ARMv6 packages for Buster and Bullseye.

## Usage

### Debian 10 (buster) and Debian 11 (bullseye)

An apt repository is available for Debian. Packages are available for amd64, armhf, and arm64. See below for raspbian setup. To use, run:

```
sudo apt install apt-transport-https dirmngr gnupg ca-certificates
wget -O - https://robotraconteur.github.io/robotraconteur-apt/wasontech-apt.gpg.key | sudo apt-key add -
echo "deb https://robotraconteur.github.io/robotraconteur-apt/debian buster main" | sudo tee /etc/apt/sources.list.d/robotraconteur.list
sudo apt update
```

#### C++

```
sudo apt-get install robotraconteur-dev
```

#### Python
```
sudo apt-get install python-robotraconteur
sudo apt-get install python3-robotraconteur
```

### Raspbian 10 (buster) and Raspbian 11 (bullseye)

The Raspberry Pi OS (raspbian) for amhf 32-bit processors is slightly different than the main debian armhf distributions. It uses ARMv6 instructions, instead of the ARMv7 instructions used by the main debian installation. Use the following to set up the raspbian repository, and see the debian section for the rest of the instructions.

**Raspberry Pi OS (raspbian) for 64-bit uses the standard debian repository. This is only for 32-bit ARMv6 installation.**

```
sudo apt install apt-transport-https dirmngr gnupg ca-certificates
wget -O - https://robotraconteur.github.io/robotraconteur-apt/wasontech-apt.gpg.key | sudo apt-key add -
echo "deb https://robotraconteur.github.io/robotraconteur-apt/raspbian buster main" | sudo tee /etc/apt/sources.list.d/robotraconteur.list
sudo apt update
```
