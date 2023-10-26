# Release Notes

## 0.2.2.1
- restored missing min/max elevation on trips

### What To Test
- complete onboarding and confirm connection to your Rivian account and the hosted InfluxDB data source
- record a trip
    - place vehicle in Drive (or any non-Park gear)
    - from the Trips drop-down menu select 'Record Trip'
    - screen changes to 'Starting' and then to 'Trip'
    - verify elapsed timer is counting up and return the gear selector back to Park
    - after a short while the screen changes to 'Ending' and the trip is logged
    - you will be returned to the Trips screen and see your first recorded trip
    - swipe left on the trip to delete it and try recording a real trip
- record a charge
    - plug in
    - from the Charges ddrop-down menu select 'Record Charge'
    - screen chnges to 'Starting' and then to 'Charging'
    - use the Rivian app to stop charging after a few minutes
    - after a short delay the screen changes to 'Ending' and the charge is logged
    - you will be returned to the Charges screen and see your first recorded charge
    - swipe left on the charge to delete it and try recording a real charge

### Known Issues
- The new iOS 17 CoreLocation live updates sometimes falls behind and updates lag the actual device position, when this occurs the path for the end of the trip will be a straight line from the last received location update to the trip end point.

## 0.2.2.1
- fixed bug in data store test command

## 0.2.1.5
- merged location live update events to try and solve occasional lagging updates
- modified onboarding to use a hosted data store, add your own datra store in Settings after confirming correct operation

## 0.2.1.4
- cached location dids to be written with the vehicle dids
- saves vehicle list so no delay when app starts to retrieve the list from Rivian (will require logging back into your account) 

## 0.2.1.3
- added moving map view to trip recording to display the reported device location (see known issues for details)
- fixed trips/charges lists to only reload from data store when the period changes or a refresh action was requested

## 0.2.1.2
- fix for charge recording to continue when not in the foreground
- added settings to disable the idle timeout for trips and charges (Settings.General)
- now store vehicle GPS and device GPS data and select which is used for the trip path display
- added maximum power field to charge detail display

## 0.2.1.1 (internal)
- remove course values of -1
- fix for trip recording to continue when not in the foreground
