Título del Proyecto: Análisis Inicial y Selección de Problema

Descripción: 
El objetivo de este proyecto es analizar y extraer información relevante a partir de cuatro conjuntos de datos distintos, cada uno relacionado con un ámbito específico: ecología (penguins_lter), educación (student-mat), comercio minorista (SuperMarket Analysis), y hospitalidad (hotel_bookings). A través del análisis de estos datos, se busca obtener una comprensión más profunda de los patrones, tendencias y relaciones entre las variables, lo que puede ofrecer información útil para la toma de decisiones.

Importancia:
Este proyecto tiene una gran relevancia en diferentes contextos, ya que proporciona herramientas para entender mejor fenómenos ecológicos, factores que influyen en el rendimiento académico de los estudiantes, hábitos de compra en supermercados y dinámicas de las reservas hoteleras. Los resultados de este análisis pueden ser utilizados para mejorar la gestión de recursos, optimizar procesos de venta, ajustar políticas educativas, y mejorar la experiencia del cliente en el sector hotelero. Además, facilita la toma de decisiones informadas y permite identificar áreas de mejora en cada uno de los sectores analizados.

Conjuntos de Datos Analizados: Descripción breve de los cuatro conjuntos de datos analizados.

1) penguins_lter
Fuente: Este conjunto de datos proviene de un estudio de largo plazo sobre los pingüinos, específicamente del programa LTER (Long-Term Ecological Research) de la Universidad de California.
Tamaño: 344 entradas, 17 columnas.
Variables:
Incluye información sobre el nombre del estudio, especie de pingüino, región, isla, medidas físicas (como largo y profundidad del pico, largo de aletas, peso corporal), y datos isotópicos, entre otros.
Algunas variables clave son Species, Island, Culmen Length (mm), Flipper Length (mm), Body Mass (g).

2) student-mat
Fuente: Este conjunto de datos proviene de una encuesta a estudiantes de Portugal, relacionada con el rendimiento académico y factores sociales.
Tamaño: 395 entradas, 33 columnas.
Variables:
Variables socioeconómicas como school, sex, address, famsize, Pstatus (estado de los padres).
Factores educativos como Medu (educación materna), Fedu (educación paterna), studytime, y resultados académicos en las variables G1, G2, G3.

3) SuperMarket Analysis
Fuente: Este conjunto de datos proviene de un análisis de ventas en supermercados, con información sobre transacciones de clientes.
Tamaño: 1000 entradas, 17 columnas.
Variables:
Información de la transacción como Invoice ID, Product line, Unit price, Sales, Payment, y Rating.
Datos demográficos y del cliente como Customer type, Gender, City, junto con detalles de las compras como Quantity, Tax 5%, y márgenes de ganancia.

4) hotel_bookings
Fuente: Este conjunto de datos proviene de un sistema de reservas de hotel.
Tamaño: 6797 entradas, 31 columnas.
Variables:
Información sobre la reserva como hotel, is_canceled, lead_time, meal, country, adr (precio promedio diario), reservation_status.
Datos sobre los clientes como adults, children, previous_cancellations, y detalles adicionales sobre las habitaciones, como tipo de habitación reservada (reserved_room_type), tipo de habitación asignada (assigned_room_type).
Este resumen proporciona una visión general de cada conjunto de datos, sus fuentes, tamaños y algunas de sus variables clave.

Resumen del EDA Inicial:

Resumen de los hallazgos principales de los EDA realizados:

a) penguins_lter (Estudio de pingüinos):

Diversidad de especies: Se identificaron tres especies principales de pingüinos: Adélie, Chinstrap y Gentoo.
Patrones en las mediciones físicas: Se observó que las especies de pingüinos tienen diferentes rangos de longitud de culmen, longitud de aletas y masa corporal.
Distribución geográfica: Los datos muestran que las especies están distribuidas entre varias islas en la región Antártica, con algunas variaciones en el tamaño de los individuos entre islas.
Faltantes: Se detectaron valores faltantes en algunas variables, como el sexo, la profundidad del culmen y la masa corporal, lo que puede requerir un tratamiento especial.

b) student-mat (Rendimiento académico de estudiantes):

Impacto de la familia: Los estudiantes con un mayor apoyo familiar (famsup y schoolsup) tienden a tener mejores calificaciones en general (especialmente en G3).
Efecto de la actividad extracurricular: Los estudiantes que participan en actividades extracurriculares tienen un rendimiento superior en las calificaciones.
Desempeño según el tiempo de estudio: Un mayor tiempo de estudio (studytime) se asocia con mejores calificaciones, aunque el impacto es menos pronunciado para los estudiantes con altos niveles de ausentismo.
Variables categóricas clave: El género, la ocupación de los padres y la situación familiar (p.ej., Pstatus) son factores que también afectan el rendimiento académico.

