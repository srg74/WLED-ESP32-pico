# Platformio [env] for ESP32 WLED dev board

```[env:esp32_pico_kit]
board = pico32
platform = espressif32@3.5
;upload_protocol = espota
# exchange for your WLED IP
;upload_port = "10.0.0.93"
upload_speed = 460800
monitor_speed = 115200
build_unflags = ${common.build_unflags}
build_flags = ${common.build_flags_esp32}
  -D SERVERNAME='"WLED-pico32"'
  -D WLED_DISABLE_BROWNOUT_DET
  -D WLED_WATCHDOG_TIMEOUT=0
  -D WLED_RELEASE_NAME=ESP32_pico_AR
  -D WLED_DISABLE_BLYNK
  -D WLED_DISABLE_CRONIXIE
  -D WLED_DISABLE_HUESYNC
  -D WLED_DISABLE_LOXONE
  -D LEDPIN=2
  -D RLYPIN=-1
  -D BTNPIN=-1
  -D IRPIN=-1
  -D USERMOD_AUDIOREACTIVE
  -D I2S_SDPIN=25
  -D I2S_WSPIN=15
  -D I2S_CKPIN=14
  ;-D MCLK_PIN=0
;  -D WLED_DEBUG
  -UWLED_USE_MY_CONFIG
lib_deps = ${esp32.lib_deps}
  https://github.com/blazoncek/arduinoFFT.git
board_build.partitions = ${esp32.default_partitions}
```
