# Introducción
El estudio de la respuesta cardiovascular frente a distintos estímulos permite comprender cómo el organismo se adapta a cambios fisiológicos como el ejercicio, la hiperventilación y la hipoxia. El electrocardiograma (ECG) es una herramienta fundamental para analizar la actividad eléctrica del corazón y detectar variaciones en su funcionamiento bajo diferentes condiciones. En este trabajo se registraron señales electrocardiográficas utilizando un sistema de adquisición de datos, con el objetivo de evaluar y comparar la respuesta cardíaca de un sujeto en estado basal y ante diversos estímulos controlados. Los datos obtenidos fueron procesados y analizados para identificar cambios en la frecuencia cardíaca y en la señal ECG, contribuyendo a una mejor comprensión del comportamiento cardiovascular.

# Metodología
Para el estudio de la respuesta cardiovascular del sujeto, fue empleado el dispositivo BITalino Core, placa especializada en la captación de señales fisiológicas, a la cual se le conectó un sensor de electrocardiograma con tres electrodos, de los cuales surgirán las tres derivaciones a ser estudiadas. El dispositivo fue conectado a una laptop con Windows 10 al software Open Signals a través de comunicación Bluetooth. El software nos permitió realizar las grabaciones de las señales en cada una de las pruebas realizadas. Los pasos realizados en la experiencia de laboratorio fueron los siguientes:
1. Los electrodos fueron conectados al puerto A2 de la placa, designado para la captación de señales ECG. Una vez conectado, fue configurado en el software como “ECG”. Los electrodos captan las señales a través de una interfaz adhesiva colocadas en puntos claves del sujeto. Los electrodos están configurados de manera positiva, negativa y de referencia. La variación de sus posiciones a través de los adhesivos es lo que nos permite captar las distintas derivaciones del electrocardiograma.
2. La primera captación que se realizó en el sujeto fue la del estado basal. Bajo un estado de relajación, se tomaron los datos del sujeto, en cada una de las derivaciones, durante 30 segundos. Esto se realizó dos veces. Con este estado basal compararemos las siguientes pruebas.
3. Después de captar el estado basal del sujeto, se le indica a este que realice una hiperventilación: rápidas inhalaciones y exhalaciones consecutivas hasta que sienta un ligero mareo. Una vez se realiza la hiperventilación, se vuelve a medir el estado del paciente, nuevamente 30 segundos por derivación. El ejercicio se realiza dos veces.
4. Una vez finalizada la prueba de hiperventilación, se deja descansar al paciente unos cinco minutos para volver a medir su estado basal. Nuevamente 30 segundos por cada derivación. A partir de esto deseamos determinar si hay algún cambio en el estado basal del paciente después de la hiperventilación.
5. Ahora es momento del ejercicio intenso. Se le indica al paciente realizar burpees por cinco minutos sin descanso.El ejercicio busca aumentar bruscamente la frecuencia cardíaca y evaluar tanto su respuesta como la del dispositivo de captación ante este aumento. Apenas terminan los cinco minutos de ejercicio, se colocan rápidamente los electrodos para la medición de las tres derivaciones (30 segundos cada una), y se cambia de derivación de la manera más rápida posible, con el fin de no presentar grandes diferencias entre las mediciones.
6. Después de que el paciente descansa 5 minutos, este es sometido a un nuevo ejercicio: subir y bajar escaleras por un total de 8 minutos. Después del ejercicio inmediatamente se colocan los electrodos para las respectivas mediciones y se deja al sujeto descansar por otros cinco minutos.
7. La última prueba es la hipoxia. Durante la prueba, el sujeto retiene el aliento por el mayor tiempo posible y apenas exhala se realiza la medición de las tres derivaciones, por 30 segundos cada una. El ejercicio se realiza dos veces.
8. Todos las mediciones son analizadas en un programa de Python, bajo la plataforma Google Colab. En esta se realizan comparaciones entre las distintas pruebas y la respuesta del paciente a ellas.


# Resultados
## Fotos
![1](VIDEOS%20Y%20FOTOS/1.png)
![2](VIDEOS%20Y%20FOTOS/2.png)
![3](VIDEOS%20Y%20FOTOS/3.png)
![4](VIDEOS%20Y%20FOTOS/4.png)
![5](VIDEOS%20Y%20FOTOS/5.png)

