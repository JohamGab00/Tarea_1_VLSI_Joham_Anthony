# Tarea_1_VLSI_Joham_Anthony
## Parte 1. Determinación de las resistencias de canal de transistores mínimos NMOS y PMOS para el proceso XH018. Módulo LPMOS: ne, pe (1,8V).

### Parte 1.A Cáculos para la resistencia efectiva. 
Segun [1] un transistor unitario tiene una resistencia effectiva R, el tamaño del transistor unitario es arbitrario pero convencionalmente el tamaño minimo de ancho y largo de difusión responde a la relación 4/2 lambda. Donde lambda se define como 0.09µm
Para los calculos se establecen diferentes niveles de voltaje por ejemplo VDD=Vs=Vg=1.8V, y Vgs=0V. Tambien se estableció la relación W/L=0.22µm/0.18µm para un transistor mínimo.

Para iniciar con el calculo de la resistencia effectiva se hace referencia a la tecnología XH018, en donde se tiene lo siguiente:

| Parámetro | NMOS | PMOS |
|---|---|---|
| ION (Idsat @ Vgs=Vds=1.8V, (W/L=10/0.18)µ A/\mu m) | 475 | 170 |
| IOFF (@Vgs=0V, Vds=1.8V, (W/L=10/0.18)pA/\mu m) | 3.0 | 3 |
| k₁(µCox)(@W/L=10/10) μΑ/V2 | 256 | 52 |
| S-1 (pendiente subumbral, @Vds=1.8V) decade/V | 12 | 11 |
| n (coeficiente subumbral, @Vds=1.8V) | 1.447 | 1.534 |
| y (coeficiente efecto de cuerpo) (@ (W/L=10/10)) √V | 0.7 | 0.86 |
| Cox (capacitancia del óxido, @ Vbias=1.8V) fF/µm² | 8.46 | 8.91 |
| Heff (movilidad efectiva) | 307 cm²/(Vs) | 59 cm²/(Vs) |
| Cov (capacitancia de traslape) | 0.33 fF/µm | 0.32 fF/µm |
| VT (@VDS=0.1V, (W/L=10/10)) | 0.53 | -0.7 |
| VT (@VDS=0.1V, (W/L=10/0.18)) | 0.58 | -0.65 |
| VT (@VDS=0.1V, (W/L=0.22/0.18)V) | 0.45 | -0.6 |
| VTEX (@VDS=0.1V, (W/L=0.22/0.18)) V | 0.45 | -0.6 |
| Leff (@Ldib=0.18) µm | 0.16 | 0.15 |
| Weff (@Wdib=0.22) µm | 0.17 | 0.25 |
| AL (Delta longitud) µm | 0.02 | 0.03 |
| AW (Delta ancho) um | 0.05 | -0.03 |

