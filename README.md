# Modelamiento-de-la-polarizacion-de-una-celda-electrol-tica-de-cobre
Este proyecto busca la modelación del voltaje o potencial total de una celda electrolítica en respuesta a diferentes densidades de corriente y condiciones de concentración o temperatura de proceso, aplicado para etapa tradicional de electro obtención o celda de síntesis nanomateriales de cobre.

1. Contexto, interrogantes y metodología general 
Chile es el mayor productor cobre en el mundo con una participación cercana al 24%, produce más de 5.5 Mt/año cobre fino y esto implica un gran aporte al PIB nacional superior al 12%. Aquello es posible a partir de la comercialización de dos productos principales, concentrados y cátodos de cobre, este último aun cuando es el más valioso o especializado solo representa un 26% de la producción nacional.  
Este producto se genera en reactores o celdas electrolíticas, las cuales a diferencia de una celda combustible que genera electricidad, estas utilizan energía eléctrica para promover reacciones catódicas o reductivas para generar los productos de cobre. 
A nivel general, se componen por un electrolito (solución contiene Cu), sin interferencia de membrana, dos electrodos planos; un ánodo inerte en el cual ocurre reacción hidrólisis de agua y generación de oxígeno. Y, por otro lado, un cátodo el cual “aporta” los electrones para la reducción de ion cúprico a cobre metálico. 

<img width="497" height="391" alt="image" src="https://github.com/user-attachments/assets/e4c15048-2ce0-4156-91dd-5eacdb1a75ef" />   <img width="503" height="281" alt="image" src="https://github.com/user-attachments/assets/dcd65fb2-56df-470e-b5d7-738951fab524" /> 
Ejemplo experimental en celda electrolítica. 2.03 A (90 A/m2), potencial celda 4.7 V

Los principales factores que impulsan el consumo o demanda de metales estratégicos como el cobre en los últimos años, involucran el desarrollo social y transición energética, particularmente mediante la manufactura de dispositivos de “energías verdes” o renovables (IEA 2024), se estima que a partir del auge de la energía solar fotovoltaica la demanda de cobre podría aumentar hasta los 6.4 millones de toneladas para el año 2040 (ICA 2022). Bajo este escenario es relevante la optimización de los recursos y recuperación de metales críticos desde fuentes tradicionales o residuos. La industria tradicional para ello aplica principalmente procesos de alto impacto ambiental como los pirometalúrgicos, los cuales pueden incluir incineración, combustión fundición y/o pirólisis (Yken V., et al., 2021). Sin embargo, una alternativa de procesamiento surge con el área hidrometalúrgica aplicando soluciones lixiviantes selectivas y con menor impacto ambiental (Kaya, M., 2016). Estos procesos de disolución de metales, pueden ser complementados con un enfoque estratégico y evaluar la producción de nanomateriales (Vakylabad et al. 2016). Los nano objetos son aquellos que tienen al menos una de sus dimensiones en el rango de la nanoescala, mientras que los materiales nanoestructurados presentan una estructura interna o superficial en la nanoescala (ISO80004/TC, 2023). En el contexto de la síntesis de nanopartículas (NPs), un precursor (como un electrolito) es el compuesto que proporciona los elementos necesarios para formar las NPs, para ello, es posible aplicar diferentes técnicas de síntesis como la electroquímica basados en los principios de una electroobtención tradicional utilizada para la producción industrial de cátodos de cobre. 

