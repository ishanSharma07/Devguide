# Modules Reference: Distance Sensor (Driver)
## sf1xx
Source: [drivers/distance_sensor/sf1xx](https://github.com/PX4/Firmware/tree/master/src/drivers/distance_sensor/sf1xx)


### Description

I2C bus driver for Lightware SFxx series LIDAR rangefinders: SF10/a, SF10/b, SF10/c, SF11/c, SF/LW20.

Setup/usage information: https://docs.px4.io/en/sensor/sfxx_lidar.html

### Examples

Attempt to start driver on any bus (start on bus where first sensor found).
```
sf1xx start -a
```
Stop driver
```
sf1xx stop
```

### Usage {#sf1xx_usage}
```
sf1xx <command> [arguments...]
 Commands:
   start         Start driver
     [-a]        Attempt to start driver on all I2C buses
     [-b <val>]  Start driver on specific I2C bus
                 default: 1
     [-R <val>]  Sensor rotation - downward facing by default
                 default: 25

   stop          Stop driver

   test          Test driver (basic functional tests)

   reset         Reset driver

   info          Print driver information
```
## teraranger
Source: [drivers/distance_sensor/teraranger](https://github.com/PX4/Firmware/tree/master/src/drivers/distance_sensor/teraranger)


### Description

I2C bus driver for TeraRanger rangefinders.

The sensor/driver must be enabled using the parameter SENS_EN_TRANGER.

Setup/usage information: https://docs.px4.io/en/sensor/rangefinders.html#teraranger-rangefinders

### Examples

Start driver on any bus (start on bus where first sensor found).
```
teraranger start -a
```
Start driver on specified bus
```
teraranger start -b 1
```
Stop driver
```
teraranger stop
```

### Usage {#teraranger_usage}
```
teraranger <command> [arguments...]
 Commands:
   start         Start driver
     [-a]        Attempt to start driver on all I2C buses (first one found)
     [-b <val>]  Start driver on specific I2C bus
                 default: 1
     [-R <val>]  Sensor rotation - downward facing by default
                 default: 25

   stop          Stop driver

   test          Test driver (basic functional tests)

   reset         Reset driver

   info          Print driver information
```