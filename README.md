# Mario-poder-sed-salto

![Boceto](mario.png)


Juego interactivo de mario que funciona con arduino explora y sensor de aire 
¡Perfecto! Te preparo un **PRD (Product Requirements Document)** para un proyecto usando Arduino Explora con esa mecánica tan creativa que me planteas. 🚀

---

# PRD - Juego interactivo con Arduino Explora y sensores externos

---

## 1. Nombre del proyecto

**“El desafío del poder, la sed y el salto”**

---

## 2. Objetivo

Crear un juego interactivo en el que el jugador debe reaccionar a distintos estímulos sensoriales: voz, temperatura, viento y joystick para realizar acciones específicas.

---

## 3. Descripción general

El sistema usa el Arduino Explora con sus sensores internos y un sensor de viento externo para crear una experiencia de juego donde:

* Al detectar 2 sonidos fuertes (sensor de voz), el jugador "lanza un poder".
* Si la temperatura sube (sensor de temperatura), el jugador siente sed y debe "tomar Coca-Cola".
* El jugador puede moverse de izquierda a derecha con la palanca (joystick).
* Si se detecta viento (sensor de viento externo), el jugador salta.

---

## 4. Requerimientos funcionales

| ID  | Requerimiento                                                                  | Prioridad | Detalles                                                                                    |
| --- | ------------------------------------------------------------------------------ | --------- | ------------------------------------------------------------------------------------------- |
| RF1 | Detectar cuando el sensor de voz detecta 2 sonidos fuertes consecutivos        | Alta      | El sensor debe contar 2 eventos de voz para activar el "poder".                             |
| RF2 | Detectar aumento de temperatura para activar estado de “sed”                   | Alta      | Al superar un umbral de temperatura, se activa alerta de sed y acción de "tomar Coca-Cola". |
| RF3 | Mover jugador de izquierda a derecha con joystick                              | Alta      | Lectura analógica del joystick para mover un indicador o sprite en pantalla.                |
| RF4 | Detectar ráfaga de viento con sensor externo para activar salto                | Alta      | Al detectar viento (pulsos o nivel analógico) el jugador debe saltar.                       |
| RF5 | Mostrar estado actual (poder, sed, posición, salto) por LEDs o pantalla serial | Media     | Indicadores visuales o salida serial para monitoreo del estado del juego.                   |

---

## 5. Requerimientos no funcionales

| ID   | Requerimiento             | Prioridad | Detalles                                              |
| ---- | ------------------------- | --------- | ----------------------------------------------------- |
| RNF1 | Respuesta en tiempo real  | Alta      | Las acciones deben ser detectadas y ejecutadas rápido |
| RNF2 | Uso eficiente de recursos | Media     | Código optimizado para Arduino Explora                |
| RNF3 | Seguridad                 | Baja      | No aplica                                             |

---

## 6. Hardware requerido

| Componente          | Descripción                             |
| ------------------- | --------------------------------------- |
| Arduino Explora     | Placa principal con sensores integrados |
| Sensor de viento    | Anemómetro o sensor de viento externo   |
| Buzzer / LEDs       | Indicadores para estados del juego      |
| Cables y protoboard | Para conexiones                         |

---

## 7. Flujo de juego (mecánica)

1. **Inicio**: El sistema inicializa sensores y variables.
2. **Escuchar voz**: Sensor de voz detecta sonidos, si cuenta 2 sonidos fuertes seguidos, lanza el poder (indicar con LED o buzzer).
3. **Medir temperatura**: Si temperatura > umbral, activar sed.

   * Jugador debe "tomar Coca-Cola" (simulado con botón o joystick).
4. **Movimiento**: Joystick mueve jugador de izquierda a derecha (puede ser un LED que se enciende en diferentes posiciones).
5. **Detectar viento**: Sensor externo detecta viento, el jugador salta (indicar con otro LED o buzzer).
6. **Estado visible**: Mostrar por LEDs o Serial los estados actuales.

---

## 8. Ejemplo de valores umbral y parámetros

| Parámetro    | Valor ejemplo                            |
| ------------ | ---------------------------------------- |
| Umbral voz   | 2 sonidos en 3 segundos                  |
| Umbral temp  | > 30 °C                                  |
| Viento       | Pulsos > 3 por segundo                   |
| Movimiento X | Joystick 0 - 1023 mapeado 0-7 posiciones |

---

## 9. Interfaz y salidas

* **LED rojo**: Poder lanzado
* **LED azul**: Sed activa (toma Coca-Cola)
* **LED verde**: Salto activado
* **Serial Monitor**: Estado completo del juego

---

## 10. Consideraciones y extensiones futuras

* Añadir pantalla LCD para interfaz gráfica
* Más niveles con diferentes umbrales y tiempos
* Integrar sonido para feedback

---



