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


#PARTE B

# Funcionamiento del circuito de medición de GSR

## 1. Principio de funcionamiento del circuito

El circuito diseñado para la medición de la **respuesta galvánica cutánea (GSR)** tiene como objetivo transformar las variaciones de la resistencia eléctrica de la piel en una señal de voltaje que pueda ser capturada y procesada por un microcontrolador. Este tipo de medición se basa en un principio eléctrico relativamente sencillo, en el cual la resistencia de la piel forma parte de un circuito resistivo que actúa como un divisor de voltaje.

El sistema se compone de varios elementos fundamentales que permiten realizar la medición de manera estable y segura. Entre estos componentes se encuentran:

- **Electrodos metálicos** colocados sobre la palma de la mano del usuario  
- **Una resistencia fija** \( R_1 = 68\,k\Omega \)  
- **Un condensador** \( C_1 = 1\,\mu F \)  
- **La entrada analógica del microcontrolador** (A0)

Los electrodos metálicos se colocan en contacto directo con la piel del usuario para establecer un camino eléctrico a través del tejido cutáneo. La resistencia que aparece entre estos electrodos corresponde a la **resistencia de la piel**, denotada como \(R_{skin}\). Este valor no es constante, ya que depende de diversos factores fisiológicos, principalmente del nivel de sudoración presente en la superficie cutánea.

Cuando se produce una activación del **sistema nervioso simpático**, como ocurre durante estados de estrés, excitación emocional o aumento de la carga cognitiva, se estimula la actividad de las **glándulas sudoríparas ecrinas**. Como resultado, aumenta la secreción de sudor en la piel. Este incremento en la humedad superficial reduce la resistencia eléctrica del tejido cutáneo, lo que provoca cambios detectables en el circuito de medición.

Desde una perspectiva eléctrica, la resistencia fija \(R_1\) y la resistencia de la piel \(R_{skin}\) se encuentran conectadas en serie, formando un **divisor de voltaje**. El voltaje resultante en el nodo intermedio del divisor corresponde a la señal de salida del circuito, la cual es enviada a la entrada analógica del microcontrolador.

Cuando la resistencia de la piel experimenta variaciones debido a cambios fisiológicos, el voltaje presente en este nodo también se modifica. De esta manera, las fluctuaciones en la conductancia eléctrica de la piel se transforman en **variaciones de voltaje**, que posteriormente pueden ser digitalizadas mediante el **convertidor analógico–digital (ADC)** del microcontrolador.

El condensador \(C_1\) cumple una función importante dentro del sistema. Este componente actúa como un **filtro pasivo**, cuya finalidad es reducir el ruido eléctrico presente en la señal y suavizar variaciones demasiado rápidas o inestables. Gracias a este filtrado, la señal obtenida presenta una mayor estabilidad, lo que facilita su posterior análisis y procesamiento.

El microcontrolador utilizado en el sistema, como **ESP32 o Arduino**, realiza mediciones continuas del voltaje presente en la salida del divisor resistivo. Los datos obtenidos pueden ser enviados a un computador a través de una interfaz de comunicación, permitiendo su visualización en tiempo real mediante herramientas de análisis y adquisición de datos, como **MATLAB**.

En conjunto, el circuito permite convertir cambios fisiológicos relacionados con la actividad del sistema nervioso autónomo en una **señal eléctrica cuantificable**, lo que posibilita el monitoreo de la actividad electrodérmica del usuario.

---

# Análisis del sistema

## 1. Eficacia del sistema para monitoreo ambulatorio del estrés

El sistema desarrollado permite registrar variaciones en la conductancia eléctrica de la piel que están asociadas con cambios en la actividad del **sistema nervioso simpático**. Este tipo de señal fisiológica es ampliamente utilizado en estudios de **psicofisiología**, ya que refleja cambios en el nivel de activación del organismo ante estímulos emocionales, cognitivos o ambientales.

Debido a estas características, el dispositivo puede considerarse una herramienta potencialmente útil para el **monitoreo ambulatorio del estrés**, es decir, para la evaluación de cambios fisiológicos en situaciones de la vida cotidiana fuera de un entorno clínico controlado.

