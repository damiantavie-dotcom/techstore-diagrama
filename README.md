# Diagrama de arquitectura TechStore

Este repositorio contiene la evidencia del desarrollo del diagrama de arquitectura de base de datos para la plataforma web TechStore.

## Objetivo

Analizar la arquitectura de base de datos, la seguridad en transacciones y las instrucciones necesarias para operar la base de datos.

## Elección de base de datos

Para TechStore se selecciona una base de datos SQL, como PostgreSQL o MySQL, porque permite trabajar con datos estructurados, relaciones entre tablas, integridad de datos y transacciones seguras.

La base de datos incluirá tablas como usuarios, productos, pedidos, transacciones e inventario.


## Seguridad en transacciones

Se consideran riesgos como inyección SQL, fraude, robo de credenciales y exposición de datos sensibles.

Para reducir estos riesgos se proponen medidas como HTTPS, consultas parametrizadas, validaciones en Backend, cifrado de contraseñas, roles y permisos, logs y auditoría.


## Instrucciones de base de datos y validación

Las instrucciones necesarias para operar la base de datos son:

- DDL: CREATE, ALTER, DROP.
- DML: SELECT, INSERT, UPDATE, DELETE.
- DCL: GRANT, REVOKE.
- TCL: BEGIN, COMMIT, ROLLBACK.

La validación de transacciones debe confirmar el pago, registrar el pedido, descontar stock y ejecutar COMMIT si todo es correcto. Si ocurre un error, se debe ejecutar ROLLBACK.
