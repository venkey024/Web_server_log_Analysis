# Web Server Log Analysis - Python Take-Home Assessment

This repository contains my solution for the **Web Server Log Analysis - Python Take-Home Assessment**. The primary goal of this assessment is to **demonstrate Python data analysis skills** by extracting meaningful insights from real-world web server log data.

## Overview

The assessment involves analyzing the **Calgary HTTP dataset**, which comprises approximately one year's worth of HTTP requests directed to the University of Calgary's Computer Science web server. This dataset is provided in the **standard Apache Common Log Format**.

## Dataset Information

*   **Dataset Name**: Calgary HTTP Dataset
*   **Source**: University of Calgary's Computer Science web server, with the original data available from `https://ita.ee.lbl.gov/html/contrib/Calgary-HTTP.html`.
*   **Format**: ASCII text file, with each line representing one request.
*   **Log Entry Structure**: Each log entry follows the Apache Common Log Format and includes several space-separated fields such as:
    *   `remotehost` (Remote hostname or IP address)
    *   `rfc931` (Remote logname of user)
    *   `authuser` (Authenticated username)
    *   `[date]` (Request timestamp, e.g., `[day/month/year:hour:minute:second zone]`)
    *   `"request"` (Full HTTP request line, e.g., `"GET index.html HTTP/1.0"`)
    *   `status` (HTTP status code, e.g., 200, 404, 500)
    *   `bytes` (Content-length transferred in bytes)
    *   Other fields like `host` and `filename` are also present in a simplified structure described for the dataset.
 ⚙️ Project Setup

### 📦 Requirements

- Python 3.8+
- Jupyter Notebook
- Pandas
- Matplotlib / Seaborn (for optional visualization)

## Assessment Tasks

The assessment is divided into two main parts:

### Part 1: Data Loading and Cleaning

This section focuses on preparing the raw log data for analysis. Key steps include:
*   **Downloading and loading the compressed dataset** (`.gz` format) from the specified FTP server.
*   **Implementing proper error handling** for network and file operations.
*   **Parsing timestamp strings** into `datetime` objects.
*   **Extracting file extensions** from the filename field.
*   **Handling missing or malformed data entries** and converting data types appropriately.
*   **Removing or flagging invalid log entries**.

### Part 2: Analysis Questions

After cleaning the data, various analytical questions are addressed to extract insights. These questions cover a range of web server metrics:
*   **Q1: Count of total log records**
*   **Q2: Count of unique hosts**
*   **Q3: Date-wise unique filename counts**
*   **Q4: Number of 404 response codes**
*   **Q5: Top 15 filenames with 404 responses**
*   **Q6: Top 15 file extensions with 404 responses**
*   **Q7: Total bandwidth transferred per day for July 1995**
*   **Q8: Hourly request distribution**
*   **Q9: Top 10 most requested filenames**
*   **Q10: HTTP response code distribution**

## Deliverables

The primary deliverable is a **Jupyter Notebook (`analysis.ipynb`)** containing all code, analysis, and visible output cells. An HTML export of this notebook (`analysis.html`) is also provided for quick viewing. Additionally, a transcript of an accompanying video explanation is included (`transcript.txt`).

---