Cuando un sistema electroquímico tradicional como la electroobtención de cobre se opera con un electrolito de soporte en exceso (minimizando los gradientes de concentración), la solución posee alta conductividad iónica, permite mayores densidades de corriente antes de lograr el corriente límite y el campo eléctrico en el seno del electrolito es prácticamente nulo, suprimiendo la migración de las especies electroactivas. En estas condiciones, la respuesta del electrodo está controlada principalmente por efector cinéticos (se minimizan los efectos por transferencia de masa), y a sobrepotenciales moderadamente grandes (≥ 50–100 mV) puede aplicarse la aproximación de Tafel, donde la corriente depende exponencialmente del sobrepotencial y una de las semirreacciones domina la transferencia de carga. En contraste, en un sistema para la síntesis de un nanomaterial, el régimen electroquímico podría cambiar a un control más mixto. El electrolito precursor tiene baja concentración (Ej. 5–10 g L⁻¹), la conductividad disminuye, se incrementa la caída óhmica (iR) y la migración iónica adquiere relevancia. Sumado a esto, la menor concentración de la especie electroactiva reduce la corriente límite difusional, generando que el sistema ingrese prematuramente en un régimen controlado por transporte de masa. Así, bajo condiciones diluidas, el comportamiento electroquímico deja de ser puramente cinético y la ecuación de Tafel perdería validez como única componente de evaluación, ya que el potencial medido reflejaría contribuciones combinadas de activación, resistencia óhmica y difusión.

A partir de lo anterior surgen interrogantes como, ¿las consideraciones y los regímenes de control para un proceso de electroobtención tradicional, son directamente extrapolables o aplicables a un contexto de síntesis electroquímica de nano cobre? en este último escenario, ¿existirá un régimen electroquímico predominante cinético, óhmico, difusional o estará en un escenario más bien mixto? 
Así, el objetivo general del presente proyecto considera el desarrollo de un modelo que permita evaluar la evolución del voltaje requerido por una celda electrolítica para nanomaterial de cobre en función de los valores de densidad de corriente, temperatura y composición, reflejados en curvas de polarización. 

La modelación de un proceso de polarización en una celda electrolítica en contexto de síntesis o fabricación de un nanomaterial de cobre buscaría la evaluación y análisis de la respuesta del voltaje total de celda (distribución de curva de polarización) a diferentes temperaturas de proceso y concentración de la especie electroactiva en el precursor, bajo determinadas densidades de corriente (Am-2). Estos procesos de producción requieren condiciones específicas y estables de polarización (corriente y potencial), minimizando las pérdidas óhmicas o asegurando una transición controlada del potencial catódico, con el propósito de favorecer la nucleación y una síntesis electroquímica más estable de nanomateriales. Dichas condiciones permitirían obtener productos con características morfológicas, topográficas y composicionales uniformes y reproducibles. Estos aspectos representan uno de los principales desafíos en la síntesis de nanomateriales, dado que los procesos suelen presentar baja estabilidad, alta variabilidad y amplios rangos en propiedades como el diámetro de partícula, la forma y la composición.

La metodología para abordar el proyecto considera la revisión de artículos científicos como base referencial para establecer las ecuaciones que modelan los fenómenos de sobrepotenciales. Así también, se utilizarían las condiciones de procesos experimentales propuestas por los investigadores del artículo para iterar y validar el modelo realizado durante el presente proyecto. Para ello, se utilizará un lenguaje de programación tipo Python y plataforma COLAB, la cual a través del soporte en nube de Google permite un acceso abierto, evaluación de código programación y obtención de gráficas pertinentes. 

El desarrollo de la temática propuesta apunta (en parte) a un aporte en las ventajas competitivas de Chile frente a otros países mineros, debido a que se buscaría el complemento de una cadena de valor principalmente extractivista, a partir de la producción de materiales de alta especialización (nanomateriales) y mayor potencial económico frente a los productos mineros tradicionales como el concentrado y cátodos de cobre.

2. Fundamentos y estructuración física del modelo.
   
En la presente sección se entregan los fundamentos y ecuaciones teóricas aplicadas al modelo de simulación. Así también, son declarados los alcances en cada caso requerido.
El potencial total de la celda (E celda) se puede expresar como:

<img width="234" height="37" alt="image" src="https://github.com/user-attachments/assets/5837a348-5391-4417-a4db-8395bb7c55c6" />

