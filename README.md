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
<p>V prohlížeči si zadáme url: <a href="https://esphome.io/" target="_blank"><b>https://esphome.io/</b></a> a zobrazíme si stránku s podporou a nastavením ESP Home</p>
<h4>Příklad přidání výpisu teploty procesoru RPi PICO:</h4>

```
sensor:
  - platform: internal_temperature
    name: "Internal Temperature"
```

<h4>Příklad přidání a ovládání RGB Neopixel LED pásku s 22 ks LED</h4>

```
light:
  - platform: rp2040_pio_led_strip
    name: led_strip
    id: led_strip
    pin: GPIO21
    num_leds: 22
    pio: 0
    rgb_order: GRB
    chipset: WS2812B
```

<p>Další příklady později....</p>
