# Installation

### Pre-installation steps

- Verifying the current Python installation
```
ubuntu@python1:~$ which python3
/usr/bin/python3
ubuntu@python1:~$ type python3
python3 is hashed (/usr/bin/python3)
ubuntu@python1:~$ python3
Python 3.10.6 (main, Nov 14 2022, 16:10:14) [GCC 11.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> 
```
- Verifying the current PiP installation
```
ubuntu@python1:~$ pip3 --version
Command 'pip3' not found, but can be installed with:
sudo apt install python3-pip
ubuntu@python1:~$ pip --version
Command 'pip' not found, but can be installed with:
sudo apt install python3-pip
```

### Installalation
- Installing the required packages for Python
```
sudo apt update
sudo apt install build-essential zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev libssl-dev libreadline-dev libffi-dev curl pkg-config
```
- Downloading the Python package
```
wget https://www.python.org/ftp/python/3.11.2/Python-3.11.2.tgz
```
- Extracting compressed files
```
tar xzvf Python-3.11.2.tgz
```
- Testing and optimizing
```
cd Python-3.11.2
./configure --enable-optimizations
```
- Install the new instance of Python
```
sudo make altinstall
```

### Verifying the installation
- Verifying Python installation
```
ubuntu@python1:~/Python-3.11.2$ which python3.11
/usr/local/bin/python3.11
ubuntu@python1:~/Python-3.11.2$ python3.11
Python 3.11.2 (main, Mar 29 2023, 07:19:40) [GCC 11.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> exit()
ubuntu@python1:~/Python-3.11.2$ type python3.11
python3.11 is hashed (/usr/local/bin/python3.11)
```
- Verifying PiP installation
```
ubuntu@python1:~/Python-3.11.2$ pip3.11 --version
pip 22.3.1 from /usr/local/lib/python3.11/site-packages/pip (python 3.11)
```

### Creating aliases
```
ubuntu@aws1:~$ nano .bash_aliases
ubuntu@aws1:~$ more .bash_aliases 
alias python=python3.11
alias pip=pip3.11
ubuntu@aws1:~$ type python
python is aliased to `python3.11'
ubuntu@aws1:~$ type pip
pip is aliased to `pip3.11'

```
