<h1 align="center">Sistema de Gestión Hotelera</h1>
<h3 align="center">Realizar el diseño e implementación de una aplicación de gestión hotelera</h3>

**Relevamiento:**

* [Requerimientos](#requerimientos)
* [Diagrama de Casos de Uso](#diagrama-de-casos-de-uso)
* [Diagrama de Clases](#diagrama-de-clases)
* [Diagrama de Actividad](#diagrama-de-actividad)

Un sistema de gestión hotelera es un software creado para gestionar todas las actividades hoteleras en línea de manera fácil y segura. Este sistema le dará a la administración del hotel el poder y flexibilidad para gestionar todo el sistema desde un único portal en línea. El sistema le permite al **administrador** realizar un seguimiento de todas las habitaciones disponibles en el sistema, así como reservar habitaciones y generar facturas.

<p align="center">
    <img src="https://github.com/ET12Objetos/TrabajoPracticoIntegrador/blob/main/diagramas/sistema-de-gestion-hotelera/hotel-management-system.png" alt="Hotel Management System">
</p>

### Requerimientos

Nos centraremos en el siguiente conjunto de requerimientos al diseñar el sistema de gestión hotelera:

1. El sistema debe admitir la reserva de diferentes tipos de habitaciones, como estándar, de lujo, suite familiar, suite de negocios etc.
2. Los huéspedes deben poder buscar en el inventario de habitaciones y reservar cualquier habitación disponible.
3. El sistema debe poder recuperar información, como quién reservó una habitación en particular o qué habitaciones reservó un huesped específico.
4. El sistema debería permitir a los huespedes cancelar su reserva.
5. El sistema debe mantener un registro de limpieza de la habitación para realizar un seguimiento de todas las tareas de limpieza.
6. Cualquier huesped debe poder agregar servicios de habitación y alimentos.
7. Los huespedes pueden solicitar diferentes articulos personales (amenities).


### Diagrama de Casos de Uso

Estos son los principales **actores** en nuestro sistema:

* **Huésped:** Todos los huéspedes pueden buscar las habitaciones disponibles, así como hacer una reserva.
* **Recepcionista:** Principalmente responsable de agregar y modificar habitaciones, crear reservas de habitaciones, hacer el check-in y check-out de los huespedes.
* **Gerente:** Principalmente responsable de agregar nuevos trabajadores (personal del hotel, e.g. mucama, recepcionista etc.).
* **Mucama:** Para agregar/modificar el registro de limpieza de habitaciones.
* **Mozo:** Para agregar/modificar el registro de servicio a la habitaciones.

Estos son los principales **casos de uso** del sistema de gestión hotelera:

* **Agregar/Eliminar/Editar habitación:** La recepcionista puede agregar, eliminar o modificar una habitación en el sistema.
* **Buscar habitación:** El huesped puede buscar habitaciones por tipo y estado de disponibilidad.
* **Registrar o borrar un usuario:** Permite agregar un nuevo usuario o borrar un usuario existente del sistema.
* **Reservar habitación:** Para reservar una habitación.
* **Check-in:** Para permitir que el huésped se registre en el hotel para efectivizar su reserva.
* **Check-out:** Para realizar un seguimiento del final de la reserva y la devolución de las llaves de la habitación.
* **Agregar gasto de habitación:** Para agregar un gasto por servicio de habitación a la factura del huesped.
* **Actualizar registro de limpieza:** Para agregar o actualizar la entrada de limpieza de una habitación.

Aquí está el diagrama de casos de uso de nuestro Sistema de Gestión Hotelera:

<p align="center">
    <img src="https://github.com/ET12Objetos/TrabajoPracticoIntegrador/blob/main/diagramas/sistema-de-gestion-hotelera/usecase.drawio.svg" alt="Hotel Management System Use Case Diagram">
</p>

### Diagrama de Clases

Estas son las principales clases de nuestro Sistema de Gestión Hotelera:

* **Hotel y HotelLocation:** Nuestro sistema admitirá múltiples ubicaciones de hoteles.
* **Habitación:** Cada habitación será identificada de forma única por el número de habitación. Cada habitación tendrá atributos como tipo de habitación, precio de reserva, etc.
* **Usuario:** Tendremos diferentes tipos de usuarios en el sistema: una será de **huesped** para buscar y reservar habitaciones, otra será de **recepcionista**. El servicio de limpieza realizará un seguimiento de los registros de limpieza de una habitación y un servidor se encargará del servicio de habitaciones.
* **RoomBooking:** Esta clase será responsable de gestionar las reservas de una habitación.
* **RoomHouseKeeping:** Para realizar un seguimiento de todos los registros de limpieza de las habitaciones.
* **RoomCharge:** Resume los detalles sobre los diferentes tipos de servicios de habitación que los huéspedes han solicitado.
* **Factura:** Contiene diferentes **items de gastos** realizados por el huesped y se cargaron contra la habitación.
* **RoomKey:** A cada habitación se le puede asignar una tarjeta llave electrónica. Las llaves tendrán un código de barras y se identificarán de forma única mediante un ID de llave.

### Diagrama de Actividad

**Hacer una reserva de habitación:** Cualquier huésped o recepcionista puede realizar esta actividad. Aquí está el conjunto de pasos para reservar una habitación:

<p align="center">
    <img src="https://github.com/ET12Objetos/TrabajoPracticoIntegrador/blob/main/diagramas/sistema-de-gestion-hotelera/hms-room-booking-activity-diagram.svg" alt="Hotel Management System Room Booking">
    <br />
    Diagrama de actividad para la reserva de habitaciones del sistema de gestión hotelera
</p>

**Check in:** El huésped se registrará para su reserva. El Recepcionista también puede realizar esta actividad. Aquí están los pasos:

<p align="center">
    <img src="https://github.com/ET12Objetos/TrabajoPracticoIntegrador/blob/main/diagramas/sistema-de-gestion-hotelera/hms-check-in-activity-diagram.svg" alt="Hotel Management System Check in">
    <br />
    Diagrama de actividades para el registro del sistema de gestión hotelera
</p>

**Cancelar una reserva:** El huésped puede cancelar su reserva. Recepcionista puede realizar esta actividad. Estos son los diferentes pasos de esta actividad:

<p align="center">
    <img src="https://github.com/ET12Objetos/TrabajoPracticoIntegrador/blob/main/diagramas/sistema-de-gestion-hotelera/hms-cancel-booking-activity-diagram.svg" alt="Hotel Management System Cancel Booking">
    <br />
    Diagrama de actividades para el sistema de gestión hotelera Cancelar reserva
</p>
