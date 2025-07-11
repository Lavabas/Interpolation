# Temporal Interpolation for EO Products using Python API (Xee)
## 🌍 Overview

This project demonstrates **temporal interpolation** of Earth Observation (EO) data using Python, [Google Earth Engine (GEE)](https://earthengine.google.com/), and the [Xee library](https://pypi.org/project/xee/). The goal is to generate **annually continuous datasets** from EO products that are originally provided only for a **few discrete years**. 

In this example, the **GHS-BUILT-S** dataset (representing built-up surface area from the JRC GHSL project) is used. The built-up data is originally only available for selected years (e.g., 2010, 2015, 2020). This project fills in the missing years between 2010 and 2020 using **linear interpolation**.

### Original GHS-BUILT-S Data (Sparse Temporal Coverage)
- Built-up surface data available only for select years (e.g., 2010, 2015, 2020), highlighting the need for temporal interpolation.
<img width="1177" height="396" alt="Screenshot (246)" src="https://github.com/user-attachments/assets/d1ac1d9c-5bcf-4819-903c-fa07ba9820d2" />

### Interpolated Annual Built-up Surface (2010–2020)
- Linearly interpolated yearly data showing smooth annual variation in built-up area, enabling consistent time series analysis.
<img width="1920" height="1080" alt="Screenshot (247)" src="https://github.com/user-attachments/assets/074d74a0-1eb3-418e-8430-94b1cb961e00" />

### Comparison of Original vs Interpolated Built-up Area
Time series plot comparing the original sparse data (blue) with interpolated values (red), showing how interpolation fills in the temporal gaps.
<img width="774" height="396" alt="Screenshot (248)" src="https://github.com/user-attachments/assets/4ed799f2-ba16-4d6a-ba5d-2800e2ee0f09" />

## 🔍 Key Objectives

- Extract EO data using the `xee` engine, directly from Earth Engine.
- Perform **temporal interpolation** to create a consistent **annual time series**.
- Visualize and analyze urban expansion trends over time.
- Demonstrate a generalized Python-based approach that works for **any temporally sparse EO dataset**.


## 📦 EO Data Used

- **Dataset**: [JRC GHS-BUILT-S (P2023A)](https://developers.google.com/earth-engine/datasets/catalog/JRC_GHSL_P2023A_GHS_BUILT_S)
- **Variable**: `built_surface` – proportion of built-up surface area (0–100%)
- **Available Years** in source: typically 2000, 2005, 2010, 2015, 2020
- **Interpolated Years** in this project: 2010–2020 (annually)


## 📌 Notes
- This workflow is generalizable. You can replace the built_surface data with any other EO product (e.g., vegetation indices, land cover, surface water, etc.) that has irregular time intervals.
- Interpolation is linear by default, but other methods (cubic, nearest, etc.) can be used depending on your needs.
- Useful for converting sparse EO datasets into time-consistent inputs for ML models, statistical trend analysis, or visual storytelling.





