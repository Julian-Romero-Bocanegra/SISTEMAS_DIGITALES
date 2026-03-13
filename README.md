# LABORATORIO N°1


**Integrantes:** Edwin Stiven Pasto / Julian Romero Bocanegra

**Docente:** Diego Alejandro Barragán Vargas

**Institución:** Fundación Universitaria Compensar.


## Introducción
El informe documenta el desarrollo y los resultados obtenidos en el primer laboratorio implementado en Sistema Digitales. Este laboratorio se focaliza en la implementación y análisis de circuitos en electrónica digital, por ejemplo, el oscilador multivibrador como mediador, el temporizador TL555, la identificación de compuertas lógicas y el diseño de un sistema hexadecimal por medio de un display. Con la implementación de este ejercicio, se busca fundamentar y validar los conocimientos conceptuales de la lógica booleana y el comportamiento de la señal digital en el tiempo.

## Hardware
### Multimetro
Especificaciones Técnicas – Fluke 179
Tipo: Multímetro digital de verdadero RMS

Pantalla: Digital con retroiluminación

Medición de voltaje CA/CC: Hasta 1000 V

Medición de corriente CA/CC: Hasta 10 A (20 A por hasta 30 segundos)

Resistencia: Hasta 50 MΩ

Capacitancia: Hasta 10,000 µF

Frecuencia: Hasta 100 kHz

Temperatura: Con termopar tipo K incluido

Prueba de diodos y continuidad: Sí

Funciones adicionales: MIN/MAX, HOLD, RANGE automático/manual

Seguridad: Categoría CAT III 1000 V, CAT IV 600 V

Alimentación: Batería de 9 V tipo bloque

<img width="406" height="770" alt="image" src="https://github.com/user-attachments/assets/eed1d437-d573-4852-a600-b24778985420" />

### Osciloscopio ROHDE & SCHWARZ RTC1002
Marca y Modelo: Rohde & Schwarz RTC1002.

Canales de Entrada: 2 canales analógicos (CH1, CH2) + Canales lógicos (D0 a D7).

Funciones Principales: Medidas automáticas, Cursor, Análisis (FFT, etc.), Vista rápida (Quick View), Zoom.

Disparo (Trigger): Tipos: Auto, Normal, Simple (Single). Incluye disparo externo (Ext. Trigger In).

Generador de Patrones: Integrado (Pattern Generator).

Salida Auxiliar: AUX OUT.

Controles Destacados: Escala (VERTICAL/HORIZONTAL), Match, Referencia (REF), Filtro (FILTER), Bus.
 
<img width="650" height="400" alt="image" src="https://github.com/user-attachments/assets/7f29114d-3620-4775-b566-ebf936e38aaf" />

### Fuente de Alimentación GWINSTEK GPS-2303
Marca y Modelo: GW Instek GPS-2303.

Número de Salidas: 2 canales independientes (CH1 y CH2).

Modos de Operación:
Independiente (INDEP): Cada canal funciona por separado.

Serie (SERIES): Para aumentar el voltaje.

Paralelo (PARALLEL): Para aumentar la corriente.

Seguimiento (TRACKING): Modo Maestro/Esclavo (MASTER/SLAVE).

Especificaciones Eléctricas:
Rango de Voltaje: 0 ~ 30V por canal.
Rango de Corriente: 0 ~ 3A por canal.

Indicadores LED:
C.C.: Modo Corriente Constante.
C.V.: Modo Voltaje Constante.

Controles: Perillas grueso/fino (COARSE/FINE) para Voltaje y Corriente.

Conexiones: Bornes de salida con conexión a tierra (GND) y botón de encendido/apagado de salida (OUTPUT ON/OFF).

<img width="696" height="449" alt="image" src="https://github.com/user-attachments/assets/7c92f446-68d0-468b-8321-3346ee5f81f8" />
 
## Punto 1 | Onda Digital:
  El objetivo del primer punto de este laboratorio es diseñar y construir un oscilador astable con el uso del temporizador TL555. Este circuito se caracteriza por no tener un estado estable; su salida se conmuta constantemente entre el alto y el bajo de voltaje, generando así una onda cuadrada continua.
  
