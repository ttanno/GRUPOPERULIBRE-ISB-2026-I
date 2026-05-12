# Filtros digitales utilizados en el procesamiento de bioseñales de EMG, ECG y EEG

---

# I. Introducción

Las señales biomédicas como el electromiograma (EMG), electrocardiograma (ECG) y electroencefalograma (EEG) son registros de actividad eléctrica fisiológica que presentan amplitudes en el rango de microvoltios a milivoltios. Un filtro digital es una herramienta matemática que modifica selectivamente el contenido frecuencial de una señal, permitiendo, por ejemplo, eliminar componentes no deseados mientras preserva la información clínica relevante [1].

Los filtros digitales se clasifican en dos categorías principales según su respuesta al impulso: filtros de respuesta al impulso infinito (IIR, Infinite Impulse Response) y filtros de respuesta al impulso finito (FIR, Finite Impulse Response). Los filtros IIR utilizan retroalimentación y requieren menor orden computacional así como menos uso de memoria, mientras que los FIR son inherentemente estables y pueden diseñarse con fase lineal [2].

La necesidad del uso de filtros en bioseñales se debe a las consecuencias que podría llevar el no emplearlos; por ejemplo:

1. **Errores diagnósticos:**  
    El ruido puede enmascarar características morfológicas esenciales como el complejo QRS en ECG o las ondas alfa en EEG, resultando en interpretaciones clínicas incorrectas [3].

2. **Saturación de amplificadores:**  
   En el caso de filtros analógicos, la interferencia de baja frecuencia (deriva de línea base) puede llevar a los amplificadores fuera de su rango lineal, distorsionando completamente la señal adquirida [4].

3. **Pérdida de información morfológica:**  
   Componentes de alta frecuencia como el segmento ST en ECG o potenciales de acción en EMG pueden ser deteriorados por ruido electromagnético, comprometiendo análisis cuantitativos posteriores [5].

---

# II. Tipos de ruidos en las bioseñales

Las señales biomédicas están contaminadas por diferentes fuentes de ruido que operan en bandas frecuenciales específicas, por ejemplo, el ruido de la red eléctrica.
La correcta identificación del tipo de ruido determina la estrategia de filtrado apropiada, ya que cada filtro está optimizado para eliminar interferencias en rangos frecuenciales específicos sin afectar los componentes fisiológicos de interés [6].
En la siguiente tabla resume los principales tipos de interferencia y sus características:

| Tipo de Ruido | Rango de Frecuencias | Causa Principal | Bioseñal Afectada |
|---|---|---|---|
| Deriva de línea base (Baseline Wander) | Menor a 1 Hz | Respiración, movimiento del paciente, variación de impedancia electrodo-piel | ECG, EMG |
| Interferencia de línea eléctrica (PLI) | 50 Hz / 60 Hz | Acoplamiento capacitivo con red eléctrica, campos electromagnéticos | ECG, EEG, EMG |
| Artefacto de movimiento | 0–20 Hz | Desplazamiento de electrodos, contacto intermitente | ECG, EEG |
| Ruido EMG interferente | 20–500 Hz | Contracción muscular involuntaria durante registro de ECG o EEG | ECG, EEG |
| Ruido térmico (Johnson noise) | Todo el espectro | Agitación térmica de electrones en componentes electrónicos | Todas |

<div align="center">

*Tabla 1. Lista de las interferencias más comunes en bioseñales y sus características.*

</div>

# III. Filtros digitales utilizados en bioseñales

A continuación, se presenta una lista de 5 tipos de filtros digitales comúnmente utilizados en el procesamiento de las bioseñales de EMG, ECG y EEG; explicando su tipo de filtro, aplicación específica, ruido que atenúa, parámetros que lo gobiernan y la ventaja de utilizarlo:

---

## 1. Filtro Butterworth (IIR)

**Tipo:**  
Filtro de respuesta al impulso infinito (IIR).

**Aplicación específica:**  
Filtrado paso-banda para EMG (15-400 Hz) [7] y paso-alto para ECG (0.5-150 Hz). También utilizado como paso-bajo para EEG (0.5-40 Hz).

**Ruido eliminado:**  
- Deriva de línea base (menor a 0.5 Hz) mediante configuración paso-alto.  
- Ruido de alta frecuencia (mayor a 450 Hz) mediante configuración paso-bajo.  
- Artefactos de movimiento en la banda menor a 20 Hz.  

**Parámetros típicos:**  
- Orden: 4to a 8vo orden (compromiso entre selectividad y estabilidad).  
- Frecuencias de corte: ECG (`fc = 0.5 Hz` paso-alto, `150 Hz` paso-bajo); EMG (`fc = 20 Hz` paso-alto, `450 Hz` paso-bajo).  

**Ventaja principal:**  
El filtro Butterworth presenta una respuesta de magnitud "máximamente plana" en la banda de paso, lo que significa que no introduce rizado ni distorsiona las amplitudes de las componentes frecuenciales de interés. Esta característica es crucial para análisis cuantitativos donde la amplitud de las ondas tiene significado clínico [7].

---

## 2. Filtro Notch o de Rechazo de Banda (IIR/FIR)