## Ploteo de señales
### Estado Basal 1
#### Derivada I
##### Registro electrocardiográfico en reposo
| Parámetro           | Valor       |
|---------------------|-------------|
| Duración total      | 32.8 s      |
| Muestras            | 32,850      |
| Picos R detectados  | 51          |
| RR medio            | 647.5 ms    |
| FC estimada         | 92.7 bpm    |
##### Graficas
![Estado Basal Derivada I](<VIDEOS Y FOTOS/EstadoBasal1/D1SIGNAL.png>)
![EKG derivada I](<VIDEOS Y FOTOS/EstadoBasal1/EKG1.png>)
![Transformada de Fourier Derivada I](<VIDEOS Y FOTOS/EstadoBasal1/FFT1.png>)

#### Derivada II
##### Registro electrocardiográfico en reposo
| Parámetro          | Valor    |
|--------------------|----------|
| Duración total     | 35.4 s   |
| Muestras           | 35,400   |
| Picos R detectados | 52       |
| RR medio           | 690.0 ms |
| FC estimada        | 87.0 bpm |

##### Graficas
![Estado Basal Derivada I](<VIDEOS Y FOTOS/EstadoBasal1/D2SIGNAL.png>)
![EKG derivada I](<VIDEOS Y FOTOS/EstadoBasal1/EKG2.png>)
![Transformada de Fourier Derivada I](<VIDEOS Y FOTOS/EstadoBasal1/FFT2.png>)

#### Derivada III
##### Registro electrocardiográfico en reposo
| Parámetro          | Valor    |
|--------------------|----------|
| Duración total     | 30.7 s   |
| Muestras           | 30,750   |
| Picos R detectados | 49       |
| RR medio           | 635.5 ms |
| FC estimada        | 94.4 bpm |
##### Graficas
![Estado Basal Derivada I](<VIDEOS Y FOTOS/EstadoBasal1/D3SIGNAL.png>)
![EKG derivada I](<VIDEOS Y FOTOS/EstadoBasal1/EKG3.png>)
![Transformada de Fourier Derivada I](<VIDEOS Y FOTOS/EstadoBasal1/FFT3.png>)
---
### Estado Basal 2
#### Derivada I
##### Registro electrocardiográfico en reposo
| Parámetro           | Valor       |
|---------------------|-------------|
| Duración total      | 31.8 s      |
| Muestras            | 31,800      |
| Picos R detectados  | 60          |
| RR medio            | 532.3 ms    |
| FC estimada         | 112.7 bpm    |
##### Graficas
![Estado Basal 2 Derivada I](<VIDEOS Y FOTOS/EstadoBasal2/D1SIGNAL.png>)
![EKG derivada I](<VIDEOS Y FOTOS/EstadoBasal2/ECG1.png>)
![Transformada de Fourier Derivada I](<VIDEOS Y FOTOS/EstadoBasal2/FFT1.png>)

#### Derivada II
##### Registro electrocardiográfico en reposo
| Parámetro          | Valor    |
|--------------------|----------|
| Duración total     | 30.6 s   |
| Muestras           | 30,600   |
| Picos R detectados | 51       |
| RR medio           | 605.7 ms |
| FC estimada        | 99.1 bpm |

##### Graficas
![Estado Basal 2 Derivada II](<VIDEOS Y FOTOS/EstadoBasal2/D2SIGNAL.png>)
![EKG derivada II](<VIDEOS Y FOTOS/EstadoBasal2/ECG2.png>)
![Transformada de Fourier Derivada II](<VIDEOS Y FOTOS/EstadoBasal2/FFT2.png>)

