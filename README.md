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

tokenAdministrador: Es un token de acceso que se les solicita a los administradores para verificar su condición de administrador.

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

RG-05 (Inicio de sesión de usuarios):

Como usuario, quiero poder acceder con mis credenciales a mi información relacionada con RentingUS, para comprobar el estado del contrato y incidencias registradas.


### 3.2. Usuarios del sistema

Cliente.
Administrador.

## 4. Catálogo de requisitos

### 4.1. Requisitos de información y requisitos funcionales

#### 4.1.1. Entidad: Cliente

**R.I.01. Información de los clientes.** El sistema deberá almacenar la información de los clientes. De cada cliente se guardarán su DNI, su nombre, su primer apellido, su segundo apellido y su fecha de nacimiento. La edad del cliente no se almacenará, sino que se calculará a partir de su fecha de nacimiento.

**R.F.01.01. Consultar mi perfil.** Como cliente, quiero consultar los datos personales que tengo registrados, para comprobar que son correctos.

Prueba de aceptación:
Un cliente que ha iniciado sesión accede a su perfil y comprueba que el DNI mostrado coincide con el que facilitó al registrarse.
Si se intenta acceder al perfil sin haber iniciado sesión, el sistema deniega el acceso.

**R.F.01.02. Listar clientes.** Como administrador, quiero obtener un listado de todos los clientes registrados, para tener control sobre la base de clientes.

Prueba de aceptación:
Un administrador solicita el listado y comprueba que aparecen, al menos, el nombre, los apellidos y el DNI de cada cliente.

**R.F.01.03. Listar clientes menores de 25 años.** Como administrador, quiero filtrar a los clientes por edad, para identificar a aquellos que tienen limitado el tipo de seguro que pueden contratar.

Prueba de aceptación:
Un administrador aplica el filtro y comprueba que ninguno de los clientes mostrados tiene 25 años o más, calculando su edad a partir de su fecha de nacimiento.

**R.F.01.04. Registrarse como cliente.** Como cliente, quiero registrarme en la aplicación facilitando mis datos personales, para poder formalizar contratos de renting.

Prueba de aceptación:
Una persona mayor de edad introduce todos sus datos correctamente y el sistema crea su perfil de cliente.
Una persona menor de 18 años intenta registrarse y el sistema rechaza el registro.
Se debe aplicar la regla de negocio R.N.03.

#### 4.1.2. Entidad: Vehículo

**R.I.02. Información de los vehículos.** El sistema deberá almacenar la información de los vehículos de la flota. De cada vehículo se guardarán su matrícula, su modelo, su color y su tipo, que podrá ser coche, moto u otro.

**R.F.02.01. Consultar el catálogo de vehículos.** Como cliente, quiero consultar los vehículos disponibles, para elegir el que deseo contratar.

Prueba de aceptación:
Un cliente accede al catálogo y comprueba que se muestran el modelo, el color y la matrícula de cada vehículo.
Un vehículo que tiene un contrato vigente no aparece como disponible.

**R.F.02.02. Filtrar el catálogo por tipo de vehículo.** Como cliente, quiero filtrar el catálogo por tipo de vehículo, para encontrar con mayor rapidez el que se ajusta a lo que busco.

Prueba de aceptación:
Un cliente selecciona el tipo «moto» y comprueba que únicamente se muestran vehículos de ese tipo.

**R.F.02.03. Dar de alta un vehículo.** Como administrador, quiero registrar un nuevo vehículo en la flota, para incorporarlo al catálogo.

Prueba de aceptación:
Un administrador introduce la matrícula, el modelo, el color y el tipo de un vehículo nuevo y comprueba que este aparece en el catálogo.

**R.F.02.04. Consultar el historial de contratos de un vehículo.** Como administrador, quiero consultar todos los contratos que ha tenido un vehículo, para conocer su historial de uso.

Prueba de aceptación:
Un administrador introduce una matrícula existente y comprueba que se muestran todos los contratos, vigentes y finalizados, asociados a ese vehículo.

#### 4.1.3. Entidad: Contrato

