# sistema-facturacion
# 🧾 Sistema de Facturación y Cuentas por Cobrar

## Objetivo
Digitalizar la gestión de ventas, clientes, productos y cobros 
del negocio de Manuel González, eliminando el registro manual 
en cuadernos y reduciendo errores de cálculo.

## Problema que resuelve
El negocio llevaba todos sus registros de forma manual, lo que 
generaba errores frecuentes, pérdida de información y dificultad 
para identificar clientes deudores.

## Funcionalidades principales
- Registro y gestión de clientes (CRUD)
- Registro y gestión de productos con control de stock
- Creación de facturas con cálculo automático de ITBIS (18%)
- Control de cuentas por cobrar con filtro por estado
- Registro de pagos parciales o totales
- Dashboard con resumen del negocio en tiempo real

## Arquitectura seleccionada
Arquitectura por Capas (3 capas) + patrón Cliente-Servidor

## Organización Frontend y Backend

### Frontend — Capa de Presentación
**Tecnología:** Windows Forms (C#)  
**Componentes:** fmMain, fmCliente, fmProducto, fmFacturacion, fmCobrar  
**Responsabilidad:** Mostrar datos al usuario y capturar sus acciones.  
No contiene lógica de negocio ni accede directamente a la base de datos.

### Backend — Capa de Lógica y Datos
**Tecnología:** Clases C# + ADO.NET + SQL Server  
**Componentes:** Cliente, Producto, Factura, DetalleFactura, Pago, ConexionBD  
**Responsabilidad:** Procesar cálculos, validaciones y transacciones SQL.

### Comunicación entre capas
El frontend llama a los métodos de las clases C# (backend), 
que a su vez utilizan ConexionBD y ADO.NET para comunicarse 
con SQL Server mediante consultas SQL.

## Herramientas utilizadas
- Lenguaje: C#
- IDE: Visual Studio
- Interfaz: Windows Forms
- Base de datos: SQL Server
- Acceso a datos: ADO.NET
- Modelado: Visual Paradigm Online
- Gestión: GitHub Projects + GitHub Issues

## Estado actual del proyecto
🟡 En desarrollo — módulos principales completados, 
en fase de pruebas y documentación final.

## Registro de cambios
| # | Avance / Ajuste | Semana |
|---|---|---|
| 1 | Diseño y creación de la base de datos en SQL Server con 5 tablas y datos de prueba | Semana 1 |
| 2 | Módulo de gestión de clientes y productos funcionando con CRUD completo | Semana 2 |
| 3 | Módulo de facturación con cálculo automático de ITBIS y transacción SQL | Semana 2 |
| 4 | Módulo de cuentas por cobrar con registro de pagos y actualización de saldo | Semana 3 |
| 5 | Diagramas UML completados: Casos de Uso, Clases, Secuencia y Actividades | Semana 3 |
