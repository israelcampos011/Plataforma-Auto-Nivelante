# Plataforma autonivelante

Prototipo experimental inspirado en una suspensión activa que mantiene una
plataforma nivelada mediante medición inercial y control electrónico de
actuadores lineales.

## Contexto

Las suspensiones activas y semiactivas usan sensores, actuadores y algoritmos
de control para ajustar en tiempo real parámetros como la amortiguación, la
rigidez o la altura del vehículo. Una de sus funciones principales es la
autonivelación, que busca mantener la plataforma cercana a la horizontal aun
con pendientes, cargas desiguales o irregularidades del terreno.

Este principio también se aplica en robótica móvil, plataformas de inspección
y vehículos autónomos, que deben estimar su inclinación (cabeceo o *pitch* y
balanceo o *roll*) y corregirla con actuadores.

## Sobre el proyecto

Este proyecto reproduce a escala de laboratorio el principio de nivelación
de una plataforma:

- **Sensado:** una IMU MPU6050 (acelerómetro y giroscopio) mide la orientación
  del sistema.
- **Procesamiento:** un Arduino UNO adquiere las mediciones, estima la
  inclinación y ejecuta el algoritmo de control.
- **Actuación:** cuatro actuadores lineales, cada uno con su propio driver
  BTS7960, corrigen la inclinación de forma independiente.
- **Alimentación:** cuatro baterías en configuración 2S2P.

El repositorio incluye el código, el diagrama de conexiones y los datos
experimentales de las pruebas.