Tenemos:
•	𝐸rx: potencial reversible o termodinámico (depende de T°, composición o concentración y presión)
•	𝜂act: sobrepotencial de activación (control cinético)
•	𝜂ohm: caída óhmica (resistencia del electrolito + resistencia de los electrodos)
•	𝜂conc: sobrepotencial por concentración o difusión (transporte de masa)

El modelo buscará interpretar o representar la evolución del E celda respecto de la densidad de corriente (i), bajo diferentes condiciones de proceso.
Reacciones electroquímicas 

Reducción catódica del Cu²⁺:

<img width="160" height="66" alt="image" src="https://github.com/user-attachments/assets/0ed0ca9a-3fb4-4ed4-ab5a-368250056de0" />

Reacción en ánodo inerte (grafito):

<img width="187" height="64" alt="image" src="https://github.com/user-attachments/assets/9408f04c-0651-4fe6-9bbf-8c6faf3b4280" />

•	Alcance declarado: para este escenario de evaluación, no se considerarán reacciones secundarias o no deseadas a partir de otros elementos como el Fe.


Ecuación general del voltaje de la celda

En función de densidad de corriente

<img width="331" height="34" alt="image" src="https://github.com/user-attachments/assets/c5ab237f-280b-49a2-844d-7bfacded03e8" />

Consideración potencial reversible (ajuste temperatura y concentración Nernst)

•	El procedimiento para el cálculo del potencial reversible considerará dos etapas. En la primera de ellas se aplicará una corrección por efecto termodinámico de la temperatura de proceso y la variación de entropía a través de la siguiente ecuación: 

<img width="475" height="86" alt="image" src="https://github.com/user-attachments/assets/b7c02559-9584-4fea-821d-7317b02d050c" />

Luego de ello, se aplicará el E^0 (T) en la ecuación de Nerst con objeto de realizar la corrección del efecto electroquímico de las concentraciones de las especies en reacción. 

<img width="232" height="53" alt="image" src="https://github.com/user-attachments/assets/8ab6445f-275a-45ff-aaf2-cbb541c68c31" />

•	Es posible generalizar coeficientes de actividad por concentración de los elementos, debido a baja concentración en electrolito o baja fuerza iónica. 

Sobrepotencial de activación (cinético)
Butler–Volmer

<img width="283" height="40" alt="image" src="https://github.com/user-attachments/assets/1e24f4b4-c7b9-470b-af1f-9eb31ecfe39d" />

Con régimen es catódico dominante, se aplicaría la simplificación de Tafel. Sin embargo, para efectos de este desarrollo se trabaja con B-V completo.

<img width="150" height="41" alt="image" src="https://github.com/user-attachments/assets/96582ada-5df5-4d6a-94dc-7b9da5178b17" />

Tenemos:
	i_0: densidad de corriente de intercambio  
	α_c: coeficiente de transferencia catódico (~0.5). Se ajustará respecto de la indicación del artículo de investigación (si corresponde).

Caída óhmica (resistencia del electrolito)

<img width="177" height="49" alt="image" src="https://github.com/user-attachments/assets/baaa36d2-0f03-43b4-a18f-4722e2e2d455" />

Tenemos:

•	𝐿: distancia entre electrodos
•	𝜅: conductividad del electrolito (dependiente de T° y concentración)
Esta conductividad del electrolito será generada o calculada a partir de ecuación y considerando datos de T° como input.  
•	Ecuación de Nernst-Einstein para cálculo de 𝜅: a partir de cada especie i en el electrolito
o	Alcance declarado: se estimarán como soluciones diluidas (< 0.1 M) o baja fuerza iónica (proyectado más a la aplicación de celda electrolítica para nanomaterial). 

<img width="136" height="43" alt="image" src="https://github.com/user-attachments/assets/43ee46bc-7735-4cde-89ce-ae60ab477fdf" />

Caída óhmica (resistencia de electrodos)

