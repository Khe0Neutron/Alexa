# Proyecto de Control de Luces con Alexa

Este proyecto permite controlar hasta ocho luces en una casa utilizando comandos de voz a través de Amazon Alexa. Está basado en un ESP32, que se conecta a la red WiFi para recibir las órdenes desde Alexa. También se pueden controlar las luces manualmente utilizando botones físicos conectados al ESP32.

## Características

- **Control de luces con Alexa**: Puedes encender y apagar las luces utilizando comandos de voz.
- **Control manual**: Cada luz puede ser controlada manualmente mediante botones físicos conectados al ESP32.
- **Retroalimentación de estado**: El ESP32 proporciona retroalimentación del estado de cada luz tanto a través de la consola serial como del estado del relé.
- **Configuración flexible**: Los nombres de los dispositivos (luces) se pueden personalizar en el código.

## Requisitos

- **Hardware:**
  - ESP32
  - 8 relés para controlar las luces
  - 8 botones físicos para control manual
  - LED para indicar estado de conexión WiFi
  - Conexión WiFi

- **Librerías Arduino:**
  - [`WiFi.h`](https://github.com/espressif/arduino-esp32/tree/master/libraries/WiFi)
  - [`Espalexa.h`](https://github.com/Aircoookie/Espalexa)
  - [`AceButton.h`](https://github.com/bxparks/AceButton)

## Configuración del Hardware

- Los pines del ESP32 están conectados a los relés y a los botones físicos. Aquí están las asignaciones de pines utilizadas en el proyecto:
  - **Relés:**
    - Relé 1: GPIO 23
    - Relé 2: GPIO 22
    - Relé 3: GPIO 21
    - Relé 4: GPIO 19
    - Relé 5: GPIO 18
    - Relé 6: GPIO 5
    - Relé 7: GPIO 25
    - Relé 8: GPIO 26
  - **Botones:**
    - Botón 1: GPIO 13
    - Botón 2: GPIO 12
    - Botón 3: GPIO 14
    - Botón 4: GPIO 27
    - Botón 5: GPIO 33
    - Botón 6: GPIO 32
    - Botón 7: GPIO 15
    - Botón 8: GPIO 4
  - **LED de estado WiFi:** GPIO 2

## Instalación y Configuración

1. **Instalación de librerías:**
   - Asegúrate de tener instaladas las librerías mencionadas en la sección de requisitos.

2. **Configuración de WiFi:**
   - Modifica las siguientes líneas en el código para configurar tu red WiFi:
     ```cpp
     const char* ssid = "Red"; // Cambiar nombre de red
     const char* password = "Contraseña"; // Cambiar contraseña de red
     ```

3. **Compilación y carga:**
   - Compila y sube el código al ESP32 utilizando el IDE de Arduino.

4. **Integración con Alexa:**
   - Una vez que el ESP32 esté conectado a la red WiFi, Alexa detectará los dispositivos automáticamente. Puedes controlar las luces diciendo comandos como "Alexa, enciende la luz de la sala".

## Uso

- **Control con Alexa:** Di "Alexa, enciende/apaga [nombre de la luz]" para controlar las luces.
- **Control manual:** Pulsa el botón físico correspondiente para encender o apagar una luz.

## Contribución

Si encuentras algún error o tienes sugerencias para mejorar el proyecto, siéntete libre de abrir un issue o hacer un pull request.

## Funcionamiento
![Instalacion de la placa con un modulo Rele de 8 canales](https://res.cloudinary.com/dtd3uxftx/image/upload/v1725308277/Whats-App-Image-2024-09-02-at-2-14-35-PM_1_djbz8j.jpg)



