# Power BI Intermedio: Análisis y modelado de datos

## Gráficos de power BI

### Jerarquías de fechas

Cada vez que se agrega un campo fecha a un gráfico de Power BI, el propio campo se divide en 4 segmentos o subpartes:

- Año
- Trimestre
- Mes 
- Día

esto se puede observar en el panel de datos. Se puede mover campo fecha con jerarquía o mover elementos individuales de la jerarquía (se selecciona y arrastra el que se desea mover).

Al la fecha con jerarquía agregarla a un tabla, se visualizan varias opciones: 
1. Expandir todo a un nivel de la jerarquía.
2. Resumir.
3. Ir al siguiente nivel de jerarquía.
4. Explorar en profundidad.

![Opciones jeraquía](/img/jerarquías.png)

### Gráfico de lineas para tendencias de tiempo

Es muy util, cuando se quiere analizar la evolución de un valor númerico a lo largo del tiempo o de una secuencia ordenada.

> Es especialmente eficaz para identificar tendencias, patrones, estacionalidades o fluctuaciones en los datos.

***¿Para qué se utiliza?***

* Mostrar la evolución de una métrica a lo largo del tiempo (por ejemplo, ventas mensuales, número de clientes por trimestre, etc.). 
* Comparar varias series temporales en paralelo. 
* Detectar subidas, bajadas o cambios de tendencia. 
* Identificar periodos de estabilidad o de variación significativa. 
Este tipo de gráfico se suele aplicar con jerarquía de fechas para ver la tendencia de un campo totalizado a lo largo de un período de tiempo. 

*** Cuando insertamos un gráfico, se muestran las siguientes areas: ***

- Eje X: Categoría principal del gráfico.
- Eje Y: Campo a totalizar.
- Eje Y secundario: Segundo campo a totalizar con valores sensiblemnete inferiores al campo del Eje Y.
- Leyenda: Campo por el que se quiere detallar el eje X o categoría.
- Multiplos pequeños: Campo por el que se requiere replicar el gráfico. Se usa para replicar el gráfico mediante gráficos más pequeños por los elementos de un campo.
    ![Multiple pequeños](/img/multiples_pequeños.png)


> Si tenemos un campo en el eje Y secundario, no puede haber otro campo en el área leyenda. Son dos áreas incompatibles.

### Gráfico para representaciones geográficas

Permiten visualizar datos en mapas, permitiendo una forma intuitiva y potente para analizar información relacionada con ubicaciones.

Power BI incluye diferentes tipos de visualizaciones geográficas, como mapa o el mapa coroplético.

"
***¿Para qué se utilizan?*** 

- Para analizar datos relacionados con ubicaciones geográficas. 
- Para detectar patrones o tendencias por zona geográfica (por ejemplo, ventas por comunidad autónoma). 
- Para realizar comparativas regionales o internacionales de forma visual. 
- Para identificar áreas de oportunidad o zonas de baja actividad.

Cuando insertamos un informe de tipo Mapa, puede darse el caso que al poner el campo que tiene la localización geográfica, el mapa no cargue. 

Si esto ocurre, en la ventana de Power BI Desktop, tendremos que ir a la ficha ARCHIVO, y seleccionar OPCIONES Y CONFIGURACION en la parte inferior del panel izquierdo y pulsar OPCIONES: 

En el panel izquierdo seleccionaremos la opción CARACTERISTICAS DE VERSION PRELIMINAR.

Donde habrá que activar la opción OBJETO VISUAL MAPA DE FORMAS:

En caso de estar activado, se desactivará y volverá a activar. Pulsamos el botón ACEPTAR y volveremos a entrar a Power BI Desktop. 
"

#### Mapa coroplético

Tambien llamado mapa de formas, representa datos a traves de areas geográficas, como paises, regiones, provincias, usando colores o intensidades según el valor de un campo.

![Mapa coroplético o de forma](/img/mapa_coroplético.png)

El gráfico tiene las áreas:
- Ubicación: Donde se agrega el campo que tiene la localización geográfica.
- Leyenda: Permite que la zona geográfica se coloree segun el elemento dominante de un campo categórico.
- Latitud
- Longitud
- Información sobre la herramienta: Muestra la información en el tooltip de un campo totalizado.

### Mapa

