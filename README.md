# Desarrollo de plan de estructuración logística para restaurante ETITC

## Descripción General
Este proyecto tiene como propósito principal proponer un plan estructurado para mejorar el desempeño del restaurante ETITC. El proyecto se centra en identificar y abordar las falencias y oportunidades del restaurante mediante herramientas de diagnóstico organizacional, como la matriz DOFA. La finalidad es optimizar los procesos internos del negocio y diseñar estrategias que permitan aumentar las ventas, fidelizar clientes actuales y atraer nuevos consumidores potenciales dentro de la comunidad.

### Objetivos

#### General
Estructurar un plan de mejora para el restaurante ETITC revisando sus falencias, problemas, debilidades y fortalezas, ordenando su método actual de funcionamiento aumente sus ventas, fidelice clientes y atraiga otros no frecuentes.

#### Específicos
•	Identificar las debilidades, oportunidades, fortalezas y amenazas del restaurante ETITC.

•	Diseñar un método de organización que permita mejorar la estructura del restaurante ETITC basado en su DOFA.

•	Presentar al restaurante ETITC la propuesta de estructuración para validar su posible implementación.

### Descripción del Problema
El restaurante ETITC ha identificado falta de orden en los procesos que el restaurante maneja de manera interna como lo son el control de inventario, los registros de compra y venta, así como los registros de proveedores, clientes y el empleado que realiza la venta, lo que genera inconvenientes para el restaurante como falta de disponibilidad de productos, descuadre de la caja o fallos al identificar los implicados en las transacciones. 

### Justificación
El restaurante ETITC, al trabajar de manera interna del campus y tener nicho reducido, debe maximizar las oportunidades, ya que tiene una variable del número de clientes donde puede aumentar o disminuir ligeramente dentro un margen de error limitado, pues el número de clientes posibles es limitado lo que a su vez limita el crecimiento del negocio. Por ello, se requiere realizar un análisis DOFA basado en datos del restaurante ETITC que permita hacer una estrategia para que las ventas puedan aumentar y los clientes compren de manera constante posiblemente atrayendo otros clientes potenciales que hacen parte de la comunidad, pero no acostumbran a comprar en la tienda. Este análisis saldría de la matriz DOFA que se propone.

### Requerimiento del Proyecto
El proyecto requiere desarrollar un sistema que permita integrar los datos del Restaurante ETITC. Se requiere diseñar una base de datos relacional con Funcionamiento CRUD y una interfaz desde donde se pueda ingresar, leer, actualizar y borrar información permitiendo así manejar temas de ventas inventario, proveedores o visualizaciones de estadísticas o previsión.

## Instrucciones de Uso

Descripción de como usar el proyecto: descargar, instalar, configurar, etc

### Requisitos

- Base de Datos: MySQL 9.0.1

## Diseño y Modelado

### Normalización

#### Diagrama ER
![Diagrama ER](Diagrama%20ER.png)
#### Diagrama EER
![](Restaurante%20ETITC%20EER.png)



## Pruebas

### Consultas 
### 1. Obtenga todos los datos de los clientes.
**Objetivo:**  Conseguir los datos de los clientes registrados.


- **Consulta en SQL:**
```sql
SELECT * FROM empleados;
```
![Imagen 1](Imagenes%20proyecto/1.PNG)
  

### 2. Obtenga el nombre completo y correo electronico de los clientes.
**Objetivo:**  Conseguir el nombre del cliente con su respectivo correo electronico.


- **Consulta en SQL:**
```sql
SELECT nombre_completo, correo_electronico FROM clientes;
```
![Imagen 2](Imagenes%20proyecto/2.PNG)

### 3. Listar los proveedores ubicados en una ciudad especifica.
**Objetivo:**  Conseguir los proveedores ubicados en Bogotá.
- **Consulta en SQL:**
```sql
SELECT * FROM proveedores WHERE ciudad = 'Bogota'; 
```
![Imagen 3](Imagenes%20proyecto/3.PNG)

### 4.Cuales son los productos disponibles, sus precios de ventas y cuantas unidades estan en stock.
**Objetivo:**  Obtener un listado con informacion clave sobre los prodcutos.
- **Consulta en SQL:**
```sql
SELECT 
    nombre_producto,
    precio_venta,
    unidades_disponibles
FROM productos;

```
![Imagen 4](Imagenes%20proyecto/4.PNG)

### 5. Actualizar el precio de venta de un producto especifico.
**Objetivo:**  Actualizar el precio del producto con código 101.
- **Consulta en SQL:**
```sql
UPDATE productos 
SET precio_venta = 7500 
WHERE codigo_producto = 101;

```
![Imagen 5](Imagenes%20proyecto/5.PNG)

### 6. Eliminar un cliente por su cedula.
**Objetivo:**  Eliminar el cliente con número de cedula 987654321.
- **Consulta en SQL:**
```sql
DELETE FROM clientes 
WHERE cedula = 987654321;
```
![Imagen 6](Imagenes%20proyecto/6.PNG)

