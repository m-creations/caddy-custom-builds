# syntax=docker/dockerfile:1
FROM caddy:2.9.1-builder AS builder

RUN xcaddy build \
    --with github.com/caddy-dns/hetzner \
    --with github.com/caddy-dns/desec \
    --with github.com/corazawaf/coraza-caddy/v2 \
    --with github.com/fabriziosalmi/caddy-mib \
    --with github.com/greenpau/caddy-security@v1.1.29 \
    --with github.com/lucaslorentz/caddy-docker-proxy/v2 \
    --with github.com/mholt/caddy-l4/modules/l4proxy \
    --with github.com/mholt/caddy-ratelimit \
    --with github.com/porech/caddy-maxmind-geolocation

FROM caddy:2.9.1

COPY --from=builder /usr/bin/caddy /usr/bin/caddy

CMD ["caddy", "docker-proxy"]
