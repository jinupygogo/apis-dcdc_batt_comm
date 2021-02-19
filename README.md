# apis-dcdc_batt_comm

## Introduction
The dcdc_batt_comm component is a Device Driver for actual control of hardware to implement energy sharing according to instructions from apis-main. The controlled DC/DC Converter is assumed to be the TDK-Lambda EZA2500(EZA-2500-32048SC0), with communication using the proprietary TDK Lambda protocol via RS485. The battery to be controlled is designed for communication using the Modbus RTU communication protocol via RS485. Communication with apis-main is accomplished via a Web API developed by Sony CSL and implemented on a Python Bottle Web server running on dcdc_batt_comm. 

![dcdc_batt_comm](https://user-images.githubusercontent.com/71874910/94906900-40b64200-04da-11eb-84b5-1134cd3d6b36.PNG)

## Installation

Here is how to install apis-dcdc_batt_comm individually.   

```bash
$ git clone https://github.com/SonyCSL/apis-dcdc_batt_comm.git
$ cd apis-dcdc_batt_comm
$ python3 -m venv venv
$ . venv/bin/activate
$ sudo pip3 install -r requirements.txt
$ deactivate
```

## Running

Here is how to run apis-dcdc_batt_comm individually.  

*By default, 2 USB-RS485 converters are required for /dev/ttyUSB0 and /dev/ttyUSB1.  
See apis-dcdc_batt_comm's [Document](https://github.com/SonyCSL/apis-dcdc_batt_comm/blob/master/doc/jp/apis-dcdc_batt_comm_specification.md) for more information.

```bash
$ cd apis-dcdc_batt_comm
$ . venv/bin/activate
$ cd drivers
$ sudo python3 essx_server.py
```

## Stopping
Here is how to stop apis-dcdc_batt_comm individually.  

```bash
$ cd apis-dcdc_batt_comm/drivers
$ bash stop.sh
$ deactivate
```


## Documentation
&emsp;[apis-dcdc_batt_comm_specification(EN)](https://github.com/SonyCSL/apis-dcdc_batt_comm/blob/master/doc/en/apis-dcdc_batt_comm_specification_en.md)  
&emsp;[apis-dcdc_batt_comm_specification(JP)](https://github.com/SonyCSL/apis-dcdc_batt_comm/blob/master/doc/jp/apis-dcdc_batt_comm_specification.md)


## License
&emsp;[Apache License Version 2.0](https://github.com/SonyCSL/apis-dcdc_batt_comm/blob/master/LICENSE)


## Notice
&emsp;[Notice](https://github.com/SonyCSL/apis-dcdc_batt_comm/blob/master/NOTICE.md)
