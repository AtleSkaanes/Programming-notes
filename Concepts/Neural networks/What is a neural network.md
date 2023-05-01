
A neural network is a program that mimics the neurons inside our brains.



```py
def connect(ssid=s.SSID, psk=s.PASSWORD):
    wlan = network.WLAN(network.STA_IF)
    wlan.active(True)
    wlan.connect(ssid, psk)
```