# Estimaci-n-del-nivel-de-estres-basada-en-la-respuesta-galv-nica-cut-nea-GSR-
Sara Damaris Vasquez Cardenas y Paula Andrea Vega Pardo


# Actividad Electrodérmica (EDA) y Respuesta Galvánica Cutánea (GSR)

## 1. Actividad electrodérmica y respuesta galvánica cutánea

La **actividad electrodérmica (EDA)** es un fenómeno fisiológico que refleja la interacción entre el sistema nervioso autónomo y la piel. Se manifiesta como variaciones en la conductancia cutánea, directamente relacionadas con la activación de las glándulas sudoríparas ecrinas, controladas por el sistema nervioso simpático.

Cuando un individuo se expone a estímulos de diversa naturaleza ya sean emocionales como el miedo, la alegría o la ansiedad; cognitivos como la atención sostenida o la concentración intensa; o fisiológicos como el dolor o el esfuerzo físico se produce una activación del sistema nervioso simpático. Este aumento en la actividad autonómica desencadena la estimulación de las glándulas sudoríparas ecrinas, responsables de la sudoración.
Aunque la cantidad de sudor liberada en estas circunstancias suele ser mínima y, en la mayoría de los casos, imperceptible para la persona, resulta suficiente para modificar las propiedades eléctricas de la piel. En particular, se altera su conductividad eléctrica, lo que permite que estos cambios sean detectados mediante sensores adecuados.
Este fenómeno constituye la base de la respuesta galvánica cutánea (GSR), ya que la variación en la conductancia refleja de manera directa la intensidad de la activación simpática frente a estímulos internos o externos. En otras palabras, la piel actúa como un indicador fisiológico sensible, capaz de registrar de forma objetiva las reacciones emocionales, cognitivas o físicas del organismo.

La señal de **respuesta galvánica cutánea (GSR)** se analiza en dos componentes:

- **Nivel de conductancia cutánea (SCL)**: refleja el estado basal o tónico de la piel, útil para evaluar tendencias prolongadas como niveles de estrés sostenido.
- **Respuestas de conductancia cutánea (SCR)**: cambios rápidos y transitorios provocados por estímulos específicos, caracterizados por una subida brusca seguida de un descenso lento hacia el nivel basal.

La **GSR** se ha convertido en un indicador clave en psicofisiología y neurociencia aplicada. Se utiliza en:

- Evaluación de estrés y carga cognitiva.
- Estudios de respuesta emocional en psicología experimental.
- Interfaces hombre–máquina, donde la señal sirve como entrada para sistemas adaptativos.
- Biofeedback terapéutico, ayudando a entrenar al usuario en el control de sus respuestas fisiológicas.

---

# 2. Efecto de las corrientes eléctricas en el cuerpo humano

El paso de corriente eléctrica a través del cuerpo humano puede producir diferentes efectos fisiológicos que dependen principalmente de la intensidad de la corriente, el tiempo de exposición, el tipo de corriente (continua o alterna), la frecuencia y la trayectoria que sigue dentro del cuerpo. Cuando la corriente atraviesa órganos vitales como el corazón o el sistema nervioso central, el riesgo de daño es considerablemente mayor.

Corrientes menores a 1 mA: generalmente son imperceptibles o apenas detectables por la persona. En la mayoría de los casos no producen efectos fisiológicos relevantes.

Entre 1 mA y 5 mA: pueden generar una sensación leve de cosquilleo o vibración en la piel, pero normalmente no representan un riesgo significativo para la salud.

Entre 5 mA y 20 mA: comienzan a producir contracciones musculares involuntarias. En este rango puede aparecer el llamado efecto de no soltar, donde la persona tiene dificultad para liberar el objeto conductor debido a la contracción de los músculos de la mano.

Mayores a 50 mA: el riesgo se vuelve mucho más grave, ya que la corriente puede interferir con la actividad eléctrica del corazón, provocando fibrilación ventricular, alteraciones del ritmo cardíaco e incluso paro cardíaco si la exposición se prolonga.

Además de la intensidad, el tipo de corriente influye en el nivel de peligro. La corriente alterna (AC), especialmente en frecuencias de red de 50–60 Hz, suele ser más peligrosa que la corriente continua (DC) porque puede generar contracciones musculares repetitivas y afectar con mayor facilidad la actividad eléctrica del corazón. También es importante considerar que el daño aumenta cuando la corriente atraviesa el tórax, ya que puede afectar directamente el sistema cardíaco.

En el campo de la instrumentación biomédica, los dispositivos están diseñados para operar con niveles de corriente extremadamente bajos con el fin de proteger al paciente. Por ejemplo, en sensores de GSR (Galvanic Skin Response) o respuesta galvánica de la piel, se utilizan corrientes muy pequeñas para medir cambios en la conductancia de la piel asociados a la actividad del sistema nervioso autónomo. Estas corrientes se mantienen muy por debajo de 1 mA, normalmente en el rango de microamperios, lo que garantiza que el procedimiento sea seguro y no genere efectos adversos en el usuario. Además, los equipos biomédicos incorporan sistemas de aislamiento eléctrico, limitadores de corriente y normas de seguridad, para evitar cualquier riesgo durante su uso clínico o experimental.

---

# 3. Cálculo de la corriente máxima en el sistema de medición

El sistema de medición propuesto utiliza fuentes de baja tensión de aproximadamente 3.3 V, que son comunes en plataformas embebidas y microcontroladores utilizados en proyectos biomédicos y de instrumentación, como Arduino o ESP32. El uso de este tipo de voltajes reducidos es una medida importante de seguridad, ya que limita naturalmente la cantidad de corriente que puede circular a través del cuerpo del usuario.

