## api/monitoring/status


#### ConnectionStatus
Status of GSM connection
Possible values: 1, 900, 901, 902, 903

    MACRO_CONNECTION_CONNECTING = "900";
    MACRO_CONNECTION_CONNECT = "901";
    MACRO_CONNECTION_DISCONNECT = "902";
    MACRO_CONNECTION_DISCONNECTING = "903";
    MACRO_CONNECTION_ROAMING = "1";

#### SignalStrength
GSM signal strength
Possible values: 0-100

Value is divided by 20 and then casted to int to get values from range 0-5:
* 0 - no signal
* 1-3 - signal weak
* 4-5 - signal strong

#### CurrentNetworkType


#### CurrentServiceDomain

#### RoamingStatus
Status of roaming
Possible values: 0, 1

* 0 - no roaming
* 1 - roaming

#### BatteryStatus
Status of battery
Possible values: -1, 0, 1

    MACRO_BATTERY_STATUS_NORMAL = "0";
    MACRO_BATTERY_STATUS_ELECT = "1";
    MACRO_BATTERY_STATUS_CHARGING_INIT = "-1";

#### BatteryLevel
Battery level
Possible values: -1-4

    MACRO_BATTERY_LEVEL_LOW = "-1";
    MACRO_BATTERY_LEVEL_ZERO = "0";
    MACRO_BATTERY_LEVEL_ONE = "1";
    MACRO_BATTERY_LEVEL_TWO = "2";
    MACRO_BATTERY_LEVEL_THREE = "3";
    MACRO_BATTERY_LEVEL_FOUR = "4";

#### SimlockStatus


#### WanIPAddress
IP address of WAN interface

#### PrimaryDns
Primary DNS IP address

#### SecondaryDns
Secondary DNS IP address

#### CurrentWifiUser
Number of currently connected devices

#### TotalWifiUser
Maximal number of connected devices

#### ServiceStatus ?
Possible values: 2

#### SimStatus

    MACRO_SIM_STATUS_USIM_N = "0";
    MACRO_SIM_STATUS_USIM_Y = "1";
    MACRO_SIM_STATUS_USIM_CS_N = "2";
    MACRO_SIM_STATUS_USIM_PS_N = "3";
    MACRO_SIM_STATUS_USIM_PS_CS_N = "4";
    MACRO_SIM_STATUS_ROMSIM = "240";
    MACRO_SIM_STATUS_USIM_NE = "255";

#### WifiStatus
Status of WiFi
Possible values: 0, 1

    MACRO_WIFI_OFF = "0";
    MACRO_WIFI_ON = "1";

## api/monitoring/checknews

   <items>
     <item>
       <NewsType>0</NewsType>
     </item>
   </items>

NewsType posible values:
* 0 - no message
* 3012, 3050 - firmware/software update?
* 1001 - new message, not SMS?

## api/monitoring/traffic-statistics


#### CurrentConnectTime
#### CurrentUpload
#### CurrentDownload
#### CurrentDownloadRate
#### CurrentUploadRate
#### TotalUpload
#### TotalDownload
#### TotalConnectTime

api/monitoring/clear-traffic - save

api/sms/sms-count
api/sms/sms-list

api/language/current-language - get and save

api/wlan/station-information
api/wlan/basic-settings
api/wlan/security-settings
api/wlan/multi-basic-settings
api/wlan/host-list

api/dialup/connection
api/dialup/auto-apn
api/dialup/profiles
api/dialup/dial - save

api/pin/status
api/pin/simlock
api/pin/verify-simlock - save
api/pin/operate - save
api/pin/save-pin - save

api/user/login - save
api/user/logout - save

configurations/language.xml
configurations/optional_feature.xml

language/lang_LANG_CODE.js


## Error codes
* code - message
* 100002 - Request not support - Jeśli podano zły adres do API lub nie ma uprawnień na poziomie firmware
* 100005 -  - brak opisu, być może brak uprawnień
* 100006 - Wrong parameter - Prawdopodobnie zły (lub brakujący) parametr przy zapisie

>100009</code><message>Save parameter fail</messa
