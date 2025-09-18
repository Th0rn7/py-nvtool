# py-nvtool
"HiveOS nvtool" rewritten in Python for Linux and Windows.

Due to limitations of the Nvidia NVML library, `--setmem` works only on GPUs of the 30xx series and newer.

## Install & Run

### Linux
# Download
wget https://github.com/Th0rn7/py-nvtool/releases/download/nvtool/py-nvtool.py
chmod +x py-nvtool.py
cp py-nvtool.py /usr/sbin/py-nvtool

# Run
sudo py-nvtool [options]

### Windows
# Python 3 is required
wget https://github.com/Th0rn7/py-nvtool/releases/download/nvtool/py-nvtool.py

# Run in administrator terminal
py py-nvtool.py [options]

## Options
  -i|--index NUM                Query specified GPU only
  -a|--all                      Get GPU info
  --setpl NUM                   Set GPU power limit (W), 0 - default
  --setcore NUM                 Set GPU locked clocks (MHz), 0 - default
  --setmem NUM                  Set MEM locked clocks (MHz), 0 - default
  --setfan NUM                  Set fan speed (%), 0 - default
  --setcoreoffset NUM           Set CORE clock offset (MHz), 0 - default
  --setmemoffset NUM            Set MEM clock offset (MHz), 0 - default

## Example
sudo py-nvtool --setclocks 1400 --setcoreoffset 200 --setmem 6800 --setmemoffset 2000 --setpl 120 --setfan 50

## Docs
- NVIDIA Device Commands: https://docs.nvidia.com/deploy/nvml-api/group__nvmlDeviceCommands.html
- Python bindings for NVIDIA Management Library: https://pypi.org/project/nvidia-ml-py/

---

This project is Open Source under the GPL-3.0-or-later license.
My fork: https://github.com/Th0rn7/py-nvtool/releases/download/nvtool/py-nvtool.py
