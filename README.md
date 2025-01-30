# HTTP Flooding Awareness & Educational Tool

## Disclaimer ⚠️

This project is intended for **educational and awareness purposes only**. It demonstrates how HTTP flooding works and should **only** be used in controlled environments where you have explicit permission. Misuse of this tool to attack websites or services without authorization is **illegal and unethical**.

## Overview

This project consists of two scripts:

- `server.py`: A simple Flask-based web server that tracks incoming requests.
- `main.py`: A multi-threaded HTTP request sender simulating high traffic to a specified URL.

## Purpose

This tool is created to educate security professionals, developers, and students about:

- The impact of HTTP flooding attacks.
- How web applications handle excessive requests.
- The importance of implementing rate limiting and DDoS protection.

## Features

- Multi-threaded request sending (`main.py`)
- Flask server with request counting (`server.py`)
- Simple monitoring endpoint (`/get_count`)

## Usage

### Running the Test Server

Ensure you have Python installed, then install dependencies:

```sh
pip install flask requests
```

Start the test server:

```sh
python server.py
```

The server will run on `http://127.0.0.1:5000/`.

### Running the HTTP Request Sender

```sh
python main.py
```

Enter the target URL (`http://127.0.0.1:5000/` for testing) and the number of threads.

## Preventing HTTP Flood Attacks

To protect web applications from HTTP flood attacks, consider:

- Implementing **rate limiting** (e.g., Flask-Limiter, Nginx, Cloudflare).
- Using **CAPTCHAs** for suspicious activity.
- Deploying **WAF (Web Application Firewalls)**.
- Monitoring logs for abnormal traffic patterns.

## Ethical Use

This project should **only** be used in an environment where you have explicit permission (e.g., personal servers, ethical hacking labs). Unauthorized use may result in legal consequences.

## License

This project is released under the MIT License. Use responsibly.