### Esquema: 
Diagrama de montaje de un circuito eléctrico para generar la onda mediante el 555.
<img width="906" height="634" alt="image" src="https://github.com/user-attachments/assets/143062f6-2fb7-4ec7-9990-84ab32542019" />
Referencia: (Cómo Construir un Oscilador con un Temporizador 555 (en Modo Astable). (n.d.). https://www.learningaboutelectronics.com/Articulos/Oscilador-con-un-temporizador-555-modo-astable.php#google_vignette)

### Componentes: 
La lista de comonente se clasifica en activos y de control, pasivos y fuente de energia:
### Componentes Activos y de Control
U2 (Temporizador 555): Es el corazón del circuito, con la configuración  de multivibrador astable lo cual nos permite  generar la señal cuadrada (señal digital).
U1 (Regulador de Voltaje 7805): Reducir y estabiliza el voltaje de entrada a 5V o 9Vencargado de la alimentación del circuito.
D1 (LED-RED): Un diodo emisor de luz de color rojo (Bombillo LED) el cual es nuestro indicador de la oscilación de salida de 2 segundos.
  
### Componentes Pasivos (Resistencias y Capacitores)
R1 (Resistencia): Valor de 1k\Omega.
R2 (Resistencia): Valor de 6.2k\Omega.
C1 (Capacitor Electrolítico): Valor de 220\muF, utilizado para el filtrado.
C2 (Capacitor Electrolítico): Valor de 220\muF; este es el componente clave que, junto con R1 y R2, permite determina el periodo de oscilación de 2 segundos.
  
### Fuente de Energía y Conexión
B1 (Batería): Fuente de alimentación de 9V o 5V o	Terminal de Tierra (GND): Punto de referencia común.

### Simulación en Proteus
<img width="921" height="410" alt="image" src="https://github.com/user-attachments/assets/d64f8cdf-ee88-4c34-b5e6-b01d2e2c8e1f" />
Referencia: (Elaborado por Edwin stiven pasto y Julian felipe Romero)

### Montaje Fisico
<img width="1534" height="807" alt="image" src="https://github.com/user-attachments/assets/1bda16ce-ead9-4fbc-b02c-39a2beb256c6" />
<img width="518" height="411" alt="image" src="https://github.com/user-attachments/assets/e67c2f98-8994-4213-92b3-529cb6b9f29e" />
<img width="451" height="341" alt="image" src="https://github.com/user-attachments/assets/ad9f0959-f56b-4d8a-babc-7020fc36fc5b" />

## Punto 2 | Compuertas Logicas: 
El objetivo del punto #2 es reconocer la caracterización técnica de las compuertas lógicas AND, OR, NOT, NAND, NOR y XOR. A través de este ejercicio, se busca validar las funciones booleanas y su comportamiento directo en circuitos integrados reales, identificando sus salidas y sus diferentes combinaciones de entrada.

### Componentes
Los componentes usados tanto en el cirucito logico como en el fisico son:
Compuerta AND: Circuito Integrado 74HC08 o 74LS08.
Compuerta OR: Circuito Integrado 74HC32 o 74LS32.
Compuerta NOT: Circuito Integrado 74HC04 o 74LS04.
Compuerta NAND: Circuito Integrado 74HC00 o 74LS00.
Compuerta NOR: Circuito Integrado 74HC02 o 74LS02.
Compuerta XOR: Circuito Integrado 74HC86 o 74LS86.

### Simulacion en proteus
#### Compuerta AND
<img width="695" height="374" alt="image" src="https://github.com/user-attachments/assets/ab100b98-c19f-4465-a705-516f56822fbc" />

#### Compuerta OR
<img width="701" height="341" alt="image" src="https://github.com/user-attachments/assets/c4d17344-4db5-41ff-8132-364d312b0294" />

#### Compuerta NOT
<img width="712" height="346" alt="image" src="https://github.com/user-attachments/assets/16bad156-d7db-405a-ac69-8784c8d15e73" />

#### Compuerta NAND
<img width="683" height="366" alt="image" src="https://github.com/user-attachments/assets/1ac67bef-c4a8-4668-a7a6-e4de9c7e2ca5" />

#### Compuertas NOR
<img width="703" height="362" alt="image" src="https://github.com/user-attachments/assets/064687f3-56d3-42b9-9921-73656547e18b" />

#### Compuertas XOR
<img width="705" height="367" alt="image" src="https://github.com/user-attachments/assets/19b4e712-99b7-420e-8a52-9c45ffdec9e7" />

### Esquema
![ESQUEMATICOS-1024x1024](https://github.com/user-attachments/assets/7c4d65f4-668d-4f11-a09c-d93cd28673b5)
Aguirre, C. (2025, July 7). Circuitos Integrados: Compuertas Lógicas AND, OR , NOR,NAND, XOR y NOT. UNIT Electronics. https://blog.uelectronics.com/electronica/circuitos-integrados-compuertas-logicas-and-or-nand-xor-y-not/

### Montaje Fisico
<img width="1600" height="716" alt="Sin título" src="https://github.com/user-attachments/assets/420790e4-8d5d-491a-9e26-df9c0e1f4b4f" />


## Punto 3 | Conversor Binario a Hexadecimal: 
El tercer punto es el diseño y construcción de un sistema decodificador combinacional. Este sistema nos permite convertir la entrada de un formato binario de 4 bits en una salida visual, por medio de un display de 7 segmentos. El principal recto es la traducción utilizando meramente compuertas lógicas.

### Lógica: 
#### 1). La Entrada: (Binario)
* **1.1)** Se le entregas al sistema un número binario usando 4 interruptores (D, C, B, A).
* **1.2)** Cada interruptor solo puede estar en 0 (apagado) o 1 (encendido).
* **1.3)** Se tienen 4 interruptores, esto quiere decir que se pueden llegar hacer 16 combinaciones diferentes (desde el 0000     hasta el 1111).
#### 2). El Procesador:  
Esa combinación de ceros y unos entra a una red de compuertas lógicas.
* **2.1)** Pensemos en las compuertas como caminos con reglas: "Si el interruptor A y el B están encendidos, deja pasar la corriente".
+ **2.2)** Este "cerebro" decide, según la combinación, qué partes del display deben brillar y cuáles no.
#### 3). La Salida: 
* **3.1)** El display tiene 7 barritas de luz (llamadas de la a a la g).
* **3.2)** Si se pone 0000 en los interruptores, el "cerebro" manda corriente a las barritas exteriores para dibujar un 0.
* **3.3)** Si pones 1010 (que es el número 10), el cerebro activa las barritas necesarias para dibujar la letra A.
    
