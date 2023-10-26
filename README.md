Constellix DNS module for Caddy
===========================

This package contains a DNS provider module for [Caddy](https://github.com/caddyserver/caddy). It can be used to manage DNS records with Constellix DNS.

## Caddy module name

```
dns.providers.constellix
```

## Config examples

To use this module for the ACME DNS challenge, [configure the ACME issuer in your Caddy JSON](https://caddyserver.com/docs/json/apps/tls/automation/policies/issuer/acme/) like so:

```json
{
	"module": "acme",
	"challenges": {
		"dns": {
			"provider": {
				"name": "constellix",
				"api_key": "CONSTELLIX_API_KEY",
				"secret_key": "CONSTELLIX_SECRET_KEY"
			}
		}
	}
}
```

or with the Caddyfile:

```
# globally
{
	acme_dns constellix ...
}
```

```
# one site
tls {
	dns constellix ...
}
```
