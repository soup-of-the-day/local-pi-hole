## What is this
Running pi-hole locally on my mac to test it out.

## Basic Set up
bring up pi-hole server:
```
docker compose up -d
```

forward traffic to DNS server:
```
// You might need to call this on your ethernet, or any other internet conection
networksetup -setdnsservers Wi-Fi 127.0.0.1

// Listing all your network services if you need to know the names
networksetup -listnetworkserviceorder
```

revert to Cloudflare DNS server:
```
networksetup -setdnsservers Wi-Fi 1.1.1.1
```