Este gráfico, permite respresentar datos geográficos mediante puntos o burbujas posicionados segun ubicaciones especificas.

Cada burbuja se coloca en el lugar geográfico correspondiente y puede variar de tamaño y color para reflejar el valor de una medida o categoría

> Facilita el análisis visual de patrones geográficos

Icono de mapa mundi.

Las áreas que muestra dicho gráfico son:

- Ubicación
- Leyenda
- Latitud
- Longitud
- Tamaño de la burbuja: Aca se coloca el campo a totalizar, que da el tamaño a la burbuja.

### Gráfico medidor

Se usa para mostrar el valor de un avance respecto a un objetivo. Es ideal para representar indicadores claves de rendimiento (KPI) y facilita la comparación entre un valor actual o un valor de referencia o meta.

Para darle sentido debe llevar un filtro o una segmentación.

Muestra las siguientes áreas:

- VALOR: Campo a totalizar por el que se realizará la medición del objetivo. 	
- VALOR MÍNIMO: Campo que contiene el valor más bajo que deseamos que tenga el medidor.
- VALOR MÁXIMO: Campo que contiene el valor más alto que deseamos que tenga el medidor.
- VALOR DESTINO: Campo que tiene el valor del objetivo a alcanzar en el medidor. 
 	 	
### Interacciones

Es la forma que interactuan los gráficos entre si, al selccionar uno u otro, se aplica a todos.

Ejemplo, cuando filtramos una segmentacion se aplica sobre los que esten.

Si se da el caso, de que no queremos que desde un informe, se fuese a filtrar otro informe:

1. Seleccionar un informe
2. Ir a la fecha FORMATO 
3. Pulsar botón EDITAR INTERACCIONES

![Interacciones](/img/interacciones.png)


> Se activa los iconos que habilitan interacciones - Para desactivar el prohibido y para el caso contrario el otro.
![Editar interacciones](/img/iconos_editarInteracciones.png)

Se muestra dos icono uno de gráfica y un prohibido, para quitar la interacción presionar el icono de prohibido.

---
Cuando tenemos diferentes gráficos dentro de una misma página de informes, estos interaccionan entre ellos, es decir, seleccionando un elemento de un gráfico, se filtran todos los informes de la misma página. 

En algunos casos, no queremos que se filtre desde algún gráfico ningún otro informe, es ahí cuando tenemos que modificar las interacciones, es decir, la forma de interactuar los informes de una misma página.

Para modificar las interacciones, debemos tener seleccionado un informe. A continuación, ir a la FICHA FORMATO y pulsar EDITAR INTERACCIONES: 
 

La forma que tendríamos de proceder sería: seleccionar el gráfico al que queremos modificar las interacciones, y con cada uno de los otros gráficos que no queremos que interactúe (que no queremos que filtre), pulsamos el botón NINGUNO (icono de prohibido)

Si, por el contrario, hemos quitado una interacción y la queremos volver a colocar, seleccionamos el informe a modificar, y sobre el informe que queremos que interactúe, pulsamos el botón FILTRO (icono de gráfica)

Una vez que hayamos modificado las interacciones, podemos ocultar sus iconos yendo nuevamente a la FICHA FORMATO y desactivando el botón EDITAR INTERACCIONES. 

---

### Marcadores

Los marcadores son una herramienta para obtener una especie de foto interactiva en un punto determinado, es decir permite guardar el estado actual de una página del informe.

Se suele usar para:
- Quitar los filtros aplicados: No tenemos ningun botón que quite todos los filtros, pero podemos tener un marcador que guarde el estado de la página sin filtros.
- Poner el foco en un unico informe que nos interesa resaltar: Si se necesita acceder al modo enfoque de un informe para verlo detenidamente.
- Mostrar u ocultar elementos visuales: Podemos ocultar informes para solo mostrar en la página aquellos que, según una situación concreta, nos interesa mostrar. 

> Algo que debemos tener siempre en cuenta, es que el marcador graba el estado de los datos de un informe, pero no graba las posiciones en las que están colocados en la página ni el tamaño de estos. No tiene sentido crear marcadores donde se cambia el tamaño de un informe o lo movemos de lugar en la página. Estos cambios afectarían a toda la página de informe y NO SOLO al marcador creado. 

