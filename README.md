# MQTT2SQL

A powerful, production-ready Python bridge that seamlessly transfers data from MQTT topics to SQL databases (MySQL or SQLite). Designed for reliability, scalability, and easy integration, this tool is ideal for IoT, automation, and data logging projects.

## Overview

**MQTT2SQL** listens to one or more MQTT topics and writes incoming messages directly into a SQL database. It supports both MySQL and SQLite backends, robust error handling, multi-threaded SQL writes, and flexible configuration via command line or config file.

---

## Features

- **MQTT to SQL Bridge**: Subscribes to MQTT topics and stores messages in a SQL table.
- **Database Support**: MySQL and SQLite, with automatic detection and configuration.
- **Threaded Writes**: Uses a thread pool and semaphores for high-throughput, non-blocking SQL operations.
- **Robust Error Handling**: Retries, backoff, and graceful shutdown on errors or signals.
- **Flexible Configuration**: All options via command line or config file (`mqtt2sql.conf`).
- **TLS/SSL Support**: Secure MQTT connections with CA, cert, and key files.
- **Logging & Debugging**: Multi-level logging to console and file, with verbose and debug modes.
- **Customizable Table/Schema**: Choose your table and database structure.
- **Production Ready**: Handles connection drops, SQL errors, and supports large-scale ingestion.

---

## Example Use Cases

- IoT sensor data logging
- Home automation event storage
- Industrial telemetry archiving
- Real-time monitoring dashboards

---

## Quick Start

1. **Install dependencies:**
   ```sh
   pip install paho-mqtt configargparse mysqlclient
   ```
   *(Add `sqlite3` if using SQLite, usually included with Python)*

2. **Configure:**
   - Edit `mqtt2sql.conf` or use command-line arguments.

3. **Run:**
   ```sh
   python mqtt2sql.py -c mqtt2sql.conf
   ```

---

## Configuration

All options can be set via command line or in `mqtt2sql.conf`:

- MQTT: host, port, username, password, topics, TLS/SSL
- SQL: type (mysql/sqlite), host, port, username, password, db, table
- Logging: logfile, debug, verbose

See the sample `mqtt2sql.conf` for details.

---

## Implementation Highlights

- **Clean OOP Design**: Core logic encapsulated in the `Mqtt2Sql` class.
- **Signal Handling**: Graceful shutdown on SIGINT/SIGTERM.
- **Retry Logic**: For both SQL connections and transactions.
- **Threaded SQL Writes**: Ensures high performance and non-blocking MQTT message handling.
- **Extensive Logging**: Timestamped logs, debug levels, and optional file output.
- **Secure by Default**: TLS/SSL support for MQTT.

---

## Why Choose This Project?

- **Production-Grade**: Built for reliability and uptime.
- **Highly Configurable**: Adapts to any MQTT/SQL environment.
- **Scalable**: Handles high message rates and large deployments.
- **Well-Documented**: Clean code, docstrings, and sample configs.
- **Showcases Advanced Python Skills**: Multi-threading, error handling, OOP, and integration with real-world protocols.

---

## About the Author

Created by a professional Python developer with expertise in IoT, automation, and backend systems. This project demonstrates advanced skills in:
- Protocol integration (MQTT, SQL)
- Robust, maintainable code
- Production deployment best practices
- Client-focused, scalable solutions

---

## License

MIT License. Free for personal and commercial use.

---

## Contact

For customizations, support, or consulting, contact me via Upwork or GitHub.
