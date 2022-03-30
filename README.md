\<PROVIDER\> ZDNS for Caddy
===========================

This package contains a DNS provider ZDNS for [Caddy](https://github.com/caddyserver/caddy). It can be used to manage DNS records with \<PROVIDER\>.

## Caddy module name

```
dns.providers.zdns
```

## Config examples

To use this module for the ACME DNS challenge, [configure the ACME issuer in your Caddy JSON](https://caddyserver.com/docs/json/apps/tls/automation/policies/issuer/acme/) like so:

```json
{
	"module": "acme",
	"challenges": {
		"dns": {
			"provider": {
				"name": "zdns",
				"api_token": "ZDNS_API_TOKEN"
			}
		}
	}
}
```

or with the Caddyfile:

```
# globally
{
	acme_dns zdns ...
}
```

```
# one site
tls {
	dns zdns ...
}
```
