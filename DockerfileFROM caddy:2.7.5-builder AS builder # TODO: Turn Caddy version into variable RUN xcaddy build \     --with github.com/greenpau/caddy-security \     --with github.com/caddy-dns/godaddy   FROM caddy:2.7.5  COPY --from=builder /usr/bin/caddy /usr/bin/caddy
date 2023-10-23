FROM caddy:2.7.5-builder AS builder
# TODO: Turn Caddy version into variable
RUN xcaddy build \
    --with github.com/greenpau/caddy-security \
    --with github.com/caddy-dns/godaddy 

FROM caddy:2.7.5

COPY --from=builder /usr/bin/caddy /usr/bin/caddy
