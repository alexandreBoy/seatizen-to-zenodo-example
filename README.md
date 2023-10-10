<div align="center">

# seatizen-to-zenodo-example


</div>
</br>

This repository contains a datarmor use case example for the [seatizen-to-zenodo](https://github.com/IRDG2OI/seatizen-to-zenodo) tool.

By using, in the same order, the configurations listed in the three folders with your own paths, you will:

1. Make a copy of your sessions to another folder. <br/>
:warning: Don't forget to complete the source and destination paths in the main() function of **copy_folders.py**!
2. Create zipped files of folders located in each raw session for the restricted deposit.
3. i. (omp queue) Prepare the public deposit with: <br/>

    - Jacques classification
    - Deletion of folders BEFORE/AFTER/USELESS
    - Creation of zipped files of folders located in each session
    - Creation of metadata_image.csv and metadata_image_stats.txt

    ii. (ftp queue) Create data previews: <br>

    - Creation of a map with all images location
    - Creation of PDF previews

You should then have a file tree that looks like this:
```
public_deposit
│
└───YYYYMMDD_countrycode-optionalplace_device_nb
│   └───000_YYYYMMDD_countrycode-optionalplace_device_nb_preview.pdf
│   └───DCIM_THUMBNAILS.zip
│   └───GPS.zip
│   └───METADATA.zip
│   └───PROCESSED_DATA.zip
│   └───SENSORS.zip
│
└───YYYYMMDD_countrycode-optionalplace_device_nb
│   └───000_YYYYMMDD_countrycode-optionalplace_device_nb_preview.pdf
│   └───DCIM.zip
│   └───DCIM_THUMBNAILS.zip
│   └───GPS.zip
│   └───METADATA.zip
│
restricted_deposit
│
└───YYYYMMDD_countrycode-optionalplace_device_nb
│   └───DCIM.zip
│   └───DCIM_THUMBNAILS.zip
│   └───GPS.zip
│   └───METADATA.zip
│   └───PROCESSED_DATA.zip
│   └───SENSORS.zip
│
└───YYYYMMDD_countrycode-optionalplace_device_nb
│   └───DCIM.zip
│   └───DCIM_THUMBNAILS.zip
│   └───GPS.zip
│   └───LABEL.zip
│   └───METADATA.zip
│
global_data
│   └───000_global_map.png
│   └───metadata_image.csv
│   └───metadata_image_stats.txt
```
---
<div align="center">

This project is being developed as part of the G2OI project, cofinanced by the European union, the Reunion region, and the French Republic.

<img src="https://github.com/IRDG2OI/seatizen-to-zenodo/blob/main/docs/logos_partenaires.png?raw=True" height="40px">

</div>