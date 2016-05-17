docker-compose-nginx-proxy-sample
=========

Sample nginx proxy container app utilizing Docker Compose.

Usage
-------
1. Install Docker and Docker Compose. If you are using a Windows/Mac OS X machine, install Docker Machine as well (all of the required Docker components can be installed together as part of the [Docker Toolbox](https://www.docker.com/products/docker-toolbox)).

2. Clone this repository.

3. Make changes to `/etc/sites/` as necessary.

4. Start the app by running `docker-compose up` in the repository root folder.

5. If you are using Weave and haven't already exposed the Weave network, run `weave expose`.

6. If necessary, update iptables to allow external connections.
```
sudo iptables -A INPUT -i lo -j ACCEPT
sudo iptables -A INPUT -p tcp -m tcp --dport 80 -j ACCEPT
```