•	Alcance declarado: no se consideran resistencias de contactos/conexiones, películas generadas en la superficie del electrodo plano (no poroso). Por tanto, la resistencia óhmica para este caso se conformará por el electrolito y electrodo (electrónica). 
Se consideran electrodos de bajo espesor (5-10 mm), sin “busbar” o barra de distribución grande, lo cual pudiese afectar la trayectoria por la cual la corriente fluye.  Así, la trayectoria es directa en el espesor del electrodo. 
Se considera la resistividad estándar y coeficiente de temperatura del metal (298.15 K) como datos tabulados o conocidos, pero, se modifica según la temperatura de proceso. 

<img width="347" height="214" alt="image" src="https://github.com/user-attachments/assets/e07f9fa2-cdb2-4110-bc8f-ff202784e70a" />

α_"cat/án" : coeficiente de temperatura de la resistividad
ρ_0: resistividad a una temperatura de referencia T_0
A_"surf" : Área transversal al flujo de corriente (área efectiva conductora) (m2) # se considerarán solo dos electrodos con una cara activa; es decir, no hay electrodo compartido por la cara posterior. En situación de múltiple electrodo o bipolar, el área efectiva se duplica. Esto último, podría disminuir la resistencia efectiva del electrodo a la mitad.
t: Espesor del electrodo (m)

Sobrepotencial por concentración (control difusional)
Nernst modificada o una relación difusional:

<img width="173" height="60" alt="image" src="https://github.com/user-attachments/assets/7487ee2a-e17e-45e0-ba18-935a586fe66c" />

i_L: corriente límite difusional, que depende de D, C^*y la capa difusional δ:

<img width="99" height="44" alt="image" src="https://github.com/user-attachments/assets/5ded9568-b34b-4f41-bd84-2d01ea3ebff2" />

Alcance declarado: para este apartado no se considerará la obtención de la i_L a partir de la movilidad de iones y los n° de transporte.
En este apartado se calculará la i_L como función de la difusividad D y variables de proceso 
Para calcular la difusividad de la especie i (Di), se utilizará la relación entre movilidad de la especie y la conductancia de esta. Así:

<img width="109" height="59" alt="image" src="https://github.com/user-attachments/assets/1c231c06-20ee-42c5-b78d-6737d9254a34" />

Alcance declarado: la λ_i se considerará como variable conocida o tabulada para la especie i (cobre)

  Parámetros involucrados en modelo: 

<img width="730" height="430" alt="image" src="https://github.com/user-attachments/assets/ae5c0464-d671-4299-9c2e-98d2727cdb54" />
# Adicionalmente se consideran constante de Faraday, constante gases ideales

Secuencia general de funcionamiento del modelo
	Se consideran parámetros fijos de entrada
	El programa solicita “inputs” para el modelo, tales como si desea evaluar diferentes T° o concentraciones. 
	En relación con la respuesta del punto anterior (2), se solicita rango de T° a evaluar o concentraciones (según corresponda) y con ello, el “salto” o paso para siguiente concentración, lo cual determinará el número de evaluación para esta variable. 
	Luego, programa solicita los rangos de densidad de corriente a evaluar (como condición de borde, máximo y mínimo), y con ello, el “salto” o paso entre la condición i1 – i2. Por ejemplo 0.1–800 A/m²); paso 25 A/ m². Con ello, indirectamente se “acota” el rango de potencial. 
	Para cada i (densidad de corriente)
	η_"act"  (i)
	η_"ohm"  (i)
	η_"conc"  (i)
	E_"celda"  (i)
	A partir de los coeficientes de difusividad, conductividad, según corresponda.
	Calcular E_"rx"  y E_"celda" . Almacenar en matriz.
	Graficar E_"celda" vs i.
	Comparar con la curva experimental del artículo. 
Alcance declarado: aun cuando puede ser una variable influyente, en el presente modelo no se consideran efectos convectivos naturales (por burbujeo) o forzada (flujo-bombeo). 


