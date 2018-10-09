# Test
A - Generar una tabla, con el listado de todos los Movimientos, con el siguiente contenido :

Fecha
Descripción de Cliente
Descripción de Proveedor
Descripción de Producto
Descripcion de Marca
Cantidad
Costo
Venta
Ganancia Neta

```SQL
CREATE TABLE MOVIMIENTOS AS Select  M.Fecha, , C.Descripcion, V.Descripcion , N.descripcion,  M.cantidad, 
M.Costo, M.venta, (M.venta – M.costo) as gananciaNeta FROM data_movimientos M 
JOIN  data_clientes C
ON M.cod_cliente = C..cod_cliente
JOIN data_productos P
ON M.cod_prod = P.cod_prod
JOIN data_proveedores  V
On  P.cod_proveedor = V. cod_proveedor
JOIN data_marcas N
On P.cod_marca = N.cod_marca
 
```


b- Mostrar un listado de todas las Marcas que no tuvieron Ventas.



c- En base a la tabla generada en a, consultar,  ordenando por fecha y descripción del cliente:

. Fecha
. Descripción de Cliente
. Ganancia Neta Acumulada en las últimas 7 operaciones

La idea del punto c es, dado un cliente y una fecha de operación, mostrar la sumatoria de las ganancias derivadas de las últimas siete operaciones que haya realizado.

Ejercicio 2 - Algo de Python (Para hacerlo interesante, usar Python 2.7)

Se deberá escribir un script que transforme el archivo datos_data_engineer.tsv en un archivo CSV que pueda ser insertado en una base de datos, y/o interpretado por cualquier parser estándar de archivos delimitados, de la manera más sencilla posible.

El archivo resultante debe tener las siguientes características:
•	Cada row contiene la misma cantidad de campos
•	Los campos se separan con un pipe |
•	Se deben poder leer correctamente los caracteres especiales que estén presentes en los campos actuales del archivo. 
•	El encoding del archivo final debe ser UTF-8 (datos_data_engineer.tsv es un archivo UTF-16LE)













Ejercicio 3 - Preguntas en general (Soluciones de pocas líneas)

a- ¿Qué formas de hacer scheduling de una tarea en linux conoce? 

b- ¿Cómo y con qué comandos guardaría la mayor cantidad de detalle sobre las salidas de un script python que desea ejecutar de forma diaria a las 6AM?

c- ¿Qué comando o serie de comandos utilizaría para subir todos los contenidos de un directorio a un bucket de S3?

d- Si una instancia de Redshift utilizada para reporting se está quedando sin espacio y se impone la necesidad de sacar algunos datos antiguos de la base, pero a pesar de que los datos de más de seis meses de antigüedad no se utilicen para reporting, se los requiere para entrenar y validar modelos predictivos, además de hacer algunos análisis ad-hoc en SQL a un precio razonable considerando tanto infraestructura como costos de consultas ¿Que tipo de solución propondría para poder consultar los datos usando servicios cloud en AWS? 


