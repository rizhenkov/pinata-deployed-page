# pinata-deployed-page

This repo contains example autodeploying static website to IPFS with connected domain. 

What action do:
- upload website directory to IPFS through [Pinata](https://pinata.cloud/)
- install doctl and auth with token
- change domain dns record to work with the updated hash

## Useful links
- [How to Easily Host a Website on IPFS](https://medium.com/pinata/how-to-easily-host-a-website-on-ipfs-9d842b5d6a01)
- [Upload to IPFS Pinata pinning service](https://dapps-delivery-guide.readthedocs.io/en/latest/hosting/ipfs.html#upload-to-ipfs-pinata-pinning-service)
- [IPFS Github Action](https://github.com/aquiladev/ipfs-action)
- [DigitalOcean doctl](https://github.com/digitalocean/doctl)
- [doctl Github Action](https://github.com/digitalocean/action-doctl)

## Tips
1. Use low TTL for txt-record if you want update quickly
2. Add your domain to [this form] to get free SSL

## Secrets for repository
`PINATA_KEY`
`PINATA_SECRET`
`PINATA_PIN_NAME` any string
`DO_TOKEN` token to digitalocean
`DO_DOMAIN_ROOT` your domain 2nd level name (even if you are using 3rd)
`DO_DOMAIN_RECORD_ID` id of TXT record which contains ipfs hash (you can find this by using `doctl compute domain records list DOMAIN_NAME`)
