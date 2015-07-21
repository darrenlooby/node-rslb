#Really Simple Load Balancer

Basic TCP Loadbalancer, based on the excellent [Loadbalancer.js](https://github.com/SocketCluster/loadbalancer).

I started playing around using Redis to allow servers to be added and removed to the target list without requiring a server restart.

This is an Alpha, it works on my dev setup working with two target machines and a single load balacing machine (all of which are Ubuntu).

It's also TCP - so it's pretty much pass through.

It has hash based stickiness (so, no storage or database calls needed to have sticky LB).
It seemlessly handles WebSockets and is tested specially with [SocketCluster](https://github.com/SocketCluster/socketcluster) SC1 and SC2.



You'll want to incorporate [node-rslb-remote](https://github.com/darrenlooby/node-rslb-remote) which will use Redis messages to add servers.

###Todo
1. Write basic documentation
2. Refactor the selectors to be able to select RoundRobin
