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
- Rivian R1T or R1S
- an optional InfluxDB data store to host the collected vehicle data should you not use the default data store provided with **My Rivian** (you can create your own at [Influx Cloud](https://cloud2.influxdata.com/signup))

<a id='installation'></a>
## Installation
The beta test releases are being distributed using the Apple TestFlight application.  If you receive an invitation or have access to a shared download link you can install **My Rivian** from the TestFlight app and share crash reports and screenshots to help improve the software.

<a id='privacy'></a>
## Privacy Notice
**My Rivian** collects location information that is used to show trips you have taken and where you have charged your vehicle.  **My Rivian** does not collect or share any other personal information or data.

**My Rivian** uses a unique Rivian vehicle identifer to identify your trips and charges in a personal data store that you create and control.  If you choose to use a shared data store, typically for evaluation and/or testing purposes, then your past location and other vehicle data could be viewed by anyone with access to the same data store.

<a id='trips'></a>
## Trips
The Trips tab displays a list of the trips made in a selected time period along with a summary of the distance and evergy used:

![image](https://github.com/my-rivian/my-rivian/assets/142558992/dbb4ec6b-83c5-4cfb-829b-3006a4075740)

Use the drop down menu in the upper right corner to view trip summaries or to record a new trip:

![image](https://github.com/my-rivian/my-rivian/assets/142558992/53399047-3b8b-4389-ada6-b4b76120ed1a)

Or select a trip from the list and view the trip details including:
- the trip path displayed on a map
- the elevation profile of the trip
- distance traveled and range consumed
- start and end points with the ability to add point of interest (POI) details
- energy used to complete the trip

![image](https://github.com/my-rivian/my-rivian/assets/142558992/0a53f3f5-3a00-4770-a8bd-191d66bcb622)

Even more trip details is available from the drop down menu, such as weather conditions during the trip:

![image](https://github.com/my-rivian/my-rivian/assets/142558992/b5760630-b097-47e2-a57e-7e0f5fd943ac)

<a id='charges'></a>
## Charges
The Charges tab displays a list of charges in the selected period along with the energy added to your Rivian:

![image](https://github.com/my-rivian/my-rivian/assets/142558992/28a36db8-cf94-4c03-a8d7-91a2221880d2)

You can select a charge from the Charges list and see the details of the charge, including:
- location, duration, and charger type
- power and energy data
- high voltage battery details such as the State pf Charge (SoC)

![image](https://github.com/my-rivian/my-rivian/assets/142558992/4167ded9-a358-42cd-a724-dcd2ed295fcc)

<a id='settings'></a>
## Settings
The Settings tab manages the selection of vehicles, data stores, and other useful features including:
- save/restore settings
- manage data stores
- manage vehicles
- manage location data
- help for various **My Rivian** features
- **My Rivian** version and other application information

![image](https://github.com/my-rivian/my-rivian/assets/142558992/abbc8f80-4a84-4358-9095-0479607224a9)