#### Derivada III
##### Registro electrocardiográfico en reposo
| Parámetro          | Valor    |
|--------------------|----------|
| Duración total     | 30.7 s   |
| Muestras           | 30,750   |
| Picos R detectados | 49       |
| RR medio           | 628.9 ms |
| FC estimada        | 95.4 bpm |
##### Graficas
![Estado Basal Derivada 2 I](<VIDEOS Y FOTOS/EstadoBasal2/D3SIGNAL.png>)
![EKG derivada I](<VIDEOS Y FOTOS/EstadoBasal2/ECG3.png>)
![Transformada de Fourier Derivada I](<VIDEOS Y FOTOS/EstadoBasal2/FFT3.png>)
---
### Ciclo 1
#### Derivada I
##### Registro electrocardiográfico en reposo
| Parámetro          | Valor    |
|--------------------|----------|
| Duración total     | 30.9 s   |
| Muestras           | 30,900   |
| Picos R detectados | 49       |
| RR medio           | 641.2 ms |
| FC estimada        | 93.6 bpm |
##### Graficas
![Ciclo 1 Derivada I](<VIDEOS Y FOTOS/Ciclo1/D1.png>)
![EKG derivada I](<VIDEOS Y FOTOS/Ciclo1/ECG1.png>)
![Transformada de Fourier Derivada I](<VIDEOS Y FOTOS/Ciclo1/FFT1.png>)

#### Derivada II
##### Registro electrocardiográfico en reposo
| Parámetro          | Valor    |
|--------------------|----------|
| Duración total     | 30.9 s   |
| Muestras           | 30,900   |
| Picos R detectados | 48       |
| RR medio           | 646.0 ms |
| FC estimada        | 92.9 bpm |

##### Graficas
![Ciclo 1 Derivada II](<VIDEOS Y FOTOS/Ciclo1/D2.png>)
![EKG derivada II](<VIDEOS Y FOTOS/Ciclo1/ECG2.png>)
![Transformada de Fourier Derivada II](<VIDEOS Y FOTOS/Ciclo1/FFT2.png>)

#### Derivada III
##### Registro electrocardiográfico en reposo
| Parámetro          | Valor    |
|--------------------|----------|
| Duración total     | 30.9 s   |
| Muestras           | 30,900   |
| Picos R detectados | 47       |
| RR medio           | 665.9 ms |
| FC estimada        | 90.1 bpm |
##### Graficas
![Ciclo1 Derivada III](<VIDEOS Y FOTOS/Ciclo1/D3.png>)
![EKG derivada III](<VIDEOS Y FOTOS/Ciclo1/ECG3.png>)
![Transformada de Fourier Derivada III](<VIDEOS Y FOTOS/Ciclo1/FFT3.png>)
---
### Ciclo 2
#### Derivada I
##### Registro electrocardiográfico en reposo
| Parámetro           | Valor       |
|---------------------|-------------|
| Duración total      | 30.9 s      |
| Muestras            | 30,900      |
| Picos R detectados  | 51          |
| RR medio            | 614.3 ms    |
| FC estimada         | 97.7 bpm    |
##### Graficas
![Ciclo 2 Derivada I](<VIDEOS Y FOTOS/Ciclo2/D1.png>)
![EKG derivada I](<VIDEOS Y FOTOS/Ciclo2/ECG1.png>)
![Transformada de Fourier Derivada I](<VIDEOS Y FOTOS/Ciclo2/FFT1.png>)

#### Derivada II
##### Registro electrocardiográfico en reposo
| Parámetro          | Valor    |
|--------------------|----------|
| Duración total     | 31.0 s   |
| Muestras           | 31,050   |
| Picos R detectados | 51       |
| RR medio           | 616.9 ms |
| FC estimada        | 97.3 bpm |

##### Graficas
![Ciclo 2 Derivada II](<VIDEOS Y FOTOS/Ciclo2/D2.png>)
![EKG derivada II](<VIDEOS Y FOTOS/Ciclo2/ECG2.png>)
![Transformada de Fourier Derivada II](<VIDEOS Y FOTOS/Ciclo2/FFT2.png>)

