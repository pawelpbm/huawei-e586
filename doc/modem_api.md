## api/monitoring/status
Only GET

    <response>
      <ConnectionStatus>901</ConnectionStatus>
      <SignalStrength>100</SignalStrength>
      <CurrentNetworkType>4</CurrentNetworkType>
      <CurrentServiceDomain>3</CurrentServiceDomain>
      <RoamingStatus>0</RoamingStatus>
      <BatteryStatus>1</BatteryStatus>
      <BatteryLevel>4</BatteryLevel>
      <SimlockStatus>0</SimlockStatus>
      <WanIPAddress>127.0.0.1</WanIPAddress>
      <PrimaryDns>8.8.8.8</PrimaryDns>
      <SecondaryDns>8.8.4.4</SecondaryDns>
      <CurrentWifiUser>5</CurrentWifiUser>
      <TotalWifiUser>5</TotalWifiUser>
      <ServiceStatus>2</ServiceStatus>
      <SimStatus>1</SimStatus>
      <WifiStatus>1</WifiStatus>
    </response>

#### ConnectionStatus
Status of GSM connection<br>
Possible values: 1, 900, 901, 902, 903

    MACRO_CONNECTION_CONNECTING = "900";
    MACRO_CONNECTION_CONNECT = "901";
    MACRO_CONNECTION_DISCONNECT = "902";
    MACRO_CONNECTION_DISCONNECTING = "903";
    MACRO_CONNECTION_ROAMING = "1";

#### SignalStrength
GSM signal strength<br>
Possible values: 0-100<br>
Value is divided by 20 and then casted to int to get values from range 0-5

    0 - no signal
    1-3 - signal weak
    4-5 - signal strong

#### CurrentNetworkType
GSM network type<br>
Possible values: 0-12

    0 - no_service
    1 - gsm
    2 - gprs
    3 - edge
    4 - wcdma
    5 - hsdpa
    6 - hsupa
    7 - hspa
    8 - scdma
    9 - hspa_plus
    10 - evdo0
    11 - evdoa
    12 - evdob

#### CurrentServiceDomain
TODO<br>
Possible values: 0, 3, 4

    0 - network searching?
    4 - network searching


#### RoamingStatus
Status of roaming<br>
Possible values: 0, 1

    0 - no roaming
    1 - roaming

#### BatteryStatus
Status of battery<br>
Possible values: -1, 0, 1

    MACRO_BATTERY_STATUS_NORMAL = "0";
    MACRO_BATTERY_STATUS_ELECT = "1";
    MACRO_BATTERY_STATUS_CHARGING_INIT = "-1";

#### BatteryLevel
Battery level<br>
Possible values: -1-4

    MACRO_BATTERY_LEVEL_LOW = "-1";
    MACRO_BATTERY_LEVEL_ZERO = "0";
    MACRO_BATTERY_LEVEL_ONE = "1";
    MACRO_BATTERY_LEVEL_TWO = "2";
    MACRO_BATTERY_LEVEL_THREE = "3";
    MACRO_BATTERY_LEVEL_FOUR = "4";

#### SimlockStatus
TODO

#### WanIPAddress
IP address of WAN interface

#### PrimaryDns
Primary DNS IP address

#### SecondaryDns
Secondary DNS IP address

#### CurrentWifiUser
Number of currently connected devices

#### TotalWifiUser
Maximum number of connected devices

#### ServiceStatus
TODO<br>
Possible values: 2

#### SimStatus
TODO

    MACRO_SIM_STATUS_USIM_N = "0";
    MACRO_SIM_STATUS_USIM_Y = "1";
    MACRO_SIM_STATUS_USIM_CS_N = "2";
    MACRO_SIM_STATUS_USIM_PS_N = "3";
    MACRO_SIM_STATUS_USIM_PS_CS_N = "4";
    MACRO_SIM_STATUS_ROMSIM = "240";
    MACRO_SIM_STATUS_USIM_NE = "255";

#### WifiStatus
Status of WiFi<br>
Possible values: 0, 1

    MACRO_WIFI_OFF = "0";
    MACRO_WIFI_ON = "1";

## api/monitoring/checknews
Only GET

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
TODO

#### CurrentConnectTime
#### CurrentUpload
#### CurrentDownload
#### CurrentDownloadRate
#### CurrentUploadRate
#### TotalUpload
#### TotalDownload
#### TotalConnectTime

## api/monitoring/clear-traffic - save
TODO

## api/sms/sms-count

* LocalUnread - Number of SMS messages on device that are unread
* LocalInbox - Number of SMS messages on device that are in Inbox
* LocalOutbox - Number of SMS messages on device that are in Outbox
* LocalDraft - Number of SMS messages on device that are saved as Draft
* LocalDeleted - Number of deleted SMS messages on device
* SimUnread - Number of SMS messages on SIM that are unread
* SimInbox - Number of SMS messages on SIM that are in Inbox
* SimOutbox - Number of SMS messages on SIM that are in Outbox
* SimDraft - Number of SMS messages on SIM that are saved as Draft
* LocalMax - Maximum number of SMS messages that can be stored on device
* SimMax - Maximum number of SMS messages that can be stored on SIM


## api/sms/sms-list
Post needed?<br>
TODO

## api/language/current-language
### GET
#### CurrentLanguage - current language code

### POST
TODO

## api/wlan/station-information
TODO<br>
Gives error

## api/wlan/basic-settings
TODO - probably GET and POST

