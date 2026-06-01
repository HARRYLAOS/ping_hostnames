A lightweight Bash-based network utility for bulk hostname resolution and ICMP reachability testing.

This script reads hostnames from a CSV or plain text file, resolves them using system DNS, performs ping validation, and exports structured CSV results for successful, failed, and unresolved hosts.

Designed for network engineers, sysadmins, and infrastructure environments where quick visibility into hostname availability is needed without deploying heavy monitoring solutions.


Features
Bulk hostname processing
DNS resolution validation
ICMP ping testing
Parallel execution for faster performance
Duplicate hostname filtering
Timestamped CSV result exports
Real-time colored terminal output
Execution summary statistics
Safe Bash practices with strict error handling
Simple and portable Linux-friendly design
Output

The script generates timestamped CSV reports:

ping_success_<timestamp>.csv
ping_failure_<timestamp>.csv

Each report contains:

Hostname
Status
Resolved IP
Timestamp
Usage
chmod +x ping_hosts.sh
./ping_hosts.sh hostnames.csv

If no file is provided, the script defaults to:

hostnames.csv
Example Input
google.com
cloudflare.com
example.local
Requirements
Bash
getent
ping
awk
xargs
Use Cases
Network validation
DNS auditing
Infrastructure troubleshooting
Pre-migration connectivity checks
Internal hostname verification
Monitoring preparation workflows
License

MIT License