3. Validación de modelo y evaluación de nuevos parámetros
El artículo Beukes & Badenhorst, 2009, desarrolla un modelo teórico y práctico para analizar y optimizar el diseño de celdas de electroobtención de cobre (EW) en solución sulfato, combinando fundamentos electroquímicos con correlaciones empíricas de transporte de masa e hidrodinámica. El trabajo busca vincular el comportamiento de polarización de los electrodos con las condiciones de operación (flujo, concentración, temperatura, geometría), buscando estimar el voltaje de celda, la eficiencia energética y la limitación difusional en distintos escenarios de planta.
Aunque el estudio se centra en electroobtención convencional (altas concentraciones) se espera que su enfoque sea directamente adaptable a un sistema de síntesis de nanomateriales de cobre (soluciones diluidas). Para este proyecto en particular se espera: 
•	Tomar como referencia las ecuaciones que los autores identifican para modelar el sistema. complementándolo con alcances o consideraciones específicas (evaluación de cambio en regímenes dominantes).
o	En contexto de nanomaterial, la difusión y caída óhmica serían más considerables, por tanto, respecto del artículo de referencia se busca validar (en una primera etapa) el modelo con mayor sensibilidad.
	Para ello, se realizará una comparación directa de las curvas de polarización simuladas (a partir de D y κ calculadas) con las curvas de los autores (referencia de comportamiento ideal a alta concentración)

Los autores presentan un comportamiento modelado del sobrepotencial respecto de cada densidad de corriente, no así, el potencial o voltaje total de la celda electrolítica para el cual debiese ser sumado el potencial de reacción considerando la reducción en cátodo de Cu+2 e hidrólisis de agua en ánodo, cuyo potencial suele estar entre 0.76-0.89 V, condiciones estándar. Así también, los autores se entregan parámetros de conductividad, difusividad y otros, a partir de ensayos experimentales en celda o referencias bibliográficas, así también, la difusión de la especie estaría “afectada” por eventos de convección. A diferencia del actual proceso/modelo, el cual realiza estas estimaciones a partir de inputs de concentración y temperatura de proceso. 
  



Referencias

    Beukes, N. T., & Badenhorst, J. (2009). Copper electrowinning: theoretical and practical design. En Hydrometallurgy Conference 2009. The Southern African Institute of Mining and Metallurgy.
    International Copper Association. (2022, mayo). Copper power cable underpins the energy transition: Power cable fact sheet. SAI Industrial LLC. Recuperado de https://internationalcopper.org/wp-content/uploads/2022/05/Power-Cable-Fact-Sheet-.pdf
    International Energy Agency (IEA). (2024). Global copper demand in the Net Zero Scenario, 2023–2040 [Gráfico]. Recuperado de https://www.iea.org/data-and-statistics/charts/global-copper-demand-in-the-net-zero-scenario-2023-2040-5856. Licencia: CC BY 4.0.
    ISO/TC 229, & IEC/TC 113. (2023). ISO 80004-1:2023 Nanotechnologies — Vocabulary — Part 1: Core terms (First edition, 2023-07). Organización Internacional de Normalización
    Kaya, M. Recovery of metals and nonmetals from electronic waste by physical and chemical recycling processes. Waste Manag. 2016, 57, 64–90
    Vakylabad, A. B., Schaffie, M., Naseri, A., Ranjbar, M., & Manafi, Z. (2016). A procedure for processing of pregnant leach solution (PLS) produced from a chalcopyrite-ore bio-heap: CuO nano-powder fabrication. Hydrometallurgy, 162, 25–32. https://doi.org/10.1016/j.hydromet.2016.03.013
    Van Yken, J.; Boxall, N.J.; Cheng, K.Y.; Nikoloski, A.N.; Moheimani, N.R.; Kaksonen, A.H. E-Waste Recycling and Resource Recovery: A Review on Technologies, Barriers and Enablers with a Focus on Oceania. Metals 2021, 11, 1313


