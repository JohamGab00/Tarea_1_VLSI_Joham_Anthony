# Tarea_1_VLSI_Joham_Anthony
## Parte 1. Determinación de las resistencias de canal de transistores mínimos NMOS y PMOS para el proceso XH018. Módulo LPMOS: ne, pe (1,8V).

### Parte 1.A Cáculos para la resistencia efectiva. 

#### Ecuación 4.16
![image](https://github.com/JohamGab00/Tarea_1_VLSI_Joham_Anthony/assets/110200214/9a7f023c-7579-4c5d-b403-5b124517a00d)

#### Ecuación 1

![image](https://github.com/JohamGab00/Tarea_1_VLSI_Joham_Anthony/assets/110200214/6c57f06a-29bc-4aab-9ae3-d6ad22dd8890)


![image](https://github.com/JohamGab00/Tarea_1_VLSI_Joham_Anthony/assets/110200214/4c138bbb-b5a9-49fd-b1d4-98b50173bfac)

#### Ecuaciónes para la simulación

![image](https://github.com/JohamGab00/Tarea_1_VLSI_Joham_Anthony/assets/110200214/d002c78e-d581-4fa0-a147-b9b51f11fab6)

![image](https://github.com/JohamGab00/Tarea_1_VLSI_Joham_Anthony/assets/110200214/0b5fe5ba-4eb9-422c-9b0a-8d404ddd7e22)




![image](https://github.com/JohamGab00/Tarea_1_VLSI_Joham_Anthony/assets/110200214/49ea0e81-021b-48b3-8d0d-9b6b96949d9f)

### Parte 1.B Cálculos para la capacitancia efectiva y la constante RC.
![image](https://github.com/JohamGab00/Tarea_1_VLSI_Joham_Anthony/assets/110200214/2793611d-4422-4ef3-8c96-860b24d27011)


![image](https://github.com/JohamGab00/Tarea_1_VLSI_Joham_Anthony/assets/110200214/16885c82-3e9d-46c3-a85d-a5e274a635dc)

![image](https://github.com/JohamGab00/Tarea_1_VLSI_Joham_Anthony/assets/110200214/5bc9d310-8657-4d3f-8923-983c19a391d4)


## Parte 2. Diseño de un inversor mínimo de tamaño óptimo


### Parte 2.A Características en DC del inversor CMOS estático. 

 - #### Regiones de operación del inversor mínimo. 

 - #### Curva característica del inversor  mínimo. 

- #### Corriente de cortocircuito del inversor mínimo. 

- #### Efecto del ratio Beta del inversor mínimo. 

- #### Solución empírica de la relación PMOS/NMOS.

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