### Tabla de Verdad: 
Por medio de la tabla de verdad se relaciona cada segmento del display para su reprsentacion hexadecimal
<img width="921" height="542" alt="image" src="https://github.com/user-attachments/assets/f3926967-59b7-4f53-a516-8c53f272af64" />

Referencia: (Elaborado por Edwin stiven pasto y Julian felipe Romero) 

### Esquema: 
<img width="858" height="592" alt="figura 1-min" src="https://github.com/user-attachments/assets/4987e4af-25c1-40ae-92ea-088639cc5580" />
Aguirre, C. (2025, July 7). Circuitos Integrados: Compuertas Lógicas AND, OR , NOR,NAND, XOR y NOT. UNIT Electronics. https://blog.uelectronics.com/electronica/circuitos-integrados-compuertas-logicas-and-or-nand-xor-y-not/


### Componentes
Para este montaje se necesita los siguientes elementos:
Compuertas NOT (74LS04): Para obtener las negaciones de las entradas.
Compuertas AND de 2 y 3 entradas (74LS08 / 74LS11): Para realizar los productos de los mapas de Karnaugh.
Compuertas OR (74LS32): Para sumar los términos y enviar la señal final a cada segmento.
Display 7 Segmentos Cátodo Común: El elemento de visualización final.Resistencias de 330-Omega: Siete unidades para proteger cada segmento del display.

### Simulacion proteus
<img width="1530" height="816" alt="image" src="https://github.com/user-attachments/assets/36bda3db-f9a7-4b79-b2ae-c8147768f2fe" />

### Montaje Fisico
(Referencial)

<img width="382" height="376" alt="image" src="https://github.com/user-attachments/assets/c980c598-1f21-460a-8940-66c3b0b34fb5" />

Debido a la ausencia de componentes físicos para la implementación final, se toma como referencia técnica el desarrollo realizado por **Juan Tellez**, el cual demuestra la viabilidad del diseño mediante el uso de lógica discreta.


# Conclusiones 

### Validación de la Oscilación Astable: 
Se comprueba que el temporizador 555 nos permite la generación de señales cuadradas, mediante la experimentación y las combinaciones de R1 = 1 kΩ, R2 = 6.2 Ω y C = 220 µF.
### Importancia de la Regulación de Voltaje: 
El implementar el regulador lm7805 es fundamental para la entrada del voltaje, esto mismo nos asegura la protección de los circuitos integrados.
### Eficacia de la Lógica Combinacional: 
El desarrollo del conversor binario a hexadecimal demostró que es posible reemplazar integrados especializados mediante el diseño de una matriz de compuertas lógicas básicas (AND, OR, NOT), logrando la visualización correcta de los 16 caracteres (0-F) en un display de 7 segmentos.

# Recomendaciones
### Gestión de Conexiones en Protoboard: 
Para el punto 3, lo recomendable es realizar el montaje de manera modular, probando segmento por segmento (del 'a' al 'g') antes de terminar el circuito por completo, debido a la alta densidad de cableado que dificulta la revisión de errores.
### Uso de Resistencias de Protección:
Es obligatorio incluir resistencias (preferiblemente de 220 a 330) en cada segmento del display y probar previamente todo para evitar sobrecargas que puedan dañar los LEDs del display o las salidas de las compuertas lógicas.

### Verificación de Fichas Técnicas: 
Antes de energizar, es importante revisar los datasheets de cada uno de circuitos integrados, especialmente en compuertas como la NOR (74LS02), cuya distribución de pines suele ser diferente al estándar de otras compuertas.

# Referencias y Atribuciones
* **Simulación:** Diseño desarrollado en Proteus Design Suite v8.13 / v9.1.
* **Licencia:** Este proyecto se distribuye bajo fines académicos para la Universidad Compensar.
* **Guía de Montaje Físico:** Tellez, J. (2016). *Decodificador binario a hexadecimal por compuertas lógicas* [Archivo de Video]. YouTube. [https://youtu.be/TKD4wU58XWE](https://youtu.be/TKD4wU58XWE).
* **Manual de Instrumentación:** Stiven (2018). *Manual resumido de multímetro* [Documento]. Scribd. [https://es.scribd.com/document/403872865/Manual-Resumido-de-Multimetro](https://es.scribd.com/document/403872865/Manual-Resumido-de-Multimetro).
* **Asistencia Técnica:** Google Gemini (2026). Apoyo en la estructuración de lenguaje Markdown y resolución de conflictos de versiones en Git
*  **Fluke Corporation. (n.d.). Fluke. https://www.fluke.com/es-mx
