# Release Notes

## 0.1.2.4
- stable release for publication to TestFlight

### What To Test
- complete onboarding and confirm connections to Rivian account and the evaluation InfluxDB data source
    - Name: My Rivian Eval (AWS)
    - URL: https://us-east-1-1.aws.cloud2.influxdata.com
    - Bucket: my-rivian-eval
    - Org: My Rivian
    - Token: YinqPc7tH-BxQNSMtsMCvs8VZRIc2eX2qqQBfUUSlHbXIwN6uRBA3cq5w2iiX3tq_o_B9Rcs84jq-kU_ZUk8KA==
- record a test trip
    - place vehicle in Drive (or any non-Park gear)
    - from the Trips ddrop-down menu select 'Record Trip'
    - screen chnges to 'Trip Starting' and then to 'Trip'
    - verify elapsed timer is counting up and return the gear selector back to Park
    - after a short while the screen changes to 'Trip Ending' and the trip is logged
    - you will be returned to the Trips screen and show your first recorded trip
- record a test charge
    - plug in
    - from the Charges ddrop-down menu select 'Record Charge'
    - screen chnges to 'Charge Starting' and then to 'Charging'
    - use the Rivian app to stop charging
    - after a short while the screen changes to 'Charge Ending' and the charge is logged
    - you will be returned to the Charges screen and show your first recorded charge

### Known Issues
There are many known quirks but I have over 150 trips and 15 charges recorded so things basically work.  I do want to hear about any crashes or failed trips or charges.

One known limitation is the phone will not complete a trip or charge if My Rivian is not active, for trips this isn't much of a problem for trips since you are driving and it can cycle freely throu the recordibng trip states.  But for charges that go on for hours this might not be the case and the charge may not be recorded until you go back to the My Rivian app and see the charge end and be logged.
