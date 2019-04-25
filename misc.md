## Find out what processes are running on Linux and kill what's needed

Sometimes when running servers and databases, there are issues with something running already on a given port. The following commands allows to figure out what the processes are, and to kill all `node` processes. 

```
sudo NETSTAT - PLNT
KILLALL -9 NODE
```

```
KILL -9 <pid>
KILLALL -9 {source}
```

## Lint and fix when there are issues linting

```
npm run lint -- --fix
```

## Neatly format objects in console.log
```
console.log(JSON.stringify({object}, null, 2))
```

## Clean reinstall node_modules if using npm as package manager

```
npm ci
```