#### Derivada III
##### Registro electrocardiográfico en reposo
| Parámetro          | Valor    |
|--------------------|----------|
| Duración total     | 30.7 s   |
| Muestras           | 30,750   |
| Picos R detectados | 47       |
| RR medio           | 654.4 ms |
| FC estimada        | 91.7 bpm |
##### Graficas
![Ciclo 2 Derivada III](<VIDEOS Y FOTOS/Ciclo2/D3.png>)
![EKG derivada III](<VIDEOS Y FOTOS/Ciclo2/ECG3.png>)
![Transformada de Fourier Derivada III](<VIDEOS Y FOTOS/Ciclo2/FFT3.png>)
---
### Burpees
#### Derivada I
##### Registro electrocardiográfico en reposo
| Parámetro           | Valor       |
|---------------------|-------------|
| Duración total      | 30.7 s      |
| Muestras            | 30,750      |
| Picos R detectados  | 44          |
| RR medio            | 680.8 ms    |
| FC estimada         | 88.1 bpm    |
##### Graficas
![Burpees Derivada I](<VIDEOS Y FOTOS/Burpees/D1.png>)
![EKG derivada I](<VIDEOS Y FOTOS/Burpees/ECG1.png>)
![Transformada de Fourier Derivada I](<VIDEOS Y FOTOS/Burpees/FFT1.png>)

#### Derivada II
##### Registro electrocardiográfico en reposo
| Parámetro          | Valor    |
|--------------------|----------|
| Duración total     | 30.7 s   |
| Muestras           | 30,750   |
| Picos R detectados | 76       |
| RR medio           | 404.3 ms |
| FC estimada        | 148.4 bpm |

##### Graficas
![Burpees Derivada II](<VIDEOS Y FOTOS/Burpees/D2.png>)
![EKG derivada II](<VIDEOS Y FOTOS/Burpees/ECG2.png>)
![Transformada de Fourier Derivada II](<VIDEOS Y FOTOS/Burpees/FFT2.png>)

#### Derivada III
##### Registro electrocardiográfico en reposo
| Parámetro          | Valor    |
|--------------------|----------|
| Duración total     | 30.7 s   |
| Muestras           | 30,750   |
| Picos R detectados | 71       |
| RR medio           | 431.5 ms |
| FC estimada        | 139.1 bpm |
##### Graficas
![Burpees Derivada III](<VIDEOS Y FOTOS/Burpees/D3.png>)
![EKG derivada III](<VIDEOS Y FOTOS/Burpees/ECG3.png>)
![Transformada de Fourier Derivada III](<VIDEOS Y FOTOS/Burpees/FFT3.png>)
---
### Escalera
#### Derivada I
##### Registro electrocardiográfico en reposo
| Parámetro           | Valor       |
|---------------------|-------------|
| Duración total      | 30.6 s      |
| Muestras            | 30,600      |
| Picos R detectados  | 60          |
| RR medio            | 511.2 ms    |
| FC estimada         | 117.4 bpm    |
##### Graficas
![Escalera Derivada I](<VIDEOS Y FOTOS/Escalera/D1.png>)
![EKG derivada I](<VIDEOS Y FOTOS/Escalera/ECG1.png>)
![Transformada de Fourier Derivada I](<VIDEOS Y FOTOS/Escalera/FFT1.png>)

#### Derivada II
##### Registro electrocardiográfico en reposo
| Parámetro          | Valor    |
|--------------------|----------|
| Duración total     | 30.9 s   |
| Muestras           | 30,900   |
| Picos R detectados | 64       |
| RR medio           | 488.8 ms |
| FC estimada        | 122.7 bpm |

##### Graficas
![Escalera Derivada II](<VIDEOS Y FOTOS/Escalera/D2.png>)
![EKG derivada II](<VIDEOS Y FOTOS/Escalera/ECG2.png>)
![Transformada de Fourier Derivada II](<VIDEOS Y FOTOS/Escalera/FFT2.png>)

#### Derivada III
##### Registro electrocardiográfico en reposo
| Parámetro          | Valor    |
|--------------------|----------|
| Duración total     | 31.0 s   |
| Muestras           | 31,050   |
| Picos R detectados | 62       |
| RR medio           | 501.3 ms |
| FC estimada        | 119.7 bpm |
##### Graficas
![Escalera Derivada III](<VIDEOS Y FOTOS/Escalera/D3.png>)
![EKG derivada III](<VIDEOS Y FOTOS/Escalera/ECG3.png>)
![Transformada de Fourier Derivada III](<VIDEOS Y FOTOS/Escalera/FFT3.png>)
---
### Apnea
#### Derivada I
##### Registro electrocardiográfico en reposo
| Parámetro           | Valor       |
|---------------------|-------------|
| Duración total      | 31.3 s      |
| Muestras            | 31,350      |
| Picos R detectados  | 50          |
| RR medio            | 632.3 ms    |
| FC estimada         | 94.9 bpm    |
##### Graficas
![Apnea Derivada I](<VIDEOS Y FOTOS/Apnea/D1.png>)
![EKG derivada I](<VIDEOS Y FOTOS/Apnea/ECG1.png>)