Por ejemplo, en ambientes de trabajo u oficinas, el sistema podría detectar incrementos en la conductancia cutánea asociados con momentos de mayor presión laboral, toma de decisiones importantes o situaciones que demanden un alto nivel de concentración. De forma similar, en contextos académicos como aulas universitarias o durante evaluaciones, el sistema podría registrar respuestas fisiológicas relacionadas con la carga cognitiva o la ansiedad.

En el entorno doméstico, el dispositivo también podría utilizarse para observar la respuesta fisiológica del usuario frente a diferentes actividades diarias, permitiendo identificar momentos de relajación o situaciones potencialmente estresantes.

No obstante, es importante considerar que la señal GSR **no es un indicador exclusivo del estrés psicológico**. La respuesta galvánica cutánea refleja la activación del sistema nervioso simpático en general, por lo que puede verse influenciada por diversos factores adicionales. Entre estos se encuentran:

- Cambios en la temperatura ambiental  
- Actividad física o movimientos del usuario  
- Variaciones emocionales no relacionadas con estrés  
- Cambios en la humedad de la piel  

Debido a esta falta de especificidad, el sistema resulta más adecuado para detectar **cambios en el nivel general de activación fisiológica** que para determinar con precisión el nivel de estrés de una persona.

En consecuencia, el dispositivo desarrollado puede ser considerado una herramienta útil para **monitoreo fisiológico en condiciones ambulatorias**, aunque la interpretación de los resultados debe realizarse en conjunto con información contextual o con otros indicadores fisiológicos complementarios.

---

## 2. Alcance y limitaciones para la detección de estrés neonatal

La medición de la respuesta galvánica cutánea también ha sido explorada en el ámbito clínico para evaluar la activación del sistema nervioso autónomo en **recién nacidos**. En algunos estudios médicos, esta señal se ha utilizado como un posible indicador fisiológico para evaluar respuestas al dolor o a estímulos médicos durante procedimientos clínicos.

En teoría, la medición de la conductancia cutánea podría proporcionar información valiosa sobre el estado fisiológico de los neonatos, ya que permite observar cambios en la actividad autonómica sin necesidad de procedimientos invasivos.

Sin embargo, el sistema desarrollado durante esta práctica presenta varias limitaciones importantes que dificultan su aplicación en este tipo de población.

En primer lugar, el **diseño físico del dispositivo** no está optimizado para el uso en recién nacidos. Los electrodos utilizados y el mecanismo de fijación fueron diseñados para adultos, por lo que podrían resultar inadecuados para la piel extremadamente sensible y delicada de los neonatos.

Además, los recién nacidos presentan movimientos frecuentes e impredecibles, lo que puede generar **artefactos significativos en la señal**. Estos artefactos dificultan la obtención de mediciones estables y confiables.

Otro aspecto importante es que el **sistema nervioso autónomo neonatal** se encuentra en desarrollo, por lo que sus patrones fisiológicos pueden diferir considerablemente de los observados en adultos. Esto hace que la interpretación de la señal GSR en neonatos sea más compleja y requiera modelos fisiológicos específicos.

Por otro lado, los dispositivos utilizados en entornos clínicos deben cumplir estrictas **normativas de seguridad médica, certificaciones regulatorias y validaciones clínicas**, requisitos que superan el alcance del prototipo desarrollado en esta práctica académica.

Por estas razones, aunque la medición de conductancia cutánea tiene potencial en el monitoreo fisiológico neonatal, el dispositivo construido en laboratorio debe considerarse únicamente como **un prototipo educativo y experimental**, y no como una herramienta clínica para la evaluación del estrés en recién nacidos.


## Análisis de gráficas y código

## Gráfica de Calibración

La primera gráfica corresponde al proceso de calibración del sistema GSR/EDA, donde se establece el nivel basal de conductancia cutánea del usuario antes de comenzar la medición en tiempo real.

Durante los primeros segundos se observa que la señal del ADC se mantiene estable alrededor de 4100 unidades, lo cual indica que el usuario se encontraba en reposo y sin estímulos que activaran el sistema nervioso simpático. Esta estabilidad es fundamental, ya que permite calcular de forma confiable los parámetros estadísticos de referencia del sistema:

μ (mu): valor promedio de la señal basal.

σ (sigma): desviación estándar de la señal.

Estos parámetros se utilizan posteriormente para normalizar la señal mediante Z-score, lo que permite comparar cambios fisiológicos respecto al estado basal del usuario.

