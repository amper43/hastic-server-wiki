You need to start two processes: nodejs and python parts. See [Architecture](https://github.com/hastic/hastic-server/wiki/Architecture) to learn more. Python side connects to node.js side with [ZeroMQ](http://zeromq.org/).
So it is possible to run node.js and python on different (virtual) machines.

We prefer to develop in [Visual Studio Code](https://code.visualstudio.com/)

## Server (Node.js)

```
cd server
npm install
npm run dev
```

There is a [config](https://github.com/hastic/hastic-server/blob/master/server/.vscode/launch.json) for that in `server/.vscode` for attaching to [dev-server](https://github.com/hastic/hastic-server/blob/master/server/build/dev-server.js).

## Analytics (Python)

```
cd analytics
python3 server.py
```

It is also possible to run python process from vscode on a different machine. For example, you may want to run python on Windows and connect it to Linux process which runs via [WSL](https://docs.microsoft.com/en-us/windows/wsl/about).

### Run tests

#### Server
```bash
cd server
npm test
```

#### Analytics
```bash
cd analytics
python3 -m unittest discover
```

`discover` flag used to look though all tests in folder.


