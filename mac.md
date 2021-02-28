### python
pip3 install --user -i https://pypi.tuna.tsinghua.edu.cn/simple numpy


### brew  arm
modify /etc/hosts
185.199.108.133 raw.githubusercontent.com
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
echo 'eval $(/opt/homebrew/bin/brew shellenv)' >> /Users/jackye/.zprofile
eval $(/opt/homebrew/bin/brew shellenv)

brew install python3
==> python@3.9
Python has been installed as
  /opt/homebrew/bin/python3

### conda
https://github.com/conda-forge/miniforge
Miniforge3-MacOSX-arm64.sh
conda install numpy scipy matplotlib