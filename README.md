# Estimaci-n-del-nivel-de-estres-basada-en-la-respuesta-galv-nica-cut-nea-GSR-
Sara Damaris Vasquez Cardenas y Paula Andrea Vega Pardo


# Actividad Electrodérmica (EDA) y Respuesta Galvánica Cutánea (GSR)

## 1. Actividad electrodérmica y respuesta galvánica cutánea

La **actividad electrodérmica (EDA)** es un fenómeno fisiológico que refleja la interacción entre el sistema nervioso autónomo y la piel. Se manifiesta como variaciones en la conductancia cutánea, directamente relacionadas con la activación de las glándulas sudoríparas ecrinas, controladas por el sistema nervioso simpático.

Cuando un individuo se expone a estímulos de diversa naturaleza —ya sean emocionales como el miedo, la alegría o la ansiedad; cognitivos como la atención sostenida o la concentración intensa; o fisiológicos como el dolor o el esfuerzo físico— se produce una activación del sistema nervioso simpático. Este aumento en la actividad autonómica desencadena la estimulación de las glándulas sudoríparas ecrinas, responsables de la sudoración.
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

El paso de corriente eléctrica por el cuerpo humano puede generar efectos que dependen de la intensidad, duración, tipo de corriente y trayectoria.

- **Corrientes menores a 1 mA:** generalmente imperceptibles o apenas detectables.
- **Entre 1 mA y 5 mA:** producen cosquilleo leve, sin riesgo significativo.
- **Entre 5 mA y 20 mA:** pueden causar contracciones musculares involuntarias, dificultando soltar un conductor.
- **Mayores a 50 mA:** existe riesgo de fibrilación ventricular y alteraciones graves en el ritmo cardíaco.

La **corriente alterna (AC)**, especialmente en frecuencias de red (50–60 Hz), es más peligrosa que la **corriente continua (DC)**, ya que puede inducir contracciones musculares sostenidas y afectar directamente la actividad cardíaca.

En sistemas biomédicos, como los sensores de **GSR**, se emplean corrientes extremadamente bajas, muy por debajo de los niveles peligrosos. El diseño de estos dispositivos debe garantizar que la corriente que atraviesa el cuerpo sea mucho menor a **1 mA**, asegurando la seguridad del usuario en todo momento.

---

# 3. Cálculo de la corriente máxima en el sistema de medición

El sistema propuesto utiliza fuentes de baja tensión (**3.3–5 V**), comunes en plataformas embebidas como Arduino o ESP32.

El circuito se modela como una resistencia fija `R1` en serie con la resistencia de la piel `R_skin`. La corriente se calcula mediante la **Ley de Ohm**:





Este valor es **mucho menor al umbral de 1 mA**, considerado seguro en aplicaciones biomédicas. Por lo tanto, el diseño garantiza que incluso en condiciones desfavorables el usuario no estará expuesto a riesgos eléctricos.

---

# 4. Diseño del dispositivo vestible

El dispositivo está concebido como un **sistema portátil y ergonómico**, que permite la adquisición continua de la señal GSR sin interferir con las actividades cotidianas del usuario.

## Componentes principales

- **Unidad electrónica:** ubicada en la muñeca, similar a un reloj inteligente. Contiene el microcontrolador **ESP32**, el circuito de medición y los módulos de transmisión de datos.
- **Electrodos:** dos discos metálicos tipo moneda, fijados en la palma de la mano mediante adhesivos o soportes flexibles, garantizando contacto estable y cómodo.

## Justificación de la ubicación de los electrodos

La palma de la mano es una región óptima porque:

- Tiene **alta densidad de glándulas sudoríparas ecrinas**, muy sensibles a la actividad simpática.
- Ofrece **mayor sensibilidad a cambios fisiológicos**.
- Presenta **mejor relación señal–ruido** y menor interferencia externa.
- Permite un **contacto estable y confiable** entre electrodo y piel.

## Ventajas del diseño

- **Portabilidad:** el módulo en la muñeca mantiene el sistema compacto.
- **Comodidad:** los electrodos en la palma no interfieren con movimientos naturales.
- **Fiabilidad:** la configuración asegura registros precisos incluso durante tareas cognitivas o actividades cotidianas.

Este diseño convierte al dispositivo en una herramienta práctica para:

- Investigación psicofisiológica  
- Monitoreo de estrés  
- Aplicaciones de interacción humano–máquina