**Tipo:**  
Puede implementarse como IIR (filtro notch digital) o FIR.

**Aplicación específica:**  
Eliminación exclusiva de la interferencia de línea eléctrica a 50 Hz o 60 Hz en ECG, EEG y EMG sin afectar frecuencias adyacentes [8].

**Ruido eliminado:**  
- Interferencia de línea eléctrica (PLI) a 50/60 Hz.  
- Armónicos de la frecuencia fundamental (100/120 Hz, 150/180 Hz) cuando se utilizan filtros notch en cascada.  

**Parámetros típicos:**  
- Frecuencia central (`f₀`): 50 Hz o 60 Hz según región.  
- Factor de calidad (`Q`): 30-50 (determina el ancho de banda rechazado).  
- Ancho de banda típico: ±1-2 Hz alrededor de la frecuencia central.  

**Ventaja principal:**  
Alta selectividad frecuencial mediante un factor Q elevado, lo que permite eliminar únicamente la componente de 50/60 Hz sin atenuar frecuencias adyacentes que contienen información fisiológica relevante. Por ejemplo, en EEG las ondas theta (4-8 Hz) y alpha (8-13 Hz) no se ven afectadas [8].

---

## 3. Filtro de Savitzky-Golay (FIR)

**Tipo:**  
Filtro FIR basado en ajuste polinomial por mínimos cuadrados.

**Aplicación específica:**  
Suavizado (*smoothing*) de señales EMG para análisis de envolvente y detección de picos R en ECG para cálculo de frecuencia cardíaca [9].

**Ruido eliminado:**  
- Ruido blanco gaussiano de alta frecuencia.  
- Fluctuaciones rápidas que no corresponden a actividad fisiológica.  
- Artefactos puntuales que distorsionan detección de picos.  

**Parámetros típicos:**  
- Longitud de ventana: 5-25 muestras (depende de la frecuencia de muestreo).  
- Orden del polinomio: 2-4 (orden 2 para suavizado general, orden 4 para preservar picos agudos).  
- Aplicación común: ventana de 11 muestras con polinomio de orden 3.  

**Ventaja principal:**  
A diferencia de un filtro de media móvil simple, el Savitzky-Golay preserva mejor los momentos estadísticos de la señal, manteniendo la altura, posición temporal y ancho de los picos. Esto es crítico en ECG para no desplazar la ubicación del pico R y en EMG para mantener la amplitud máxima de las contracciones [9].

---

## 4. Filtro Chebyshev (IIR)

**Tipo:**  
Filtro IIR con rizado controlado en banda de paso (Tipo I) o banda de rechazo (Tipo II).

**Aplicación específica:**  
Separación de bandas de ritmos cerebrales en EEG: delta (0.5-4 Hz), theta (4-8 Hz), alpha (8-13 Hz), beta (13-30 Hz), gamma (30-100 Hz) [10].

**Ruido eliminado:**  
- Componentes frecuenciales fuera de la banda de interés específica.  
- Artefactos de movimiento cuando se diseña como paso-alto con `fc = 0.5 Hz`.  
- Ruido EMG interfiriente cuando se diseña como paso-bajo con `fc = 40 Hz`.  

**Parámetros típicos:**  
- Orden: 4to a 8vo orden.  
- Rizado en banda de paso: 0.5-3 dB (Chebyshev Tipo I).  
- Frecuencias de corte: según banda de interés (ej: 8-13 Hz para ritmo alpha).  

**Ventaja clave:**  
El filtro Chebyshev presenta una transición extremadamente abrupta (*roll-off* pronunciado) entre la banda de paso y la banda de rechazo, lo que permite aislar ritmos cerebrales adyacentes con mínima superposición. Aunque introduce un pequeño rizado en la banda de paso, este compromiso es aceptable cuando la prioridad es la selectividad frecuencial [10].

**Referencia:**  
Swami PD, Patil SH, Gaikwad MS. *Analysis and design of Chebyshev filter for EEG signal processing*. Int J Innov Res Electr Electron Instrum Control Eng. 2015;3(5):146-50.

---

## 5. Filtro de Fase Lineal / Parks-McClellan (FIR)

**Tipo:**  
Filtro FIR diseñado mediante algoritmo de Remez (*equiripple*).

**Aplicación específica:**  
Procesamiento de ECG para análisis morfológico del segmento ST, onda T y detección de isquemia, donde la preservación de la forma temporal es crítica [11].

**Ruido eliminado:**  
- Deriva de línea base mediante configuración paso-alto (`fc = 0.5-1 Hz`).  
- Ruido de alta frecuencia mediante configuración paso-bajo (`fc = 40-100 Hz`).  
- Interferencia de línea eléctrica cuando se diseña como rechazo de banda.  

**Parámetros típicos:**  
- Orden: 50-200 coeficientes (mayor que IIR equivalente).  
- Fase lineal: retardo de grupo constante en toda la banda de paso.  
- Rizado equiripple: distribuido uniformemente en banda de paso y rechazo.  

