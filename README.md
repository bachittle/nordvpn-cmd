# nordvpn-cli
A quick little script for opening nordvpn with OpenVPN

## setup

Make sure you have python3. Try running this:

`python --version`

if the version is 2 or lower, try this:

`python3 --version`

if none of these commands you need to install python. Go here to install python: https://www.python.org/downloads/

I'm going to be using `python` as my command of choice. If yours is `python3` make sure to use that instead

Now we're going to install some dependencies. All the python dependencies you need are selenium. Here's how you install:

```
python -m pip install -U selenium
```

Now all you need the chrome webdriver for your version of google chrome (if you use firefox, microsoft edge, etc. sorry about your luck. Might update in the future). 
Find your version using this tutorial: https://help.zenplanner.com/hc/en-us/articles/204253654-How-to-Find-Your-Internet-Browser-Version-Number-Google-Chrome
Here's how you get the webdriver:

---
### Linux

- make sure you have wget and unzip. Type in `wget --version` and `unzip --version`. If nothing shows up, 
install it with your package manager of choice
- go to a folder that is in your PATH. If you don't know where this is type in `env | grep PATH` and pick a directory. Preferably, put it in your
`~/.local/bin` if you have one.
- type the following into the command line:
FOR VERSION 81 OF CHROME
```
sudo wget https://chromedriver.storage.googleapis.com/81.0.4044.69/chromedriver_linux64.zip
sudo unzip chromedriver_linux64.zip
sudo rm chromedriver_linux64.zip
```
FOR VERSION 80 OF CHROME
```
sudo wget https://chromedriver.storage.googleapis.com/80.0.3987.106/chromedriver_linux64.zip
sudo unzip chromedriver_linux64.zip
sudo rm chromedriver_linux64.zip
```
FOR VERSION 79 OF CHROME
```
sudo wget https://chromedriver.storage.googleapis.com/79.0.3945.36/chromedriver_linux64.zip
sudo unzip chromedriver_linux64.zip
sudo rm chromedriver_linux64.zip
```
---
### Mac

Haven't tested this yet. A similar installion method to linux, just get the zip file for your version, unzip zip file to folder, 
make sure that folder is in your environment variables

---

Finally, you need to set up some nordvpn config files for openvpn. This is easy to follow here: https://support.nordvpn.com/Connectivity/Linux/1047409422/How-can-I-connect-to-NordVPN-using-Linux-Terminal.htm

then run nordvpn.py and it should connect

TODO's
- [ ] Mac Version
- [ ] Firefox Version

