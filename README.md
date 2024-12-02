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
```
![Imagen 1](Imagenes%20proyecto/1.PNG)
  

### 2. Obtenga el nombre completo y correo electronico de los clientes.
**Objetivo:**  Conseguir el nombre del cliente con su respectivo correo electronico.


 **Consulta en SQL:**
  ```sql
```
![Imagen 2](Imagenes%20proyecto/2.PNG)

### 3. Listar los proveedores ubicados en una ciudad especifica.
**Objetivo:**  Conseguir los proveedores ubicados en Bogotá.
**Consulta en SQL:**
  ```sql
```
![Imagen 3](Imagenes%20proyecto/3.PNG)

### 4.Cuales son los productos disponibles, sus precios de ventas y cuantas unidades estan en stock.
**Objetivo:**  Obtener un listado con informacion clave sobre los prodcutos.
```sql
```
![Imagen 4](Imagenes%20proyecto/4.PNG)

### 5. Actualizar el precio de venta de un producto especifico.
**Objetivo:**  Actualizar el precio del producto con código 101.
```sql
```
![Imagen 5](Imagenes%20proyecto/5.PNG)

### 6. Eliminar un cliente por su cedula.
**Objetivo:**  Eliminar el cliente con número de cedula 987654321.
```sql
```
![Imagen 6](Imagenes%20proyecto/6.PNG)

### 7. Consultar  los productos con unidades disponibles mayores a 10.
**Objetivo:**  Es filtrar la lista de productos para identificar aquellos con exitencias superiores a 10 unidades.
```sql
```
![Imagen 7](Imagenes%20proyecto/7.PNG)

### 8. Obtener ventas realizadas por un empleado especifico.
**Objetivo:**  Obtener ventas realizadas por un empleado especifico.
```sql
```
![Imagen 8](Imagenes%20proyecto/9.PNG)

### 9. Mostrar el detalle de una de una venta especifica.
**Objetivo:**  Mostrar los datalles de la venta con código de 1.
```sql
```
![Imagen 9](Imagenes%20proyecto/9.PNG)

### 10. Calcular el total de ventas realizadas.
**Objetivo:**  Calcular el total de ventas realizadas(sumando los valores totales con iva).
```sql
```
![Imagen 10](Imagenes%20proyecto/10.PNG)

### 11. Que peoductos tienen mayor de 10 unidades disponibles en el inventario.
**Objetivo:** Identificar productos con bajo stock.
```sql
```
![Imagen 11](Imagenes%20proyecto/11.PNG)

### 12. Obtener todas las ventas realizadas por el empleado cuyo usuario es admiinicial.
**Objetivo:**  Obtener todas las ventas realizadas por el empleado cuyo usuario es admiinicial.
```sql
```
![Imagen 12](Imagenes%20proyecto/12.PNG)

### 13. Cuales son los detalles de los productos vendidos en la venta con el codigo 1.
**Objetivo:**  Obtener informacion especifica sobre los productos incluidos en una venta en particular.
```sql
```
![Imagen 13](Imagenes%20proyecto/13.PNG)

### 14. Obtener ventas realizadas por cada cliente.
**Objetivo:**  Obtener un la mayoria de clientes con la cantidad total de ventas realizadas incluyendo el iva.
```sql
```
![Imagen 14](Imagenes%20proyecto/14.PNG)

### 15. Cuales son los clientes que han gastado mas de 500 ordenados de mayor a menor gasto.
**Objetivo:**  El objetivo de la consulta es identificar y listar los clientes con compras mayores a 500 mostrando el monto gastado de mayor a menor.
```sql
```
![Imagen 15](Imagenes%20proyecto/15.PNG)

### 16. Obtener el proveedor con mayor numero de productos disponibles en stock.
**Objetivo:**  Obtener el proveedor con mayor stock.
```sql
```
![Imagen 16(Imagenes%20proyecto/16.PNG)

### 17. Actualizar el precio de venta de un producto basado en el precio de compra.
**Objetivo:**  Actualiza el precio de el producto segun el precio base de la compra.
```sql
```
![Imagen 17](Imagenes%20proyecto/17.PNG)

### 18. Cuales son los 5 productos mas vendidos en terminos de cantidad.
**Objetivo:**  El objetivo de esta consulta es identificar los 5 productos mas populares basandose en la cantidad total de unidades vendidas y ordenados de mayor a menor.
```sql
```
![Imagen 18](Imagenes%20proyecto/18.PNG)

### 19. Listar todos los empleados que han realizado almenos una venta.
**Objetivo:** El objetivo es listar los empleados que han realizado minimo una venta.
```sql
```
![Imagen 19](Imagenes%20proyecto/19.PNG)

### 20. Obtener los productos mas vendidos (TOP 5).
**Objetivo:**  Obtener los 5 productos mas vendidos en la tienda.
```sql
```
![Imagen 20](Imagenes%20proyecto/20.PNG)

### Funciones y/o Rutinas

## Futuras Mejoras

## Autores
Torres Mancipe Daniel Arturo 
Lara Uñate Juan Pablo
Ochoa Blanco Kevin David
Burgos Ortega Diego Alberto 


Nombres de los participantes del proyecto con una breve descripción de su rol y enlaces de sus Github o páginas web.

## Conclusiones

## Referencias
