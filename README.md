# RentingUS

## Miembros del grupo

1. Pareja Buzón, José Alberto
2. Pérez Hermo, Javier
3. Rosado Alba, Hugo
4. Saldaña González, Héctor
## 1. Introducción al problema

Los jóvenes de hoy en día no tenemos tiempo para decidirnos por qué coche comprar ni queremos ataduras a largo plazo. Entonces... ¿Por qué no probar uno cada año?

En RentingUS podrás disfrutar, mediante una tarifa plana, de un renting anual de coches, eligiendo entre más de 30 modelos distintos. Nuestra aplicación permite gestionar todo el ciclo de vida del arrendamiento: desde la visualización del catálogo y contratación, hasta la gestión de documentación y seguros obligatorios, que se suman a la cuota anual de forma sencilla.

Actualmente disponemos de un catálogo con 32 modelos de vehículos que cualquier conductor puede rentar en modalidad anual, bienal o trienal, cada una con su tarifa correspondiente, incluyendo una modalidad de tarifa Ultimate de exclusividad anual. Los clientes gestionan todos los pagos por la aplicación y son responsables de las incidencias (multas o accidentes), las cuales deben ser registradas directamente en el sistema.


## 2. Glosario de términos

Incidencia: Evento negativo (clasificado estrictamente como multa o daño) que sufre un vehículo de la flota durante la vigencia de un contrato, y del cual el cliente titular debe hacerse responsable económicamente.

Renting: Alquiler de un vehículo de nuestra flota durante uno o varios años a cambio de una cuota fija, sin transferencia de la propiedad del mismo al cliente.

Tarifa Ultimate: Modalidad de renting premium y de disponibilidad exclusiva para contratos de periodicidad anual.

## 3. Visión general del sistema

### 3.1. Requisitos generales
RG-01 (Gestión de contratos):

Como cliente, quiero contratar el renting anual, bienal o trienal de vehículos desde la aplicación móvil, para disfrutar de una tarifa plana de movilidad adaptada a mis necesidades sin ataduras a largo plazo.

RG-02 (gestión de incidencias):

Como cliente, quiero notificar y consultar las incidencias (multas y daños) de mis vehículos asignados a través de la aplicación, para realizar la gestión documental y asumir las responsabilidades asociadas de forma sencilla.

RG-03 (Control de mantenimiento de vehículos):

Como administrador, quiero registrar el historial de reparaciones y piezas sustituidas en cada vehículo, para garantizar el correcto mantenimiento y la seguridad de la flota.

RG-04 (Gestión de cliente):
Como administrador, quiero gestionar los perfiles de los usuarios que se registran, para validar su viabilidad económica y legal.


### 3.2. Usuarios del sistema

Usuario: cualquier entidad que se registre en el sistema de información

Cliente: Persona física que se registra en el sistema, aporta sus datos económicos (renta) y de conducción, y formaliza contratos de arrendamiento de vehículos.

Administrador: Persona empleada por RentingUS con acceso privilegiado al sistema para gestionar el catálogo de vehículos, revisar mantenimientos, controlar el estado de los contratos e incidencias globales.

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

4.1.1 Entidad: CLIENTE
R.I.01 Información del Cliente: El sistema deberá almacenar los datos de los clientes. Los atributos a guardar serán: DNI, Nombre, Apellidos, Renta Mensual (en euros), Fecha de nacimiento, Fecha de expedición del carnet de conducir, Usuario y Contraseña.

R.F.01.01. Consultar mi perfil. Como cliente quiero consultar mis datos personales introducidos para verificar que mi información (como la renta aportada) está correcta.

Prueba de aceptación 1: Entrar al apartado perfil y comprobar que el DNI mostrado coincide con el registrado. (SÍ/NO)

Prueba de aceptación 2: Intentar modificar la Renta Mensual sin estar logueado y recibir error de autenticación. (SÍ/NO)

R.F.01.02. Listar clientes (Admin). Como administrador quiero obtener un listado de todos los clientes registrados para tener control sobre la base de usuarios.

Prueba de aceptación 1: Ejecutar la consulta como Admin y verificar que la lista devuelve al menos los nombres y DNI. (SÍ/NO)

