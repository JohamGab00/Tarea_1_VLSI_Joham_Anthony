

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
Se simula el comportamiento en hspice para obtener la curva característica de un transistor NMOS mínimo, (la simulación de este punto se obtiene del script de SPICE llamado XXXX en la carpeta de scripts de este repositorio). 

![WhatsApp Image 2024-03-13 at 1 49 26 AM](https://github.com/JohamGab00/Tarea_1_VLSI_Joham_Anthony/assets/110150220/a21fa454-7591-46d6-a52f-0dad0c673462)


 - #### Regiones de operación del inversor mínimo. 
Como se observa en la siguiente figura tomada de [1], representa la curva característica del inversor y sus regiones de operación.


![image](https://github.com/JohamGab00/Tarea_1_VLSI_Joham_Anthony/assets/110200214/228030f0-0fb7-4c8f-95c6-be6bc4a4f42a)


Vemos que en la tabla 2.3 tomada de [1] se caracterizan cada una de las regiones correspondientes. 


![image](https://github.com/JohamGab00/Tarea_1_VLSI_Joham_Anthony/assets/110200214/799cf881-674a-4b7e-bdc9-df0072585d0c)

Basado en lo anterior, se calcula una tabla con los valores de las regiones de operación teóricos para nuestro inversor y posteriormete con la simulación obtenemos los valores experimentales, de esta manera, para el inversor mínimo se sabe en qué regiones está operando. 

![image](https://github.com/JohamGab00/Tarea_1_VLSI_Joham_Anthony/assets/110200214/4f09d39f-748c-44f4-ad5e-2f25ca99984d)
En la siguiente imagen se evidencia dicha simulación y sus regiones de operación, (la simulación de este punto se obtiene del script de SPICE llamado [Inversor_Curva_Caracteristica] en la carpeta de scripts de este repositorio). 

![image](https://github.com/JohamGab00/Tarea_1_VLSI_Joham_Anthony/assets/110200214/99d7054b-4bc4-4b54-a372-2e63c7320c6d)

 - #### Curva característica del inversor  mínimo. 
 En la siguiente imagen tomada de [1], se observa la curva característica teórica del inversor MOS de tamaño mínimo, esta se puede comparar con la curva obtenida en las simulaciones, (la simulación de este punto se obtiene del script de SPICE llamado [Inversor_Curva_Caracteristica] en la carpeta de scripts de este repositorio). 
 
![image](https://github.com/JohamGab00/Tarea_1_VLSI_Joham_Anthony/assets/110200214/9d505872-1958-48f5-88c5-5e3726aa005b)

![image](https://github.com/JohamGab00/Tarea_1_VLSI_Joham_Anthony/assets/110200214/86b51053-8683-4ab7-aaa0-cea2fb0494d6)

- #### Corriente de cortocircuito del inversor mínimo. 

 En la siguiente imagen tomada de [1], se observa la gráfica teórica de la corriente de cortocircuito del inversor MOS de tamaño mínimo, esta se puede comparar con la gráfica obtenida en las simulaciones, (la simulación de este punto se obtiene del script de SPICE llamado [Modelo_Inversor_Corriente_Corto] en la carpeta de scripts de este repositorio). 

![image](https://github.com/JohamGab00/Tarea_1_VLSI_Joham_Anthony/assets/110200214/75f330c6-aeb7-4753-a8d8-6d9dd293e87e)

![image](https://github.com/JohamGab00/Tarea_1_VLSI_Joham_Anthony/assets/110200214/2fea04d3-149e-4d3f-8423-44cab8da2c87)
- #### Efecto del ratio Beta del inversor mínimo. 

 En la siguiente imagen tomada de [1], se observa la gráfica teórica del ratio beta para diferentes relaciones de beta de un inversor MOS de tamaño mínimo, esta se puede comparar con la gráfica obtenida en las simulaciones, dichos valores se graficaron en Excel para analizar los valores obtenidos, (la simulación de este punto se obtiene del script de SPICE llamado [Inversor] en la carpeta de scripts de este repositorio). 

![image](https://github.com/JohamGab00/Tarea_1_VLSI_Joham_Anthony/assets/110200214/b53d6685-36a5-40a1-8087-58f6d5c24284)

Se diseñó un inversor con medidas mínimas para obtener la corriente de cortocircuito y su curva de salida, con el fin de determinar la mejor relación PMOS/NMOS para diseñar el inversor, las relaciones de \Beta_p/\Beta_n se muestran en la siguiente figura:

![WhatsApp Image 2024-03-17 at 4 04 19 PM](https://github.com/JohamGab00/Tarea_1_VLSI_Joham_Anthony/assets/110200214/229d361e-6fc3-42f6-a20e-d59082097e24)

De acuerdo con lo observado en la figura anterior la mejor relacion PMOS/NMOS es la de 4/1, esto debido a que el punto de inflexión de la curva se acerca más a VDD/2 = 0.9V que las otras relaciones, valores más grandes se alejan de este valor, y valores más pequeños también se alejan.

- #### Simulaciones sobre las esquinas de variabilidad del proceso.  

 Usando una relación 2/1 como nos indica,  Para el transistor NMOS se usó W=220nm y para PMOS W=440nm, ambos con L=180nm, es sobre estos valores que corremos la variabilidad del proceso, donde en las siguientes imágenes vemos una tabla con los valores de pontencia, tpdr, tpdf y temperatura constante obtenidos y una gráfica que los representa. (la simulación de este punto se obtiene del script de SPICE llamado [Inversor_Esquinas] en la carpeta de scripts de este repositorio). 
 
![465682a8-08b9-4b7c-a228-ae9b022abb4f](https://github.com/JohamGab00/Tarea_1_VLSI_Joham_Anthony/assets/110200214/10e26ede-8da8-4528-9cb8-7fa65633f7ab)


![WhatsApp Image 2024-03-17 at 7 08 46 PM](https://github.com/JohamGab00/Tarea_1_VLSI_Joham_Anthony/assets/110200214/897c594d-0863-4455-b0b9-6c653be6c363)





### Parte 2.B

- #### Deck de SPICE equivalente  de las figuras 8.9-8.10 de [1] sus tiempos de retardo tpdf y tpdr además de sus variaciones del  tamaño  del  transistor  PMOS, alrededor  de  la  relación  2/1 y sus  gráficas  tpdf,  tpdr  vs.  la  relación PMOS/NMOS, tomando como referencia las definiciones de la siguiente imagen: 

![image](https://github.com/JohamGab00/Tarea_1_VLSI_Joham_Anthony/assets/110200214/536e7e8c-9a96-40c5-9216-44ce9e1116b8)

En el script llamado [inversor_3] se establecio el parametro A, el cual multiplica el ancho del transistor PMOS para asi variar la relacion PMOS/NMOS, se miden los retardos tpdr, tpdf y tpd, se muestran los siguientes resultados en pico segundos:

![image](https://github.com/JohamGab00/Tarea_1_VLSI_Joham_Anthony/assets/110200214/63c18cfb-2f23-4c98-a491-824078d5672a)


![image](https://github.com/JohamGab00/Tarea_1_VLSI_Joham_Anthony/assets/110200214/9de1eaf7-7955-4d4e-8521-d3f55532f8a2)

De lo anterior se observa que la relación con el menor tiempo de retardo y menor diferencia de tpdf y tpdr se logra cuando la relación PMOS/NMOS es de 2.5/1.

- #### Cálculo de la optimización automatizada

Para dicho cálculo se realiza una optimizacion automatizada utilizando Hspice, dicho script utilizado es el que se llama [Inversor_4] y tomando los resultados obtenidos y comparando con los resultados obtenidos manualmete se tiene: 

![image](https://github.com/JohamGab00/Tarea_1_VLSI_Joham_Anthony/assets/110200214/45c07974-959b-45ff-b59d-aacca147cb59)


  
Para determinar cuál de las dos alternativas es más favorable, es esencial considerar exhaustivamente los requisitos de diseño. La optimización manual exhibe un área reducida en comparación con la optimización automática, lo cual se atribuye al hecho de que el ancho del transistor PMOS es 2.5 veces mayor que el del transistor NMOS, en contraste con la relación de 4 veces en el otro escenario. Esta optimización también presenta un menor tiempo de propagación de la señal (tpd), lo que implica que, en promedio, el retardo de propagación es menor para esta configuración. Por último, la relación 2.5/1 también conlleva un consumo de potencia promedio inferior en comparación con la relación obtenida mediante Hspice.

La relación derivada automáticamente presenta una diferencia menor entre los tiempos de propagación de subida (tpdr) y de bajada (tpdf), lo que se traduce en una simetría casi igualitaria en el retardo cuando la compuerta cambia de 0 a 1 o de 1 a 0. Desafortunadamente, la relación 4/1 conlleva un mayor consumo de potencia, una mayor área y un ligero aumento en el retardo de propagación promedio.

En resumen, la elección entre las soluciones dependerá de las prioridades del diseño. Si se busca una compuerta con la menor área, el menor retardo de propagación y el menor consumo de potencia, la relación 2.5/1 obtenida manualmente es la mejor opción. Por otro lado, si se prioriza la igualdad entre los tiempos de propagación de subida y bajada, la relación 4/1 obtenida automáticamente con Hspice es más adecuada.




### Parte 3.C

- #### Con la razón de tamaños provista del punto b (relación  2/1) se muestran las pruebas implementadas  por  la  ecuación  (8.7)  y  la  figura  8.26  de  la  sección  8.4.5  de  [1].  


- ####  Suponiendo primero  la  capacitancia calculada en 1.b se comparan los valores de Rp y Rn hallados contra lo que  obtuvo en 1.a. ¿Cuál resultado se prefiere?.
