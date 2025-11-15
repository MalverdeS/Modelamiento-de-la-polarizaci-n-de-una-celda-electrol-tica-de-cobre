# Modelamiento-de-la-polarizacion-de-una-celda-electrol-tica-de-cobre
Este proyecto busca la modelación del voltaje o potencial total de una celda electrolítica en respuesta a diferentes densidades de corriente y condiciones de concentración o temperatura de proceso, aplicado para etapa tradicional de electro obtención o celda de síntesis nanomateriales de cobre.

1. Contexto, interrogantes y metodología general 
Chile es el mayor productor cobre en el mundo con una participación cercana al 24%, produce más de 5.5 Mt/año cobre fino y esto implica un gran aporte al PIB nacional superior al 12%. Aquello es posible a partir de la comercialización de dos productos principales, concentrados y cátodos de cobre, este último aun cuando es el más valioso o especializado solo representa un 26% de la producción nacional.  
Este producto se genera en reactores o celdas electrolíticas, las cuales a diferencia de una celda combustible que genera electricidad, estas utilizan energía eléctrica para promover reacciones catódicas o reductivas para generar los productos de cobre. 
A nivel general, se componen por un electrolito (solución contiene Cu), sin interferencia de membrana, dos electrodos planos; un ánodo inerte en el cual ocurre reacción hidrólisis de agua y generación de oxígeno. Y, por otro lado, un cátodo el cual “aporta” los electrones para la reducción de ion cúprico a cobre metálico. 

<img width="497" height="391" alt="image" src="https://github.com/user-attachments/assets/e4c15048-2ce0-4156-91dd-5eacdb1a75ef" />

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




