# Unifii Monitor

Welcome to my **Unifi Monitor** script, a comprehensive and efficient solution for [Monitoring https://store.ui.com for NEW products].

## Table of Contents

- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- 

## Getting Started

To get a local copy up and running, follow these simple steps.

### Prerequisites

Ensure you have the following installed:

- Go programming language

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/authrequest/Unifi-Monitor.git
   ```
2. Navigate to the project directory:
   ```bash
   cd Unifi-Monitor
   ```
3. Install dependencies:
   ```bash
   # Install any Go dependencies if applicable
   go mod tidy
   ```

## Usage

Before running the project, make sure to configure the Discord webhook URL. Open the `all_products.go` file and set the `DiscordWebhookURL` variable

Run the project:

```bash
go run all_products.go or go run *
```

## Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

## License

Distributed under the [MIT License](LICENSE). See `LICENSE` for more information.

---

Thank you for considering contributing to this project!

## Debian Packaging

There's a Go dependency issue, specific to Debian packaging:

This program uses `github.com/bensch777/discord-webhook-golang`, but that doesn't have a matching .deb in the Debian archives. Debian wants to ensure that no Internet connection is required to build **all** software. Since this package can't pull down all it's dependencies with `apt`, the solutions we have are to break policy. Unless this is intended to land in the official Debian repos, that doesn't matter.

A package whose build requires Internet access is still a valid package, it's just not allowed into Debian itself.
