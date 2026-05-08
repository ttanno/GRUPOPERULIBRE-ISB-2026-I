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
### Derivada I
#### Registro electrocardiográfico en reposo
| Parámetro           | Valor       |
|---------------------|-------------|
| Duración total      | 32.8 s      |
| Muestras            | 32,850      |
| Picos R detectados  | 51          |
| RR medio            | 647.5 ms    |
| FC estimada         | 92.7 bpm    |
#### Graficas
![Estado Basal Derivada I](<VIDEOS Y FOTOS/D1SIGNAL.png>)
![EKG derivada I](<VIDEOS Y FOTOS/EKG1.png>)
![Transformada de Fourier Derivada I](<VIDEOS Y FOTOS/FFT1.png>)

### Derivada II
#### Registro electrocardiográfico en reposo
## Estado Basal 1 — Derivación II
| Parámetro          | Valor    |
|--------------------|----------|
| Duración total     | 35.4 s   |
| Muestras           | 35,400   |
| Picos R detectados | 52       |
| RR medio           | 690.0 ms |
| FC estimada        | 87.0 bpm |

#### Graficas
![Estado Basal Derivada I](<VIDEOS Y FOTOS/D2SIGNAL.png>)
![EKG derivada I](<VIDEOS Y FOTOS/EKG2.png>)
![Transformada de Fourier Derivada I](<VIDEOS Y FOTOS/FFT2.png>)

### Derivada III
#### Registro electrocardiográfico en reposo
| Parámetro          | Valor    |
|--------------------|----------|
| Duración total     | 30.7 s   |
| Muestras           | 30,750   |
| Picos R detectados | 49       |
| RR medio           | 635.5 ms |
| FC estimada        | 94.4 bpm |
#### Graficas
![Estado Basal Derivada I](<VIDEOS Y FOTOS/D3SIGNAL.png>)
![EKG derivada I](<VIDEOS Y FOTOS/EKG3.png>)
![Transformada de Fourier Derivada I](<VIDEOS Y FOTOS/FFT3.png>)
### Frecuencia cardiaca en cada caso
![Frecuencia cardiaca en cada caso por derivada](<VIDEOS Y FOTOS/FrecuenciaCardiaca.png>)

# Discusión

# Referencias