**R.I.03. Información de los contratos.** El sistema deberá almacenar los contratos de renting que un cliente formaliza sobre un vehículo. De cada contrato se guardarán su fecha de contrato, su fecha de expiración, su tipo (anual, bienal o trienal), su cuota y el tipo de seguro contratado (ninguno, básico o completo). Cada contrato corresponde a un único cliente y a un único vehículo.

**R.F.03.01. Formalizar un contrato.** Como cliente, quiero contratar el renting de un vehículo eligiendo el tipo de contrato y de seguro, para disponer del vehículo durante el periodo acordado.

Prueba de aceptación:
Un cliente selecciona un vehículo disponible, un tipo de contrato y un tipo de seguro, y el sistema registra el contrato con sus fechas y su cuota.
Si el vehículo ya tiene un contrato cuyo periodo se solapa con el nuevo, el sistema rechaza la operación.
Si el cliente tiene menos de 25 años y elige el seguro básico, el sistema rechaza la operación.
Si el cliente ya tiene tres contratos vigentes, el sistema rechaza la operación.
Si el cliente se encuentra bloqueado por acumulación de incidencias, el sistema rechaza la operación.
Se deben aplicar las reglas de negocio R.N.01, R.N.02, R.N.04 y R.N.05.

**R.F.03.02. Consultar mis contratos.** Como cliente, quiero consultar mis contratos vigentes y mi historial de contratos finalizados, para saber hasta cuándo dispongo de cada vehículo y qué rentings he tenido.

Prueba de aceptación:
Un cliente accede a sus contratos vigentes y comprueba que solo aparecen contratos cuya fecha de expiración es posterior a la fecha actual.
Un cliente accede a su historial y comprueba que solo aparecen contratos cuya fecha de expiración ya ha pasado.

**R.F.03.03. Listar contratos próximos a expirar.** Como administrador, quiero listar los contratos cuya fecha de expiración se encuentre dentro de los próximos 30 días, para ofrecer su renovación a los clientes.

Prueba de aceptación:
Un administrador solicita el listado y comprueba que no aparece ningún contrato que expire dentro de más de 30 días ni ninguno que ya haya expirado.

**R.F.03.04. Listar contratos por tipo de seguro.** Como administrador, quiero filtrar los contratos vigentes según el tipo de seguro contratado, para analizar los riesgos asumidos por la empresa.

Prueba de aceptación:
Un administrador filtra por seguro básico y comprueba que no aparece ningún contrato con otro tipo de seguro.

#### 4.1.4. Entidad: Incidencia

**R.I.04. Información de las incidencias.** El sistema deberá almacenar las incidencias que se producen durante los contratos. De cada incidencia se guardarán su fecha, su gravedad (leve, moderada o alta) y una descripción de lo sucedido. Cada incidencia corresponde a un único contrato, y un contrato puede no tener ninguna incidencia o tener varias.

**R.F.04.01. Registrar una incidencia.** Como cliente, quiero registrar una incidencia en uno de mis contratos, para notificar a la empresa lo sucedido con el vehículo.

Prueba de aceptación:
Un cliente registra una incidencia indicando su fecha, su gravedad y su descripción, y comprueba que queda asociada al contrato correspondiente.
Se debe aplicar la regla de negocio R.N.05.

**R.F.04.02. Consultar mis incidencias.** Como cliente, quiero consultar las incidencias asociadas a mis contratos, para tener controladas mis responsabilidades.

Prueba de aceptación:
Un cliente accede a sus incidencias y comprueba que todas pertenecen a alguno de sus contratos.

**R.F.04.03. Listar incidencias por gravedad.** Como administrador, quiero listar las incidencias filtradas por su gravedad, para dar prioridad a las más graves.

Prueba de aceptación:
Un administrador selecciona la gravedad alta y comprueba que todas las incidencias mostradas tienen esa gravedad.

**R.F.04.04. Consultar las incidencias de un vehículo.** Como administrador, quiero consultar todas las incidencias de un vehículo a partir de su matrícula, para conocer su historial de daños y multas.

Prueba de aceptación:
Un administrador introduce una matrícula y comprueba que se muestran las incidencias de todos los contratos que ha tenido ese vehículo.

#### 4.1.5. Entidad: Usuario

**R.I.05. Información de los usuarios.** El sistema deberá almacenar la información de todos los usuarios que acceden a la aplicación. De cada usuario se guardarán su correo electrónico y su contraseña. Todo usuario será, de forma exclusiva, cliente o administrador.

