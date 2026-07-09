
# Solar Flare Analysis Pipeline: Multi-Instrument Data Downloader and Plotter

This repository contains Python scripts developed for the automated retrieval, processing, and multi-instrument visualization of Solar Flare data. The pipeline integrates data from **Fermi/GBM**, **Fermi/LAT**, and **GOES** satellites to generate comprehensive light curves.

## 🚀 Features
* **Automated Data Downloading:** Reads an input catalog of solar events, dynamically formats dates, and automatically fetches the required `.pha` (Fermi/GBM) files from the NASA HEASARC FTP server.
* **Multi-Instrument Light Curve Plotting:** Processes the downloaded FITS/PHA files and plots aligned light curves. It features:
  * Fermi/GBM counts across specific energy bands.
  * GOES X-ray fluxes (1.0–8.0 Å and 0.5–4.0 Å) and their derivatives.
  * Fermi/LAT counts (>100 MeV) binned effectively.
  * Peak time alignment and GOES class annotations.

## 📂 Repository Structure
* `notebooks/`: Contains the core Jupyter notebooks (`01_automated_data_downloader.ipynb` and `02_multi_instrument_plotter.ipynb`).
* `sample outputs/`: Contains generated high-resolution multipanel plots (PNG and PDF formats) showcasing the pipeline's final results.

## 🛠 Prerequisites
The scripts run on Python 3 and require the following libraries:
* `pandas`, `numpy`, `matplotlib`, `scipy`
* `astropy` (for FITS file handling)
* `requests` (for automated downloads)
* `reportlab`, `Pillow` (for PDF report generation)

## 📄 Output Example
The code generates stacked multipanel figures containing GBM rates, GOES flux, GOES flux derivative, and LAT counts, properly aligned to the flare's start, peak, and end times.