EVALUACIÓN DE CASOS:

Respuesta de voltaje total de celda (considerando sobrepotenciales) en función de las densidades de corriente y evaluación de concentración de electrolito.
Para Figura y escenario 1

•	Condiciones aplicadas para modelación.
•	Concentración mínima [mol/m³]: 538
•	Concentración máxima [mol/m³]: 692
•	Paso de concentración [mol/m³]: 15
•	Temperatura fija [K]: 338.15
•	Densidad de corriente mínima [A/m²]: 0.1
•	Densidad de corriente máxima [A/m²]: 50
•	Paso de corriente [A/m²]: 0.0001

Se observa caída de potencial como respuesta en el aumento del voltaje que debe compensar la celda electrolítica para operar a cada densidad de corriente. 

En la Figura 1, a baja densidad de corriente se observa principalmente el efecto cinético-activación por modelo B-V. Hasta 10 A/m2 se observa el aumento de potencial de celda cercano a 0.75 V. Sin embargo, no se observan mayores diferencias debido a la concentración del electrolito soportante. 

Por otro lado, en la región de caída óhmica o aumento de potencial lineal, marca mayor diferencia del voltaje total en función a la concentración del electrolito. El escenario de mayor concentración presenta un menor potencial o “caída” de este, atribuido en parte a una mayor conductividad del electrolito. 
En Figura 2, se presenta un mismo escenario de condiciones en función a la concentración del electrolito, sin embargo, se aumenta el rango de evaluación de densidad de corriente, logrando identificar una tercera zona de aumento de potencial atribuido al control difusional. Esto ocurre a altas densidades de corriente debido a que la corriente límite es muy alta en función a las concentraciones de cobre en un electrolito tradicional de electroobtención. Así, dependiente de la concentración se identifica que para un electrolito a 538 mol/m3 con una densidad de corriente aplicada en torno a 410 A/m2 se “ingresa” a una etapa de control difusional y refleja un potencial total de celda de 3.7 V.  Por otro lado, para concentraciones mayores a 658 mol/m3, bajo estas condiciones no se ingresa u observa un control difusional. 

Obs: el modelo no presenta restricción hasta corriente límite, por lo cual, el modelo podría estimar en una zona no física. 

<img width="597" height="481" alt="image" src="https://github.com/user-attachments/assets/6615507a-dc97-4ce0-81bb-9c437f8951d2" />

Para Figura y escenario 2:
•	Condiciones aplicadas para modelación.
•	Concentración mínima [mol/m³]: 538
•	Concentración máxima [mol/m³]: 692
•	Paso de concentración [mol/m³]: 15
•	Temperatura fija [K]: 338.15
•	Densidad de corriente mínima [A/m²]: 0.1
•	Densidad de corriente máxima [A/m²]: 500
•	Paso de corriente [A/m²]: 0.0001

<img width="708" height="569" alt="image" src="https://github.com/user-attachments/assets/fdf2870c-413d-4ac3-83b8-e451a45f8ec8" />


Resultados de evaluación en condición celda electrolítica ajustada 
Simulación condiciones síntesis nanomaterial: respuesta de voltaje total de celda (considerando sobrepotenciales) en función de las densidades de corriente y evaluación de concentración de electrolito.

•	Concentración mínima [mol/m³]: 78.7
•	Concentración máxima [mol/m³]: 157.5
•	Paso de concentración [mol/m³]: 7.88
•	Temperatura fija [K]: 298.15
•	Densidad de corriente mínima [A/m²]: 0.1
•	Densidad de corriente máxima [A/m²]: 50
•	Paso de corriente [A/m²]: 0.001

