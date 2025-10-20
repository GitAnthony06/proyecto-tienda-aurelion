# 🛒 Aurelion – Sistema de Gestión de Ventas de Supermercado

## 📘 Contexto del proyecto
Este proyecto forma parte del **Programa de Formación en Fundamentos de Inteligencia Artificial y Análisis de Datos**, impulsado por **IBM SkillsBuild** y **Guayerd**.  
Su desarrollo responde a una consigna práctica en la que los participantes deben **plantear un escenario realista**, definir un **problema de negocio** y proponer una **solución basada en análisis de datos**.

> 🧠 *Nota:* Aurelion no es una tienda real, sino un escenario educativo creado para aplicar los conocimientos adquiridos durante el curso.

---

## 🧩 Escenario planteado

**Aurelion** es un supermercado de productos de consumo masivo que ofrece artículos de diferentes categorías (alimentos, limpieza, hogar, etc.).  
La tienda registra sus ventas, clientes y productos de manera manual, lo que dificulta el análisis general de su desempeño.  
Los responsables del negocio desean **mejorar la gestión de sus ventas** y **entender mejor el comportamiento de los clientes**.

---

## ❌ Problema identificado
La tienda **no cuenta con un sistema centralizado** para registrar y analizar su información comercial.  
Esto genera dificultades al momento de:
- Conocer los productos más vendidos.
- Determinar el ingreso total por periodo.
- Identificar clientes frecuentes o con mayores compras.
- Analizar la demanda por categoría o tipo de producto.

---

## 💡 Solución propuesta
Diseñar un **sistema de gestión de ventas simple en Python** que:
1. Registre datos de clientes, productos y ventas.
2. Genere un archivo consolidado (`CSV`) que unifique toda la información.
3. Permita analizar los datos posteriormente en **Power BI** o herramientas similares.
4. Muestre indicadores clave como:
   - Total recaudado  
   - Productos más vendidos  
   - Ticket promedio  
   - Ventas por ciudad o categoría  

El objetivo es **automatizar procesos básicos** y **sentar las bases de un análisis de datos confiable** sin depender de sistemas costosos o complejos.

---

## 🧠 Metodología de desarrollo
El proyecto sigue un enfoque estructurado inspirado en la **Investigación Operativa** y el **Análisis de Procesos**:

1. **Definición del problema** – Limitaciones actuales del registro de ventas.  
2. **Modelado del sistema** – Identificación de entidades: clientes, productos, ventas y detalle de ventas.  
3. **Obtención de datos** – Simulación de datasets coherentes.  
4. **Desarrollo** – Construcción del flujo lógico y pseudocódigo.  
5. **Validación** – Comprobación de cálculos e integridad de datos.  
6. **Análisis** – Generación de resultados interpretables.

---

## 🗂️ Datasets utilizados

| Dataset | Descripción | Campos principales |
|----------|--------------|--------------------|
| **clientes.csv** | Datos de los clientes registrados | id_cliente, nombre, email, ciudad |
| **productos.csv** | Información de productos disponibles | id_producto, nombre, categoría, precio |
| **ventas.csv** | Registro general de ventas realizadas | id_venta, id_cliente, fecha, total |
| **detalle_ventas.csv** | Detalle de productos por venta | id_detalle, id_venta, id_producto, cantidad, subtotal |

---
