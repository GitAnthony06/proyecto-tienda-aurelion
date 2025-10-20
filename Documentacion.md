# Proyecto Aurelion – Documentación
1ra demo: asincrónica

## 1. Tema, problema y solución 

### Tema
Tienda Aurelion: Tienda de productos de consumo masivo

### Problema
La Tienda Aurelion enfrenta una disminución en sus ventas y en mantener una rentabilidad sostenible.

Mediante un análisis realizado se identificó que la dispersión de la información de ventas, clientes y productos impide contar con datos claros y centralizados, lo que limita la capacidad de la empresa para:
- Identificar productos y categorías más rentables, perdiendo oportunidades de impulsar ventas estratégicamente.
- Ajustar precios o promociones basadas en patrones reales de compra.
- Planificar el inventario de manera eficiente, provocando sobrestock o desabastecimiento.
- Comprender el comportamiento de sus clientes y segmentar estrategias de marketing.
Esta falta de información confiable puede generar pérdidas de ingresos, decisiones comerciales tardías y oportunidades de crecimiento desaprovechadas.

### Solución:
Implementar un sistema digital que centralice los datos de ventas, productos y clientes, y que permita su análisis estratégico, con el objetivo de aumentar los ingresos y mejorar la toma de decisiones comerciales.
La solución permitirá:
- Detectar los productos y categorías más rentables y ajustar inventario y precios según la demanda.
- Analizar patrones de compra y segmentar clientes para promociones personalizadas que incrementen ventas.
- Generar reportes claros de desempeño diario y ticket promedio, mejorando la planificación financiera.
- Optimizar inventario y reducir pérdidas por productos no vendidos o desabastecimiento.
Con esta herramienta, Aurelion podrá tomar decisiones basadas en datos reales, incrementar su rentabilidad y ser más competitivo en el mercado.


## 2. Dataset de referencia  

**Fuente:**  
clientes.xlsx  

**Definición:**  
Proporciona los datos personales y de contacto de cada cliente.

**clientes.csv (~344 filas)** 

| Campo            | Tipo | Escala   |  
|------------------|------|----------|  
| id_cliente       | int  | Nominal  |  
| nombre_cliente   | str  | Nominal  |  
| email            | str  | Nominal  |  
| ciudad           | str  | Nominal  |  
| fecha_alta       | date | Intervalo|  


**Fuente:**  
detalle_ventas.xlsx

**Definición:**  
Detalle la cantidad de unidades vendidas por producto, su precio por unidad y la venta a la que corresponde.

**detalle_ventas.csv (~344 filas)**  
| Campo            | Tipo | Escala   |  
|------------------|------|----------|  
| id_venta         | int  | Nominal  |  
| id_producto      | int  | Nominal  |  
| nombre_producto  | str  | Nominal  |  
| cantidad         | int  | Razón    |  
| precio_unitario  | int  | Razón    |  
| importe          | int  | Razón    |  


**Fuente:**  
productos.xlsx  


**Definición:**  
Lista de productos disponibles, con su categoría, id y precio por unidad.


**productos.csv (~101 filas)**  
| Campo            | Tipo | Escala   |  
|------------------|------|----------|  
| id_producto      | int  | Nominal  |  
| nombre_producto  | str  | Nominal  |  
| categoria        | str  | Nominal  |  
| precio_unitario  | int  | Razón    |  


**Fuente:**  
ventas.xlsx  


**Definición:**  
Contiene los datos de contacto de los clientes vinculados a cada venta realizada, en conjunto con la fecha y el medio de pago.  


**ventas.csv (~121 filas)**  
| Campo            | Tipo | Escala   |  
|------------------|------|----------|  
| id_venta         | int  | Nominal  |  
| fecha            | date | Intervalo|  
| id_cliente       | int  | Nominal  |  
| nombre_cliente   | str  | Nominal  |  
| email            | str  | Nominal  |  
| medio_pago       | str  | Nominal  |  


## 3. Información, pasos, pseudocódigo y diagrama del programa (Sprint 1)

### 3.1 Contenidos accesibles desde el menú
1. Tema, problema y solución.
2. Fuente, definición, estructura, tipos y escala.
3. Pasos, pseudocódigo y diagrama.
4. Sugerencias y mejoras con Copilot.
5. Salir.

