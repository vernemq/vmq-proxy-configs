# vmq-proxy-configs


(Note: WIP!) This shall be a community collection of configuration files for different Loadbalancers and/or Proxies to run in front of a VerneMQ cluster.

Let's share what we know. Document what works and what does not work. Full configuration files are welcome, but also documented snippets. Use the Wiki, and also feel welcome to just open Github issues with questions and observations.

Note that (with the exception of WebSocket support) we are only concerned with TCP (not HTTP) based load balancers and proxies here. It's always about load balancing MQTT, a TCP-based protocol.

The difference between "TCP Proxies" and "MQTT Proxies" below simply means that Proxies can be aware of the underlying MQTT protocol, or not.
Normally, a TCP based proxy is enough to load balance MQTT endpoints. MQTT protocol awareness can offer additional features like load balancing based on MQTT ClientIDs, or offload features from the broker (like pre-authentication).

### TCP Proxies
- HAProxy
- NGINX
- Traefik
- Envoy
- ... etc

### Loadbalancers
- Loadbalancers on all cloud platforms
- Kubernetes Ingress
- IPVS (LVS)
- F5
- ...etc

### MQTT Proxies
- NGINX+
- MQTT.Cool
- Mainflux MProxy
- ... etc

### Blog Post about Proxies and MQTT

### HAProxy

### Traefik

https://jurian.slui.mn/posts/smqttt-or-secure-mqtt-over-traefik/


traefik: node-red + mosquitto using letsencrypt:  https://gist.github.com/natcl/ed8253a34e7b87d879baabeba82cb846

### Amazon

 - CLB (Classic Load Balancer)
 - ALB (Application Load Balancer)
 - NLB (Network Load Balancer) 

### Azure
- Load Balancer

### Google Cloud
- Load Balancing: https://cloud.google.com/load-balancing/
https://cloud.google.com/load-balancing/docs/load-balancing-overview

### Links to Official Documentation

MetalLB: https://metallb.universe.tf/

HAProxy Enterprise: https://www.haproxy.com/documentation/hapee/

HAProxy Ingress: https://haproxy-ingress.github.io/about/
Github: https://github.com/jcmoraisjr/haproxy-ingress

HAProxy Ingress Controller: https://github.com/haproxytech/kubernetes-ingress#readme

HAProxy Community Edition: http://www.haproxy.org/#docs

NGINX: https://nginx.org/en/docs/

NGIXN (commercial editions): https://docs.nginx.com/

Kubernetes: 
- Ingress Controllers: https://kubernetes.io/docs/concepts/services-networking/ingress-controllers/

- Gobetween: https://github.com/yyyar/gobetween
(has aynone used it with MQTT?)


### Wiki Topics

#### TLS termination

#### Loadbalancing Strategies

#### WebSockets

#### Proxy Protocol

#### Know Issues for different LBs/Proxies

#### Protocol (MQTT) awareness

#### Quickstarts

#### DNS topics

#### Kubernetes Ingress