En la Figura 3 se observa que el efecto de aumento potencial en celda por efecto de sobre potencial óhmico es el predominante. El efecto cinético toma menor predominancia respecto de la resistencia total óhmica, esto atribuido a la baja conductividad del electrolito. Así podemos observar que la condición a 157 mol/m3, presenta un sobrepotencial entorno a un 42% menos respecto del proceso con precursor diluido a 79mol/m3, representando voltajes de celda total en torno a 1.8 V y 3.1 V, respectivamente. Así también, estos potenciales son mayores respecto de celda electrolítica tradicional, debido a la menor temperatura y concentración en proceso de síntesis electrolítica de cobre. 

<img width="698" height="561" alt="image" src="https://github.com/user-attachments/assets/3a0ff859-5af7-434b-b9bd-4e0af6e6a7c8" />

En una siguiente iteración (Figura 4) bajo las mismas concentraciones y temperatura 298.15 K, aumentando la densidad de corriente hasta 65 A/m2, se observa que 3 condiciones de procesos a concentraciones menores de 94 mol/m3 ingresan a zona de control difusional. Así, a una densidad de corriente de 53 A/m2 y una concentración de Cu en precursor de 79 mol/m3, se ingresa a control difusional y representa un potencial total de celda de 3.25 V. Se ingresa a este régimen a una densidad de corriente hasta un 87% más baja respecto de una condición estándar de electroobtención de cobre (538 mol/m3, 35 g/L y 410 A/m2)

<img width="698" height="561" alt="image" src="https://github.com/user-attachments/assets/b5d83462-e7c9-4f93-963b-c63e6758fa36" />


Caso N° 2: Variación de material y propiedades de electrodos 

Para el caso N° 2 se realiza una evaluación en escenario típico de electroobtención, es decir Ánodo de Pb y Cátodo de Inox. 316L. Propiedades de materiales en referencia portal Engineer calculator.

•	rho0_cat = 7.4e-7      # Resistividad Inox 316L a 298K [Ω·m] 
•	rho0_an = 2.2e-7       # Resistividad Pb sin aleación a 298K [Ω·m] 
•	alpha_rho_cat = 0.00094  # Coeficiente de temperatura resistividad [1/K] Inox 316L
•	alpha_rho_an = 0.0040    # Coeficiente de temperatura resistividad [1/K] Pb sin aleación

La resistencia electrónica total (ánodo + cátodo) en el Caso N° 2 aumentaría, respecto del caso N° 1 el cual considera electrodos de un mismo material y tipo Cobre (cátodo madre), por tanto, se esperaría mayor caída óhmica, mayor sobrepotencial total y mayor voltaje de celda requerido

# Mismas condiciones de electrolito respecto de escenario N°1; solo cambio de electrodos de cobre (ambos) por ánodo de plomo sin aleación y cátodo de acero inoxidable 316L.

•	Concentración mínima [mol/m³]: 538
•	Concentración máxima [mol/m³]: 692
•	Paso de concentración [mol/m³]: 15
•	Temperatura fija [K]: 338.15
•	Densidad de corriente mínima [A/m²]: 0.1
•	Densidad de corriente máxima [A/m²]: 50
•	Paso de corriente [A/m²]: 0.001

Simulación caso N° 2:

Se observa en la Figura 5 que la respuesta del voltaje total de la celda no varía de manera significativa respecto del caso N° 1 con electrodos de cobre, esto debido a que la resistividad del electrolito (κ del Cu²⁺ en solución) domina completamente la caída óhmica. El electrolito es bastante más resistivo que los electrodos, por lo cual, al modificar la resistividad de cobre: 1.7×10⁻⁸ Ω·m a plomo / inox: 10⁻⁷ Ω·m, tenemos sólo 1 orden de magnitud. Así también, el espesor de los electrodos es muy pequeño (5 mm), y el área es relativamente grande (0.01 m²).
Por lo tanto, la resistencia electrónica total sigue siendo muy baja: ~ micro-ohms a mili-ohms → contribución mínima al voltaje, respecto de los sobre potenciales a partir del electrolito, cinética-activación y concentración-difusión.

<img width="611" height="491" alt="image" src="https://github.com/user-attachments/assets/22823af5-525b-47fa-9601-8c4fe579e038" />