#### Derivada II
##### Registro electrocardiográfico en reposo
| Parámetro          | Valor    |
|--------------------|----------|
| Duración total     | 30.7 s   |
| Muestras           | 30,750   |
| Picos R detectados | 58       |
| RR medio           | 532.8 ms |
| FC estimada        | 112.6 bpm |

##### Graficas
![Apnea Derivada II](<VIDEOS Y FOTOS/Apnea/D2.png>)
![EKG derivada II](<VIDEOS Y FOTOS/Apnea/ECG2.png>)

#### Derivada III
##### Registro electrocardiográfico en reposo
| Parámetro          | Valor    |
|--------------------|----------|
| Duración total     | 30.6 s   |
| Muestras           | 30,600   |
| Picos R detectados | 58       |
| RR medio           | 528.6 ms |
| FC estimada        | 113.5 bpm |
##### Graficas
![Apnea Derivada III](<VIDEOS Y FOTOS/Apnea/D3.png>)
![EKG derivada III](<VIDEOS Y FOTOS/Apnea/ECG3.png>)
---
### Frecuencia cardiaca en cada caso
![Frecuencia cardiaca en cada caso por derivada](<VIDEOS Y FOTOS/FrecuenciaCardiaca.png>)

# Discusión
## Análisis de resultados
En el presente laboratorio se evaluó la respuesta cardiovascular mediante electrocardiografía en un sujeto universitario de 20 años sometido a diferentes estímulos fisiológicos controlados. Los resultados obtenidos muestran variaciones características en la frecuencia cardíaca (FC) y morfología del ECG que son consistentes con la literatura reciente sobre respuestas cardiovasculares autónomas, como se verá más adelante. Por otro lado, el análisis será en base a las etapas y ejercicios realizados, los cuales fueron 3 etapas, la primera con 3 ejercicios (basal, hiperventilación, basal); la segunda con ejercicios de burpees y subir y bajar escaleras; finalmente, la última etapa con una actividad de hipoventilación.
### I) Primera etapa:
#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1. Estado basal y variabilidad entre derivaciones
    En las mediciones basales se registraron frecuencias cardíacas entre 87.0-94.4 bpm (Basal 1) y 95.4-112.7 bpm (Basal 2), con variaciones entre derivaciones. La FC promedio en reposo para adultos jóvenes sanos se reporta típicamente entre 60-100 bpm [1], por lo que nuestros valores se encuentran dentro del rango normal pero en el extremo superior, posiblemente influenciado por la activación simpática asociada al contexto experimental, actividad que no es usual en la vida del sujeto de estudio. Las diferencias entre derivaciones (hasta 7.7 bpm en Basal 1) reflejan principalmente variaciones en la detección de ondas R debido a diferencias en la amplitud de señal entre configuraciones de electrodos, más que cambios fisiológicos reales, como ha sido documentado en estudios de validación de ECG portátiles [2].
#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2. Respuesta a hiperventilación forzada
    Tras la hiperventilación (Ciclo 1 y Ciclo 2), las frecuencias cardíacas registradas fueron 90.1-93.6 bpm y 91.7-97.7 bpm respectivamente, valores similares o ligeramente superiores al estado basal. Este hallazgo contrasta parcialmente con lo esperado, ya que la hiperventilación típicamente induce taquicardia transitoria por activación simpática y reducción de CO₂ [3]. Sin embargo, las mediciones se realizaron inmediatamente después del ejercicio respiratorio, no durante el mismo, lo que explica el retorno parcial a valores basales. Estudios recientes sobre arritmia sinusal respiratoria han demostrado que la variabilidad de FC durante respiración controlada depende fuertemente del momento de medición y normalización post-ejercicio [4].
