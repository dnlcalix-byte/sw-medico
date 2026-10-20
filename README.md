# Sistema de Distribución de Insumos Médicos

Sistema de operación para una unidad de distribución de insumos médicos y odontológicos
en Tegucigalpa, Honduras. Entrega rápida a consultorios, con control de margen por pedido.

**Aplicación en vivo:** https://dnlcalix-byte.github.io/sw-medico/

## Qué hace

- **Toma de pedido** con catálogo visual, recompra rápida y productos habituales por cliente
- **Motor de asignación de canal**: decide entre courier y moto dedicada al menor costo
- **Regla de no-pérdida**: no permite confirmar un pedido con contribución negativa
- **Despacho** tipo monitor de cocina, con compuerta de pago por depósito bancario
- **Inventario** con existencia física, comprometido y disponible
- **Reposición** predictiva según el consumo histórico de cada cliente

## Cómo funciona

Es un solo archivo HTML sin dependencias. No requiere servidor ni instalación.
Los datos se guardan en el navegador de cada dispositivo (localStorage).

> **Importante:** al ser almacenamiento local, los datos **no se comparten entre
> dispositivos**. Cada navegador tiene su propia copia. Para operación multiusuario
> se requiere una base de datos compartida — ver `SIGUIENTE-PASO.md`.

## Uso local

Descargar `index.html` y abrirlo con doble clic. Funciona sin internet.

## Respaldo

Ajustes → Descargar respaldo. Genera un archivo JSON con todos los datos.
Se restaura desde la misma pantalla.

## Datos de prueba

Ajustes → Probar el sistema → Cargar datos de ejemplo.
