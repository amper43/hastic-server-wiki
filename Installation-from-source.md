## Build & run from source 

Possible to install on:

* [Linux](#linux)
* [Docker](#docker)

### Linux

#### System prerequisites:

* [git](https://git-scm.com/download/linux)
* [nodejs >= 6.14](https://nodejs.org/en/download/package-manager/#debian-and-ubuntu-based-linux-distributions)
* [python >= 3.6.5 and < 3.7.0](https://www.python.org/downloads/) with [pip3](https://packaging.python.org/guides/installing-using-linux-tools/#installing-pip-setuptools-wheel-with-linux-package-managers)

#### Installation
```bash
git clone --recursive https://github.com/hastic/hastic-server.git
# or `git submodule update --init --recursive` if it's already cloned
cd hastic-server
pip3 install -r analytics/requirements.txt
python -m pip install -r analytics/requirements.txt
cd server
npm install
npm run build
```

#### Run
```bash
cd hastic-server/server
npm start
```

### See also 

* [Development](https://github.com/hastic/hastic-server/wiki/Development-mode)