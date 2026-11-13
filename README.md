# BIS router blocklists

Shared AdGuard Home filter lists for all BIS Xiaomi AX3000T routers.

## How updates work

| Layer | Where to edit | Propagates to |
|-------|---------------|---------------|
| **1. NextDNS categories** | https://my.nextdns.io → config `ec2284` | All routers (DNS upstream) immediately |
| **2. Custom domains/keywords** | `bis-adult.txt` / `bis-gaming.txt` here | All routers on next filter refresh (~24h) or after `sync-fleet-filters.sh` |

## Publish after editing

```bash
./scripts/publish-blocklist.sh
./scripts/sync-fleet-filters.sh   # optional: force refresh now on every router
```

## Router inventory

Copy `scripts/routers.example.txt` → `scripts/routers.txt` and list one LAN/WAN-reachable IP per line.