**Ventaja clave:**  
La fase lineal garantiza que todas las componentes frecuenciales experimenten el mismo retardo temporal, evitando distorsión de la forma de onda. Esto es fundamental en ECG clínico, donde el desplazamiento temporal relativo entre ondas P, QRS y T conduciría a errores diagnósticos en la medición de intervalos PR, QT y análisis del segmento ST [11].

**Referencia:**  
Madeiro JP, Cortez PC, Marques JA, Seisdedos CR, Sobrinho CR. *An innovative approach of QRS segmentation based on first-derivative, Hilbert and Wavelet Transforms*. Med Eng Phys. 2012;34(9):1236-46.

---

# IV. Tabla comparativa de filtros

| Filtro | Tipo | Bioseñal Destino | Ruido Eliminado | Ventaja Principal |
|---|---|---|---|---|
| Butterworth | IIR | EMG, ECG, EEG | Deriva de línea base, ruido HF | Respuesta plana en banda de paso, no distorsiona amplitudes. |
| Notch | IIR/FIR | ECG, EEG, EMG | Interferencia eléctrica (50/60 Hz) | Alta selectividad (Q alto), elimina frecuencia específica. |
| Savitzky-Golay | FIR | EMG, ECG | Ruido blanco, fluctuaciones rápidas | Preserva momentos estadísticos y morfología de picos. |
| Chebyshev | IIR | EEG | Componentes fuera de ritmos cerebrales | Transición abrupta (roll-off), ideal para separar bandas adyacentes. |
| Parks-McClellan | FIR | ECG | Ruido HF, análisis morfológico | Fase lineal (retardo constante), preserva forma temporal de ondas. |

<div align="center">

*Tabla 2. Tabla comparativa de los filtros.*

</div>

---

# V. Conclusiones

La selección del filtro digital apropiado para señales biomédicas depende fundamentalmente de dos criterios técnicos: la prioridad entre preservación de fase versus selectividad frecuencial, y el tipo específico de ruido a eliminar.
Criterio de fase versus magnitud: Cuando el análisis morfológico es crítico, como en la medición de intervalos PR y QT en ECG o la localización temporal de potenciales evocados en EEG, los filtros FIR de fase lineal (Parks-McClellan, Savitzky-Golay) son indispensables porque garantizan que no haya distorsión temporal entre componentes frecuenciales. En contraste, cuando la prioridad es la eficiencia computacional y la forma de onda exacta es menos crítica (análisis espectral de potencia en EEG, cálculo de frecuencia cardíaca promedio), los filtros IIR (Butterworth, Chebyshev) son preferibles por su menor orden y menor carga computacional.
Estrategia de filtrado en cascada: En la práctica clínica, se utilizan múltiples filtros en serie: un filtro paso-alto Butterworth (0.5 Hz) para eliminar deriva de línea base, seguido de un filtro notch (50/60 Hz) para interferencia eléctrica, y finalmente un filtro paso-bajo Butterworth (40-150 Hz según la aplicación) para ruido de alta frecuencia. Esta arquitectura en cascada permite optimizar independientemente cada etapa de filtrado.
Consideraciones finales: El diseño del filtro debe considerar la frecuencia de muestreo de la señal (cumplir criterio de Nyquist), el orden del filtro (balance entre selectividad y estabilidad numérica), y las características espectrales de la señal fisiológica de interés. Un filtrado excesivo puede eliminar componentes clínicamente relevantes, mientras que un filtrado insuficiente compromete la relación señal-ruido y la interpretación diagnóstica.

---

# VI. Bibliografía

1. Rangayyan RM. *Biomedical signal analysis*. 2nd ed. Wiley-IEEE Press; 2015.

2. Proakis JG, Manolakis DG. *Digital signal processing: principles, algorithms, and applications*. 4th ed. Pearson; 2006.

3. Sörnmo L, Laguna P. *Bioelectrical signal processing in cardiac and neurological applications*. Elsevier Academic Press; 2005.

4. Webster JG. *Medical instrumentation: application and design*. 4th ed. John Wiley & Sons; 2009.

5. De Luca CJ, Kuznetsov S, Gilmore LD, Roy SH. Inter-electrode spacing of surface EMG sensors. *J Biomech*. 2012;45(3):555-61.

6. Metting van Rijn AC, Peper A, Grimbergen CA. High-quality recording of bioelectric events. *Med Biol Eng Comput*. 1990;28(5):389-97.

7. Donisi L, Jacob D, Guerrini L, et al. sEMG Spectral Analysis and Machine Learning Algorithms. *Bioengineering*. 2023;10(9):1103.

8. Boda S, Mahadevappa M, Dutta PK. Removal of power line interference and baseline wander in ECG signals. *Biomed Signal Process Control*. 2021;67:102466.

9. Vondrak J, Penhaker M, Kubicek J. Detection of myocardial infarction using vectorcardiographic loops. *Measurement*. 2024;226:114094.

10. Turjya SM. Adaptive Interaction in the Metaverse Using a Hybrid EEG-Based Brain–Computer Interface. *Preprints*. 2026.

11. Ozaydin S, Ahmad I. Comparative performance analysis of filtering methods for ECG baseline wander removal. *Fluct Noise Lett*. 2024;23(4):2450046.