# ZenCMS

[![PHP Version](https://img.shields.io/badge/PHP-5.6-blue.svg)](https://php.net/)
[![MySQL Version](https://img.shields.io/badge/MySQL-5.7-blue.svg)](https://mysql.com/)
[![Docker](https://img.shields.io/badge/Docker-Supported-informational.svg)](https://www.docker.com/)
[![License](https://img.shields.io/badge/License-GPL%20v3-green.svg)](https://www.gnu.org/licenses/gpl-3.0)

ZenCMS is a legacy Content Management System originally developed by Zen Thang. This repository provides a Dockerized environment to easily run and develop the CMS on modern machines without compatibility issues.

## Quick Start

Ensure you have **Docker** and **Docker Compose** installed.

```bash
# Clone the repository
git clone <your-repo-url>
cd ZenCMS

# Start the environment
docker-compose up -d --build
```

The system will be available at:

- **Website:** [http://localhost:8080](http://localhost:8080)
- **Installer:** [http://localhost:8080/install](http://localhost:8080/install)
- **phpMyAdmin:** [http://localhost:8089](http://localhost:8089)

## Configuration

During the installation process in the browser, use the following database credentials:

| Setting               | Value            |
| :-------------------- | :--------------- |
| **Database Host**     | `db`             |
| **Database Name**     | `zencms`         |
| **Database User**     | `zencms`         |
| **Database Password** | `zencmspassword` |

_Note: The MySQL server is configured with `sql-mode=""` to support legacy insert queries._

## Development

- **Instant Reload:** Source code is mounted via Docker volumes (`.:/var/www/html`), so any local file changes will immediately reflect without rebuilding the container.
- **Legacy Support:** The container is pre-configured with PHP 5.6 and older extensions (`gd`, `mysql`, `iconv`) required to run this legacy CMS.

## License

Distributed under the GNU General Public License v3.0. See `license.txt` for more information.
