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