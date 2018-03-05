# GPS readlast
## Behavior
The ```readlast``` command will be polled in ```POLL_GPS_1```, ```POLL_GPS_2```, ```GPS_READING```, and ```GPS_RESULTS```. If a GPS reading was taken that is within ```gps_desired_accuracy``` and more than ```gps_max_elapsed_time``` has not passed then these values will be used when the user is prompted to take a GPS reading. From the users perspective the GPS reading will appear to be instantaneous. However, if no usable GPS values are collected during the polling phase then the ```read``` command will be used to take a new reading. If a new reading within ```gps_desired_accuracy``` cannot be attained then the GPS values from any successful read will be used.
## Dictionary variables
Note that *Decimal Char* was set to *Yes* for any value with a decimal part. This states the decimal point will be present in the data file and adds to the length of the numeric.
* Latitude
    * Length: 10
        * Sign: 1
        * Integer part: 2
        * Decimal point: 1
        * Decimal part: 6
            * The sixth decimal place is worth up to 11 cm of granularity
* Longitude
    * Length: 11
        * Sign: 1
        * Integer part: 3
        * Decimal point: 1
        * Decimal part: 6
            * The sixth decimal place is worth up to 11 cm of granularity
* Altitude
    * Length: 7
        * Sign: 1
        * Integer part: 4
        * Decimal point: 1
        * Decimal part: 1
            * The first decimal place is worth up to 10 cm of granularity
* Accuracy
    * Length: 6
        * Integer part: 4
        * Decimal point: 1
        * Decimal part: 1
            * The first decimal place is worth up to 10 cm of granularity
* Satellites
    * Length: 3
        * Integer part: 3
* Readtime
    * Length: 6
        * Integer part: 6