### 3.2 Pasos
1. El programa lee el archivo documentacion.md y separa su contenido por secciones numeradas. 
2. Muestra un menú principal con las opciones disponibles. El usuario elige una opción del 1 al 5. 
3. Según la opción seleccionada, se muestra el texto correspondiente a esa sección. 
4. El programa espera que el usuario presione “Enter” para volver al menú. 
5. Si el usuario selecciona 5 (Salir), el programa finaliza mostrando un mensaje de despedida.

### 3.3 Pseudocódigo
Inicio
    Mostrar "Bienvenido al Programa de Navegación de contenidos del Proyecto Aurelion"
    
    nro =0
    Mientras nro =! 5
    
        Mostrar "Menú Principal:
        1. Tema, problema y Solución.
        2. Fuente, definición estructura, tipos y escala.
        3. Pasos, pseudocódigo y diagrama.
        4. Sugerencias y mejoras con Copilot.
        5. Salir "

        Leer nro

        Si nro = 1 
            Mostrar "Texto correspondiente a la sección 1"
            Esperar a que el usuario presione enter
        Si nro = 2
            Mostrar "Texto correspondiente a la sección 2"
            Esperar a que el usuario presione enter
        Si nro = 3
            Mostrar "Texto correspondiente a la sección 3"
            Esperar a que el usuario presione enter
        Si nro = 4 
            Mostrar "Texto correspondiente a la sección 4"
            Esperar a que el usuario presione enter
        Si nro = 5 
            Mostrar "Gracias por usar el programa"
            Fin del programa
        else  
            Mostrar "Opcción invalida. Intente nuevamente"

### 3.4 Diagrama de flujo:
![Diagrama del flujo](./Diagrama_Flujo.pdf)


## 4. Sugerencias y mejoras aplicadas con Copilot
**Pasos (acciones concretas y breves):**

1. Normalizar encabezados y numeración
Revisar que todos los títulos numerados usen el mismo nivel (p. ej. "## 1. ..." para secciones principales) y corregir inconsistencias.
Alternativas: (1) renumerar automáticamente vía búsqueda regex; (2) renumerar manualmente si pocos cambios.

2. Corregir pseudocódigo y lógica del menú
Cambiar condición inválida "Mientras nro =! 5" → "Mientras nro != 5" y unificar opciones (actualmente el archivo muestra 5 opciones).
Alternativas: (1) exponer función route_option(op) para tests; (2) dejar flujo sencillo en main() y añadir wrapper testable.

3. Estandarizar la sección de datasets
Convertir descripciones en una tabla clara con columnas: fuente, archivo, filas aproximadas, campos clave. Verificar que los nombres de archivo (.xlsx/.csv) coincidan con los recursos reales.
Alternativas: (1) mantener tabla Markdown en el mismo md; (2) mover metadatos a YAML front-matter para consumo automático.

4. Separar textos reutilizables
Extraer cada sección a un recurso externo (módulo o carpeta de md) e importar desde el menú.
Alternativas: (1) textos.py con dict{id: texto} (simple, testable); (2) carpeta /docs/ con .md por sección (editable sin redeploy).

5. Añadir búsqueda y exportación (UX mínima)
Añadir sección en el documento que describa la API de búsqueda (substring case-insensitive) y la opción exportar (ruta por defecto: sección_<id>.md).
Alternativas: (1) búsqueda por substring (rápida); (2) búsqueda por regex para mayor precisión.

6. Tests mínimos documentados
Documentar tests esperados: route_option(1..N) devuelve strings con identificadores de sección; búsqueda devuelve lista relevante; exportación crea archivo UTF-8.
Alternativas: (1) usar unittest (ejemplos simples); (2) usar pytest si ya existe en el proyecto.

7. Archivos y diagramas
Verificar rutas relativas del Diagrama (./Diagrama_Flujo_Proyecto_Aurelion.pdf) y agregar texto alternativo / leyenda. Si PDF no carga en vista, exportar a PNG.
Alternativas: (1) mantener PDF y añadir enlace; (2) generar PNG para integración en Markdown.

8. Redacción y metadatos
Corregir gramática menor (p. ej. puntuación en listas), añadir encabezado metadata: autor, fecha, versión y contacto.
Alternativas: (1) editar inline en el .md; (2) agregar un bloque CHANGELOG.md para versiones.