=== RESUMEN DE PARÁMETROS CALCULADOS ===
 C (mol/m³)  κ (S/m)     D (m²/s)  i_L (A/m²)
      538.0  2.88368 4.046734e-10  420.123215
      553.0  2.96408 4.046734e-10  431.836688
      568.0  3.04448 4.046734e-10  443.550160
      583.0  3.12488 4.046734e-10  455.263633
      598.0  3.20528 4.046734e-10  466.977105
      613.0  3.28568 4.046734e-10  478.690578
      628.0  3.36608 4.046734e-10  490.404050
      643.0  3.44648 4.046734e-10  502.117523
      658.0  3.52688 4.046734e-10  513.830996
      673.0  3.60728 4.046734e-10  525.544468
      688.0  3.68768 4.046734e-10  537.257941
      703.0  3.76808 4.046734e-10  548.971413


Caso N° 3: Variación de material y propiedades de ánodo

De acuerdo con lo observado en el caso N°2 es que se propuso evaluar el efecto considerando otro material en el electrodo de ánodo. Así, se evaluó un ánodo en material de grafito o carbono, el cual es utilizado en diferentes aplicaciones. Se consideró el mismo escenario de electrolito, diseño de celda, cátodo Inoxidable 316L, solo modificando las propiedades del ánodo por:
•	rho0_an = 3.0e-3       # Resistividad grafito plano basal sin aleación a 298K [Ω·m]. Ref. Anne Marie Helmenstine, Ph.D. Thoughtco
•	alpha_rho_an = 0.00303    # Coeficiente de temperatura resistividad [1/K] grafito plano basal (depende de orientación del grafito) 

Condiciones de simulación:

•	Concentración mínima [mol/m³]: 538
•	Concentración máxima [mol/m³]: 692
•	Paso de concentración [mol/m³]: 15
•	Temperatura fija [K]: 338.15
•	Densidad de corriente mínima [A/m²]: 0.1
•	Densidad de corriente máxima [A/m²]: 50
•	Paso de corriente [A/m²]: 0.001


En la Figura 6 se observa un aumento y diferencia en el voltaje total de la celda electrolítica para este caso evaluado con un ánodo de grafito. Se alcanzan voltajes de hasta 1.18 V, representando para la condición de 538 mol/m3 un aumento estimado de 10 mV atribuido a un sobrepotencial óhmico entre 9.2-10% mayor respecto escenarios precios. Esto, afectado en particular R_electrónica implicada por el material de grafito y la mayor resistividad respecto de los electrodos de cobre y plomo evaluados en los casos 1 y 2, respectivamente

<img width="645" height="518" alt="image" src="https://github.com/user-attachments/assets/bccb6379-8bcb-4b40-b19d-d79704399d83" />


=== RESUMEN DE PARÁMETROS CALCULADOS ===
 C (mol/m³)  κ (S/m)     D (m²/s)  i_L (A/m²)
      538.0  2.88368 4.046734e-10  420.123215
      553.0  2.96408 4.046734e-10  431.836688
      568.0  3.04448 4.046734e-10  443.550160
      583.0  3.12488 4.046734e-10  455.263633
      598.0  3.20528 4.046734e-10  466.977105
      613.0  3.28568 4.046734e-10  478.690578
      628.0  3.36608 4.046734e-10  490.404050
      643.0  3.44648 4.046734e-10  502.117523
      658.0  3.52688 4.046734e-10  513.830996
      673.0  3.60728 4.046734e-10  525.544468
      688.0  3.68768 4.046734e-10  537.257941
      703.0  3.76808 4.046734e-10  548.971413


Aspectos en los cuales el modelo aún puede optimizado. 
•	Considerar efectos de convección natural o forzada
•	Consideración de bajas [Fe+2]
•	“Barrido o evaluación” en modo potenciostato, forzando el potencial y evaluando la respuesta de la densidad de corriente
