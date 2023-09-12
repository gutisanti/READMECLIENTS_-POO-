## Requisitos funcionales

### R1 - Registro de cliente

| <!-- --> 	      | <!-- --> 	                                                                                                                                                                                         |
|:----------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Resumen** 	   |  El sistema debe permitir a los empleados de la concesionaria registrar nuevos clientes en la base de datos. 	                                                                                                                        |
| **Entrada** 	   | - Nombre del cliente.
-- Dirección de correo electrónico.
-- Número de teléfono.
-- Información adicional (?).                                                                                                                |
| **Resultado** 	 | 1. El sistema muestra la información del cliente correspondiente.<br>2.  Asigna un número de cliente único.<br>3.  Muestra un mensaje de confirmación de registro.  |


#### Descomposición del requisito

| Paso              | Método                       | Responsable |
|-------------------|------------------------------|-------------|
| Crear perfil del cliente | crear_perfil_cliente()    | Sistema   |
| Asignar numero de cliente unico    | asignar_numero_cliente() | Sistema     |
| Mostrar mensaje de confirmacion     | mostrar_confirmacion_registro() | Sistema     |






### R2 - Busqueda de cliente

| <!-- --> 	      | <!-- --> 	                                                                                                                                                                                         |
|:----------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Resumen** 	   |  El sistema debe permitir a los empleados buscar y acceder a la información de un cliente existente. 	                                                                                                                        |
| **Entrada** 	   | - Número de cliente o nombre del cliente.                                                                                                             |
| **Resultado** 	 | 1. El sistema muestra la información del cliente correspondiente.<br> 2. Permite la edición de la información si es necesario. |


#### Descomposición del requisito

| Paso              | Método                       | Responsable |
|-------------------|------------------------------|-------------|
| Mostrar informacion del cliente | mostrar_informacion_cliente()    | Sistema   |
| Permitir edicion de informacion     | permitir_edicion_informacion()| Sistema     |




### R3 - Actualización de Información del Cliente

| <!-- --> 	      | <!-- --> 	                                                                                                                                                                                         |
|:----------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Resumen** 	   |  El sistema debe permitir a los empleados actualizar la información de un cliente. 	                                                                                                                        |
| **Entrada** 	   | - Información actualizada (nombre, correo electrónico, teléfono, etc.).                                                                                                                |
| **Resultado** 	 | 1. El sistema actualiza la información del cliente en la base de datos.<br> 2. Muestra un mensaje de confirmación de actualización. |


#### Descomposición del requisito

| Paso              | Método                       | Responsable |
|-------------------|------------------------------|-------------|
| Actualizar informacion del cliente | actualizar_informacion_cliente()    | Sistema   |
| Mostrar mensaje de confirmacion     |mostrar_mensaje_confirmacion()| Sistema     |

## Requisitos funcionales

### R4 - Registro de Compras



| <!-- --> 	      | <!-- --> 	                                                                                                                                                                                         |
|:----------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Resumen** 	   |  El sistema debe permitir registrar las compras de vehículos realizadas por un cliente. 	                                                                                                                        |
| **Entrada** 	   | - Detalles de la compra (modelo del auto, fecha, precio, etc.).                                                                                                                |
| **Resultado** 	 | 1. El sistema registra la compra asociada al cliente.<br>2. Actualiza el historial de compras del cliente.<br>3.  Muestra un resumen de la compra. |


#### Descomposición del requisito

| Paso              | Método                       | Responsable |
|-------------------|------------------------------|-------------|
| Registrar compra | registrar_compra()    | Sistema   |
| Actualizar historial de compras   | actualizar_historial_compras() | Sistema     |
|Mostrar un resumen de la compra| mostrar_resumen_compra()|Sistema|



### R5 - Historial de Compras del Cliente

| <!-- --> 	      | <!-- --> 	                                                                                                                                                                                         |
|:----------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Resumen** 	   |  El sistema debe permitir a los empleados consultar el historial de compras de un cliente. 	                                                                                                                        |
| **Entrada** 	   | - Número de cliente o nombre del cliente                                                                                                            |
| **Resultado** 	 | 1. El sistema muestra el historial de compras del cliente, incluyendo detalles de cada compra realizada. |


#### Descomposición del requisito

| Paso              | Método                       | Responsable |
|-------------------|------------------------------|-------------|
| Mostrar historial de compras | mostrar_historial_compra()   | Sistema   |





### R6 - Gestión de Intereses y Preferencias

| <!-- --> 	      | <!-- --> 	                                                                                                                                                                                         |
|:----------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Resumen** 	   | El sistema debe permitir a los empleados registrar los intereses y preferencias de un cliente para futuras recomendaciones. 	                                                                                                                        |
| **Entrada** 	   | - Intereses y preferencias del cliente (tipo de vehículo, marca, características, etc.)                                                                                                                |
| **Resultado** 	 | 1. El sistema almacena los intereses y preferencias del cliente.<br>2. Utiliza esta información para ofrecer recomendaciones personalizadas. |


#### Descomposición del requisito

| Paso              | Método                       | Responsable |
|-------------------|------------------------------|-------------|
| Almacenar intereses y preferencias | almacenar_intereses_preferencias()  | Sistema   |
| Ofrecer recomendaciones personalizadas   | ofrecer_recomendaciones_pesonalizadas() | Sistema     |




### R7 - Eliminación de Cliente

| <!-- --> 	      | <!-- --> 	                                                                                                                                                                                         |
|:----------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Resumen** 	   |  El sistema debe permitir a los empleados eliminar un cliente de la base de datos si es necesario. 	                                                                                                                        |
| **Entrada** 	   | - Confirmación para eliminar el cliente.                                                                                                                |
| **Resultado** 	 | 1. El sistema elimina el perfil del cliente de la base de datos.<br>2. Muestra un mensaje de confirmación de eliminación. |


#### Descomposición del requisito

| Paso              | Método                       | Responsable |
|-------------------|------------------------------|-------------|
| Eliminar perfil de cliente | eliminar_perfil_cliente()    | Sistema   |
| Mostrar mensajen de confirmacion    | mostrar_mensaje_confirmacion_eliminacion() | Sistema    |