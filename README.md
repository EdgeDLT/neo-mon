# NeoMon - Neo Network Status Monitor
> NeoMon is a tool for monitoring the status of popular RPC Nodes and REST endpoints on the Neo network.

## Install, Build and Run
```cmd
npm install
bash build.sh
```

## Manage Endpoints

Endpoints can be configured by editing the following JSON files directly. Commits to this repository update the monitor.cityofzion.io web site immediately.

```
mainnet.json
```

```
testnet.json
```


## Manage Flag Icons

Each endpoint in the json has a locale property. Get the corresponding SVG from

https://github.com/lipis/flag-icon-css/tree/master/flags/1x1

Copy the raw source to a new file and add it to /src/assets/icons. Make sure to follow the same file naming convention.

Remove `id` property from the SVG and add ` viewBox="0 0 512 512"`. See one of the other SVGs for an example.

## Deploy

Neomon is hosted on GitHub pages by publishing to the `gh-pages` branch. GitHub Settings are configured to use the custom domain: monitor.cityofzion.io

New updates to the published website are done by CI (GitHub actions).

## Common questions

The following is a list of common problems that developers may have while developing an application on the Neo network.

### Is an endpoint up or down? 

Developers will not be able to communicate with the Neo Network if an endpoint is down. They can use NeoMon to decide which is the best endpoint to use based on whether the endpoint is up and its current block height.

### Is the endpoint fully synced?  

If transactions are being sent to a Node with the intention of them being relayed to the network, the confirmations will not be seen until the Node is fully synced. There is also a risk that the transactions will be rejected by other Nodes as the transactions being sent may be based on outdated information.

## Feature Requests

Do you see any features missing or have any ideas for improvements, you can add feature requests and bugs under Issues.
