# Release Notes

## 0.2.5.2
- Settings restore will trigger a refresh of the Trips/Chrgesviews
- the charge idle timer is now disabled by default (since charging does not yet have background mode support)
- added the timeout progress to the dyanmic island when waiting for a new trip to start
- improved map display when recording a trip (map top is now your heading)
- added rated distance to the Trips summary
- recorded trips/charges data store are now cached and written later if the initial write attempt failed

## 0.2.4.12
- retries starting CoreLocation live updates when no location updates are received within a few seconds (workaround)
- added time remaining to active charge screen
- location manager code clean up and single reverse geocoding symbol in status bar
- better auto sizing of data store/vehicle names for different iPhone screen sizes
- account credentials and OTP code auto verify during the login process
- added a 5 minute timeout to start a trip
- chain multiple trips if there is less than 5 minutes since the previous trip
- lock screen and dynamic island show trip start countdowns

## 0.2.4.10
- fix for long vehicle/data store names hidding the trip/charge menu button
- renamed default hosted data store to 'My Rivian' (shorter and less likely to be truncated)
- fix for missing range added field in charge detail
- fix for bug not detecting a DCFC charge
- added 5 minute record charge timeout
- added distance to empty tp logged charge data
- eliminated unnecessary refresh operations for trip/charge graphs
- added charge limit and distance to empty charging view

## 0.2.4.7
- removed unused speed code from trip recording
- fixed missing range added regression in recorded charges
- fix login bug when no name has been defined for a vehicle
- added model and exterior color to Rivian vehicle detail
- flush trips and charges after a data store restore operation
- fixed crash in Trips Monthly Efficiency when no trips were recorded
- removed Start At field in charge detail since the time is in the title
- - fixed typos and other minor issues
- reworked data store backup/restore to speed up save and restoring operations (but still too slow)
- dropped course and speed from supported DIDs since they aren't being used
- internal work on deleting trips/charges from the data store
- refresh trips/charges after vehicle or data store changes
- added LiveActivity and Dynamic Island support for recording trips and charges
- added the change in distance to empty in detailed trip view (compare to the actual distance)

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

## What To Test
1. Save your settings should you wish to restore them
2. Remove the My Rivian app and re-install from TestFlight (you will be logging to the hosted data store)
3. Complete onboarding and confirm connection to your Rivian account and the hosted InfluxDB data source
4. Record a trip to the hosted data store
    - place vehicle in Drive (or any non-Park gear)
    - from the Trips drop-down menu select 'Record Trip'
    - screen changes to 'Starting' and then to 'Trip'
    - verify elapsed timer is counting up and return the gear selector back to Park
    - after a short while the screen changes to 'Ending' and the trip is logged
    - you will be returned to the Trips screen and see your first recorded trip
    - send a screenshot using TestFlight to show you can record a trip
5. Record a charge to the hosted data store
    - enable settings to disable Charge idle timer 
    - plug in
    - from the Charges drop-down menu select 'Record Charge'
    - screen chnges to 'Starting' and then to 'Charging'
    - use the Rivian app to stop charging after a few minutes
    - after a short delay the screen changes to 'Ending' and the charge is logged
    - you will be returned to the Charges screen and see your first recorded charge
    - send a screenshot using TestFlight to show you can record a charge
6. Visit Settings.Vehicles, select your vehicle and then delete the vehicle data from the hosted data store
7. Restore your own data store(s) from your saved settings if necessary