### II) Segunda etapa:
#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1. Respuesta al ejercicio intenso
    Los ejercicios de burpees y escaleras produjeron incrementos marcados y sostenidos en la FC. Durante burpees, se registraron las frecuencias más elevadas del estudio: 88.1-148.4 bpm, con la Derivación II alcanzando 148.4 bpm, representando un incremento del 60-70% respecto al estado basal. Este incremento es consistente con la respuesta cardiovascular típica a ejercicio de alta intensidad en adultos jóvenes [5]. El ejercicio de escaleras produjo FC de 117.4-122.7 bpm, valores menores que burpees pero aún sustancialmente elevados, reflejando la naturaleza aeróbica moderada-alta de esta actividad.
    La respuesta cronotrópica al ejercicio está mediada principalmente por retiro parasimpático rápido (primeros segundos) seguido de activación simpática progresiva [6]. El hecho de que las mediciones se realizarán inmediatamente post-ejercicio y en orden secuencial (Derivación I, II, III) explica la tendencia decreciente observada en algunos casos, reflejando el inicio de la fase de recuperación cardiovascular.
### III) Tercera etapa:
#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1. Respuesta a apnea
    Durante la retención respiratoria, se registraron FC de 94.9-113.5 bpm, valores inesperadamente elevados para una maniobra de apnea. La respuesta fisiológica esperada ante apnea voluntaria es bradicardia progresiva mediada por el reflejo de inmersión mamífera, caracterizado por activación vagal y reducción de FC que puede alcanzar 30-50% del valor basal [7,8]. Sin embargo, varios factores metodológicos explican nuestros resultados: (1) la apnea se realizó en ambiente seco sin inmersión facial, reduciendo drásticamente la magnitud del reflejo; estudios recientes confirman que la bradicardia es significativamente menor en apnea seca versus inmersión facial, con reducciones de solo 5-15% de FC basal [9]; (2) el sujeto había realizado ejercicio intenso previo, con posible activación simpática residual; (3) la medición se realizó inmediatamente post-apnea.

### Análisis espectral y morfología ECG
Los gráficos de FFT muestran concentración de energía en frecuencias bajas (0-10 Hz) correspondientes a la frecuencia fundamental del ECG y sus primeros armónicos, patrón normal en registros de corta duración. Las señales crudas en dominio del tiempo evidencian morfología QRS característica con ondas R claramente identificables, permitiendo cálculos fiables de intervalos RR. La variabilidad visible en la línea basal, particularmente notable en algunas derivaciones, refleja artefactos de movimiento y variabilidad respiratoria (arritmia sinusal respiratoria), fenómenos fisiológicos normales documentados extensamente en la literatura [4,10].
## Evaluación de limitaciones basadas en evidencia
### Limitaciones técnicas de adquisición
El uso de electrodos colocados en cuello y cadera en lugar de las posiciones torácicas estándar del triángulo de Einthoven representa la principal limitación técnica, esto se debe a la longitud de los cables, los cuales no son lo suficientemente largos para poder usar el protocolo estandar. Aunque esta configuración permitió registro funcional de actividad eléctrica cardíaca, las "derivaciones" obtenidas no son equiparables a las derivaciones estándar I, II y III clínicas. Estudios de validación de dispositivos ECG portátiles han demostrado que configuraciones no estándar pueden mantener precisión en detección de FC y ritmo, pero alteran significativamente amplitudes de onda y morfología de complejos [2]. Esta limitación afecta principalmente la interpretación morfológica detallada del ECG, no la medición de intervalos RR y FC, que fueron nuestros parámetros principales.
### Orden secuencial de mediciones
La adquisición secuencial de derivaciones (I→II→III) introdujo un sesgo temporal sistemático, particularmente problemático en condiciones post-ejercicio donde la FC cambia rápidamente. En muchos de los ejercicios se medía 30 segundos por derivada, por lo que la Derivación III se midió hasta 1 minuto después de finalizar el ejercicio, momento en que la recuperación cardiovascular ya estaba iniciada. Esto explica parcialmente la tendencia a FC menores en Derivación III observada en algunos protocolos.
### Factores ambientales y contexto experimental
El protocolo no controló temperatura ambiente, nivel de hidratación, estado nutricional ni hora del día, variables que influyen significativamente en FC basal y respuestas al ejercicio [11]. Las condiciones fueron las permitidas por el horario en el que se da el laboratorio. Además, la realización de múltiples protocolos en una sesión extendida pudo generar fatiga acumulativa y activación simpática sostenida, elevando valores basales progresivamente (observable en Basal 2 vs Basal 1). Adicionalmente, el desplazamiento gradual de electrodos adhesivos por sudoración y movimiento pudo afectar la calidad de señal, particularmente en mediciones finales; donde no se pudo realizar la segunda medición de la hipoventilación, pues los electrodos cedieron y la batería del Bitalino se terminó.
### Ausencia de grupo control y n=1
El diseño con un único sujeto imposibilita la generalización de resultados y evaluación de variabilidad inter-individual, por lo que nuestros hallazgos representan únicamente la respuesta de este individuo específico.
### Limitaciones del protocolo de apnea
La apnea se realizó sin estandarización de volumen pulmonar previo ni control de técnica respiratoria, factores críticos que determinan la magnitud del reflejo de inmersión y el volumen pulmonar al inicio de apnea modula significativamente la respuesta cardiovascular [8]. La ausencia de medición de saturación de oxígeno impidió evaluar el grado de hipoxemia alcanzado, variable fundamental para interpretar respuestas cardiovasculares durante apnea [9].
A pesar de estas limitaciones, el estudio cumplió su objetivo educativo de registrar y caracterizar señales electrocardiográficas bajo diferentes condiciones fisiológicas, proporcionando resultados cualitativamente consistentes con respuestas cardiovasculares autónomas documentadas en la literatura científica reciente.

