# NetPerf - Network Diagnostic Tool

Bash script for Linux that centralizes network diagnostics: interfaces, latency, packet loss, and download speed.

## Features
- Network interfaces and default route display
- Latency test (ping) with packet loss rate
- Download speed test (Mbps)
- Final summary with timestamp

## Requirements
- Linux with `bash`, `ping`, `ip`, `curl`, `bc`

## Usage
```bash
chmod +x netperf.sh
./netperf.sh                          # default test (8.8.8.8, 10 pings)
./netperf.sh -h 1.1.1.1 -c 20         # custom host and ping count
./netperf.sh -i eth0                  # target a specific interface
```

## Options
| Option | Description                  | Default |
|--------|-------------------------------|---------|
| `-h`   | Host to test                  | 8.8.8.8 |
| `-c`   | Number of ping packets sent   | 10      |
| `-i`   | Network interface to display  | all     |

## Possible improvements
- Export results to CSV/JSON for history
- Upload speed test
- Threshold alerts (email/log if latency > X ms)
