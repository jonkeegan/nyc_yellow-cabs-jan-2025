# nyc_yellow-cabs-jan-2025
NYC TLC data for yellow cab rides in January 2025

These records are generated from the trip record submissions made by yellow taxi Technology Service Providers (TSPs). Each row represents a single trip in a yellow taxi. The trip records include fields capturing pick-up and drop-off dates/times, pick-up and drop-off taxi zone locations, trip distances, itemized fares, rate types, payment types, and driver-reported passenger counts.

Data source: (https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page)[https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page]
Orignal data derived from PARQUET file: https://d37ci6vzurychx.cloudfront.net/trip-data/yellow_tripdata_2025-01.parquet

## Data dictionary

| Field Name | Description |
|---|---|
| VendorID | TPEP provider: 1 = Creative Mobile Technologies, 2 = Curb Mobility, 6 = Myle Technologies, 7 = Helix |
| tpep_pickup_datetime | Date and time when the meter was engaged |
| tpep_dropoff_datetime | Date and time when the meter was disengaged |
| passenger_count | Number of passengers in the vehicle |
| trip_distance | Elapsed trip distance in miles reported by the taximeter |
| RatecodeID | Final rate code: 1 = Standard, 2 = JFK, 3 = Newark, 4 = Nassau/Westchester, 5 = Negotiated, 6 = Group ride, 99 = Unknown |
| store_and_fwd_flag | Whether record was held in vehicle memory before sending: Y = store and forward, N = not store and forward |
| PULocationID | TLC Taxi Zone where the taximeter was engaged |
| DOLocationID | TLC Taxi Zone where the taximeter was disengaged |
| payment_type | Payment method: 0 = Flex Fare, 1 = Credit card, 2 = Cash, 3 = No charge, 4 = Dispute, 5 = Unknown, 6 = Voided |
| fare_amount | Time-and-distance fare calculated by the meter |
| extra | Miscellaneous extras and surcharges |
| mta_tax | Tax automatically triggered based on metered rate in use |
| tip_amount | Tip amount (credit card only; cash tips not included) |
| tolls_amount | Total amount of all tolls paid in trip |
| improvement_surcharge | Surcharge assessed at flag drop, levied since 2015 |
| total_amount | Total amount charged to passengers (excludes cash tips) |
| congestion_surcharge | Amount collected for NYS congestion surcharge |
| airport_fee | Pickup fee at LaGuardia and JFK airports only |
| cbd_congestion_fee | Per-trip charge for MTA Congestion Relief Zone (starting Jan 5, 2025) |
| PU_Zone | Taxi zone lookup for PULocationID |
| DO_Zone | Taxi zone lookup for DOLocationID |
