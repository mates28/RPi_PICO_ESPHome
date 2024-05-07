# RPi_PICO_ESPHome
<b>Příklady využití RPi PICO jako ESPHome kontroleru.</b>

<h2>Nastavení HomeAssistanta na WiFi připojení (default je na LAN)</h2>
<p>Připojte monitor a klávesnici k Raspberry PI s nainstalovaným HA a napište do konzole: <b>'login' a stiskněte ENTER</b></br>
(symbol před kurzorem se změní na <b>'#'</b>)</p>
<ol>
 <li>Zjistíme jestli je WiFi funkční: <b>'nmcli radio'</b> a stiskněte ENTER</li>
 <li>Oskenujeme si všechny WiFi v okolí: <b>'nmcli device wifi rescan'</b> a stiskněte ENTER</li>
 <li>Vypíšeme si všechny WiFi ze skenu: <b>'nmcli device wifi'</b> a stiskněte ENTER</li>
 <li>Připojíme se k požadované WiFi: <b>'nmcli device wifi connect “SSID” password “HESLO”'</b> a stiskněte ENTER</br>(tím dojde k vytvoření profilu a připojení na WiFi - zařízení 'wlan0')</li>
 <li>Zobrazíme si zda jsme připojeni na WiFi ('wlan0'): <b>'nmcli con show'</b> a stiskněte ENTER</li>
 <li>Zjistíme si přidělenou IP adresu: <b>'ip addr show'</b> a stiskněte ENTER</li>
 <li>Pomocí prohlížeče se připojíme na HA <b>'http(s)://wifi_ip:8123'</b></li>
</ol>
<h2>Příprava RPi PICO (ESP32, ESP8266) pro ESPHome firmware</h2>
<p>V prohlížeči si zadáme url: <b>https://esphome.io/</b> a zobrazíme si stránku s podporou a nastavením ESP Home</p>