Para analizar el comportamiento del circuito, el sistema puede modelarse de forma sencilla como una resistencia fija 
𝑅1 conectada en serie con la resistencia de la piel 𝑅𝑠𝑘𝑖𝑛	​

La resistencia de la piel humana puede variar dependiendo de factores como la humedad, la presión de los electrodos, la temperatura y el estado fisiológico de la persona. En general, este valor puede encontrarse en un rango aproximado de varios kiloohmios a cientos de kiloohmios.

La corriente que circula por el circuito se puede calcular aplicando la Ley de Ohm, considerando que las resistencias están en serie:

$I = \frac{V}{R_1 + R_{skin}}$

Donde:

𝐼 es la corriente que circula por el sistema
𝑉 es el voltaje de alimentación (3.3 V)
𝑅1 es la resistencia fija del circuito
𝑅𝑠𝑘𝑖𝑛 es la resistencia de la piel del usuario

Al considerar valores típicos de resistencia en este tipo de mediciones, la corriente resultante es extremadamente baja, generalmente en el orden de microamperios (µA). Incluso si se analiza una condición desfavorable en la que la resistencia de la piel disminuye, la presencia de la resistencia fija en serie limita significativamente el paso de corriente.

Este valor calculado es mucho menor al umbral de 1 mA, que se considera el límite a partir del cual una persona puede empezar a percibir el paso de corriente eléctrica. Por lo tanto, el diseño del sistema asegura que la corriente que atraviesa el cuerpo sea muy inferior a los niveles peligrosos, cumpliendo con los principios de seguridad eléctrica utilizados en instrumentación biomédica.

En consecuencia, el circuito propuesto puede considerarse seguro para el usuario, ya que la combinación de bajo voltaje de alimentación y limitación de corriente mediante resistencias garantiza que incluso en condiciones desfavorables el usuario no estará expuesto a riesgos eléctricos significativos durante la medición.


---

# 4. Diseño del dispositivo vestible

El dispositivo está concebido como un **sistema portátil, ligero y ergonómico**, diseñado para permitir la **adquisición continua de la señal GSR (Galvanic Skin Response)** sin interferir significativamente con las actividades cotidianas del usuario. 

El objetivo del diseño es que el sistema pueda utilizarse durante periodos prolongados de tiempo, permitiendo registrar cambios fisiológicos asociados al **estrés, excitación emocional o actividad del sistema nervioso autónomo**, mientras la persona realiza actividades normales como trabajar, estudiar o interactuar con dispositivos electrónicos.

---

## Componentes principales

El sistema está compuesto por varios elementos electrónicos que permiten la medición, procesamiento y transmisión de la señal fisiológica.

### Unidad electrónica

Ubicada en la muñeca, con un formato similar al de un **reloj inteligente o pulsera biométrica**. Esta unidad contiene:

- Microcontrolador ESP32
- Circuito de medición de conductancia de la piel
- Sistema de acondicionamiento de señal
- Fuente de alimentación
- Módulo de comunicación inalámbrica (Bluetooth)

El ESP32 se encarga de adquirir la señal analógica proveniente de los electrodos, procesarla y transmitir los datos hacia un computador o dispositivo móvil para su posterior análisis.

### Electrodos

Se utilizan dos electrodos metálicos tipo disco o moneda, colocados sobre la superficie de la piel.

Los electrodos se fijan en la palma de la mano mediante adhesivos médicos o soportes flexibles que permiten:

- Mantener contacto estable con la piel  
- Reducir artefactos por movimiento  
- Garantizar comodidad durante el uso  

Estos electrodos permiten medir los cambios en la **conductancia eléctrica de la piel**, asociados a la actividad de las glándulas sudoríparas.

---

## Justificación de la ubicación de los electrodos

La **palma de la mano** es una de las zonas más utilizadas en mediciones de GSR debido a sus características fisiológicas.

Las principales razones son:

- Alta densidad de glándulas sudoríparas ecrinas, controladas por el sistema nervioso simpático.
- Mayor sensibilidad a cambios fisiológicos relacionados con el estrés o la actividad emocional.
- Mejor relación señal ruido, lo que facilita la detección de variaciones en la conductancia.
- Contacto más estable entre electrodo y piel, reduciendo interferencias externas.

Por estas razones, la palma es una ubicación ampliamente utilizada en estudios psicofisiológicos y experimentos de respuesta emocional.

---

## Ventajas del diseño

El diseño propuesto busca combinar **precisión en la medición, comodidad para el usuario y portabilidad**.

**Portabilidad**
- El módulo electrónico en la muñeca mantiene el sistema compacto y fácil de transportar.

**Comodidad**
- Los electrodos en la palma permiten mediciones sin limitar significativamente los movimientos naturales de la mano.

**Fiabilidad**
- La configuración mejora la estabilidad de la señal y reduce interferencias externas.

**Monitoreo continuo**
- Permite registrar señales fisiológicas durante periodos prolongados.

---

## Aplicaciones del dispositivo

Este sistema puede utilizarse en diferentes áreas:

- Investigación psicofisiológica
- Monitoreo de estrés
- Estudios de respuesta emocional
- Interacción humano–máquina

Gracias a su diseño portátil y seguro, el dispositivo puede emplearse como una herramienta práctica para el monitoreo fisiológico en tiempo real.
