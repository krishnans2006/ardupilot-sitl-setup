# ArduPilot SITL Setup
Setup Instructions for ArduPilot SITL on Linux

```bash
sudo apt install git gitk git-gui
git clone --recurse-submodules https://github.com/ArduPilot/ardupilot.git
cd ardupilot
Tools/environment_install/install-prereqs-ubuntu.sh -y
```

Restart your computer.

```bash
sudo apt install gcc-arm-none-eabi python3-empy
source ~/venv-ardupilot/bin/activate
./waf configure --board PixHawk1
./waf plane
```

Run SITL:
```bash
Tools/autotest/sim_vehicle.py --no-mavproxy -v ArduPlane
```
