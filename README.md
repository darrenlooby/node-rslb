#Really Simple Load Balancer

Basic TCP Loadbalancer, based on excellent [Loadbalancer.js](https://github.com/SocketCluster/loadbalancer).

I started playing around using Redis to allow servers to be added and removed to the target list without requiring a server restart.

This is an Alpha, it works on my dev setup working with two target machines and a single load balacing machine (all of which are Ubuntu).

It's also TCP - so it's pretty much pass through. I've kept the hash based stickiness.

You'll want to incorporate [node-rslb-remote](https://github.com/darrenlooby/node-rslb-remote) which will use Redis messages to add servers.

###Todo
1. Write basic documentation
2. Refactor the selectors to be able to select RoundRobin
