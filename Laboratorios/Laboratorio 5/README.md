# Introducción
El estudio de la respuesta cardiovascular frente a distintos estímulos permite comprender cómo el organismo se adapta a cambios fisiológicos como el ejercicio, la hiperventilación y la hipoxia. El electrocardiograma (ECG) es una herramienta fundamental para analizar la actividad eléctrica del corazón y detectar variaciones en su funcionamiento bajo diferentes condiciones. En este trabajo se registraron señales electrocardiográficas utilizando un sistema de adquisición de datos, con el objetivo de evaluar y comparar la respuesta cardíaca de un sujeto en estado basal y ante diversos estímulos controlados. Los datos obtenidos fueron procesados y analizados para identificar cambios en la frecuencia cardíaca y en la señal ECG, contribuyendo a una mejor comprensión del comportamiento cardiovascular.

# Metodología
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Para el estudio de la respuesta cardiovascular del sujeto, fue empleado el dispositivo BITalino Core, placa especializada en la captación de señales fisiológicas, a la cual se le conectó un sensor de electrocardiograma con tres electrodos, de los cuales surgirán las tres derivaciones a ser estudiadas. El dispositivo fue conectado a una laptop con Windows 10 al software Open Signals a través de comunicación Bluetooth. El software nos permitió realizar las grabaciones de las señales en cada una de las pruebas realizadas.  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Los electrodos fueron conectados al puerto A2 de la placa, designado para la captación de señales ECG. Una vez conectado, fue configurado en el software como “ECG”. Los electrodos captan las señales a través de una interfaz adhesiva colocadas en puntos claves del sujeto. Los electrodos están configurados de manera positiva, negativa y de referencia. La variación de sus posiciones a través de los adhesivos es lo que nos permite captar las distintas derivaciones del electrocardiograma.  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;La primera captación que se realizó en el sujeto fue la del estado basal. Bajo un estado de relajación, se tomaron los datos del sujeto, en cada una de las derivaciones, durante 30 segundos. Esto se realizó dos veces. Con este estado basal compararemos las siguientes pruebas.  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Después de captar el estado basal del sujeto, se le indica a este que realice una hiperventilación: rápidas inhalaciones y exhalaciones consecutivas hasta que sienta un ligero mareo. Una vez se realiza la hiperventilación, se vuelve a medir el estado del paciente, nuevamente 30 segundos por derivación. El ejercicio se realiza dos veces.  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Una vez finalizada la prueba de hiperventilación, se deja descansar al paciente unos cinco minutos para volver a medir su estado basal. Nuevamente 30 segundos por cada derivación. A partir de esto deseamos determinar si hay algún cambio en el estado basal del paciente después de la hiperventilación.  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Ahora es momento del ejercicio intenso. Se le indica al paciente realizar burpees por cinco minutos sin descanso. El ejercicio busca aumentar bruscamente la frecuencia cardíaca y evaluar tanto su respuesta como la del dispositivo de captación ante este aumento. Apenas terminan los cinco minutos de ejercicio, se colocan rápidamente los electrodos para la medición de las tres derivaciones (30 segundos cada una), y se cambia de derivación de la manera más rápida posible, con el fin de no presentar grandes diferencias entre las mediciones.  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Después de que el paciente descansa 5 minutos, este es sometido a un nuevo ejercicio: subir y bajar escaleras por un total de 8 minutos. Después del ejercicio inmediatamente se colocan los electrodos para las respectivas mediciones y se deja al sujeto descansar por otros cinco minutos.  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;La última prueba es la hipoxia. Durante la prueba, el sujeto retiene el aliento por el mayor tiempo posible y apenas exhala se realiza la medición de las tres derivaciones, por 30 segundos cada una. El ejercicio se realiza dos veces.  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Todos las mediciones son analizadas en un programa de Python, bajo la plataforma Google Colab. En esta se realizan comparaciones entre las distintas pruebas y la respuesta del paciente a ellas.

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

# Referencias