Aproximadamente entre −3 s y −2 s se observa una caída pronunciada de la señal hasta cerca de 2700 unidades ADC. Este cambio puede interpretarse como un aumento temporal en la conductancia de la piel, lo cual implica una disminución de la resistencia cutánea. Fisiológicamente esto ocurre cuando:

aumenta la actividad del sistema nervioso simpático

se activan las glándulas sudoríparas ecrinas

se incrementa ligeramente la humedad de la piel

Posteriormente la señal regresa gradualmente al nivel basal cercano a 4100, lo cual indica que la activación fisiológica fue momentánea.

En términos de GSR, este comportamiento corresponde a una respuesta de conductancia cutánea (SCR) caracterizada por:

incremento rápido

recuperación lenta hacia el nivel basal

Este tipo de respuesta puede estar asociado a estímulos como:

una respiración profunda

un pequeño movimiento

un cambio emocional leve

variación en la presión de los electrodos.

En general, la gráfica muestra que el sistema es capaz de detectar cambios fisiológicos reales en la conductancia cutánea, lo que confirma el correcto funcionamiento del circuito y del proceso de adquisición.


### Gráfica en tiempo real

La segunda figura muestra la señal normalizada mediante Z-score, lo que permite evaluar el nivel de activación fisiológica respecto a la calibración inicial.

En esta gráfica se incluyen tres referencias importantes:

Baseline (Z = 0) → estado basal del usuario

Umbral de relajación (~0.5 σ)

Umbral de estrés (~1.5 σ)

Durante el intervalo observado, la señal presenta valores negativos entre −0.5 y −1.5 σ, lo que indica que la conductancia de la piel es menor que el promedio registrado durante la calibración. Esto puede interpretarse como un estado de baja activación simpática, coherente con un estado fisiológico relajado.

Además, el sistema muestra el indicador:

Estado: RELAJADO
Z_mean ≈ −0.09
SCR ≈ 0 picos/min

Esto significa que:

el promedio del Z-score está muy cercano al baseline

no se detectan respuestas rápidas de conductancia (SCR) en la ventana analizada

la actividad fisiológica es estable

Por lo tanto, el algoritmo clasifica correctamente el estado del usuario como relajado, lo cual sugiere que el sistema de detección y clasificación está funcionando adecuadamente.


## Funcionamiento del código

