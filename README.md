# RPi_PICO_ESPHome
<b>Příklady využití RPi PICO jako ESPHome kontroleru.</b>

<h2>Nastavení HomeAssistanta na WiFi připojení (default je na LAN)</h2>
<p>Připojte monitor a klávesnici k Raspberry PI s nainstalovaným HA a napište do konzole: <b>'login' a stiskněte ENTER</b></br>
(symbol před kurzorem se změní na <b>'#'</b>)</p>
<ul>
 <li>To assure wifi is functioning, enter: nmcli radio</li>
 <li>Scan available wifi access enter: nmcli device wifi rescan</li>
 <li>List available wifi access enter: nmcli device wifi</li>
 <li>Connect to your wifi (incude quotes) enter: nmcli device wifi connect “YOUR_SSID” password “YOUR_WIFI_PASSWORD”</li>
This will try to connect to your SSID and will generate a network profile for you if successfull.
The output will be similar to
"Device 'wlan0' successfully activated with...."
Show connections enter: nmcli con show
There may be two separate ip addresses on your network: one for ethernet, one for wifi.
Check the ip addresses enter: ip addr show
Now connect to http(s)://your_wifi_ip:8123 in your browser.
 <li></li>
</ul>
