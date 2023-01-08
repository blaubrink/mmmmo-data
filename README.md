# MMMMO Data
MMMMO (Metchild's Medieval Mystical Manuscripts Online) is a project that aims to visualize the handwritten tradition of the *Liber Specialis Gratiae* by Mechtilde of Hackeborn on an interactive map. The map can be accessed fia the following URL: https://helftamysticism.org.

This repository holds all the data that is displayed on [helftamysticism.org](https://helftamysticism.org). This includes all manuscripts and their locations, the libraries they are kept in today and the info texts displayed in the sidebar.

## Documentation

### Manuscripts
Manuscripts are divided into five csv files, one for each possible language category of the particular text:

1. Upper German
2. Middle German
3. Lower German and Dutch
4. Latin
5. Other languages

Each manuscript corresponds to an entry in one of the csv files. For each manuscript there is the following information:

- **id:** Unique ID that consists of a shorthand for the language and a consecutive number. Multiple entries for the same manuscript can be made (for example if the location changed at a later time) by appending a consecutive letter (i.e. "od1a", "od1b" etc.).
- **year:** Year of origin. Timespans (i.e. "15th century" or "1400-1500") are not recognized. In these cases a mean value must be determined.
- **order:** A selection of monastic orders to show the possession of the manuscript. The possible choices can be seen by accessing the filter options in the taskbar of the map.
- **library:** The library or archive where this manuscript is kept today. Must previosly be defined in `06-Bibliotheken.csv`
- **category (desc)**: Free text  field displayed in the sidebar. It is possible to enter a category for the manuscript (i.e. to tell that is is a prayer book or an anthology).
- **date (desc):** Free text field displayed in the sidebar. Can therefore also be used to state timespans or estimations.
- **location (desc):** Free text field displayed in the sidebar to describe the location of this manuscript.
- **extract (desc):** Free text field displayed in the sidebar to indicate which parts of the *Liber* have been transmitted to this manuscript.
- **description:** Free text field displayed in the sidebar for any other notes regarding this manuscript.
- **hsc, catalog and digital copy:** References to the HSC entry, the catalog or a digital copy of this manuscript. Entries starting with `http` will automatically be displayed as links.
- **additional info:** Additional links or references regarding this manuscript.
- **origin:** In case it can clearly be determined which source this manuscript is derived from, the ID of the source manuscript can be entered here.
- **radius:** In ace the location for this manuscrit can only be estimated, the entry can be given a radius (in kilometres) that will be displayed on the map.
- **long and lat:** Longitude and latitude for the position of the marker of this manuscript on the map. Rounded to max. four decimal places.

### Libraries

For each manuscript a library must be assigned where the manuscript can be found today. All assigned libraries must be defined in `06-Bibliotheken.csv`.

- **name:** Name of the library. Must exactly match the library name that is assigned to one or multiple manuscripts.
- **long and lat:** Longitude and latitude for the position of the marker of this library on the map. Rounded to max. four decimal places.

## How to contribute

### Via pull request

In case you want to contribute by adding new data or updating existing data, you can do so by creating a pull request. To do so, follow these steps:

1. Fork this repository to your own GitHub account.
2. Make your changes by editing the csv files.
3. Commit your changes to your repository.
4. Create a pull request from your repository back to this one.

Your pull request will be reviewed and once it has been approved, your changes will be merged and appear on the map afterwards.

### Via email

In case you are not familiar with GitHub, but want to inform the authors of this project about missing, outdated, or incorrect information, you can send a message to the following email address:

[mailto:linus.ubl@mod-langs.ox.ac.uk](linus.ubl@mod-langs.ox.ac.uk)

## Usage of this data

This project is published under the GPL-3.0 license. This means that you can distribute, modify and use this data to your liking. Please refer to the license to learn about the conditions that apply.