```
clc
clear
close all

%% ================== CONFIG ==================
puerto   = "COM3";
baudrate = 115200;

fs = 500;                     % OJO: si tu ESP32/Arduino NO envía 500 muestras/s reales, baja esto (p.ej. 50-200)
Ts = 1/fs;

calibSec  = 20;               % segundos de calibración (quieto, sin moverte)
windowVis = 5;                % segundos visibles en la gráfica
winClass  = 10;               % ventana (s) para clasificar estrés/relajación

% Umbrales (por Z-score respecto a calibración)
Z_STRESS   = 1.5;             % si sube > 1.5 sigmas sostenido → estrés probable
Z_RELAX    = 0.5;             % si está cerca de baseline (< 0.5 sigmas) → relajado probable

% Parámetros de "eventos" (SCR) para robustez
peakMinDistSec = 1.0;         % mínimo 1s entre picos
peakMinPromZ   = 1.0;         % prominencia mínima en unidades Z (aprox)

%% ================== SERIAL ==================
s = serialport(puerto, baudrate);
configureTerminator(s,"LF");
s.Timeout = 2;                % evita bloqueos eternos
flush(s);

fprintf("Conectado a %s @ %d\n", puerto, baudrate);

%% ================== FUNCIÓN LECTURA ROBUSTA ==================
readOne = @() localReadLineAsDouble(s);

%% ================== 1) CALIBRACIÓN ==================
Ncal = round(calibSec*fs);
cal  = nan(Ncal,1);

fprintf("\n=== CALIBRACIÓN (%ds) ===\n", calibSec);
fprintf("Quédate quiet@ y relajad@...\n");

% Gráfica calibración
Nvis = max(10, round(windowVis*fs));
buf  = zeros(Nvis,1);
tvis = (-Nvis+1:0)'/fs;

figure('Name','GSR/EDA - Calibración')
h = plot(tvis, buf, 'LineWidth', 1.5); grid on
xlabel('Tiempo [s]')
ylabel('Señal (ADC / unidades crudas)')
title('CALIBRACIÓN: mantente quiet@')
drawnow

i = 1;
while i <= Ncal
    v = readOne();
    if ~isnan(v)
        cal(i) = v;

        buf(1:end-1) = buf(2:end);
        buf(end)     = v;

        % Suavizado solo visual
        yv = movmean(buf, 5);
        h.YData = yv;

        % Escala suave
        ytmp = yv(~isnan(yv));
        if ~isempty(ytmp)
            yr = max(1, 1.2*range(ytmp));
            ym = mean(ytmp);
            ylim([ym-yr ym+yr]);
        end

        drawnow limitrate
        i = i + 1;
    end
end

% Baseline de calibración (suaviza un poco para robustez)
cal_f = movmean(cal, 5, 'omitnan');
base_mu  = mean(cal_f, 'omitnan');
base_sig = std(cal_f,  'omitnan');

% Evitar sigma cero
if base_sig < 1e-6
    base_sig = 1e-6;
end

fprintf("Baseline (mu)=%.3f | sigma=%.3f\n", base_mu, base_sig);

%% ================== 2) ADQUISICIÓN + CLASIFICACIÓN ==================
respuesta = inputdlg("Tiempo de grabación (s):","GSR/EDA",1,{"30"});
T = str2double(respuesta{1});
if isnan(T) || T<=0
    clear s
    error("Tiempo inválido");
end

N = round(T*fs);
t = (0:N-1)'/fs;
datos = nan(N,1);

% buffers para clasificación
Nclass = max(5, round(winClass*fs));
bufClass = nan(Nclass,1);

% Parámetros pico
peakMinDist = round(peakMinDistSec*fs);

figure('Name','GSR/EDA - Tiempo real')
buf2  = zeros(Nvis,1);
h2 = plot(tvis, buf2, 'LineWidth', 1.5); grid on
xlabel('Tiempo [s]')
ylabel('Z-score (respecto a calibración)')
title('GSR/EDA en tiempo real')
hold on
yline(Z_STRESS,'--','Estrés (umbral)');
yline(Z_RELAX ,'--','Relajado (cerca baseline)');
yline(0,'-','Baseline');
hold off

txt = annotation('textbox',[0.15 0.80 0.7 0.12], ...
    'String',"Estado: ...", 'FitBoxToText','on', ...
    'FontSize',12,'FontWeight','bold');

fprintf("\n=== GRABACIÓN (%ds) ===\n", T);
fprintf("Leyendo y clasificando...\n");

i = 1;
while i <= N
    v = readOne();
    if ~isnan(v)

        datos(i) = v;

        % --------- buffer visual (convertido a Z para ver claro) ----------
        buf2(1:end-1) = buf2(2:end);
        z = (v - base_mu)/base_sig;
        buf2(end) = z;

        % suavizado visual
        yv = movmean(buf2, 9);
        h2.YData = yv;

        % eje Y fijo razonable (evita saltos molestos)
        ylim([-4 6]);

        % --------- buffer clasificación (últimos winClass s) ----------
        bufClass(1:end-1) = bufClass(2:end);
        bufClass(end)     = v;

        % Clasificar cuando ya hay suficiente historia
        if sum(~isnan(bufClass)) > 0.7*Nclass
            x = bufClass;
            x = movmean(x, 9, 'omitnan');      % suaviza para rasgo tónico
            zwin = (x - base_mu)/base_sig;

            % Rasgo 1: nivel tónico (promedio Z en ventana)
            z_mean = mean(zwin, 'omitnan');

            % Rasgo 2: "eventos" (picos) por minuto aprox
            zw = zwin(~isnan(zwin));
            scr_rate_min = 0;
            if numel(zw) > peakMinDist+10
                % contamos picos en Z (prominencia y distancia)
                [pks, locs] = findpeaks(zw, ...
                    'MinPeakDistance', peakMinDist, ...
                    'MinPeakProminence', peakMinPromZ);
                scr_rate_min = (numel(pks) / winClass) * 60; % picos/min
            end

            % Reglas simples (robustas)
            if (z_mean >= Z_STRESS) || (scr_rate_min >= 12)    % >=12 picos/min (ajustable)
                estado = "ESTRÉS probable";
            elseif (z_mean <= Z_RELAX) && (scr_rate_min <= 6)  % <=6 picos/min
                estado = "RELAJADO";
            else
                estado = "NEUTRO / transitorio";
            end

            txt.String = sprintf("Estado: %s\nZ_mean=%.2f | SCR≈%.1f picos/min", ...
                                 estado, z_mean, scr_rate_min);
        end

        drawnow limitrate
        i = i + 1;
    end
end

%% ================== GUARDADO ==================
out.nombre_archivo = "GSR_EDA_" + datestr(now,"yyyymmdd_HHMMSS") + ".mat";
out.fs = fs;
out.t  = t;
out.datos = datos;
out.calibracion = cal;
out.baseline_mu = base_mu;
out.baseline_sigma = base_sig;
save(out.nombre_archivo, "-struct", "out");

fprintf("\nGuardado: %s\n", out.nombre_archivo);

clear s
disp("Listo: calibración + grabación + clasificación finalizadas")

%% ================== FUNCIÓN LOCAL ==================
function v = localReadLineAsDouble(s)
    v = nan;
    try
        if s.NumBytesAvailable > 0
            str = readline(s);
            str = strtrim(str);
            % limpia cosas raras tipo "GSR:1234"
            tok = regexp(str,'[-+]?\d*\.?\d+','match');
            if ~isempty(tok)
                v = str2double(tok{end});
                if ~isfinite(v), v = nan; end
            end
        end
    catch
        v = nan;
    end
% end
```