c) SuperMarket Analysis (Análisis de ventas de supermercado):

Preferencia de productos: Las categorías de productos más comprados incluyen alimentos, bebidas y productos de higiene personal.
Patrones de compra según el tipo de cliente: Los clientes recurrentes tienden a comprar más productos de líneas específicas (p.ej., tecnología) y muestran un mayor nivel de satisfacción (Rating).
Relación entre precio y ventas: Se observó que los precios más altos (Unit price) tienden a correlacionarse con un mayor volumen de ventas en ciertos productos, aunque esto varía según la categoría de productos.
Métodos de pago populares: El pago en efectivo y las tarjetas de crédito fueron los métodos más comunes, con una ligera preferencia por las tarjetas.

d) hotel_bookings (Reservas de hotel):

Tendencias de cancelación: Un alto porcentaje de reservas (aproximadamente el 37%) son canceladas, con mayores tasas de cancelación en ciertos tipos de clientes (e.g., "repeated guest").
Patrones de reservas: Las reservas se concentran principalmente en los meses de verano (junio a septiembre) y los fines de semana.
Factores de satisfacción: La "average daily rate" (ADR) es un factor importante que afecta la probabilidad de cancelación y las preferencias de los huéspedes.
Diferencias entre tipos de clientes: Los "repeat guests" tienen tasas de cancelación más bajas y suelen reservar por más noches, con una preferencia por ciertos tipos de habitación.
Datos faltantes: Se encontraron algunas columnas con valores faltantes, como el tipo de habitación asignada, que deben ser tratados para mejorar la calidad de los análisis.

* Conclusión general de los hallazgos:
Los análisis exploratorios de estos datasets proporcionan una visión integral de las dinámicas en los ámbitos ecológico, educativo, comercial y hotelero. Las variables clave como el soporte familiar en el rendimiento académico, las preferencias de los clientes en supermercados, y la tasa de cancelación en las reservas de hotel son factores determinantes en estos contextos. Además, los datos faltantes y la necesidad de limpiar ciertos atributos fueron hallazgos importantes que deben ser abordados para garantizar un análisis más preciso.


Problema Seleccionado: Descripción detallada del problema seleccionado, la justificación de la elección y los objetivos específicos.

Penguins: Se analiza el comportamiento y características de diferentes especies de pingüinos en su hábitat. El objetivo es entender cómo factores como el tamaño del cuerpo, la longitud de las aletas y otros indicadores biológicos se relacionan con su bienestar y supervivencia. Esto es importante para la conservación y estudio de estas especies en su entorno natural.

Estudiantes: El análisis se centra en el rendimiento académico de los estudiantes, explorando cómo variables como el tipo de familia, la cantidad de tiempo dedicado al estudio, y la presencia de actividades extracurriculares afectan sus calificaciones. El objetivo es identificar los factores clave para mejorar el rendimiento académico y brindar apoyo efectivo a los estudiantes.

Ventas de Supermercado: Se investiga cómo diferentes características de los clientes (género, tipo de cliente, productos comprados) y factores como promociones y métodos de pago afectan las ventas en un supermercado. El objetivo es optimizar la estrategia de ventas, ajustar inventarios y mejorar la experiencia del cliente para aumentar los ingresos y la fidelidad.

Reservas de Hotel: El análisis busca entender los patrones de reservas y cancelaciones en un hotel, explorando factores como el tipo de cliente, la temporada y las solicitudes especiales. El objetivo es mejorar la gestión de reservas, reducir cancelaciones y optimizar la ocupación de habitaciones para aumentar la rentabilidad del hotel.

Cada uno de estos análisis tiene como objetivo mejorar la toma de decisiones en su área respectiva, ya sea en conservación de especies, educación, ventas o gestión hotelera.

Instrucciones para Ejecutar: Pasos para ejecutar los notebooks y reproducir los resultados.
/Proyecto2
|-- /datasets
|   |-- dataset1.csv
|   |-- dataset2.csv
|   |-- dataset3.csv
|   |-- dataset4.csv
|-- /EDA
|   |-- EDA_dataset1.ipynb
|   |-- EDA_dataset2.ipynb
|   |-- EDA_dataset3.ipynb
|   |-- EDA_dataset4.ipynb
|-- /selected_dataset
|   |-- selected_dataset.csv
|   |-- EDA_selected_dataset.ipynb
|-- README.md

Autores: Alejandro Romero.

Licencia: Información sobre la licencia del proyecto.

