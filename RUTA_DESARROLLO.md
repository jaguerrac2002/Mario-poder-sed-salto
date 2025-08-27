# Ruta de Desarrollo - Prototipo Inicial

## Fase 1: Configuración Base del Hardware
1. **Conexiones Básicas** (2-3 días)
   - Conectar Arduino Esplora
   - Prueba básica de LEDs integrados
   - Configuración del sensor de viento externo
   - Verificar funcionamiento del joystick integrado

2. **Pruebas de Sensores Individuales** (3-4 días)
   - Test del sensor de sonido
   - Test del sensor de temperatura
   - Test del sensor de viento
   - Test del joystick
   - Calibración inicial de umbrales

## Fase 2: Desarrollo del Firmware Arduino (4-5 días)
1. **Estructura Base**
   - Inicialización de sensores
   - Configuración de la comunicación serial
   - Estructura básica del loop principal

2. **Implementación de Funciones Core**
   ```cpp
   // Ejemplo de estructura del código
   void detectarSonido()
   void medirTemperatura()
   void leerJoystick()
   void detectarViento()
   void enviarDatosSerial()
   ```

3. **Formato de Datos Serial**
   ```
   formato: "S:{sonido},T:{temp},J:{joystick},V:{viento}"
   ejemplo: "S:1,T:28.5,J:512,V:0"
   ```

## Fase 3: Servidor Node.js (3-4 días)
1. **Configuración Inicial**
   - Instalación de dependencias
   - Configuración de p5.serialserver
   - Estructura básica del servidor

2. **Manejo de Datos**
   - Lectura del puerto serial
   - Procesamiento de datos
   - Envío a cliente web

## Fase 4: Frontend con p5.js (5-6 días)
1. **Configuración Base**
   - Setup del canvas
   - Conexión con p5.serialport
   - Estructura básica del loop de dibujo

2. **Visualización Básica**
   - Sprite de Mario (versión simple)
   - Indicadores de estado
   - Movimiento horizontal básico
   - Animación de salto

## Fase 5: Integración y Pruebas (3-4 días)
1. **Pruebas de Integración**
   - Test de latencia end-to-end
   - Verificación de umbrales
   - Ajuste de animaciones

2. **Depuración**
   - Corrección de bugs
   - Optimización de rendimiento
   - Ajuste de valores

## Entregables del Prototipo

1. **Hardware**
   - Arduino Esplora configurado
   - Sensor de viento conectado
   - LEDs indicadores funcionando

2. **Firmware**
   - Código Arduino funcional
   - Comunicación serial establecida
   - Detección básica de eventos

3. **Software**
   - Servidor Node.js corriendo
   - Interfaz web básica
   - Visualización de Mario respondiendo a inputs

## Limitaciones del Prototipo
- Gráficos simples (sprite básico)
- Sin niveles ni puntuación
- Sin efectos de sonido
- Sin persistencia de datos
- Animaciones básicas

## Tiempo Estimado Total: 17-21 días

## Siguiente Fase
Después de validar el prototipo funcional, se puede proceder a:
- Mejorar gráficos
- Añadir niveles
- Implementar sistema de puntuación
- Agregar efectos de sonido
- Crear menú de juego
