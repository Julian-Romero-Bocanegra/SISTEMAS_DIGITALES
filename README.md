# SISTEMAS_DIGITALES 
# LABORATORIO #1


Institución: Fundación Universitaria Compensar.
Integrantes: Edwin stiven pasto / Julian Romero bocanegra
Docente: Diego Alejandro Barragán Vargas

Introducción
El informe documenta el desarrollo y los resultados obtenidos en el primer laboratorio implementado en Sistema Digitales. Este laboratorio de focaliza en la implementación y análisis de circuitos en electrónica digital, por ejemplo, el oscilador multivibrador como mediador el temporizador TL555, la identificación de compuertas lógicas y el diseño de un sistema hexadecimal por medio de un display, con la implementación de este ejercicio se busca fundamentar y validar los conocimientos conceptuales de la lógica booleana y el comportamiento de la señal digital en el tiempo.

INFORME DE LABORATORIO
Desarrollo de Puntos 

Punto 1: Oscilador Astable con TL555 
  •	Objetivo: Por medio de un regulador 555 crear una onda digital con un tiempo de 2 segundos intermedios.
  •	Cálculos: 


  •	Esquema: Diagrama de montaje de circuito eléctrico para la creación de la onda por medio del 555.
 

<img width="906" height="634" alt="image" src="https://github.com/user-attachments/assets/143062f6-2fb7-4ec7-9990-84ab32542019" />



Referencia: (Cómo Construir un Oscilador con un Temporizador 555 (en Modo Astable). (n.d.). https://www.learningaboutelectronics.com/Articulos/Oscilador-con-un-temporizador-555-modo-astable.php#google_vignette)

  •	Componentes: 
  Componentes Activos y de Control
    o	U2 (Temporizador 555): Es el corazón del circuito, con la configuración  de multivibrador astable lo cual nos permite  generar la señal cuadrada (señal digital).
    o	U1 (Regulador de Voltaje 7805): Reducir y estabiliza el voltaje de entrada a 5V o 9Vencargado de la alimentación del circuito.
    o	D1 (LED-RED): Un diodo emisor de luz de color rojo (Bombillo LED) el cual es nuestro indicador de la oscilación de salida de 2 segundos.
  Componentes Pasivos (Resistencias y Capacitores)
    o	R1 (Resistencia): Valor de 1k\Omega.
    o	R2 (Resistencia): Valor de 6.2k\Omega.
    o	C1 (Capacitor Electrolítico): Valor de 220\muF, utilizado para el filtrado.
    o	C2 (Capacitor Electrolítico): Valor de 220\muF; este es el componente clave que, junto con R1 y R2, permite determina el periodo de oscilación de 2 segundos.
  Fuente de Energía y Conexión
    o	B1 (Batería): Fuente de alimentación de 9V o 5V.
    o	Terminal de Tierra (GND): Punto de referencia común.
  •	Simulación en Proteus

<img width="921" height="410" alt="image" src="https://github.com/user-attachments/assets/d64f8cdf-ee88-4c34-b5e6-b01d2e2c8e1f" />

 
Referencia: (Elaborado por Edwin stiven pasto y Julian felipe Romero)


  •	Resultados: Fotos del montaje físico y captura de la onda en osciloscopio (si aplica).

IMAGEN


Punto 2: Caracterización de Compuertas Lógicas 
•	Componentes: Crea una tabla con los integrados usados (74HC08, 74HC32, 74HC04, etc.).
•	Fichas Técnicas: Inserta imágenes de los diagramas de pines (pinout) de cada integrado.
•	Tablas de Verdad: Registra los resultados de las pruebas (LED encendido/apagado) y compáralos con la función booleana teórica.



Punto 3: Conversor Binario a Hexadecimal 
  •	Objetivo: Desarrollar un esquema conversor de numeración binaria a hexadecimal, que nos permita visualizar diferentes caracteres en un display de 7 segmentos, haciendo uso meramente de compuertas lógicas.
  •	Lógica: 
1). La Entrada: (Binario)
    1.1). Se le entregas al sistema un número binario usando 4 interruptores (D, C, B, A).
    1.2). Cada interruptor solo puede estar en 0 (apagado) o 1 (encendido).
    1.3). Se tienen 4 interruptores, esto quiere decir que se pueden llegar hacer 16 combinaciones diferentes (desde el 0000 hasta el 1111).
    2). El Procesador:  Esa combinación de ceros y unos entra a una red de compuertas lógicas.
    2.1). Pensemos en las compuertas como caminos con reglas: "Si el interruptor A y el B están encendidos, deja pasar la corriente".
    2.2). Este "cerebro" decide, según la combinación, qué partes del display deben brillar y cuáles no.
    3). La Salida: (Display 7 Segmentos)
    3.1). El display tiene 7 barritas de luz (llamadas de la a a la g).
    3.2). Si se pone 0000 en los interruptores, el "cerebro" manda corriente a las barritas exteriores para dibujar un 0.
    3.3). Si pones 1010 (que es el número 10), el cerebro activa las barritas necesarias para dibujar la letra A.
•	Esquema: Diagrama de montaje de circuito eléctrico para la creación de la onda por medio del 555.

 <img width="921" height="705" alt="image" src="https://github.com/user-attachments/assets/4b5da4a1-ed78-42a6-adeb-08792e46697a" />

Referencia:  (Cómo Construir un Oscilador con un Temporizador 555 (en Modo Astable). (n.d.). https://www.learningaboutelectronics.com/Articulos/Oscilador-con-un-temporizador-555-modo-astable.php#google_vignette)

  •	Mapa de Karnaugh: Para cada segmento se debe realizar un mapa de 4 variables. Por ejemplo, para el Segmento "a", la función booleana simplificada tras agrupar los 1s en el mapa de Karnaugh sería:
    •	$$a = D + B + (C \cdot A) + (\overline{C} \cdot \overline{A})$$
    •	(Nota: Debes repetir este proceso para los segmentos b, c, d, e, f, g en tu informe).
    
    •	Tabla de Verdad Completa: Por medio de la tabla de verdad se relaciona cada segmento del display para su reprsentacion hexadecimal

<img width="921" height="542" alt="image" src="https://github.com/user-attachments/assets/f3926967-59b7-4f53-a516-8c53f272af64" />

 
Referencia: (Elaborado por Edwin stiven pasto y Julian felipe Romero)


Conclusiones y Recomendaciones
