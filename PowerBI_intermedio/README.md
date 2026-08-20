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