R.F.01.03. Listar clientes menores de 25 años. Como administrador quiero filtrar a los clientes por edad para identificar los perfiles con seguro limitado.

Prueba de aceptación 1: Filtrar la lista y verificar que ningún cliente mostrado tiene una fecha de nacimiento anterior al año en curso menos 25. (SÍ/NO)

R.F.01.04. Iniciar sesión. Como cliente quiero introducir mis credenciales para acceder a la aplicación.

Prueba de aceptación 1: Introducir usuario y contraseña correctos y acceder a la portada. (SÍ/NO)

4.1.2 Entidad: VEHÍCULO
R.I.02 Información de Vehículos: El sistema deberá almacenar los datos de la flota. Atributos: Matrícula, Modelo, Tipo de vehículo, Fecha de matriculación, Tarifa asignada (Anual/Bienal/Trienal/Ultimate), y listado de piezas cambiadas. (Nota: La "antigüedad" será una propiedad derivada de la Fecha de matriculación, no se guardará el número estático).

R.F.02.01. Consultar el catálogo de vehículos. Como cliente quiero listar los vehículos disponibles para elegir el que quiero rentar.

Prueba de aceptación 1: Pulsar en catálogo y visualizar los 32 modelos con sus matrículas. (SÍ/NO)

R.F.02.02. Filtrar catálogo por tarifa. Como cliente quiero filtrar los vehículos por su tarifa (ej. Ultimate) para ver cuáles puedo permitirme.

Prueba de aceptación 1: Seleccionar filtro "Ultimate" y comprobar que solo se muestran vehículos con esa etiqueta. (SÍ/NO)

R.F.02.03. Listar historial de reparaciones. Como administrador quiero consultar las piezas cambiadas de una matrícula concreta para llevar el control de mantenimiento.

Prueba de aceptación 1: Introducir una matrícula existente y ver la lista de piezas sustituidas. (SÍ/NO)

R.F.02.04. Listar vehículos por antigüedad. Como administrador quiero listar los vehículos ordenados por su antigüedad (derivada de la fecha de matriculación) para saber cuáles retirar de la flota.

Prueba de aceptación 1: Comprobar que los coches matriculados en 2020 aparecen antes que los de 2024. (SÍ/NO)

4.1.3 Entidad: CONTRATO (Entidad asociativa Cliente-Vehículo)
R.I.03 Información de los Contratos: El sistema almacenará los contratos que conectan un Cliente y un Vehículo. Atributos: ID Contrato, DNI Cliente (Clave foránea), Matrícula (Clave foránea), Fecha de Inicio, Fecha de Expiración, Tipo de Seguro contratado, Cuota final asignada.

R.F.03.01. Consultar mis contratos. Como cliente quiero listar mis contratos vigentes para saber hasta cuándo tengo rentados mis vehículos actuales.

Prueba de aceptación 1: Entrar en "Mis Contratos" y comprobar que figuran las matrículas de los coches rentados. (SÍ/NO)

R.F.03.02. Listar contratos a expirar en 30 días. Como administrador quiero listar los contratos cuya Fecha de Expiración sea en los próximos 30 días para ofrecer renovaciones.

Prueba de aceptación 1: Comprobar que en la lista resultante no aparece ningún contrato cuya fecha de expiración sea superior a 31 días vista. (SÍ/NO)

R.F.03.03. Listar historial de contratos finalizados. Como cliente quiero consultar los contratos cuya Fecha de Expiración ya pasó para tener un histórico de mis rentings.

Prueba de aceptación 1: Filtrar por "Histórico" y ver solo contratos con fecha final anterior a la de hoy. (SÍ/NO)

R.F.03.04. Listar contratos por tipo de seguro. Como administrador quiero filtrar los contratos activos según su seguro (básico/premium) para análisis de riesgos.

Prueba de aceptación 1: Filtrar por "Seguro Básico" y verificar que la lista no incluye contratos premium. (SÍ/NO)

4.1.4 Entidad: INCIDENCIA
R.I.04 Información de Incidencias: El sistema almacenará los partes de daños y multas. Estos se asocian al Contrato (no al cliente suelto). Atributos: ID Incidencia, ID Contrato asociado (Clave Foránea), Fecha del suceso, Tipo (Multa / Daño), Gravedad, Descripción.

