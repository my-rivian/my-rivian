# Release Notes

## 0.2.3.6
- reverted charge recoding back to original deisgn (requires foreground operation for now)
- improved charge detail menu since it only has one item in it
- onboarding/login improvements
- use delegates to update vehicle/data store names in settings feature
- now supports multiple vehicles (if anyone has two R1s please try this out)
- changed trip elevation code to use the trip ID and not the trip start/end times
- added vehicle odometer/SoC/battery capacity to the vehicle inspector
- added Rivian account 2FA support
- trips/charges refresh only on completed trip/charge
- updated help screens
- fixed POI not presented for trip starting location bug
- allow deletion of trips/charges by vehicle from current data store (Settings.Vehicles)
- reduced trips/charges summary field height by incorporating the count in the disclosure group text
- fixed unneeded trip/charge refresh after using local menu
- set reasonable default settings
    - General: Metric (false)
    - General: Use Vehicle For Path Data: (false)
    - General: Disable Trip Idle Timer (false)
    - General: Disable Charge Idle Time (false)
    - General.Map Styles: Use Trip Map Type (standard)
    - General.Map Styles: Use Charge Map Type (standard)
    - General.Points Of Interest: Threshold (50m or 164')
    - General.Advanced: Path Threshold (5m or 16')
    - General.Advanced: Pretty Print Backups (true)
- trElevationStart/trElevationEnd missing from data store regression fixed
- cleaned up trip/charges/did types
- changing data store will now reload trips/charges from the new data store
- updated Rivian API login errors with better diagnostic
- invalidate trips/charges when Rivian account is logged out

## 0.2.2.3
- updated to TCA 1.3

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

## 0.2.2.2
- restored missing min/max elevation on trips

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
