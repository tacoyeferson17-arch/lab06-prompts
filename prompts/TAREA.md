# Tarea: Mi prompt profesional

## Funcionalidad elegida
Sistema CRUD (Crear, Leer, Actualizar, Eliminar) para la gestión de productos en una tienda usando Java Swing.

---

## Version 1: prompt basico

```text
Hazme un programa en Java para registrar productos.
```

* **Qué se cambió / Por qué:** Es la primera versión, muy general e imprecisa.
* **Qué mejoró:** Produce un código funcional muy básico por consola, pero no cumple con interfaz gráfica ni con estructura orientada a objetos adecuada.

---

## Version 2

```text
Actua como desarrollador Senior Java. Crea un programa con interfaz grafica Java Swing para un sistema CRUD de productos (codigo, nombre, precio, stock). Muestra la lista de productos y explica el codigo.
```

* **Qué se cambió:** Se añadió un ROL (Desarrollador Senior Java), CONTEXTO (CRUD de productos con atributos) e INSTRUCCIÓN explícita de usar Java Swing.
* **Qué mejoró:** La respuesta ahora incluye una ventana gráfica con formulario y tabla (`JTable`), además de organizar mejor las funciones básicas.

---

## Version 3: prompt final

```text
Actua como desarrollador Senior Java. Diseña un modulo con interfaz grafica en Java Swing para la gestion CRUD de productos (atributos: codigo, nombre, precio y stock).

Requisitos y Restricciones:
1. No uses librerias externas, solo Java Standard SDK (Swing y AWT).
2. Separa la solucion en dos capas claras: Modelo (clase Producto) e Interfaz Grafica (JFrame).
3. Incluye validacion de datos (el precio y stock deben ser numeros mayores a cero).
4. Muestra mensajes de confirmacion o error utilizando JOptionPane.

Estructura de respuesta: Explica brevemente la arquitectura de la solucion en 2 parrafos y luego presenta el codigo limpio y comentado.
```

* **Qué se cambió:** Se incluyeron EJEMPLOS de estructura, FORMATO de salida estricto y RESTRICCIONES clave ("no usar librerías externas", "validación numérica").
* **Qué mejoró:** El código generado es profesional, modular, robusto ante errores de usuario y con una arquitectura fácil de mantener.

---

## Componentes del prompt final

| Componente | Texto de mi prompt |
|------------|--------------------|
| **Rol** | Actúa como desarrollador Senior Java. |
| **Instrucción** | Diseña un módulo con interfaz gráfica en Java Swing para la gestión CRUD de productos. |
| **Contexto** | Atributos: código, nombre, precio y stock. |
| **Ejemplos / Restricciones** | No uses librerías externas; separa en Modelo e Interfaz; valida precio y stock; usa JOptionPane. |
| **Formato** | Explica brevemente la arquitectura en 2 párrafos y luego presenta el código limpio y comentado. |

---

## Evaluacion del resultado

| Criterio | Cumple (Sí / No) |
|----------|-------------------|
| ¿Utiliza interfaz gráfica Java Swing sin librerías externas? | Sí |
| ¿Está estructurado en capas (Modelo y Vista)? | Sí |
| ¿Valida que precio y stock sean valores numéricos válidos? | Sí |
| ¿Presenta la explicación previa en 2 párrafos antes del código? | Sí |

---

## Errores que evite

1. **Ser demasiado general:** En la V1 el pedido era vago ("un programa en Java"). Lo evité en la V3 especificando la tecnología (Swing), los campos exactos del objeto y las funciones CRUD requeridas.
2. **No indicar restricciones ni formato:** Inicialmente no se aclaró cómo estructurar la respuesta. Lo evité estableciendo la prohibición de librerías externas y exigiendo una explicación en 2 párrafos antes del bloque de código.
- [Bitácora de prompts](prompts/BITACORA.md)
- [Tarea: mi prompt profesional](prompts/TAREA.md)