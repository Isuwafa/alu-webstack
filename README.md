# HTTPS SSL - Web Stack Project

## Description
This project focuses on configuring DNS subdomains and understanding how to use SSL/HTTPS in a web stack environment. It involves setting up domain subdomains pointing to load balancers and web servers, and writing Bash scripts to audit subdomain configurations.

## Servers
| Name | Username | IP |
|------|----------|----|
| web-01 | ubuntu | 3.92.239.4 |
| web-02 | ubuntu | 34.238.49.220 |
| lb-01 | ubuntu | 13.222.29.180 |

## Requirements
- Ubuntu 16.04 LTS
- Bash scripts must be executable
- Bash scripts must pass Shellcheck (version 0.3.7) without errors
- First line of all Bash scripts: `#!/usr/bin/env bash`
- Second line of all Bash scripts: a comment explaining what the script does

## Tasks

### 0. World Wide Web
**File:** `https_ssl/0-world_wide_web`

Configures domain subdomains and displays information about them.

#### Subdomains configured:
| Subdomain | Type | Points to |
|-----------|------|-----------|
| www | A | 13.222.29.180 (lb-01) |
| lb-01 | A | 13.222.29.180 |
| web-01 | A | 3.92.239.4 |
| web-02 | A | 34.238.49.220 |

#### Usage:
```bash
# Query all default subdomains
./0-world_wide_web yourdomain.com

# Query a specific subdomain
./0-world_wide_web yourdomain.com web-01
```

#### Example output:
```
The subdomain www is a A record and points to 13.222.29.180
The subdomain lb-01 is a A record and points to 13.222.29.180
The subdomain web-01 is a A record and points to 3.92.239.4
The subdomain web-02 is a A record and points to 34.238.49.220
```

## Author
- GitHub: [alu-webstack](https://github.com/your-username/alu-webstack)
