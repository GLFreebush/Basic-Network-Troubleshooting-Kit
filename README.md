# Basic-Network-Troubleshooting-Kit

A basic network troubleshooting guide with three essential checks:

1. Ping test
2. DNS check
3. Tracert/Traceroute

## 1) Ping

Use ping to verify if a host is reachable and measure latency.

### Windows
```powershell
ping google.com
```

### Linux/macOS
```bash
ping -c 4 google.com
```

What to look for:
- Replies returned = host/network path is reachable
- Packet loss or timeout = possible network/firewall/routing issue

## 2) DNS Checks

Use DNS tools to confirm that domain names resolve to IP addresses.

### Using `nslookup` (Windows/Linux/macOS)
```bash
nslookup google.com
```

### Using `dig` (Linux/macOS)
```bash
dig google.com
```

What to look for:
- A valid IP address in the result
- Server failures or no answer can indicate DNS problems

## 3) Tracert / Traceroute

Use tracert/traceroute to see the path packets take to a destination.

### Windows (`tracert`)
```powershell
tracert google.com
```

### Linux/macOS (`traceroute`)
```bash
traceroute google.com
```

What to look for:
- Where delays or timeouts start
- Whether a route fails before reaching the destination