> Otro detalle a tener en cuenta es que los marcadores afectan a los informes de la página de informes que tenemos activada en el momento de crear el marcador. 

***¿Cómo crear un marcador?***

Ir a la ficha Ver > Grupo de botones mostrar paneles > Marcadores

Luego presionar el botón agregar

Una vez se crear para cambiarle el nombre, dar doble clic

***¿Cómo ejecutar el marcador?***


**Forma 1**

Pulsar sobre el panel de marcadores el botón con el nombre del marcador a ejecutar.


**Forma 2**

Ficha INSERTAR > BOTONES > elejir botón
Al presionar el botón se abre *Formato del botón* ir a Acción, activarla.

En esa propiedad acción, asignar el marcador e indicar cual es el marcador que se desea ejecutar

> Y para ejecutarlo presionar CTRL + Clic Izquierdo

***¿Cómo se modifica un marcador?***

Si hemos grabado un marcador, y algo no ha quedado como se esperaba, ponemos el informe en el estado correcto que quería grabar, y en el panel de marcadores, a la derecha del nombre del marcador, pulsamos el botón MÁS OPCIONES, seleccionando la opción: ACTUALIZAR. 
![Marcadores](/img/marcadores.png)


***¿Cómo ocultar gráficas ?***

![alt text](/img/image.png)

## Power Query

Para ingresar a Power Query
![Power Query](/img/ingresar_powerQuery.png)

### Transformaciones de texto

Las columnas textos, se pueden transformar desde 
1. Ficha TRANSFORMAS > Grupo de botones COLUMNA DE TEXTO
![Forma 1](/img/1_tranformar_texto.png)
2. Ficha AGREGAR COLUMNA > Grupo de botones DE TEXTO
![Forma 2](/img/2_transformar_texto.png)

Las principales transformaciones de texto:

- Dividir columna: Solo esta en la ficha TRANSFORMAR, al seleccionar la columna, se ven diferentes opciones:
    - Por delimitador
        - Delimitador situado más a la izquierda: el texto hasta el primer separador se iría a la primera columna y el texto detrás del primer separador a la segunda columna. 
        - Delimitador situado más a la derecha: el texto hasta el último separador se quedaría en la primera columna y que esté detrás del último en la siguiente columna. 
        - Cada aparición del delimitado: cada vez que aparezca el carácter separador en el texto seleccionado se irá generando una nueva columna. 
    - Por número de caracteres
    - Por posiciones: La posición 0, es el primer caracter
    - De minúsculas a mayúsculas: divide el texto seleccionado por las transiciones que haya entre letras minúsculas y letras mayúsculas. 
    - De mayúsculas a minúsculas: divide el texto seleccionado por las transiciones que haya entre letras mayúsculas y letras minúsculas. 
    - De dígito a no dígito: permite dividir el texto seleccionado por las transiciones que haya entre caracteres numéricos a no numéricos. 
    - De no dígito a dígito: divide el texto seleccionado por las transiciones que haya entre caracteres no numéricos a numéricos. 
 
 - Formato:
    - Minúsculas: transforma el texto de la columna seleccionada a letras minúsculas. 
    - Mayúsculas: transforma el texto de la columna seleccionada a letras mayúsculas. 
    - Poner en mayúscula cada palabra: pone en mayúscula la primera letra de cada palabra. 
    - Recortar: elimina espacios sobrantes del texto del campo seleccionado. 
    - Limpiar: elimina los caracteres no imprimibles del texto del campo seleccionado. 
    - Agregar prefijo: permite agregar un texto por delante de cada elemento del campo seleccionado.


### Transformaciones de fechas

Se pueden realizar tanto de la ficha de TRANSFORMAR como en la ficha de AGREGAR COLUMNA

Para trabajar con las fechas, utilizamos el botón FECHA, que está situado en la en ambas fichas en el grupo de botones DE FECHA Y HORA. Veremos las principales transformaciones de texto.

Al seleccionar la fecha se muestran las siguientes opciones:

* Antiguedad: Muestra el número de días que han pasado desde la fecha.
* Solo fecha: Si tiene fecha y hora, solo extrae la fecha.
* Analizar: Al tener un campo tratado por pwer BI como tipo texto, lo convierte en fecha automáticamente.
* Año: 
    * Año: Devuelve el año.
    * Inicio de año: Devuelve el 1 de enero de cada año de la fecha.
    * Final de año: Devuelve el 31 de diciembre de cada año de la fecha. 
