PROYECTO: VENTILADOR Y HUMIDIFICADOR

1.COMPONENTES:
Los componentes que constituyen este proyecto son:
1. ESP32-s3: 
2. Ventilador:
3. Sensor AHT10:
4. Pantalla OLED:
5. Relé:
6. Himudificador:
7. 

2. Presupuesto:
3. Diagrama de bloques:

```mermaid
graph LR

    %% Parte central: ESP32-S3 con "línea horizontal" simulada
    ESP32["Esp32 - S3<br>----------------------------------<br>Servidor web local"]

    %% Lado izquierdo (entradas)
    Sensor["Sensor Temperatura (I2C)"] --- ESP32
    LED_Aviso["LED (izquierdo) - Se tiene que encender humidificador"] --- Sensor

    %% Lado derecho (salidas)
    ESP32 --- Display["Display (Pantalla OLED)"]
    ESP32 --- Rele_Hum["Relé (Humidificador 5V)"]
    ESP32 --- Pulsador_Modo["Pulsador (Modo Auto / Modo Manual)"]
    ESP32 --- Pulsador_Activar["Pulsador (Para activar Ventilador)"]

    Pulsador_Activar --- Rele_Ventilador["Relé Ventilador 12V"]
    Pulsador_Activar --- LED_Ventilador["LED (derecho) - Ventilador encendido"]

    %% Flecha hacia abajo desde el ESP32
    ESP32 --> abajo[" web "]

```

4. Montaje:
5. Funcionalidades:
6. Conclusiones:

Codigo main.cpp:
```


```
