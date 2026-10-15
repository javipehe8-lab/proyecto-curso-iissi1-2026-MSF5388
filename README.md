# RentingUS

## Miembros del grupo

1. Pareja Buzón, José Alberto
2. Pérez Hermo, Javier
3. Rosado Alba, Hugo
4. Saldaña González, Héctor
## 1. Introducción al problema

Los jóvenes hoy en día no tenemos tiempo para decidirnos por qué coche comprar, entonces... ¿Porqué no probar uno cada año?
¡En rentingUS podrás disfrutar por una tarifa plana de un renting anual de coches, eligiendo entre más de 30 modelos distintos!
¿No tienes seguro? Nosotros nos encargamos de ello! Se te sumará a la cuota anual de forma sencilla y todos los pagos y gestiones de documentación se harán a través de la aplicación.

Los clientes son los que rentan los coches, los usuarios son los que usan la aplicación. Hay un usuario administrador y un usuario cliente. Actualmente tenemos 32 modelos distintos de vehiculos que cualquier conductor puede rentar de forma anual bienal o trienal, con su respectiva tarifa cada uno. [Tambien disponemos de la tarifa Ultimate, exclusivamente anual]. Un cliente puede tener en su tarifa hasta 3 vehículos rentados simultáneamente en su tarifa. Los clientes son responsables de las incidencias sufridas ya sean multas o accidentes, las cuales se notificarán en la aplicación.

<img width="1170" height="936" alt="IMG_0546" src="https://github.com/user-attachments/assets/503561cc-c241-4b2e-ab2e-ed4b7000d8fb" />



## 2. Glosario de términos

Admin: Usuario de la aplicación que se encarga de gestionar los datos del sistema.

Antigüedad: Clasificación de un vehículo según su edad. Puede ser antiguo, promedio o nuevo.

Carné de conducir: Permiso de conducción del cliente. Es obligatorio tenerlo para poder rentar un vehículo.

Catálogo: Conjunto de vehículos que rentingUS ofrece para rentar.

Cliente: Persona que renta vehículos a través de rentingUS. De cada cliente se guarda su DNI, nombre, apellidos (el segundo es opcional), carné de conducir y fecha de nacimiento.

Contrato: Acuerdo que firma un cliente para rentar entre uno y tres vehículos. Indica la fecha en que se firmó, la fecha en que expira, la tarifa elegida y el tipo de seguro contratado.

Daño en el vehículo: Incidencia en la que el vehículo resulta dañado, por ejemplo en un accidente. Se indica qué zona del vehículo se ha visto afectada.

Gravedad: Nivel de importancia de una incidencia. Puede ser leve, moderada o grave.

Incidencia: Suceso del que el cliente es responsable y que notifica a través de la aplicación, como una multa o un daño en el vehículo. Se registra la fecha en que ocurrió, su gravedad y una descripción.

Matrícula: Identificador oficial y único de cada vehículo.

Modelo: Marca y versión concreta de un vehículo, por ejemplo un Seat Ibiza.

Multa: Incidencia por una sanción de tráfico recibida mientras el cliente tiene el vehículo rentado.

Pieza cambiada: Registro de una pieza sustituida en un vehículo. Se guarda qué pieza fue, en qué fecha se cambió y en qué lugar.

Renting: Alquiler de un vehículo durante uno o varios años a cambio de una cuota fija, sin necesidad de comprarlo.

Sanción: Castigo económico o de puntos que conlleva una multa.

Sancionador: Organismo que impone la multa, por ejemplo un ayuntamiento.

Seguro: Cobertura del vehículo que el cliente puede contratar junto con el renting. Puede ser ninguno, básico o completo, y su precio se suma a la cuota anual.

Tarifa: Modalidad del contrato según su duración: anual, bienal o trienal. Existe además la tarifa Ultimate, que solo puede contratarse de forma anual.

Tipo de vehículo: Categoría del vehículo. Puede ser moto, coche o helicóptero.

Usuario: Persona que accede a la aplicación identificándose con su correo y contraseña. Puede ser administrador o cliente.

Vehículo: Unidad que se renta, identificada por su matrícula. De cada vehículo se guarda su modelo, su tipo y su antigüedad.

## 3. Visión general del sistema

### 3.1. Requisitos generales
RG-01 (Gestión de alquiler y contratos):

Como cliente, quiero contratar el renting anual, bienal o trienal de vehículos desde la aplicación móvil, para disfrutar de una tarifa plana de movilidad adaptada a mis necesidades sin ataduras a largo plazo.

RG-02 (Gestión del catálogo y flota):

Como administrador, quiero gestionar el catálogo global de vehículos y su disponibilidad, para mantener una oferta variada y actualizada de modelos para los usuarios.

RG-03 (Notificación y gestión de incidencias):

Como cliente, quiero notificar y consultar las incidencias (multas y daños) de mis vehículos asignados a través de la aplicación, para realizar la gestión documental y asumir las responsabilidades asociadas de forma sencilla.

RG-04 (Control de mantenimiento de vehículos):

Como administrador, quiero registrar el historial de reparaciones y piezas sustituidas en cada vehículo, para garantizar el correcto mantenimiento y la seguridad de la flota.



### 3.2. Usuarios del sistema