**R.F.05.01. Iniciar sesión.** Como usuario, quiero introducir mi correo y mi contraseña, para acceder a la aplicación.

Prueba de aceptación:
Un usuario introduce un correo y una contraseña correctos y accede a las funciones de su rol.
Un usuario introduce una contraseña incorrecta y el sistema le deniega el acceso.

**R.F.05.02. Cerrar sesión.** Como usuario, quiero cerrar mi sesión, para que nadie pueda utilizar mi cuenta desde el dispositivo.

Prueba de aceptación:
Tras cerrar sesión, el usuario intenta acceder a una sección privada y el sistema le solicita de nuevo sus credenciales.

**R.F.05.03. Cambiar mi contraseña.** Como usuario, quiero modificar mi contraseña, para mantener la seguridad de mi cuenta.

Prueba de aceptación:
Un usuario cambia su contraseña y comprueba que solo puede iniciar sesión con la nueva.

**R.F.05.04. Cambiar mi correo electrónico.** Como usuario, quiero modificar mi correo electrónico, para mantener actualizados mis datos de acceso.

Prueba de aceptación:
Un usuario cambia su correo y comprueba que puede iniciar sesión con el nuevo y no con el anterior.

#### 4.1.6. Entidad: Administrador

**R.I.06. Información de los administradores.** El sistema deberá almacenar, además de los datos comunes a todo usuario, el token de administrador de cada administrador.

**R.F.06.01. Acceder como administrador.** Como administrador, quiero introducir mi token además de mis credenciales, para acceder a las funciones de gestión.

Prueba de aceptación:
Un administrador introduce su correo, su contraseña y su token correctos y accede al panel de gestión.
Un administrador introduce un token incorrecto y el sistema le deniega el acceso al panel.

**R.F.06.02. Dar de alta un administrador.** Como administrador, quiero registrar a un nuevo administrador, para incorporar a otro empleado a la gestión de la plataforma.

Prueba de aceptación:
Un administrador registra a un nuevo administrador y este puede acceder al panel con sus credenciales y su token.

**R.F.06.03. Listar administradores.** Como administrador, quiero consultar el listado de administradores, para saber quién tiene acceso a la gestión de la plataforma.

Prueba de aceptación:
Un administrador solicita el listado y comprueba que aparecen todos los administradores registrados y ningún cliente.

**R.F.06.04. Dar de baja a un administrador.** Como administrador, quiero dar de baja a otro administrador, para retirar el acceso a quien ya no deba tenerlo.

Prueba de aceptación:
Tras dar de baja a un administrador, este intenta acceder al panel y el sistema se lo impide.

### 4.2. Reglas de negocio

**R.N.01. Contratos sin solapamiento.** Un vehículo no podrá tener dos contratos cuyos periodos, comprendidos entre la fecha de contrato y la fecha de expiración, se solapen.

**R.N.02. Seguro básico limitado por edad.** Un contrato no podrá tener el seguro básico si el cliente titular tiene menos de 25 años en la fecha del contrato, calculando su edad a partir de su fecha de nacimiento.

**R.N.03. Mayoría de edad.** Todo cliente deberá tener al menos 18 años en el momento de su registro, calculando su edad a partir de su fecha de nacimiento.

**R.N.04. Límite de contratos vigentes.** Un cliente no podrá tener más de tres contratos vigentes de forma simultánea.

**R.N.05. Bloqueo por acumulación de incidencias.** Cuando un contrato acumule al menos una incidencia de gravedad alta, tres de gravedad moderada, cinco de gravedad leve, o dos moderadas y dos leves, el cliente titular no podrá formalizar nuevos contratos ni renovar los existentes.


## 5. Modelo conceptual

<img width="1321" height="1000" alt="Imagen JPEG-43D5-B5B1-9A-0" src="https://github.com/user-attachments/assets/f9fc0eb0-4349-4f82-9c23-d7c435df7cac" />

### 5.1. Diagramas de clases UML

<img width="1208" height="437" alt="imagen" src="https://github.com/user-attachments/assets/7a9e5388-dcb6-4286-9a3f-3be9ef527b6e" />


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


