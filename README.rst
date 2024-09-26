.. _bme68x:

BME68X: Gas Sensor
##################

.. contents::
   :local:
   :depth: 2

This sample application sets up the BME68X gas sensor with the Bosch Sensor Environmental Cluster (BSEC) library.

Requirements
************

To use the BME68X IAQ driver, you must manually download the BSEC library.
See the :ref:`bme68x_iaq` documentation for more details.

The sample supports the following devices:

.. table-from-sample-yaml::

Building and running
********************

This project outputs sensor data to the console.
It requires a BME68X sensor.

.. |sample path| replace:: :file:`samples/sensor/bme68x_iaq`

.. include:: /includes/build_and_run.txt
   
copy the folder files "Libs_to_put_in_ncs" in to the path ncs\v2.6.0\modules\lib

Testing
=======

After programming the sample to your development kit, test it by performing the following steps:

1. |connect_terminal|
#. Reset the kit.
#. Observe that output similar to the following is logged on UART:

   .. parsed-literal::
      :class: highlight

      *** Booting Zephyr OS build v3.2.99-ncs1-1531-gaf18f6b63608 ***
[00:41:19.313,873] <inf> app: temp: 30.570060; press: 92174.945312; humidity: 30.380367; iaq: 70; CO2: 636.225524; VOC: 0.613977
[00:41:22.318,695] <inf> app: temp: 30.562461; press: 92176.125000; humidity: 30.466053; iaq: 69; CO2: 634.266723; VOC: 0.607197
[00:41:25.323,516] <inf> app: temp: 30.554866; press: 92175.546875; humidity: 30.486797; iaq: 69; CO2: 633.748596; VOC: 0.605417
[00:41:28.328,338] <inf> app: temp: 30.554866; press: 92176.960937; humidity: 30.452066; iaq: 69; CO2: 633.978881; VOC: 0.606207
[00:41:31.333,160] <inf> app: temp: 30.564994; press: 92176.148437; humidity: 30.442623; iaq: 70; CO2: 635.522888; VOC: 0.611536
[00:41:34.337,982] <inf> app: temp: 30.567531; press: 92178.289062; humidity: 30.427658; iaq: 69; CO2: 633.961181; VOC: 0.606146
[00:41:37.342,803] <inf> app: temp: 30.694156; press: 92178.804687; humidity: 30.429019; iaq: 70; CO2: 636.038085; VOC: 0.613325
[00:41:40.347,656] <inf> app: temp: 31.256404; press: 92184.359375; humidity: 29.566469; iaq: 200; CO2: 1506.391357; VOC: 4.897916
[00:41:43.352,447] <inf> app: temp: 32.337844; press: 92173.531250; humidity: 28.986194; iaq: 349; CO2: 2519.351562; VOC: 48.699157
[00:41:46.357,269] <inf> app: temp: 32.596176; press: 92174.226562; humidity: 28.724224; iaq: 426; CO2: 3048.906738; VOC: 161.807952
[00:41:49.362,121] <inf> app: temp: 32.783596; press: 92178.539062; humidity: 28.592306; iaq: 458; CO2: 3278.104980; VOC: 272.083465
[00:41:52.366,943] <inf> app: temp: 32.401165; press: 92179.593750; humidity: 28.917455; iaq: 451; CO2: 3239.747558; VOC: 249.419250

.. note::
   BSEC takes about 24 hours to calibrate the indoor air quality (IAQ) output.

References
**********

`BME680`_
