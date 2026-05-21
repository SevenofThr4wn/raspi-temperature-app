# Raspberry Pi Temperature App

A Flask-based web application that runs on a Raspberry Pi to record and display internal temperature data from a wired temperature sensor. Fetches external weather data (temperature, humidity, apparent temperature) via the Australian Bureau of Meteorology API and displays everything on a simple web interface. Designed to help workplace managers monitor indoor temperatures and maintain healthy working conditions.

---

## Table of Contents

- [Raspberry Pi Temperature App](#raspberry-pi-temperature-app)
  - [Table of Contents](#table-of-contents)
  - [About](#about)
  - [Tech Stack](#tech-stack)
  - [Features](#features)
  - [Getting Started](#getting-started)
    - [Prerequisites](#prerequisites)
    - [Installation](#installation)
    - [Running the App](#running-the-app)
  - [Contributing](#contributing)

---

## About

This project provides a lightweight monitoring solution for indoor environments. A temperature sensor connected to the Raspberry Pi feeds readings into a local SQLite database, while the BOM API supplies real-time outdoor conditions. Both are surfaced through a minimal Flask web interface accessible from any device on the local network.

---

## Tech Stack

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Flask](https://img.shields.io/badge/flask-%23000.svg?style=for-the-badge&logo=flask&logoColor=white)
![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/css-%23663399.svg?style=for-the-badge&logo=css&logoColor=white)
![Jinja](https://img.shields.io/badge/jinja-white.svg?style=for-the-badge&logo=jinja&logoColor=black)
![SQLite](https://img.shields.io/badge/sqlite-%2307405e.svg?style=for-the-badge&logo=sqlite&logoColor=white)

---

## Features

- Real-time temperature logging from a connected sensor (e.g. DS18B20)
- Web interface displaying:
  - Local sensor temperature
  - Current external temperature & humidity via BOM API
- Historical temperature data stored in a SQLite database
- JSON-based sensor data handling

---

## Getting Started

### Prerequisites

- Raspberry Pi with a compatible temperature sensor connected (e.g. DS18B20)
- Python 3
- Access to the [Australian BOM API](http://www.bom.gov.au/) for external weather data
- Internet connection (required for BOM API)

### Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/SevenofThr4wn/Raspberry-Pi-Temperature-App.git
    cd Raspberry-Pi-Temperature-App
    ```

2. Create and activate a virtual environment:
    ```sh
    python -m venv venv
    source venv/bin/activate
    ```

3. Install dependencies:
    ```sh
    pip install -r requirements.txt
    ```

### Running the App

Start the application (accessible on all network interfaces):

```sh
flask run --host=0.0.0.0
Then open a browser on any device on the same network and navigate to http://<raspberry-pi-ip>:5000.
```
## Contributing
Contributions are welcome. If you have a suggestion or improvement:

- Fork the project
- Create a feature branch
- Commit your changes
- Push to the branch
- Open a pull request
