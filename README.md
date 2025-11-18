# Android-TCF-Analysis-Data
This repository presents the raw datasets related to the research paper "Automatic Privacy Analysis and Compliance of TCF-based Android Applications".

## Description of the files
Hereby follows descriptions of the file contents.
### scraped_apps.csv
- Contains all the applications we scraped (packages and names)
  - *'Category'* describes the Google Play Store category the app was scraped from
  - *'Date'* states the date the app was scraped
### app_status.csv
- Contains the data gathered while downloading and analyzing the applications
  - *'Status'* describes whether the app uses the TCF or not, or if the app was not downloadable
  - *'Date'* states the date the app was downloaded from the Google Play Store
- Unattainable data is marked as '-'
### traffic_analysis_stage_1.csv
- Contains the data gathered from our first stage of traffic analysis (passive)
  - *'Request'* describes the HTTP request type, where the personal data was found (URL or payload), key related to the data (if any), the personal data itself
  - *'PD'* contains the type of the collected personal data (AAID or public_IP)
  - *'Analysis'* explains the related dynamic analysis approach (C+LI is **'All'**, Ø is **'Nothing'**, LI is **'LI'**)
  - *'Date'* states the collection date of the data.
- '60e5d787-7b10-4341-8289-a784280e7f1f' is our emulated device's AAID
- 'OUR_PUBLIC_IP' replaced our own public IP
### traffic_analysis_stage_2.csv
- Contains the data gathered from our second stage of traffic analysis (active)
  - Follows the same structure as traffic_analysis_stage_1
  - *'Analysis'* contains another option called **'Dialog Interaction'**, meaning data collected before or during dialog interaction 
