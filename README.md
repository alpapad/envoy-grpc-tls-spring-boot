# Setup

for mtls + certs to work you will need to modify /etc/hosts and add 

`127.0.1.1	my-webserver.internal.ekervhen.xyz`

# Communication

 `client` -> (mtls) - > `api gw` -> (mtls) -> `envoy proxy (sidecar)` -> (mtls) -> `spring boot sample application`
 
# How to test

in parent folder:
 - `docker-compose up`
 
in parent folder (different window)
 - `sh test.sh`
