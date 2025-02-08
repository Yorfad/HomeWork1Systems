Base de Datos BANKING

/////////////////////////////////////////////////////Descripción//////////////////////////////////////////////////////////
Este es un proyecto de un sistema de gestión de datos para bancos, enfocado es optimizar el almacenamiento y consulta de datos de manera que sea fácil de usar sin comprometer ninguna funcionalidad esencial.
Estructura de la Base de Datos
La base de datos se compone de las siguientes tablas:
1.	CENTRALS: Contiene información sobre las centrales o bancos mas impoortantes
2.	BRANCHES: Contiene información sobre las sucursales asociadas a cada banco central.
3.	ATMS: Registra las múltiples cajas asociadas a cada central o sucursal
4.	ACCOUNTS_HOLDERS: Almacena información sobre los Clientes
5.	ACCOUNTS: Registra las cuentas bancarias asociadas a cada cliente y sucursal.
6.	TRANSACTIONS: Almacena las transacciones bancarias como depósitos y retiros.

Cada tabla tiene relaciones bien definidas mediante claves foráneas para almacenar la informacion
Instalación

//////////////////////////////////////////////////////////////Requisitos Previos/////////////////////////////////////////////////
●	Microsoft SQL Server 2022 instalado y en ejecución.
●	SQL Server Management Studio (SSMS) o cualquier cliente compatible con SQL Server.

//////////////////////////////////////////////////////////////Pasos de Instalación/////////////////////////////////////////////////

Crear la base de datos ejecutando:
CREATE DATABASE [BANKING]
GO
1.	USE [BANKING]
2.	Crear las tablas ejecutando los comandos SQL proporcionados.
3.	Insertar datos de prueba con los comandos INSERT INTO.
4.	Crear índices para optimizar la velocidad de búsqueda.
5.	Implementar particionamiento de datos en la tabla de transacciones.
6.	Habilitar compresión de datos para optimización del almacenamiento.
7.	Configurar optimizaciones de memoria y aislamiento de transacciones para mejorar el rendimiento.


//////////////////////////////////////////////////////////Funcionalidades Implementadas///////////////////////////////////////////
●	Gestión de entidades bancarias: Se mejoro la forma de consultar información de las centrales y sucursales
●	Gestión de clientes y cuentas: Almacena la información de los clientes y sus cuentas bancarias.
●	Gestión de transacciones: Controla depósitos y retiros mediante cajeros automáticos.
●	Optimización del rendimiento: Uso de índices, particionamiento y compresión de datos para mejorar la eficiencia en consultas.
●	Seguridad y concurrencia: Habilitación de Snapshot Isolation para evitar bloqueos y mejorar la consistencia de los datos.
Mejoras y Modificaciones Realizadas
●	Particionamiento de la tabla TRANSACTIONS: Hacemos particiones en la tabla transacciones para poder almacenar grandes volúmenes de datos de manera comprimida, principalmente para datos viejos poder almacenarlos de manera segura y que ocupen menos espacio
●	Compresión de datos en ACCOUNTS y TRANSACTIONS para optimizar el uso del almacenamiento y optimizar los tiempos de carga de las consultas de estos
●	Índices en columnas clave para mejorar el rendimiento de búsqueda.
●	Vista AccountDetails para obtener información detallada de cuentas con sus titulares de manera rápida y sencilla

////////////////////////////////////////////////////////////Consultas SQL de Ejemplo//////////////////////////////////////////////////
Para visualizar que la base de funcione correctamente podemos ejecutar los siguientes scripts:
SELECT * FROM CENTRALS;
SELECT * FROM BRANCHES;
SELECT * FROM ATMS;
SELECT * FROM ACCOUNTS_HOLDERS;
SELECT * FROM ACCOUNTS;
SELECT * FROM TRANSACTIONS;