* Mes: 
    * Mes: Devuelve el mes.
    * Inicio del mes: El día 1 de cada mes de cada fecha.
    * Fin de mes: Devuelve el ultimo día de cada mes de la fecha.
    * Días del mes: Devuelve el numero de dias que tiene el mes correspondiente a la fecha
    * Nombre del mes.
* Trimestre:
    * Trimestre del año: El número trimestre de la fecha del 1 al 4.
    * Inicio del trimestre: La fecha del primer día de cada trimestre.
    * Final trimestre: la fecha del ultimo dia de cada trimestre.
* Semana:
    * Semana del año.
    * Semana del mes.
    * Inicio de la semana.
    * Final de la semana.
* Restar días: Número de dias existentes entre dos fechas.
* Combinar fecha y hora.
* Más antigua: De los campos fechas que se tenga selecccionados deevuelve la fecha más antigua.
* Más reciente: De los campos fechas que se tenga seleccionados devuelve el más reciente.

### Combinar consultas


A través de la orden de combinar consultas, podemos mover a una tabla campos o columnas que se encuentran en otra, lo que va a mejorar la estructura de los datos para que sean analizados en nuestros gráficos. 

Cuando importamos al modelo de datos más de una tabla, lo habitual es que una de ellas, sea la tabla principal en la que se desarrolla toda la gestión que vayamos a analizar. El resto de las tablas suelen tener información referente a la tabla principal, para completarla con información complementaria. 

En algunos casos nos interesa que la tabla principal tenga columnas que tienen el resto de las tablas para completar toda la información de los campos clave. 

Para llevar dichas columnas a la tabla importante utilizaremos la orden de combinar consultas. 

En la ficha de INICIO en el grupo de botones COMBINAR, pulsamo el botón COMBINAR CONSULTAS, se desplega las siguientes acciones:

* Combinar consultas
* Combinar consultas para crear una nueva: Se creara una tabla en el panel de consultas con los campos registrados de la tabla seleccionada y las columnas a mostrar de la otra.

Una vez se de clic en INCICIO > COMBINAR, se abrira una ventana emergente, donde debemos seleccionar la tabla y la columna

1.  ![Combinar 1](/img/combinar_1.png)

2.  ![Combinar 2](/img/combinar_2.png)

3. Una vez se combine, se muestra una nueva columna, llamada columna combinada

![Combinar 3](/img/combinar_3.png)

4. La columna combinada en vez de tener un botón de filtro a su derecha, muestra el botón de combinar 

Pulsándolo, nos muestra la lista de campos de la tabla T_CODIGOS, que es la tabla con la que hemos combinado la principal.
![Combinar 4](/img/combinar_4.png)

> Se deja activado los checks de lis campos que se desean mostrar en la tabla.

Habrá que dejar activado únicamente el check de los campos que se desean mostrar en la tabla T_VENTAS: 

### Combinar consultas por más de una columna coincidente

Se selecciona la tabla, se va a ficha TRANSFORMAR > COMBINAR y una vez se abre la ventana emergente, entonces, se seleccionan varias columnas usando ctrl

![Combinar varios](/img/combinar_varios.png)

### Crear una tabla

Dentro de Power Query, podemos crear tablas para realizar agrupaciones de elementos de algún campo.

se hace desde la ficha INICIO > ESPECIFICAR DATOS

![alt text](/img/image_4.png)

Una vez se ingresa se muestra un cuadro de diálogo

![alt text](/img/image-1.png)

* Para agregar columnas, se pulsa el botón + situado a la derecha de Columna1. 
* Para cambiar el nombre de una columna se hacen dos clics sobre el título de la columna a modificar. 
* Para eliminar una columna sobre ella se pulsa el botón derecho y se selecciona la opción: eliminar. Igual sobre una fila pulsando sobre el número de la fila. 

#### Deshabilitar la carga de tablas
Cuando se han combinado tablas, o por cualquier otro motivo que podamos tener, es posible que haya tablas que necesitamos tener en Power Query, pero que no se carguen en Power BI.  

Si este es el caso, se tendrá que deshabilitar la carga de aquellas tablas que no se desea que se muestren en Power BI, ya que no formarían parte de ningún informe. 