- #### Ecuación 4.16
![image](https://github.com/JohamGab00/Tarea_1_VLSI_Joham_Anthony/assets/110200214/9a7f023c-7579-4c5d-b403-5b124517a00d)

- #### Ecuación 1


![image](https://github.com/JohamGab00/Tarea_1_VLSI_Joham_Anthony/assets/110200214/6c57f06a-29bc-4aab-9ae3-d6ad22dd8890)

Se utilizó la Ecuación 4.16 para calcular la Resistencia por µm, utilizando el valor de Idsat obtenido en la Ecuación 1.

![image](https://github.com/JohamGab00/Tarea_1_VLSI_Joham_Anthony/assets/110200214/4c138bbb-b5a9-49fd-b1d4-98b50173bfac)

Una vez obtenida la resistencia por micrómetro se procede a multiplicar W=0.22µm para obtener las resistencias efectivas del NMOS y PMOS obteniendo

| Parámetro | NMOS | PMOS |
|---|---|---|
| Resistencia efectiva| 6405.13022Ω | 12810.26046Ω  |

- #### Ecuaciónes para la simulación

![image](https://github.com/JohamGab00/Tarea_1_VLSI_Joham_Anthony/assets/110200214/d002c78e-d581-4fa0-a147-b9b51f11fab6)

![image](https://github.com/JohamGab00/Tarea_1_VLSI_Joham_Anthony/assets/110200214/0b5fe5ba-4eb9-422c-9b0a-8d404ddd7e22)


Seguidamente, se procede a calcular el valor de la resistencia efectiva con la Ecuación 4.19, el cual da como resultado:

![image](https://github.com/JohamGab00/Tarea_1_VLSI_Joham_Anthony/assets/110200214/49ea0e81-021b-48b3-8d0d-9b6b96949d9f)

### Parte 1.B Cálculos para la capacitancia efectiva y la constante RC.
Para calcular la capacitancia efectiva, es importante conocer la Capacitancia por µm del transistor, para ello se utiliza la Ecuación 2.14 para obtener la Cpermicron, y seguidamente se multiplica por los anchos del transistor para obtener la capacitancia equivalente para PMOS y NMOS.
![image](https://github.com/JohamGab00/Tarea_1_VLSI_Joham_Anthony/assets/110200214/2793611d-4422-4ef3-8c96-860b24d27011)

Los resultados de capacitancia equivalente se muestran a continuación:

![image](https://github.com/JohamGab00/Tarea_1_VLSI_Joham_Anthony/assets/110200214/16885c82-3e9d-46c3-a85d-a5e274a635dc)

Finalmente se multiplican los resultados de la capacitancia equivalente por la resistencia efectiva de ambos transistores, dando como resultado las constantes RC de:

![image](https://github.com/JohamGab00/Tarea_1_VLSI_Joham_Anthony/assets/110200214/5bc9d310-8657-4d3f-8923-983c19a391d4)


## Parte 2. Diseño de un inversor mínimo de tamaño óptimo


### Parte 2.A Características en DC del inversor CMOS estático. 
Se utilizó el siguiente código de hspice para obtener la curva característica de un transistor NMOS de:

El resultado de la curva característica del NMOS fué el siguiente:

![WhatsApp Image 2024-03-13 at 1 49 26 AM](https://github.com/JohamGab00/Tarea_1_VLSI_Joham_Anthony/assets/110150220/a21fa454-7591-46d6-a52f-0dad0c673462)


 - #### Regiones de operación del inversor mínimo. 

 - #### Curva característica del inversor  mínimo. 

- #### Corriente de cortocircuito del inversor mínimo. 

- #### Efecto del ratio Beta del inversor mínimo. 
Se diseñó un inversor con medidas mínimas para obtener la corriente de cortocircuito y su curva de salida, con el fin de determinar la mejor relación PMOS/NMOS para diseñar el inversor, las relaciones de \Beta_p/\Beta_n se muestran en la siguiente figura:


- #### Solución empírica de la relación PMOS/NMOS.

De acuerdo con lo observado en la figura anterior la mejor relacion PMOS/NMOS es la de 4/1, esto debido a que el punto de inflexión de la curva se acerca más a VDD/2=0.9V que las otras relaciones, valores más grandes se alejan de este valor, y valores más pequeños también se alejan.

- #### Simulaciones sobre las esquinas de variabilidad del proceso.  



### Parte 2.B

- #### Deck de SPICE equivalente  de las figuras 8.9-8.10 de [1] sus tiempos de retardo tpdf y tpdr.

- #### Variaciones del  tamaño  del  transistor  PMOS, alrededor  de  la  relación  2/1 y sus  gráficas  tpdf,  tpdr  vs.  la  relación PMOS/NMOS

- #### SPICE deck de la figura 8.11 y  las soluciones de las razones  PMOS/NMOS  para  los  distintos  objetivos  indicados  al  optimizador  (diff=0,  tpd (tpfr+tpdf)/2)=0).

- #### Solución seleccionada (cálculos manuales vs la del  optimizador),  según  criterios de rendimiento, potencia y área. 

- #### ¿Conviene  ampliar  el  rango  de  búsqueda  del  algoritmo  o  situarse  cerca  del punto ya averiguado manualmente en el punto anterior?

### Parte 3.C

- #### Con la razón de tamaños provista del punto b (relación  2/1) se muestran las pruebas implementadas  por  la  ecuación  (8.7)  y  la  figura  8.26  de  la  sección  8.4.5  de  [1].  


- ####  Suponiendo primero  la  capacitancia calculada en 1.b se comparan los valores de Rp y Rn hallados contra lo que  obtuvo en 1.a. ¿Cuál resultado se prefiere?.
