<h1 align="center">Estacionamiento</h1>
<h3 align="center">Realizar el diseño e implementación de una aplicación para un estacionamiento de varios pisos</h3>

**Relevamiento:**

* [Requerimientos](#requerimientos)
* [Diagrama de Casos de Uso](#diagrama-de-casos-de-uso)
* [Diagrama de Clases](#diagrama-de-clases)
* [Diagrama de Actividad](#diagrama-de-actividad)

Un estacionamiento es una area dedicada para estacionar vehiculos por periodos largos de tiempo. En muchos paises donde automoviles se utlizan a diario para transporte, los estacionamientos son una caracteristica de cada ciudad y area urbana. Centros comerciales, estadios, restaurantes, e industrias simiales a menudo ofrecen grades estacionamientos.

<p align="center">
    <img src="https://github.com/ET12Objetos/TrabajoPracticoIntegrador/blob/main/diagramas/estacionamiento/parking-lot.png" alt="Estacionamiento">
</p>

### Requerimientos

Nuestro cliente nos pido que demos prioridad a los siguientes requerimientos de diseño para la aplicación del estacionamiento:

1. El estacionamiento debe tener multiples plantas donde los clientes pueden estacionar sus vehiculos.
2. El estacionamiento debe tener multiplies puntos de entradas y salidas.
3. Los clientes reciben un ticket de estacionamiento en los puntos de entrada y pueden pagar la tarifa de estacionamiento en los puntos de salida al salir.
4. Los clientes pueden pagar los tickets en un **dispositivo de pago** a la salida o al **asistente de estacionamiento**.
5. Los clientes pueden pagar mediante el uso de efectivo y tarjetas de credito.
6. Los clientes también deberan poder pagar la **tarifa de estacionamiento** en el **portal de información** del cliente en cada piso. Si el cliente ha pagado en el **portal de información**, no tiene que pagar a la salida.
7. El sistema no debe permitir más vehículos que la capacidad máxima del estacionamiento. Si el estacionamiento está lleno, el sistema debería poder mostrar un mensaje en el cartel de la calle y en el **panel de visualización** del estacionamiento en la planta baja.
8. Cada piso de estacionamiento tendrá muchos lugares de estacionamiento. El sistema debe admitir varios tipos de lugares de estacionamiento, como automoviles compactos, grande, para discapacitados, para motocicletas, etc.
9. El estacionamiento debe tener algunos lugares de estacionamiento especificaos para autos eléctricos. Estos puntos deberán contar con un tablero eléctrico a través del cual los clientes puedan pagar y cargar sus vehículos.
10. El sistema debe admitir estacionamiento para diferentes tipos de vehículos como automóviles, camiones, camionetas, motocicletas, etc.
11. Cada piso de estacionamiento debe tener un tablero que muestre cualquier lugar de estacionamiento libre para cada tipo de lugar.
12. El sistema debe admitir un modelo de tarifa de estacionamiento por hora. Por ejemplo, los clientes tienen que pagar $400 por la primera hora, $350 por la segunda y tercera hora y $250 por todas las horas restantes.


### Diagrama de casos de uso

Estos son los principales Actores en nuestro sistema:

* **Administrador:** Principalmente responsable de agregar y modificar pisos de estacionamiento, lugares de estacionamiento, paneles de entrada y salida, agregar/eliminar asistentes de estacionamiento, etc.
* **Cliente:** Todos los clientes pueden obtener una multa de estacionamiento y pagarla.
* **Asistente de estacionamiento:** Los asistentes de estacionamiento pueden realizar todas las actividades en nombre del cliente y pueden tomar efectivo para el pago del ticket.
* **Sistema:** Para mostrar mensajes en diferentes paneles de información, así como asignar y quitar un vehículo de un lugar de estacionamiento.

Estos son los principales casos de uso del estacionamiento:

* **Agregar/Eliminar/Editar piso de estacionamiento:** Para agregar, eliminar o modificar un piso de estacionamiento del sistema. Cada piso puede tener su propio tablero de anuncios para mostrar los lugares de estacionamiento disponibles.
* **Agregar/Eliminar/Editar lugar de estacionamiento:** Para agregar, eliminar o modificar un lugar de estacionamiento en un piso de estacionamiento.
* **Agregar/Eliminar un asistente de estacionamiento:** Para agregar o eliminar un asistente de estacionamiento del sistema.
* **Emitir ticket:** Para proporcionar a los clientes un nuevo ticket de estacionamiento al ingresar al estacionamiento.
* **Escanear ticket:** Para escanear un ticket y averiguar el cargo total.
* **Pago con tarjeta de crédito:** Para pagar la tarifa del ticket con tarjeta de crédito.
* **Pago en efectivo:** Para pagar el ticket de aparcamiento en efectivo.
* **Agregar/Modificar tarifa de estacionamiento:** Para permitir que el administrador agregue o modifique la tarifa de estacionamiento por hora.

Aquí está el diagrama de caso de uso de nuestro estacionamiento:

<p align="center">
    <img src="https://github.com/ET12Objetos/TrabajoPracticoIntegrador/blob/main/diagramas/estacionamiento/parking-use-case-diagram.svg" alt="Parking Lot Use Case Diagram">
</p>

### Diagrama de Clases

Estas son las principales clases de nuestro sistema de estacionamiento:

* **Estacionamiento:** La parte central de la organización para la que se ha diseñado este software. Tiene atributos como 'Nombre' para distinguirlo de cualquier otro estacionamiento y 'Dirección' para definir su ubicación.
* **PisoEstacionamiento:** El estacionamiento tendrá muchos pisos de estacionamiento.
* **LugarEstacionamiento:** Cada piso de estacionamiento tendrá muchos lugares de estacionamiento. Nuestro sistema admitirá diferentes lugares de estacionamiento 1) Discapacitados, 2) Compacto, 3) Grande, 4) Motocicleta y 5) Eléctrico.
* **Cuenta:** Tendremos dos tipos de cuentas en el sistema: una para un administrador y otra para un asistente de estacionamiento.
* **TicketEstacionamiento:** Esta clase encapsulará un ticket de estacionamiento. Los clientes tomarán un ticket cuando ingresen al estacionamiento.
* **Vehículo:** Los vehículos se estacionarán en los lugares de estacionamiento. Nuestro sistema admitirá diferentes tipos de vehículos 1) Automóvil, 2) Camión, 3) Eléctrico, 4) Camioneta y 5) Motocicleta.
* **PanelEntrada y PanelSalida:** PanelEntrada imprimirá los tickets y PanelSalida facilitará el pago de la tarifa del ticket.
* **Pago:** Esta clase será responsable de realizar los pagos. El sistema admitirá transacciones con tarjeta de crédito y en efectivo.
* **Tarifa:** Esta clase hará un seguimiento de las tarifas de estacionamiento por hora. Se especificará un monto por cada hora. Por ejemplo, para una multa de estacionamiento de dos horas, esta clase definirá el costo de la primera y la segunda hora.
* **PanelEstacionamiento:** Cada piso de estacionamiento tendrá un panel de visualización para mostrar los lugares de estacionamiento disponibles para cada tipo de lugar. Esta clase será responsable de mostrar la última disponibilidad de plazas de aparcamiento disponibles a los clientes.
* **PortalAsistenteEstacionamiento:** esta clase encapsulará todas las operaciones que un asistente puede realizar, como escanear tickets y procesar pagos.
* **PortalInformacionCliente:** Esta clase encapsulará el portal de información que los clientes usan para pagar la multa de estacionamiento. Una vez pagado, el portal de información actualizará el ticket para realizar un seguimiento del pago.
* **PanelElectrico:** Los clientes utilizarán los paneles eléctricos para pagar y cargar sus vehículos eléctricos.

### Diagrama de Actividad

**Cliente pagando ticket de parking:** Cualquier cliente puede realizar esta actividad. Aquí está el conjunto de pasos:

<p align="center">
    <img src="https://github.com/ET12Objetos/TrabajoPracticoIntegrador/blob/main/diagramas/estacionamiento/parking-ticket.svg" alt="Parking Ticket Activity Diagram">
</p>