Usuario: cualquier entidad que se registre en el sistema de información
Cliente: persona física o entidad que haya firmado un contrato de arrendamiento para un vehículo
Administrador: persona o entidad que tenga acceso a los datos de todos los usuarios y pueda modificar el sistema de información

## 4. Catálogo de requisitos

### 4.1. Requisitos funcionales

#### R.F.01. Título requisito funcional

Como [tipo de usuario]
quiero [servicio]
para [razón]

**Prueba de aceptación**
- Descripción de la primera comprobación a realizar
- Descripción de la segunda comprobación a realizar
- Se debe aplicar la regla de negocio R.N.XX.
- ...

#### 4.1.1. Requisitos de información

R.F.01. Consultar el catálogo de vehículos
Como cliente
quiero consultar los vehículos del catálogo y filtrarlos por modelo, tipo de vehículo y antigüedad
para elegir el vehículo que quiero rentar


R.F.02. Consultar contratos
Como cliente
quiero consultar mis contratos con los vehículos que incluyen, la fecha de contrato, la fecha de expiración, la tarifa y el tipo de seguro
para saber qué vehiculos tengo rentados y hasta cuándo


R.F.03. Consultar mis incidencias
Como cliente
quiero consultar las incidencias que he registrado, con su fecha, gravedad, descripción y si son una multa o un daño en el vehículo
para tener controladas las incidencias de las que soy responsable

Como administrador
quiero obtener un listado de los contratos cuya fecha de expiración sea en los próximos 30 días
para ofrecer a esos clientes la renovación con otro vehículo


R.F.04. Listar vehículos disponibles
Como administrador
quiero obtener un listado de los vehículos del catálogo que no estén incluidos en ningún contrato vigente
para saber qué vehículos se pueden ofrecer a los clientes

Como administrador
quiero consultar las piezas cambiadas de un vehículo a partir de su matrícula
para conocer su estado y el mantenimiento que ha tenido


R.F.05. Listar incidencias por gravedad
Como administrador
quiero obtener un listado de las incidencias filtradas por gravedad, indicando el cliente responsable
para dar prioridad a las incidencias más graves

#### 4.1.2. Reglas de negocio

R.N.01 - Edad mínima:
El cliente deberá de tener al menos 18 años

R.N.02 - Renta mínima:
El cliente deberá de disponer de una renta mínima establecida en el contrato en relación al vehículo a alquilar

R.N.03 - Declarar incidencias:
El cliente estará obligado a registrar las incidencias que pueda sufrir su vehículo rentado

R.N.04 - Conductor único:
La empresa no se encargará de daños producidos en el vehículo si estos fueron causados por una persona que no esté registrada en la póliza

R.N.05 - Seguro obligatorio y tarifa dependiendo de la edad:
Si el cliente tiene menos de 25 años o menos de 2 años de carnet, no podrá contratar un seguro básico, y se le cargará un importe extra por su experiencia en la conducción



##### R.N.01. Título regla negocio

Descripción de la regla de negocio.

### 4.2. Mapa de historias de usuario (opcional)

### 4.3. Requisitos no funcionales (opcional)

**R.N.F. 01. Título requisito no funcional**
Como [tipo de usuario]
quiero [servicio]
para [razón]

-- fin entregable 1 --

## 5. Modelo conceptual

### 5.1. Diagramas de clases UML

- con restricciones.

### 5.2. Escenarios de prueba

- con descripción textual y diagrama de objetos UML.

## 6. Matrices de trazabilidad

- Matriz de trazabilidad entre los elementos del modelo conceptual y los requisitos.

|       | EntidadX   | AsociaciónX  | RestricciónX  | Entidad2 ...   | 
|:------|:-----------|:-----------|:-----------|:-----------|
| RI-1  | X          | X          | X          | X          |
| RI-2  |            | X          |            | X          |
| RF-1  |            | X          |            | X          |
| RF-2  | X          |            | X          | X          |
| RN-1  |            | X          |            |            |
| RN-2  | X          | X          | X          |            |
| ...   |            |            |            |            |

-- fin entregable 2 --

## 7. Modelo relacional en 3FN

- Relaciones obtenidas al aplicar la transformación del modelo conceptual.

### 7.1.  Justificación de la estrategia de transformación de jerarquías

- si se identificaron jerarquías en el MC.


### 8. Matriz de trazabilidad MC/SQL (opcional):

- Restricciones sobre el MC / Elementos del modelo tecnológico (SQL) (Triggers, checks, etc.)
- Incluir Reglas de negocio — Constraints/Triggers en las matrices de trazabilidad para el entregable 3

|       | EntidadX   | AsociaciónX  | RestricciónX  | Entidad2 ...   | 
|:-------|:-------|:-------|:-------|:-------|
| TABLA-1 |        |        |        |        |
| TABLA-2 |        |        |        |        |
| TABLA-3 |        |        |        |        |
| TABLA-4 |        |        |        |        |
| TRIG-1 |        |        |        |        |
| TRIG-2 | X      | X      |        | X      |
| TRIG-3 |        | X      |        | X      |
| TRIG-4 |        |        | X      |        |
| CONST-1 |        |        |        |        |
| CONST-2 | X      | X      |        | X      |
| CONST-3 |        | X      |        | X      |
| CONST-4 |        |        | X      |        |

Se consideran todo tipo de constraints declarativas (aquellas definidas durante el CREATE TABLE).
-- fin entregable 3 --

## Referencias