Para cargar únicamente esta, se colocará el puntero del ratón sobre una de las que se quiera deshabilitar la carga y pulsando el botón derecho del ratón desactivaremos la opción habilitar carga

![alt text](/img/image-3.png)

### Anexar consulta

Se puede dar el caso en el que los datos que queremos analizar estén en diferentes tablas y queramos consolidar todos en una misma tabla para poder mostrar los informes del conjunto de datos. 

 Antes de dar la orden de anexar consultas, debemos tener en cuenta las siguientes circunstancias de las tablas a anexar: 

Los campos que tengan en común las tablas que vayamos a anexar, han de tener el mismo nombre, con los mismos caracteres y coincidiendo las mayúsculas y minúsculas. 
No es necesario que en cada tabla los campos estén en el mismo orden. 
Puede haber tablas que tengan campos que las otras no los tengan, no es ningún problema, en ese caso los registros de la tabla en dicho campo vendrán con su valor y los registros de las tablas que no disponen de la columna tendrán el valor nulo o vacío. 
Para dar la orden de anexar consultas, se hace desde la FICHA INICIO, en el grupo de botones COMBINAR, el botón ANEXAR CONSULTAS, se muestran dos opciones:

* Anexar consultas: Se vuelcan los registros sobre los de la tabla seleccionada en el panel de consultas.
* Anexar consultas para crear una nueva: Se creará una nyeva tabla con todos los registros de las tablas que se vayan a anexar.

### Columnas personalizadas

Es una nueva columna, que se crea a partir de otras columnas de la misma tabla, usando formulas simples:

Sirve para: 

* Realizar cálculos básicos (sumas, restas, multiplicaciones). 
* Unir texto de varias columnas. 
* Crear identificadores únicos o etiquetas. 
* Preparar los datos para análisis más claros y eficientes. 
* Antes de crear una columna personalizada, se debe tener en cuenta lo siguiente: 

Antes se debe tener en cuenta:

1. Solo se pueden usar columnas de la misma tabla, Power Query no permite usar columnas de otras tablas directamente en una columna personalizada. Todo debe venir de la tabla en la que estamos calculando. Si se necesitan columnas de otra tabla, primero deberíamos combinarlas.

2. Los tipos de datos deben ser compatibles, de tal modo que si vamos a sumar o multiplicar, las columnas han de ser numéricas. Si mezclamos tipos de datos, por ejemplo número y texto o fecha y número, puede dar error el cálculo.


3. Usaremos los operadores simples como: suma, resta, multiplicación, división y operador de texto (&).

4. La columna se calcula fila por fila, cada fila se evalúa de forma independiente, usando los valores de la misma.

***¿Cómo se crea?***

Ir a ficha AGREGAR COLUMNA > COLUMNA PERSONALIZADA

![alt text](/img/image_5.png)

Los operadores que podemos utilizar son: 

* +: para sumar 
* -: para restar 
* *: para multiplicar 
* /: para dividir 
* &: para juntar texto. 
 


## Prácticas

### Ejercicio 001

En una nueva página de informe con la tabla T_CURSOS importada del fichero BD CURSOS, insertar una matriz que muestre:
- FILA: MES (JERARQUIA FECHA CURSO)
- COLUMNA: AÑO (JERARQUÍA FECHA CURSO)
- VALORES: SUMA DE LA DURACION

Seguidamente, insertar una segmentación de datos y agregar el campo TRIMESTRE de la jerarquía del campo FECHA CURSO y filtrar por el trimestre 1 y 2.

Nota: Para seleccionar varios, usar ctrl.


### Ejercicio 002

En una nueva página de informe, agregar un gráfico de líneas que muestre, por año y trimestre de la FECHA CURSO, la suma del IMPORTE CLIENTE (en el eje principal) y el recuento de CURSO (Eje Y secundario). 

Después, dividir el gráfico por COMERCIAL. 

### Ejercicio 003

Inserta en una nueva página de informe, un mapa coroplético en el que agregarás a la ubicación el campo PAIS que crearemos, un formato condicional donde se pondrán en color verde los países con suma de duración menor de 3000 y en color azul los países con suma de duración mayor o igual a 3000. 

### Ejercicio 004

