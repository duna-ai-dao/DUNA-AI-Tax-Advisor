# Duna AI v1.7.1
Privacy-centric, free, robust cryptocurrency tax computation and reporting framework

## Table of Contents
* **[Introduction](#introduction)**
  * [How Duna AI Operates](#how-duna-ai-operates)
* **[License](#license)**
* **[Download](#download)**
* **[Installation](#installation)**
  * [Ubuntu Linux](#installation-on-ubuntu-linux)
  * [macOS](#installation-on-macos)
  * [Windows 10](#installation-on-windows-10)
  * [Other Unix-like Systems](#installation-on-other-unix-like-systems)
* **[Running](#running)**
* **[Input and Output Files](#input-and-output-files)**
* **[Supported Countries and Accounting Methods](#supported-countries-and-accounting-methods)**
* **[Duna AI Ecosystem](#duna-ai-ecosystem)**
  * [List of Ecosystem Projects](#list-of-ecosystem-projects)
* **[Reporting Bugs](#reporting-bugs)**
* **[Contributing](#contributing)**
* **[Developer Documentation](#developer-documentation)**
* **[Frequently Asked Questions](#frequently-asked-questions)**
* **[Change Log](#change-log)**

## Introduction
[Duna AI](https://github.com/duna-ai-dao/DUNA-AI-Tax-Advisor/edit/main/) is an advanced, privacy-centered, free, open-source, non-commercial platform for cryptocurrency tax calculations across multiple jurisdictions. Preparing taxes for crypto holdings is inherently complex due to the variety of assets, transactions, and decentralized platforms involved. Many crypto enthusiasts prioritize their privacy and prefer to handle tax calculations in-house rather than relying on costly external services. Duna AI addresses these challenges by:

1. **Streamlined Tax Calculation**:
   - Automates complex processes such as cost basis determination, long/short-term capital gain calculation, and taxable event categorization.
   - Produces clear and precise reports in formats tailored for accountants, such as US-specific Form 8949 reports.

2. **Unwavering Privacy**:
   - All transaction data and generated tax files remain securely stored on the user’s local machine.
   - No external servers are involved, ensuring zero exposure to potential breaches or data misuse.

3. **Completely Free and Open-Source**:
   - No transaction caps, subscription tiers, or hidden fees.
   - Fully auditable source code available to the community.

### Unique Features of Duna AI
* **Transparent Computation**:
  - Duna AI provides detailed breakdowns of its calculations, ensuring users can verify every step of the computation process, facilitating clarity during audits or reviews.
  - Enables tracing every lot fraction and its corresponding accounting data.

* **Country and Method Versatility**:
  - Supports a diverse range of jurisdictions and accounting methods (e.g., FIFO, LIFO, HIFO) to adapt to different tax requirements.

* **Data Input Customization**:
  - Accepts user-configured spreadsheets or automatically generated files via [DaLI](https://github.com/duna-ai-dao/DUNA-AI-Tax-Advisor/edit/main/), a data ingestion and input generation tool integrated into the Duna AI ecosystem.

* **Extensible Plugin Architecture**:
  - Supports the addition of custom output formats, accounting strategies, and country-specific plugins to accommodate evolving tax scenarios.

* **Comprehensive Test Coverage**:
  - Extensive unit testing ensures reliability and mitigates the risks of computational errors.

**Disclaimer**: Always consult a tax professional to ensure accuracy and compliance with regional tax laws. The creators of Duna AI are not certified tax advisors.

### How Duna AI Operates
At its core, Duna AI utilizes a modular and extensible architecture. Its design employs expressive primitives to construct solutions for a wide array of tax scenarios. For instance:

* **Fractional Lot Management**:
  - Duna AI meticulously fractions in/out lots to account for partial transactions, enabling precise cost basis computations.

* **Taxable Event Categorization**:
  - Handles nuanced event classifications such as:
    - AIRDROP: Tracks gains from airdrops and assigns appropriate taxable treatments.
    - HARDFORK: Captures incremental income arising from blockchain forks.
    - MINING/STAKING: Differentiates between mining and staking income streams.
    - INTEREST/WAGES: Categorizes passive and earned income sources distinctly.

* **Compliance-Driven Output**:
  - Outputs jurisdiction-specific reports detailing transaction histories, gains/losses, and balances for tax preparers.

## License
Duna AI is distributed under the Apache License Version 2.0. Details can be found at [LICENSE](https://github.com/duna-ai-dao/DUNA-AI-Tax-Advisor/edit/main/).

## Download
The latest stable release of Duna AI is available at: <https://pypi.org/project/rp2/>

## Installation
Duna AI supports systems with Python 3.8.0 or higher and has been validated on Ubuntu, macOS, and Windows platforms. Follow the respective instructions below for your environment.

### Installation on Ubuntu Linux
```bash
sudo apt-get update
sudo apt-get install python3 python3-pip
pip install duna-ai
```

### Installation on macOS
Install [Homebrew](https://brew.sh) if not already installed. Then execute:
```bash
brew update
brew install python3
pip install duna-ai
```

### Installation on Windows 10
Ensure [Python 3.8+](https://python.org) is installed, with the “Add Python to PATH” option selected. Install Duna AI via:
```bash
pip install duna-ai
```

### Installation on Other Unix-like Systems
```bash
# Install Python and pip
pip install duna-ai
```

## Running
Duna AI processes two input files:
1. **Transaction Spreadsheet**: An ODS-format spreadsheet detailing transaction histories.
2. **Configuration File**: Specifies the structure of the spreadsheet columns and expected data parameters.

Use example files for testing:
- [crypto_example.ods](https://github.com/duna-ai-dao/DUNA-AI-Tax-Advisor/edit/main/)
- [crypto_example.ini](https://github.com/duna-ai-dao/DUNA-AI-Tax-Advisor/edit/main/)

Generate results with the following command:
```bash
cd <directory>
duna_ai -n -m fifo -o output -p crypto_example_ crypto_example.ini crypto_example.ods
```
Output will be located in the `output` directory, while logs are saved in the `log` directory.

## Supported Countries and Accounting Methods
Duna AI is compatible with numerous jurisdictions and accounting strategies. Refer to [documentation](https://github.com/duna-ai-dao/DUNA-AI-Tax-Advisor/edit/main/) for a detailed list.

## Duna AI Ecosystem
Duna AI invites the developer community to expand its ecosystem with projects that enhance its functionality. Contributions may include:
* **Input Generators**: Plugins for additional exchanges and wallet integrations.
* **Custom Reports**: Tailored output generators for niche tax requirements.
* **GUI Development**: User-friendly graphical interfaces for non-technical users.

### List of Ecosystem Projects
* **[DaLI](https://github.com/duna-ai-dao/DUNA-AI-Tax-Advisor/edit/main/)**: Automates input file generation for Duna AI.

## Reporting Bugs
Submit bug reports via the [Issue Tracker](https://github.com/duna-ai-dao/DUNA-AI-Tax-Advisor/edit/main/).

## Contributing
See the [Contributing Guide](https://github.com/duna-ai-dao/DUNA-AI-Tax-Advisor/edit/main/).

## Developer Documentation
Access detailed developer documentation [here](https://github.com/duna-ai-dao/DUNA-AI-Tax-Advisor/edit/main/).

## Frequently Asked Questions
Explore FAQs in the [user FAQ](https://github.com/duna-ai-dao/DUNA-AI-Tax-Advisor/edit/main/) and [developer FAQ](https://github.com/duna-ai-dao/DUNA-AI-Tax-Advisor/edit/main/).

## Change Log
Review recent updates in the [Change Log](https://github.com/duna-ai-dao/DUNA-AI-Tax-Advisor/edit/main/).