R.F.04.01. Consultar mis incidencias registradas. Como cliente quiero ver las incidencias conectadas a mis contratos para tener controladas mis responsabilidades.

Prueba de aceptación 1: Ingresar en incidencias y ver si coincide el ID Contrato con alguno de los míos. (SÍ/NO)

R.F.04.02. Listar incidencias por gravedad. Como administrador quiero listar las incidencias filtradas por gravedad para dar prioridad a los accidentes graves.

Prueba de aceptación 1: Seleccionar "Gravedad Alta" y verificar que las incidencias mostradas corresponden a ese filtro. (SÍ/NO)

R.F.04.03. Consultar incidencias de un coche. Como administrador quiero listar todas las incidencias introduciendo la matrícula de un coche (buscando a través de sus contratos).

Prueba de aceptación 1: Introducir una matrícula y ver el historial de incidencias que sufrieron los distintos contratos de ese vehículo. (SÍ/NO)

R.F.04.04. Listar multas. Como administrador quiero separar las incidencias que sean exclusivamente de Tipo "Multa" para agilizar los trámites burocráticos.

Prueba de aceptación 1: Filtrar por tipo "Multa" y verificar que no aparece ningún registro de "Daño" físico en la chapa. (SÍ/NO)

#### 4.1.2. Reglas de negocio

R.N.01 - Límite de vehículos simultáneos: Un cliente solo podrá tener un máximo de 3 contratos vigentes (fecha de expiración superior a hoy) simultáneamente.

R.N.02 - Contrato con cláusula de renta mínima: Se impedirá formalizar un contrato en la base de datos si el campo Renta Mensual del Cliente es inferior a la cuota establecida para la tarifa de ese vehículo.

R.N.03 - Incidencias en contratos vigentes: No se puede levantar ni registrar una incidencia asociándola a un ID Contrato cuya Fecha de expiración sea anterior a la fecha del suceso. (La incidencia va sobre contrato conectado y vigente).

R.N.04 - Seguro obligatorio por edad/experiencia: Si la edad calculada del cliente es menor a 25 años, o la diferencia entre la fecha actual y la Fecha de expedición del carnet es menor a 2 años, el sistema no permitirá asociar el "Seguro Básico" al contrato.

R.N.05 - Antigüedad derivada: El sistema nunca almacenará un número fijo para los años del vehículo. La antigüedad debe ser extraída dinámicamente restando la Fecha de matriculación a la fecha actual del servidor.

Pruebas de aceptación de reglas de negocio:

Prueba R.N.03: Intentar insertar en la tabla Incidencia un parte de accidente asociándolo a un ID Contrato que terminó hace dos meses.

Comprobación: El sistema de base de datos (Trigger) debe abortar la operación y lanzar un error indicando que el contrato ha expirado. (SÍ/NO)

Prueba R.N.01: Un cliente con 3 contratos vigentes intenta firmar el cuarto mediante la App.

Comprobación: El sistema bloquea la transacción y muestra el mensaje de límite alcanzado. (SÍ/NO)


##### R.N.01. Título regla negocio

Descripción de la regla de negocio.

### 4.2. Mapa de historias de usuario (opcional)

### 4.3. Requisitos no funcionales (opcional)

**R.N.F. 01. Título requisito no funcional**
Como [tipo de usuario]
quiero [servicio]
para [razón]

R.N.F. 01. Rendimiento del catálogo: Como usuario, quiero que la lista de catálogo de vehículos cargue desde la base de datos en menos de 3 segundos, para tener una experiencia fluida al buscar coche.

Comprobación: Medir el tiempo de respuesta del servidor al hacer SELECT de la tabla Vehículos. (SÍ/NO).

R.N.F. 02. Disponibilidad del gestor de incidencias: Como cliente, quiero que el módulo para subir incidencias esté disponible el 99% del tiempo, para no incurrir en demoras legales tras un accidente o multa de tráfico.




-- fin entregable 1 --

## 5. Modelo conceptual

<img width="1170" height="936" alt="IMG_0546" src="https://github.com/user-attachments/assets/503561cc-c241-4b2e-ab2e-ed4b7000d8fb" />

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


