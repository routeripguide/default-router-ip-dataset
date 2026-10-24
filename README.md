# Default Router IP & Gateway Dataset

An open-source reference database containing manufacturer default gateway IPv4 addresses, access domains, and subnet defaults for consumer networking equipment.

## Purpose

When troubleshooting local area networks or configuring custom subnet routing, identifying whether a device defaults to `192.168.1.1`, `192.168.0.1`, or `10.0.0.1` is essential for direct administrative access. This repository provides structured data and CLI verification utilities.

## Dataset Structure

The core records are maintained in [`data/router-gateways.json`](data/router-gateways.json):

| Brand | Default IP | Fallback IP | Admin Domain | Default User |
| :--- | :--- | :--- | :--- | :--- |
| TP-Link | `192.168.0.1` | `192.168.1.1` | `tplinkwifi.net` | `admin` |
| Netgear | `192.168.1.1` | `192.168.0.1` | `routerlogin.net` | `admin` |
| Asus | `192.168.1.1` | `192.168.50.1` | `router.asus.com` | `admin` |
| Linksys | `192.168.1.1` | `192.168.0.1` | `myrouter.local` | `admin` |
| D-Link | `192.168.0.1` | `192.168.1.1` | `dlinkrouter.local` | `admin` |

For hardware-specific setup procedures, firmware recovery steps, and default password variants across specific revisions, refer to the [routeripguide.com hardware documentation and gateway guides](https://routeripguide.com/).

## Quick Verification Script

Run the included discovery script to identify your current machine's active network gateway:
bash
python scripts/check_gateway.py


## Contributing

1. Fork this repository.
2. Verify hardware model specifications against official vendor manuals.
3. Submit a Pull Request updating `data/router-gateways.json`.

---
Maintained as an open networking resource by [Router IP Guide](https://routeripguide.com/)