---

# Preguntas de análisis

## 1. ¿Por qué una inspiración profunda aumenta la respuesta galvánica cutánea?

Una inspiración profunda puede provocar un aumento en la respuesta galvánica cutánea debido a los efectos que la respiración ejerce sobre la regulación del **sistema nervioso autónomo**.

Durante la respiración profunda se producen variaciones en el equilibrio entre la actividad del sistema nervioso simpático y parasimpático. Estos cambios pueden modificar diversas funciones fisiológicas del organismo, incluyendo la actividad de las **glándulas sudoríparas**.

Cuando se produce una activación del sistema nervioso simpático, las glándulas sudoríparas ecrinas presentes en la piel incrementan su actividad secretora. Como consecuencia, aumenta la cantidad de sudor en la superficie cutánea.

El sudor contiene electrolitos que facilitan el paso de corriente eléctrica a través de la piel. Por lo tanto, un aumento en la sudoración provoca una **disminución de la resistencia eléctrica de la piel** y, en consecuencia, un **incremento en la conductancia cutánea**.

Debido a este fenómeno, durante o inmediatamente después de una inspiración profunda suele observarse un aumento temporal en la señal GSR, seguido posteriormente por un retorno gradual al nivel basal.

---

## 2. Ventajas y desventajas del uso de la GSR como indicador de estrés

La respuesta galvánica cutánea presenta diversas ventajas como herramienta para el estudio de la actividad fisiológica del organismo. Una de sus principales fortalezas es que constituye una **medida objetiva de la activación del sistema nervioso simpático**, lo que permite evaluar cambios fisiológicos asociados con diferentes estados emocionales o cognitivos.

Otra ventaja importante es que la medición de esta señal puede realizarse mediante **circuitos relativamente simples y de bajo costo**, lo que facilita el desarrollo de dispositivos portátiles y sistemas de monitoreo fisiológico accesibles.

Además, la señal GSR presenta una **alta sensibilidad a cambios en la activación emocional y cognitiva**, lo que la convierte en un indicador útil en áreas como la psicofisiología, la neurociencia aplicada y la interacción humano–máquina.

Sin embargo, también existen algunas limitaciones importantes. Una de las principales es que la respuesta galvánica cutánea **no es específica del estrés**, ya que cualquier estímulo que active el sistema nervioso simpático puede generar cambios en la conductancia de la piel.

Asimismo, factores externos como:

- la temperatura ambiental  
- el movimiento del usuario  
- la presión o estabilidad del contacto de los electrodos  

pueden introducir **ruido o artefactos en la señal**.

Otra limitación relevante es que la respuesta fisiológica puede variar considerablemente entre individuos, debido a diferencias en la actividad de las glándulas sudoríparas, la hidratación de la piel o características fisiológicas propias de cada persona.

Por estas razones, la GSR suele utilizarse como **un indicador complementario dentro de sistemas de monitoreo fisiológico multimodal**, en los que se combinan diferentes señales biomédicas para obtener una evaluación más completa del estado fisiológico del usuario.

