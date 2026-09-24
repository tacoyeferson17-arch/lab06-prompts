# Bitacora de prompts
 
Laboratorio 06: Fundamentos de Ingenieria de Prompts.
 
Herramienta de IA usada: (escribe aqui cual usaste)
 use la IA gemini y en el primer chat respondio tal y como se dijo en el lab pero en el 5 paso gemini respondio con un proyecto que yo tenia ateriormente 
 aplicación web se llama NexusGG.

En cuanto al conjunto de tecnologías (tech stack) que utilizas en tus proyectos, destacan las siguientes:

Frontend: Bootstrap para el diseño y maquetación responsiva, junto con JavaScript para la interactividad y navegación.

Backend y desarrollo general: Java para proyectos académicos, haciendo uso de entrada de datos (Scanner) y aplicando principios de programación orientada a objetos (POO), como encapsulamiento, atributos privados y métodos getters/setters.

Control de versiones y despliegue: Git y GitHub para el control de versiones local/remoto y la gestión de ramas.
## Ejercicio 2: Tokens y ventana de contexto
| Texto | Caracteres | Tokens |
|-------|------------|--------|
| Los estudiantes programan en Java. | | |
| The students program in Java. | | |
| desafortunadamente | | | 
## Ejercicio 3: Temperatura

| Temperatura | % de BiblioTec | Nombres en los 5 intentos |
|-------------|----------------|---------------------------|
| 0 | 100.0% | BiblioTec, BiblioTec, BiblioTec, BiblioTec, BiblioTec |
| 0.5 | 86.8% | BiblioTec, BiblioTec, LibroYa, BiblioTec, PrestaLibro |
| 1 | 54.3% | BiblioTec, LectoGo, LibroYa, PrestaLibro, BiblioTec |
| 1.8 | 32.1% | LectoGo, NubeDeTinta, LibroYa, PaginaLibre, PrestaLibro |
Al subir la temperatura, la probabilidad se reparte entre las alternativas y genera nombres más variados en los intentos.
El simulador no inventa nombres nuevos porque solo cambia el riesgo al elegir entre las palabras de su lista predefinida.

## Ejercicio 4: Prompt vago vs estructurado
 | Criterio | Prompt vago | Prompt estructurado |
|----------|-------------|---------------------|
| Menciona el objetivo del sistema |si|si|
| Menciona a los usuarios principales |no|si|
| Tiene exactamente 3 funcionalidades |no|si|
| Esta en 3 parrafos |no|si|
| Lo usaria en un informe real |no|si|

## Ejercicio 5: Anatomia de un prompt
 | Componente | Texto de mi prompt |
|------------|--------------------|
| Rol |Aquí tienes una solución completa y modular en Java para gestionar el inventario de una tienda. El programa está implementado en la consola siguiendo buenas prácticas de programación orientada a objetos (POO), con clases separadas para el modelo de datos, la gestión y la interfaz. |
| Instruccion |Aquí tienes una solución completa y modular en Java usando Programación Orientada a Objetos (POO). He estructurado el programa en dos clases principales: Producto (para definir la entidad) y Tienda (con el método main y un menú interactivo).|
| Contexto |Estructura de la Clase Producto
Para representar un producto dentro del sistema, definimos la clase Producto con los siguientes componentes:

Atributos privados (Encapsulamiento):

codigo (String): Identificador único del producto.

nombre (String): Nombre o descripción del producto.

precio (double): Precio unitario.

stock (int): Cantidad disponible en inventario.

Constructor: Permite inicializar los cuatro atributos al instanciar un nuevo objeto.

Métodos Getters y Setters: Permiten acceder y modificar los atributos de forma segura.

Métodos de Negocio:

vender(int cantidad): Reduce el stock si hay suficiente disponibilidad.

reponer(int cantidad): Aumenta el stock del producto.

Método toString(): Devuelve una representación legible en texto de la información del producto.

Código en Java|
| Ejemplo |// Clase Producto
public class Producto {
    // Atributos privados
    private String codigo;
    private String nombre;
    private double precio;
    private int stock;

    // Constructor completo
    public Producto(String codigo, String nombre, double precio, int stock) {
        this.codigo = codigo;
        this.nombre = nombre;
        this.precio = precio;
        this.stock = stock;
    }

    // Getters y Setters
    public String getCodigo() {
        return codigo;
    }

    public void setCodigo(String codigo) {
        this.codigo = codigo;
    }

    public String getNombre() {
        return nombre;
    }

    public void setNombre(String nombre) {
        this.nombre = nombre;
    }

    public double getPrecio() {
        return precio;
    }

    public void setPrecio(double precio) {
        if (precio >= 0) {
            this.precio = precio;
        } else {
            System.out.println("Error: El precio no puede ser negativo.");
        }
    }

    public int getStock() {
        return stock;
    }

    public void setStock(int stock) {
        if (stock >= 0) {
            this.stock = stock;
        } else {
            System.out.println("Error: El stock no puede ser negativo.");
        }
    }

    // Método auxiliar para imprimir los detalles del producto
    public void mostrarInformacion() {
        System.out.println("Código: " + codigo + 
                           " | Nombre: " + nombre + 
                           " | Precio: $" + precio + 
                           " | Stock: " + stock + " unidades");
    }
}|
| Formato |Para gestionar los productos de una tienda en Java, estructuraremos la clase Producto con los atributos solicitados y aplicaremos encapsulamiento (atributos privados y métodos de acceso get/set públicos).

Estructura de la Clase Producto
Atributos (Privados):

codigo (String): Identificador único del producto.

nombre (String): Nombre o descripción del producto.

precio (double): Costo unitario del producto.

stock (int): Cantidad de unidades disponibles en inventario.

Métodos:

Constructor: Permite inicializar un objeto Producto con sus cuatro atributos al momento de instanciarlo.

Getters y Setters: Métodos como getPrecio() y setPrecio(double precio) para consultar y modificar el valor de los atributos de manera segura.

Métodos de negocio opcionales: actualizarStock(int cantidad) o mostrarDetalle() para facilitar la lógica de la tienda.|
## Ejercicio 6: Del prompt basico al profesional
| Qué revisar | Cumple (Sí / No) |
|-------------|-------------------|
| ¿Está escrito en Java y usa Swing? | Sí |
| ¿Pide correo y contraseña? | Sí |
| ¿Explica el funcionamiento antes o después del código? | Sí |
| ¿El código está organizado en clases? | Sí |
| ¿Valida los datos que ingresa el usuario? | Sí |
```text
Actúa como un desarrollador Senior en Java. Crea un programa con interfaz gráfica usando Java Swing para un sistema de inicio de sesión (Login). 

Requisitos:
1. Debe solicitar un correo electrónico y una contraseña.
2. Organiza la solución en clases de forma limpia y orientada a objetos.
3. Agrega validación para los datos ingresados por el usuario.
4. Incluye una breve explicación del funcionamiento antes o después del código.
```
- [Bitacora de prompts](prompts/BITACORA.md)