#### WifiSsid
SSID of Wifi network

#### WifiChannel
Channel of Wifi network

#### WifiHide
Is SSID hidden?<br>
Possible values - 0, 1

#### WifiCountry
Country TODO

#### WifiMode
Supported Wifi modes<br>
Possible values: b/g/n

#### WifiRate
TODO<br>
Possible values: 0

#### WifiTxPwrPcnt
TODO<br>
Possible values: 100

#### WifiMaxAssoc
TODO<br>
Possible values: 5

#### WifiEnable
TODO<br>
Possible values: 1

#### WifiFrgThrshld
TODO<br>
Possible values: 2346

#### WifiRtsThrshld
TODO<br>
Possible values: 2347

#### WifiDtmIntvl
TODO<br>
Possible values: 1

#### WifiBcnIntvl
TODO<br>
Possile values: 1

#### WifiWme
TODO<br>
Possible values: 0

#### WifiPamode
TODO<br>
Possible values: 0

#### WifiIsolate
TODO<br>
Possible values: 0

#### WifiProtectionmode
TODO<br>
Possible values: 0

#### Wifioffenable
TODO<br>
Possible values: 1

#### Wifiofftime 
TODO<br>
Possible values: 1800

## api/wlan/security-settings

#### WifiAuthmode
TODO<br>
Possible values: WPA/WPA2-PSK

#### WifiBasicencryptionmodes
TODO<br>
Possible values: NONE

#### WifiWpaencryptionmodes
TODO<br>
Possible values: MIX

#### WifiWepKey1, WifiWepKey2, WifiWepKey3, WifiWepKey4
Used WEP keys.<br>
Default value: 12345

#### WifiWepKeyIndex
WEP key that is used at the moment.<br>
Possible values: 1

#### WifiWpapsk
Plain text WPA password

#### WifiWpsenbl
TODO<br>
Possible values: 1

#### WifiWpscfg
TODO<br>
Possible values: 1

## api/wlan/multi-basic-settings
TODO<br>
Gives error

## api/wlan/host-list

    <Hosts>
      <Host>
        <ID></ID>
        <MacAddress></MacAddress>
        <IpAddress></IpAddress>
        <HostName></HostName>
        <AssociatedTime></AssociatedTime>
      </Host>
    </Hosts>

#### ID
ID number of connected device

#### MacAddress
MAC address of connected device

#### IpAddress
IP address of connected device

#### HostName
Hostname of connected device

#### AssociatedTime
Time of connection of this device

## api/dialup/connection

#### RoamAutoConnectEnable
TODO<br>
Possible values: 0

#### AutoReconnect
TODO<br>
Possible values: 0

#### ReconnectInterval
TODO<br>
Possible values: 0

#### MaxIdelTime
TODO<br>
Possible values: 600

#### ConnectMode
TODO<br>
Possible values: 2

## api/dialup/auto-apn

#### AutoAPN
TODO<br>
Possible values: 0

## api/dialup/profiles

    <Profiles>
      <Profile>
        <Index>1</Index>
        <IsValid>1</IsValid>
        <Name>PLAY</Name>
        <ApnIsStatic>1</ApnIsStatic>
        <ApnName>internet</ApnName>
        <DailupNum>*99#</DailupNum>
        <Username></Username>
        <Password></Password>
        <AuthMode>2</AuthMode>
        <IpIsStatic>0</IpIsStatic>
        <IpAddress></IpAddress>
        <DnsIsStatic>0</DnsIsStatic>
        <PrimaryDns></PrimaryDns>
        <SecondaryDns></SecondaryDns>
        <ReadOnly>1</ReadOnly>
      </Profile>
    </Profiles>
    <CurrentProfile>1</CurrentProfile>

#### Index

#### IsValid

#### Name

#### ApnIsStatic

#### ApnName

#### DailupNum

#### Username

#### Password

#### AuthMode

#### IpIsStatis

#### IpAddress

#### DnsIsStatic

#### PrimaryDns, SecondaryDns

#### ReadOnly

## api/dialup/dial
TODO<br>
Probably only POST with params

## api/pin/status

#### SimState
TOOD<br>
Possible values: 257

#### PinOptState
TODO<br>
Possible values: 259

#### SimPinTimes
TODO<br>
Possible values: 3

#### SimPukTimes
TODO<br>
Possible values: 10

## api/pin/simlock

#### SimLockEnable
TODO<br>
Possible values: 0

#### SimLockRemainTimes
TODO<br>
Possible values: 10

#### pSimLockEnable
TODO<br>
Possible values: 0

#### pSimLockRemainTimes
TODO<br>
Possible values: 0

## api/pin/verify-simlock
TODO<br>
Only POST

## api/pin/operate
TODO<br>
Obly POST

## api/pin/save-pin
TODO<br>
Only POST

#### SimSavepinStatus
TODO<br>
Possible values: 1

#### SimSavepinScid
TODO<br>
Possible values: some long number

## api/user/login
TODO<br>
Only POST

## api/user/logout
TODO<br>
Only POST


## configurations/language.xml
## configurations/optional_feature.xml

## language/lang_LANG_CODE.js


## Error codes
* code - message
* 100002 - Request not support - Jeśli podano zły adres do API lub nie ma uprawnień na poziomie firmware
* 100005 -  - brak opisu, być może brak uprawnień
* 100006 - Wrong parameter - Prawdopodobnie zły (lub brakujący) parametr przy zapisie
* 100009 - Save parameter fail
