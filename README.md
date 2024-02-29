# docker-ocserv

This provides testing images for OpenConnect VPN Server. These are intended
to be used to test openconnect clients.





Originally based on images built by [Tommy Lau](mailto:tommy@gen-new.com).

## How to use this image

Get the docker image by running the following commands:

```bash
docker pull nmav/ocserv
```

Start an ocserv instance:

**Note: must use --privileged**

```bash
docker run --name ocserv --privileged -p 443:443 -p 443:443/udp -d tommylau/ocserv
```

This will start an instance with the a test user named `test` and password is also `test`.

### Environment Variables

All the variables to this image is optional, which means you don't have to type in any environment variables, and you can have a OpenConnect Server out of the box! However, if you like to config the ocserv the way you like it, here's what you wanna know.

`OCSERV_SERVER_NAME`, this is the common name used to generate the CA(Certificate Authority).

The default values of the above environment variables:

|   Variable   |     Default     |
|:------------:|:---------------:|
|  **OCSERV_SERVER_NAME**  | www.example.com |
