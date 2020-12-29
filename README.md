# FreeRTOS_STM32F411_BMP280_AutoZero

-This FreeRTOS programs uses C programming language that enables the STM32 mcu to get the pressure data from the BMP280 sensor through I2C communication channel.

-A reference pressure value is used as a fixed variable, which in my case I used the SEA_LEVEL_PRESSURE = 1013.23f.

-The pressure (hpa) will be zero if the relative pressure value is less than 0.07, indicating it has return to the reference point.

-Positive changes means the device is going downwards where the relative pressure value would be >= 0.8

-Negative changes means the device is going upwards where the relative pressure value would be < 0.8

-These value were tested based on the location that I am sitting that time. It may differs from location to location.


-The Test Data in Excel file is the movement data from Ground floor up to 3rd floor and lastly stopped at 1st floor.


## Requirements

 **1 STM32F411**
  
 **2 BMP280**
  
 **3 STM32CUBEMX**
  
 **4 Keil/Eclipse  (I'm using Keil)**


## How to use this
You need to build the project using stm32cubemx software.
I had provided the .ioc file for this purpose

Utilize the Inc and Src files.


## Data Logger using Keil

The alt_log.Ini file is a logger file that capture average pressure and relative pressure. You may change this accordingly.

## How to Use Data Logger in Keil

**1.	Connect the device as usual and get into debug mode**

**2.	Go to debug - Function Editor (ini file) - choose the file that I gave**

**3.	Compile the function**

**4.	Type in the name of function “pressure_log()” into Kiel’s console & press enter**

**5.	Run debugger**


