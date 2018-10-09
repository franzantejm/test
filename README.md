# Test
A - Generar una tabla, con el listado de todos los Movimientos, con el siguiente contenido :

. Fecha
. Descripción de Cliente
. Descripción de Proveedor
. Descripción de Producto
. Descripcion de Marca
. Cantidad
. Costo
. Venta
. Ganancia Neta

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
