# Sqizzle

Based on seeker, Sqizzle is simple, just like we host phishing pages to get credentials why not host a fake page that requests your location like many popular location based websites.

Sqizzle Hosts a fake website on In Built PHP Server and uses Serveo to generate a link which we will forward to the target, website asks for Location Permission and if the target allows it, we can get :
* Longitude
* Latitude
* Accuracy
* Altitude - Not always available
* Direction - Only available if user is moving
* Speed - Only available if user is moving
* Webcam Photos (Will be saved in ./templates/nearyou/php/log)

Along with Location Information we also get Device Information without any permissions :

* Operating System
* Platform
* Number of CPU Cores
* Amount of RAM - Approximate Results
* Screen Resolution
* GPU information
* Browser Name and Version
* Public IP Address
* IP Address Reconnaissance

This tool is a Proof of Concept and is for Educational Purposes Only, Sqizzle shows what data a malicious website can gather about you and your devices and why you should not click on random links and allow critical permissions such as Location etc.



Based on https://github.com/thewhiteh4t/seeker and https://github.com/thelinuxchoice/saycheese

## Installation:
### Kali Linux / Ubuntu / Parrot OS
```
git clone https://github.com/Samarine/Sqizzle.git
cd Sqizzle
chmod 777 install.sh
./install.sh
```
### Termux
```
git clone https://github.com/Samarine/Sqizzle.git
cd Sqizzle
chmod 777 termux_install.sh
./termux_install.sh
```
## Usage

```bash
python3 sqizzle.py -h

usage: sqizzle.py [-h] [-s SUBDOMAIN]

optional arguments:
  -h, --help                              show this help message and exit
  -s SUBDOMAIN, --subdomain Subdomain 	Provide Subdomain for Serveo URL ( Optional )

# Example

python3 sqizzle.py --subdomain google
```
## Known Problems

* Services like Serveo and Ngrok are banned in some countries such as Russia etc., so if it's banned in your country you may not get a URL, if not then first READ CLOSED ISSUES, if your problem is not listed, create a new issue.



