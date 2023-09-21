## Requisitos funcionales

### R1 - Registro de cliente

| <!-- --> 	      | <!-- --> 	                                                                                                                                                                                         |
|:----------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Resumen** 	   |  El sistema debe permitir a los empleados de la concesionaria registrar nuevos clientes en la base de datos. 	                                                                                                                        |
| **Entrada** 	   | - Nombre del cliente. - Dirección de correo electrónico. - Número de teléfono. - Información adicional (?).                                                                                                                |
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
////////////////////////////////////////
class Cliente:
    def __init__(self, nombre, correo, telefono, info_adicional=None):
        self.nombre = nombre
        self.correo = correo
        self.telefono = telefono
        self.info_adicional = info_adicional
        self.numero_cliente = None

    def asignar_numero_cliente(self, numero_cliente):
        self.numero_cliente = numero_cliente

    def mostrar_informacion(self):
        return f"Cliente {self.numero_cliente}: Nombre - {self.nombre}, Correo - {self.correo}, Teléfono - {self.telefono}, Info Adicional - {self.info_adicional}"

    def actualizar_informacion(self, nombre=None, correo=None, telefono=None, info_adicional=None):
        if nombre:
            self.nombre = nombre
        if correo:
            self.correo = correo
        if telefono:
            self.telefono = telefono
        if info_adicional is not None:
            self.info_adicional = info_adicional

class Compra:
    def __init__(self, cliente, detalles_compra):
        self.cliente = cliente
        self.detalles_compra = detalles_compra

class Concesionaria:
    def __init__(self):
        self.clientes = []
        self.numero_cliente_actual = 1
        self.compras = []

    def registrar_cliente(self, nombre, correo, telefono, info_adicional=None):
        cliente = Cliente(nombre, correo, telefono, info_adicional)
        cliente.asignar_numero_cliente(self.numero_cliente_actual)
        self.numero_cliente_actual += 1
        self.clientes.append(cliente)
        return f"Cliente {cliente.numero_cliente} registrado con éxito."

    def buscar_cliente(self, numero_cliente=None, nombre_cliente=None):
        if numero_cliente:
            for cliente in self.clientes:
                if cliente.numero_cliente == numero_cliente:
                    return cliente
        elif nombre_cliente:
            for cliente in self.clientes:
                if cliente.nombre == nombre_cliente:
                    return cliente
        return None

    def actualizar_informacion_cliente(self, numero_cliente, nombre=None, correo=None, telefono=None, info_adicional=None):
        cliente = self.buscar_cliente(numero_cliente=numero_cliente)
        if cliente:
            cliente.actualizar_informacion(nombre, correo, telefono, info_adicional)
            return f"Información de cliente {cliente.numero_cliente} actualizada con éxito."
        else:
            return "Cliente no encontrado."

    def registrar_compra(self, cliente, detalles_compra):
        compra = Compra(cliente, detalles_compra)
        self.compras.append(compra)
        return "Compra registrada con éxito."

    def historial_compras_cliente(self, numero_cliente, nombre_cliente=None):
        cliente = self.buscar_cliente(numero_cliente=numero_cliente, nombre_cliente=nombre_cliente)
        if cliente:
            historial = [compra.detalles_compra for compra in self.compras if compra.cliente == cliente]
            return historial
        else:
            return "Cliente no encontrado."

    def gestion_intereses_preferencias(self, numero_cliente, intereses_preferencias):
        cliente = self.buscar_cliente(numero_cliente=numero_cliente)
        if cliente:
            # Aquí puedes implementar la lógica para gestionar intereses y preferencias del cliente.
            return f"Intereses y preferencias de cliente {cliente.numero_cliente} actualizados con éxito."
        else:
            return "Cliente no encontrado."

    def eliminar_cliente(self, numero_cliente, confirmacion_eliminacion):
        cliente = self.buscar_cliente(numero_cliente=numero_cliente)
        if cliente:
            if confirmacion_eliminacion:
                self.clientes.remove(cliente)
                return f"Cliente {cliente.numero_cliente} eliminado de la base de datos."
            else:
                return "Confirmación de eliminación requerida."
        else:
            return "Cliente no encontrado."

    def enviar_notificacion(self, tipo_notificacion, mensaje, destinatarios):
        # Aquí puedes implementar la lógica para enviar notificaciones a los clientes.
        return "Notificación enviada con éxito."

# Ejemplo de uso
concesionaria = Concesionaria()
print(concesionaria.registrar_cliente("Juan", "juan@example.com", "123-456-7890"))
print(concesionaria.buscar_cliente(numero_cliente=1).mostrar_informacion())
print(concesionaria.actualizar_informacion_cliente(1, nombre="Juan Pérez"))
print(concesionaria.buscar_cliente(numero_cliente=1).mostrar_informacion())
print(concesionaria.registrar_compra(concesionaria.buscar_cliente(numero_cliente=1), "Modelo: Sedán, Precio: $20,000"))
print(concesionaria.historial_compras_cliente(numero_cliente=1))
print(concesionaria.gestion_intereses_preferencias(1, "SUV, Marca: Toyota"))
print(concesionaria.eliminar_cliente(1, confirmacion_eliminacion=True))