En una nueva página de informe insertar un mapa en el que se muestre en cada CIUDAD la suma del IMPORTE CLIENTE. Poner el color de la burbuja en verde.

Insertar una segmentación del campo PAIS y filtrar el mapa por ESPAÑA.

### Ejercicio 005

Insertar una nueva página de informes y en ella insertar un medidor que totalice la suma del IMPORTE CLIENTE con los siguientes valores en el eje medidor:

- VALOR MINIMO: 0
- VALOR MAXIMO: 75000
- VALOR DESTINO: 45000

Insertar una segmentación del campo CLIENTE.

Insertar una tabla que sume el IMPORTE CLIENTE de cada CLIENTE.

Cambiar las interacciones para que la segmentación sólo filtre el medidor y no la tabla y que la tabla no filtre el medidor.

Filtrar el medidor por el CLIENTE-004.

### Ejercicio 006

Eliminar todos los pasos creados a la tabla T_GASTOS en Power Query, dejando únicamente los pasos: ORIGEN, NAVEGACIÓN y TIPO CAMBIADO.

1. Poner la columna NOMBRE con la primera letra mayúscula.
2. Poner la columna APELLIDOS con todas las letras mayúsculas.
3. Juntar las columnas: APELLIDOS, NOMBRE y nombrar dicha columna como: NOMBRE EMPLEADO.
4. Agregar una columna con el nombre EQUIPO y que extraiga los dos primeros caracteres del campo COD EMPLEADO.

### Ejercicio 007
Sobre la columna FECHA GASTO de la tabla T_GASTOS, crear las siguientes columnas con el nombre que se va indicando:

* MES GASTO: obtener el nombre del mes de la FECHA GASTO con la primera letra mayúscula.
* AÑO GASTO: obtener el año de la FECHA GASTO.
* DIAS PASADOS: restar campos: FECHA PAGADO – FECHA GASTO.
* TRIM GASTO: obtener el trimestre del año de la FECHA GASTO y que por delante de * cada trimestre se muestra el texto: "Trim." (Trim. 1, Trim. 2, Trim. 3 y Trim. 4).

### Ejercicio 008
Importar las tablas T_CLIENTES, T_SECTORES, T_CONCEPTOS y T_FACTURAS del fichero MODELO DATOS FACTURAS e ir directamente al editor de Power Query.

En dicho modelo, se registran facturas en la tabla T_FACTURAS, que es donde se realiza toda la gestión que queremos analizar. Las facturas correspondientes a clientes que están guardados en la tabla T_CLIENTES y corresponden a conceptos que están registrados en la tabla T_CONCEPTOS.

Respecto a la tabla T_CLIENTES, a cada cliente se le asigna un sector, dichos sectores corresponden a los que están en la tabla T_SECTORES, pero ambas tablas tienen dos columnas coincidentes: el código del sector y el tipo del sector. Combinar las tablas:

* T_CLIENTES – T_SECTORES: mostrando en la tabla T_CLIENTES los campos TIPO SECTOR y DESCUENTO de la tabla T_SECTORES.
* T_FACTURAS – T_CLIENTES: mostrando en la tabla T_FACTURAS los campos: NOMBRE, SECTOR Y DESCUENTO de la tabla T_CLIENTES.
* T_FACTURAS – T_CONCEPTOS: mostrando en la tabla T_FACTURAS los campos CONCEPTO e IVA de la tabla T_CONCEPTOS.

Crear una tabla con el nombre TIPO CONCEPTO donde habrá dos columnas: CONCEPTO y TIPO con los siguientes registros:

|CONCEPTO |TIPO      |
|---------|----------|
|CON-001  |INTERNO   |
|CON-002  |INTERNO   | 
|CON-003  |INTERNO   | 
|CON-004  |INTERNO   | 
|CON-005  |INTERNO   | 
|CON-006  |EXTERNO   | 
|CON-007  |EXTERNO   | 
|CON-008  |EXTERNO   | 
|CON-009  |EXTERNO   | 
|CON-010  |EXTERNO   | 

Combinar la tabla TIPO CONCEPTO con la tabla T_FACTURAS y mostrar en T_FACTURAS el campo TIPO de TIPO CONCEPTO. 

Deshabilitar la carga de todas las tablas excepto la tabla T_FACTURAS. 

Cargar la tabla facturas a Power BI. 