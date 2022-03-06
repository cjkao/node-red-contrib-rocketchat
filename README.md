Running node module locally:

In the directory containing the node’s package.json file, run: sudo npm link

In your node-red user directory, typically ~/.node-red run: npm link node-red-contrib-rocketchat

# vscode debug configuration

```
{
	"version": "0.2.0",
	"configurations": [
		{
			"type": "node",
			"request": "launch",
			"name": "Launch Node-red",
			"program": "/path/to/repo/of/node-red/packages/node_modules/node-red/red.js",
			"runtimeArgs": [
				"--preserve-symlinks",
				"--experimental-modules"
			],
			"env": {
				"NO_UPDATE_NOTIFIER": "1",
				"env_roomId": "Z*******Q"
			},
			"cwd": "/path/to/repo/of/github/node-red"
		},
		{
			"type": "node",
			"request": "launch",
			"name": "Debug Current File",
			"program": "${file}"
		},
		{
			"type": "node",
			"request": "attach",
			"name": "Attach to Process",
			"processId": "${command:PickProcess}"
		}
	]
}
```