### 7. Consultar  los productos con unidades disponibles mayores a 10.
**Objetivo:**  Es filtrar la lista de productos para identificar aquellos con exitencias superiores a 10 unidades.
- **Consulta en SQL:**
```sql
SELECT * FROM productos 
WHERE unidades_disponibles > 10;

```
![Imagen 7](Imagenes%20proyecto/7.PNG)

### 8. Obtener ventas realizadas por un empleado especifico.
**Objetivo:**  Obtener ventas realizadas por un empleado especifico.
- **Consulta en SQL:**
```sql
SELECT * FROM ventas 
WHERE cedula_usuario = 123456789;
```
![Imagen 8](Imagenes%20proyecto/9.PNG)

### 9. Mostrar el detalle de una de una venta especifica.
**Objetivo:**  Mostrar los datalles de la venta con código de 1.
- **Consulta en SQL:**
```sql
SELECT * FROM detalle_ventas 
WHERE codigo_venta = 1;

```
![Imagen 9](Imagenes%20proyecto/9.PNG)

### 10. Calcular el total de ventas realizadas.
**Objetivo:**  Calcular el total de ventas realizadas(sumando los valores totales con iva).
- **Consulta en SQL:**
```sql
SELECT SUM(valor_total_con_iva) AS total_ventas FROM ventas;

```
![Imagen 10](Imagenes%20proyecto/10.PNG)

### 11. Que peoductos tienen mayor de 10 unidades disponibles en el inventario.
**Objetivo:** Identificar productos con bajo stock.
- **Consulta en SQL:**
```sql
SELECT codigo_producto, nombre_producto, unidades_disponibles, Max_unidades
FROM productos
WHERE unidades_disponibles > 10;

```
![Imagen 11](Imagenes%20proyecto/11.PNG)

### 12. Obtener todas las ventas realizadas por el empleado cuyo usuario es admiinicial.
**Objetivo:**  Obtener todas las ventas realizadas por el empleado cuyo usuario es adminicial.
- **Consulta en SQL:**
```sql
SELECT ventas.codigo_venta, clientes.nombre_completo AS cliente, empleados.nombre_completo AS empleado, ventas.valor_total_con_iva
FROM ventas
INNER JOIN clientes ON ventas.cedula_cliente = clientes.cedula
INNER JOIN empleados ON ventas.cedula_usuario = empleados.cedula
WHERE empleados.usuario = 'admininicial';

```
![Imagen 12](Imagenes%20proyecto/12.PNG)

### 13. Cuales son los detalles de los productos vendidos en la venta con el codigo 1.
**Objetivo:**  Obtener informacion especifica sobre los productos incluidos en una venta en particular.
- **Consulta en SQL:**
```sql
SELECT dv.codigo_detalle, p.nombre_producto, dv.cantidad, dv.valor_unitario, dv.valor_total
FROM detalle_ventas dv
INNER JOIN productos p ON dv.codigo_producto = p.codigo_producto
WHERE dv.codigo_venta = 1; 

```
![Imagen 13](Imagenes%20proyecto/13.PNG)

### 14. Obtener ventas realizadas por cada cliente.
**Objetivo:**  Obtener un la mayoria de clientes con la cantidad total de ventas realizadas incluyendo el iva.
- **Consulta en SQL:**
```sql
SELECT c.nombre_completo AS cliente, COUNT(v.codigo_venta) AS cantidad_ventas, SUM(v.valor_total_con_iva) AS total_gastado
FROM ventas v
INNER JOIN clientes c ON v.cedula_cliente = c.cedula
GROUP BY c.nombre_completo
ORDER BY total_gastado DESC;

```
![Imagen 14](Imagenes%20proyecto/14.PNG)

### 15. Cuales son los clientes que han gastado mas de 500 ordenados de mayor a menor gasto.
**Objetivo:**  El objetivo de la consulta es identificar y listar los clientes con compras mayores a 500 mostrando el monto gastado de mayor a menor.
- **Consulta en SQL:**
```sql
SELECT 
    c.nombre_completo AS cliente,
    SUM(v.valor_total_con_iva) AS total_gastado
FROM ventas v
JOIN clientes c ON v.cedula_cliente = c.cedula
GROUP BY c.nombre_completo
HAVING SUM(v.valor_total_con_iva) > 500
ORDER BY total_gastado DESC;

```
![Imagen 15](Imagenes%20proyecto/15.PNG)

