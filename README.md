# My Rivian

## Table of Contents
- [Overview](#overview)
- [Requirements](#requirements)
- [Installation](#installation)
- [Privacy Notice](#privacy)
- [Trips](#trips)
- [Charges](#charges)
- [Settings](#settings)

<a id='overview'></a>
## Overview
**My Rivian** is a iPhone application for logging the trips and charges of your Rivian R1T/R1S.

<a id='requirements'></a>
## Requirements
- Apple iPhone running iOS 17.0 or later
- InfluxDB data store to supply vehicle data (you can create your own at [Influx Cloud](https://cloud2.influxdata.com/signup))

<a id='installation'></a>
## Installation
The beta test releases are being distributed using the Apple TestFlight application.  If you receive an invitation or have access to a shared download link you can install **My Rivian** from the TestFlight app and share crash reports and screenshots to help improve the software.

<a id='privacy'></a>
## Privacy Notice
**My Rivian** collects location information that is used to show trips you have taken and where you have charged your vehicle.  **My Rivian** does not collect or share any other personal information or data.

**My Rivian** uses a cryptographic hash to uniquely identify your trips and charges in a personal data store that you create and control.  If you choose to use a shared data store, typically for evaluation and/or testing purposes, then your location and other vehicle data could be viewed by anyone with access to the same data store.

<a id='trips'></a>
## Trips
The Trips tab displays a list of the trips made in a selected time period along with a summary of the distance and evergy used.

Each recorded trip can view detailed trip data specific to the trip, including:
- the trip path displayed on a map
- the elevation profile of the trip
- start and end points with the ability to add point of interest (POI) details
- energy used to complete the trip

<a id='charges'></a>
## Charges
The Charges tab displays a list of charges in the selected period along with the energy added to your Rivian.

You can select a charge from the Charges list and see the details of the charge, including:
- location, duration, and charger type
- power and energy data
- high voltage battery details such as the State pf Charge (SoC)

<a id='settings'></a>
## Settings
The Settings tab manages the selection of vehicles, data stores, and other useful features including:
- save/restore settings
- manage data stores
- manage vehicles
- manage location data
- help for various **My Rivian** features
- **My Rivian** version and other application information
