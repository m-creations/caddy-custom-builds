This is the original image with these additional modules:

- [**layer4**](https://caddyserver.com/docs/modules/layer4.handlers.proxy): Matt Holt's [Caddy app for proxying OSI layer 4 (TCP/UDP) connections](https://github.com/mholt/caddy-l4)
- [**Rate Limit**](https://github.com/serfriz/caddy-custom-builds?tab=readme-ov-file#rate-limit): implements both internal and distributed HTTP rate limiting | [mholt/caddy-ratelimit](https://github.com/mholt/caddy-ratelimit)
- [**Caddy Security**](https://github.com/serfriz/caddy-custom-builds?tab=readme-ov-file#caddy-security): to add different authentication methods including MFA/2FA support | [greenpau/caddy-security](https://github.com/greenpau/caddy-security)
- [**Middleware IP Ban**](https://github.com/fabriziosalmi/caddy-mib): add fail2ban like functionality based on downstream server HTTP errors

# Caddy Docker build with deSEC DNS, GeoIP Filter, Coraza WAF and Docker Proxy modules

[![Docker Hub](https://img.shields.io/badge/Docker%20Hub%20-%20serfriz%2Fcaddy--desec--geoip--coraza--dockerproxy%20-%20%230db7ed?style=flat&logo=docker)](https://hub.docker.com/r/serfriz/caddy-desec-geoip-coraza-dockerproxy)
[![GitHub](https://img.shields.io/badge/GitHub%20-%20serfriz%2Fcaddy--desec--geoip--coraza--dockerproxy%20-%20%23333?style=flat&logo=github)](https://ghcr.io/serfriz/caddy-desec-geoip-coraza-dockerproxy)
[![Quay](https://img.shields.io/badge/Quay%20-%20serfriz%2Fcaddy--desec--geoip--coraza--dockerproxy%20-%20%23CC0000?style=flat&logo=redhat)](https://quay.io/serfriz/caddy-desec-geoip-coraza-dockerproxy)

[![GitHub release (latest SemVer)](https://img.shields.io/github/v/release/serfriz/caddy-custom-builds?label=Release)](https://github.com/serfriz/caddy-custom-builds/releases)
[![GitHub build status](https://img.shields.io/github/actions/workflow/status/serfriz/caddy-custom-builds/build.caddy-desec-geoip-coraza-dockerproxy.yml?label=Build)](https://github.com/serfriz/caddy-custom-builds/actions/workflows/build.caddy-desec-geoip-coraza-dockerproxy.yml)

This image is updated automatically by GitHub Actions when a new version of [Caddy](https://github.com/caddyserver/caddy) is released using the official [Caddy Docker](https://hub.docker.com/_/caddy) image and the following modules:
- [**deSEC DNS**](https://github.com/serfriz/caddy-custom-builds?tab=readme-ov-file#dns-modules): for deSEC DNS-01 ACME validation support | [caddy-dns/desec](https://github.com/caddy-dns/desec)
- [**GeoIP Filter:**](https://github.com/serfriz/caddy-custom-builds?tab=readme-ov-file#geoip-filter) to allow or block traffic from specific regions based on [Maxmind GeoLite2 database](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data) | [porech/caddy-maxmind-geolocation](https://github.com/porech/caddy-maxmind-geolocation)
- [**Coraza WAF**](https://github.com/serfriz/caddy-custom-builds?tab=readme-ov-file#coraza-waf): a Web Application Firewall (WAF) for Caddy | [corazawaf/coraza-caddy](https://github.com/corazawaf/coraza-caddy)
- [**Docker Proxy**](https://github.com/serfriz/caddy-custom-builds?tab=readme-ov-file#docker-proxy): enables Caddy to be used for Docker containers via labels | [lucaslorentz/caddy-docker-proxy](https://github.com/lucaslorentz/caddy-docker-proxy)

## Usage

Since this image built off the official Caddy Docker image, the same [volumes](https://docs.docker.com/storage/volumes/) and/or [bind mounts](https://docs.docker.com/storage/bind-mounts/), ports mapping, etc. can be used with this container. Additional [environment variables](https://caddyserver.com/docs/caddyfile/concepts#environment-variables) may be needed for the added modules. Please, refer to the repository's [README](https://github.com/serfriz/caddy-custom-builds?tab=readme-ov-file#container-creation) file for further usage instructions.

Docker builds for all Caddy supported platforms available at the following container registries:
- [**Docker Hub**](https://hub.docker.com/r/serfriz/caddy-desec-geoip-coraza-dockerproxy) `docker pull serfriz/caddy-desec-geoip-coraza-dockerproxy:latest`
- [**GitHub Packages**](https://ghcr.io/serfriz/caddy-desec-geoip-coraza-dockerproxy) `docker pull ghcr.io/serfriz/caddy-desec-geoip-coraza-dockerproxy:latest`
- [**Quay**](https://quay.io/serfriz/caddy-desec-geoip-coraza-dockerproxy) `docker pull quay.io/serfriz/caddy-desec-geoip-coraza-dockerproxy:latest`

### Tags

The following tags are available for the `serfriz/caddy-desec-geoip-coraza-dockerproxy` image:

- `latest`
- `<version>` (eg: `2.7.4`, including: `2.7`, `2`, etc.)

## Contributing

Feel free to contribute, request additional Caddy images with your preferred modules, and make things better by opening an [Issue](https://github.com/serfriz/caddy-custom-builds/issues) or [Pull Request](https://github.com/serfriz/caddy-custom-builds/pulls).

## License

Software under [GPL-3.0](https://github.com/serfriz/caddy-custom-builds/blob/main/LICENSE) ensures users' freedom to use, modify, and distribute it while keeping the source code accessible. It promotes transparency, collaboration, and knowledge sharing. Users agree to comply with the GPL-3.0 license terms and provide the same freedom to others.
