# A docker image for mkcert.dev

mkcert.dev is a tool for developer to generate valid certificates.
Those certificates can then be used in their dev environment.

This repository provides a dockerfile and a helper script to:

- Create CA certificate
- Create a server certificate (key + crt)
- Create a server certificate (p12)
- Convert the server certificate to JKS format
- Convert the CA certificate to JKS format

## Usage

```sh
git clone https://github.com/nmasse-itix/mkcert
cd mkcert
docker build . mkcert:dev
docker run -v /tmp/certs:/certs -e SERVER_HOSTNAMES="localhost.localdomain localhost" -it mkcert:dev
```
