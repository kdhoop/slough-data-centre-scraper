# Slough Data Centre Scraper

## Automated Site Acquisition Intelligence for the Slough Data Centre Cluster

This repository contains a Python-based intelligence tool designed to automate the surveying of Slough Borough Council planning portals. It identifies and extracts critical infrastructure metrics from complex planning publications to assist developers in site selection and due diligence.

### Project Overview

Manual analysis of council planning policy is time-intensive and prone to oversight. This engine crawls fragmented data sources to identify the intersection of power availability, land scale, and planning permission. It transforms lengthy technical appendices into a prioritized dashboard for acquisition teams.

### Key Features

* **Multi-Source Data Integration**: Aggregates data from three distinct architectures: statutory planning portals, CitizenSpace consultation hubs, and ModernGov committee management systems.
* **URL Normalisation Engine**: Implements logic to repair broken relative paths and common Content Management System (CMS) errors, ensuring consistent document retrieval.
* **Technical Metric Extraction**: Uses the PyMuPDF library and regular expressions to isolate key performance indicators (KPIs) from high-volume PDF documents:
    * **Power Capacity**: Megawatt (MW) and MVA mentions.
    * **Development Scale**: Square meter (SQM) allocations.
    * **Infrastructure Proximity**: Identification of substations and grid supply points.
* **Weighted Priority Scoring**: Automatically ranks documents based on data density, flagging Environmental Impact Assessments (EIA) and Written Schemes as high-priority leads.

### Technical Requirements

The following Python libraries are required to run the scraper:

* **requests**: For handling HTTP protocols and document downloads.
* **beautifulsoup4**: For parsing HTML and identifying document links.
* **pymupdf (fitz)**: For deep-text extraction from PDF files.
* **pandas**: For data structuring and CSV export.

### Installation and Usage

1.  **Clone the repository**:
    ```bash
    git clone [https://github.com/yourusername/slough-data-centre-scraper.git](https://github.com/yourusername/slough-data-centre-scraper.git)
    cd slough-data-centre-scraper
    ```

2.  **Install dependencies**:
    ```bash
    pip install requests beautifulsoup4 pymupdf pandas
    ```

3.  **Execute the script**:
    ```bash
    python main.py
    ```

### Output and Reporting

The script generates a real-time Executive Dashboard in the terminal and exports the full findings to a structured CSV file (`slough_opportunity_report.csv`).

### Value Added

In the data centre sector, identifying power and land capacity ahead of the market is a primary competitive advantage. This tool reduces manual survey time significantly, allowing developers to focus on technical due diligence and land acquisition rather than document discovery.

## Potential Improvements
* Use Parallelisation to speed the process when considering multiple councils.
* Clean the format of the output units.