# Referencias
1. Sobieraj P, Siński M, Lewandowski J. Resting heart rate and cardiovascular outcomes during intensive and standard blood pressure reduction: an analysis from SPRINT trial. J Clin Med. 2021;10(15):3264.
2. Rajbhandary PL, Nallathambi G, Selvaraj N, Ratchford SM, Stickford JL, Stickford AS. ECG signal quality assessments of a small bipolar single-lead wearable patch sensor. Cardiovasc Eng Tech. 2022;13(5):783-96.
3. Hu B, Liu Z, Zhao J, Zeng L, Hao G, Shui D, et al. The global prevalence of amblyopia in children: a systematic review and meta-analysis. Front Pediatr. 2022;10:819998.
4. Ghibaudo V, Granget J, Dereli M, Buonviso N, Garcia S. A unifying method to study respiratory sinus arrhythmia dynamics implemented in a new toolbox. eNeuro. 2023;10(10):ENEURO.0197-23.2023.
5. Chiang JK, Lin YC, Hung TY, Kao HH, Kao YH. The impact on autonomic nervous system activity during and following exercise in adults: a meta-regression study and trial sequential analysis. Medicina (Kaunas). 2024;60(8):1223.
5. Fornasiero A, Zignoli A, Rakobowchuk M, Pellegrini B, Schena F, Bortolan L. Post-exercise cardiac autonomic and cardiovascular responses to heart rate-matched and work rate-matched hypoxic exercise. Eur J Appl Physiol. 2021;121(7):2061-76.
6. Kjeld T, Isbrand AB, Linnet K, Zerahn B, Højberg J, Hansen EG, et al. Extreme hypoxia causing brady-arrythmias during apnea in elite breath-hold divers. Front Physiol. 2021;12:712573.
7. Taboni A, Vinetti G, Bruseghini P, Cevese A, Tam E. Advances in breath-hold diving research: a state-of-the-art review. Eur J Appl Physiol. 2025;125(3):963-1006.
8. Ackermann S, Raab M, Backschat S, Smith DJC, Javelle F, Laborde S. The diving response and cardiac vagal activity: a systematic review and meta-analysis. Psychophysiology. 2023;60(3):e14183.
9. Plews DJ, Scott B, Altini M, Wood M, Kilding AE, Laursen PB. Monitoring training adaptation and recovery status in athletes using heart rate variability via mobile devices: a narrative review. Sensors. 2026;26(1):3.
10. Düking P, Fuss FK, Holmberg HC, Sperlich B. Recommendations for assessment of the reliability, sensitivity, and validity of data provided by wearable sensors designed for monitoring physical activity. JMIR Mhealth Uhealth. 2018;6(4):e102