### 16. Obtener el proveedor con mayor numero de productos disponibles en stock.
**Objetivo:**  Obtener el proveedor con mayor stock.
- **Consulta en SQL:**
```sql
SELECT pr.nombre_proveedor, COUNT(p.codigo_producto) AS cantidad_productos
FROM proveedores pr
INNER JOIN productos p ON pr.nit = p.nit_proveedor
GROUP BY pr.nombre_proveedor
ORDER BY cantidad_productos DESC
LIMIT 1;

```
![Imagen 17](Imagenes%20proyecto/16.PNG)
### 17. Actualizar el precio de venta de un producto basado en el precio de compra.
**Objetivo:**  Actualiza el precio de el producto segun el precio base de la compra.
- **Consulta en SQL:**
```sql
UPDATE productos
SET precio_venta = precio_compra * 1.2 -- Se puede aplicar un margen de hasta 20%
WHERE codigo_producto = 1
```
![Imagen 17](Imagenes%20proyecto/17.PNG)

### 18. Cuales son los 5 productos mas vendidos en terminos de cantidad.
**Objetivo:**  El objetivo de esta consulta es identificar los 5 productos mas populares basandose en la cantidad total de unidades vendidas y ordenados de mayor a menor.
- **Consulta en SQL:**
```sql
SELECT p.nombre_producto, SUM(dv.cantidad) AS total_vendido
FROM detalle_ventas dv
INNER JOIN productos p ON dv.codigo_producto = p.codigo_producto
GROUP BY p.nombre_producto
ORDER BY total_vendido DESC
LIMIT 5;

```
![Imagen 18](Imagenes%20proyecto/18.PNG)

### 19. Listar todos los empleados que han realizado almenos una venta.
**Objetivo:** El objetivo es listar los empleados que han realizado minimo una venta.
- **Consulta en SQL:**
```sql
SELECT e.nombre_completo, e.usuario, COUNT(v.codigo_venta) AS cantidad_ventas
FROM empleados e
INNER JOIN ventas v ON e.cedula = v.cedula_usuario
GROUP BY e.nombre_completo, e.usuario
ORDER BY cantidad_ventas DESC;

```
![Imagen 19](Imagenes%20proyecto/19.PNG)

### 20. Obtener los productos mas vendidos (TOP 5).
**Objetivo:**  Obtener los 5 productos mas vendidos en la tienda.
- **Consulta en SQL:**
```sql
SELECT 
    c.nombre_completo AS cliente,
    SUM(dv.cantidad) AS total_productos_adquiridos,
    SUM(dv.valor_total) AS total_gastado
FROM detalle_ventas dv
JOIN ventas v ON dv.codigo_venta = v.codigo_venta
JOIN clientes c ON v.cedula_cliente = c.cedula
GROUP BY c.nombre_completo
ORDER BY total_productos_adquiridos DESC;

```
![Imagen 20](Imagenes%20proyecto/20.PNG)

### Funciones y/o Rutinas
Actualiza el stock de un producto
Permite modificar las unidades disponibles de un producto.
```sql
DELIMITER $$
CREATE PROCEDURE RegistrarCliente (
    IN cedulaCliente INT,
    IN nombreCliente VARCHAR(40),
    IN direccionCliente VARCHAR(40),
    IN telefonoCliente VARCHAR(40),
    IN correoCliente VARCHAR(40)
)
BEGIN
    INSERT INTO clientes (cedula, nombre_completo, direccion, telefono, correo_electronico)
    VALUES (cedulaCliente, nombreCliente, direccionCliente, telefonoCliente, correoCliente);
END $$
DELIMITER ;
```
![Imagen1](Imagenes%20proyecto/20.PNG)
## Autores
•	Torres Mancipe Daniel Arturo 

•	Lara Uñate Juan Pablo

•	Ochoa Blanco Kevin David

•	Burgos Ortega Diego Alberto 



## Conclusiones
Este proyecto cumplió con los objetivos planteados, resolviendo el problema identificado de manera efectiva. Se diseñó un sistema bien estructurado, con una base de datos optimizada y un modelado claro que garantiza un buen manejo de la información.
Las pruebas realizadas confirmaron que el sistema funciona correctamente, cumpliendo con los requisitos técnicos. Además, se dejaron bases para futuras mejoras que permitan ampliar las capacidades del proyecto y adaptarlo a nuevas necesidades.
En resumen, el proyecto es funcional, escalable y cumple con su propósito, mostrando la importancia del trabajo en equipo y la buena planificación.


## Referencias
canadiancollege. (4 de 9 de 2024). www.canadiancollege.edu.co. Obtenido de www.canadiancollege.edu.co: https://www.canadiancollege.edu.co/blog/20-ejemplos-de-matriz-dofa-para-empresas#:~:text=La%20matriz%20DOFA%20es%20una%20herramienta%20de%20planificaci%C3%B3n%20estrat%C3%A9gica%20que,te%20dan%20una%20ventaja%20competitiva.
Kotler, P. (2001). DIRECCIÓN DE MERCADOTECNIA. En P. Kotler, DIRECCIÓN DE MERCADOTECNIA - OCTAVA EDICIÓN (pág. 84). Pearson Education.
