
### Definición de Proceso:
Conjunto de acciones que logran pasar de un Estado inicial a un estado final. 
- Materia prima (Datos)‒‒> Procesamiento ‒‒> Resultado final (Información)

### Acciones y Estados: 
Las acciones representan las operaciones que un programa o proceso puede realizar, mientras que los estados son las condiciones y atributos que definen a un sistema en un momento dado.

Ejemplo en Java:*

```markdown
```java
public class AccionesEstados {
    public static void main(String[] args) {
        int a = 5;
        int b = 3;
        // Acción: Sumar
        int suma = a + b;
        System.out.println("La suma es: " + suma);
        // Estado: Comparación
        if (a > b) {
            System.out.println("El estado es: 'a' es mayor que 'b'.");
        } else {
            System.out.println("El estado es: 'a' no es mayor que 'b'.");
        }
    }
}
```

### Variables y Constantes: 
Las variables son espacios de memoria que contienen datos que pueden cambiar durante la ejecución del programa, mientras que las constantes son valores que no cambian durante la ejecución del programa.

Ejemplo en Java:*

```java
public class VariablesConstantes {
    public static void main(String[] args) {
        // Variables
        int variableEntera = 10; 
        // Constantes
        final double PI = 3.14159;

        System.out.println("Variable entera: " + variableEntera);
        System.out.println("Constante PI: " + PI);
    }
}
```

### Tipos de Datos: 
Los tipos de datos en programación definen qué tipo de valores pueden almacenarse en las variables. Los tipos de datos pueden ser primitivos (como int, double, boolean, etc.) o de referencia (como String, arrays, objetos, etc.).

```java
public class TiposDeDatosPrimitivos {
    public static void main(String[] args) {
        byte byteVariable = 127; // byte: 8 bits, rango de -128 a 127.
        short shortVariable = 32767; // short: 16 bits, rango de -32,768 a 32,767.
        int intVariable = 2147483647; // int: 32 bits, rango de -231 a (231 - 1).
        long longVariable = 9223372036854775807L; // long: 64 bits, rango de -263 a (263 - 1).
        float floatVariable = 3.4028235e+38f; // float: 32 bits, rango de ±1.4e-45 a ±3.4028235e+38 (precisión de 7 decimales).
        double doubleVariable = 1.7976931348623157e+308; // double: 64 bits, rango de ±4.9e-324 a ±1.7976931348623157e+308 (precisión de 15 decimales).
        boolean booleanVariable = true; // boolean: representa dos valores: true o false.
        char charVariable = 'A'; // char: 16 bits Unicode, rango de '\u0000' (0) a '\uffff' (65,535).
        // No, en Java, un solo carácter (tipo char) solo puede contener un único carácter Unicode. No puede contener una cadena completa de texto como “Hola como estás”.
    }
}
```
### Tipos de datos referencia
```markdown
```java
public class TiposDeDatos {
    public static void main(String[] args) {
        // Array de enteros
        int[] enteros = {1, 2, 3, 4, 5};
        // Array de doubles
        double[] doubles = {3.14, 2.718, 1.618};
        // Array de booleanos
        boolean[] booleanos = {true, false, true};
        // Array de caracteres
        char[] caracteres = {'a', 'b', 'c'};
        // Array de floats
        float[] floatArray = {3.14f, 2.718f, 1.618f, 4.2f, 5.6f};
        // Array de cadenas
        String[] cadenas = {"Hola", "Mundo", "Java"};
    }
}
```

### Operaciones
A tener en cuenta java
```java
public class ExcepcionesAritmeticas {
    public static void main(String[] args) {
        int divisionCero = 10 / 0; // Error: División por cero (ArithmeticException)
        int divisionEnteros = 5 / 2; // Resultado: 2 (ArithmeticException)
        double conversionImplicita = 5 / 2; // Resultado: 2.0 (ArithmeticException) Sucede porque primero se hace la división que se consideran enteros
        int tipoIncompatible = 5 + "2"; // Error: Operación entre tipos incompatibles (ClassCastException)
        int desbordamientoTipo = Integer.MAX_VALUE + 1; // Error: Desbordamiento de tipo (ArithmeticException)
        double divisionFloatInt = 10 / 3.0; // Resultado: 3.3333333333333335
        double divisionDoubleInt = 10.5 / 2; // Resultado: 5.25
        float multiplicacionFloatDouble = 3.5f * 2.0; // Resultado: 7.0
        double sumaDoubleInt = 5.0 + 3; // Resultado: 8.0
    }
}
```

### La estructura de decisión:
La estructura de decisión permite ejecutar diferentes bloques de código dependiendo de si se cumple una condición o no. Por ejemplo, el if.
```java
int edad = 20;
if (edad >= 18) {
    System.out.println("Eres mayor de edad.");
} else {
    System.out.println("Eres menor de edad.");
}
```

### Estructura de decisión múltiple:
La estructura de decisión múltiple permite elegir entre varias opciones de ejecución. En Java, esto se realiza con la sentencia switch.
```java
int dia = 3;
switch (dia) {
    case 1:
        System.out.println("Lunes");
        break;
    case 2:
        System.out.println("Martes");
        break;
    default:
        System.out.println("Día no válido");
}
```

**¿Qué sucede si no uso “break” en el Switch?**
Si no utilizas la instrucción break dentro de un bloque switch, el flujo de ejecución continuará pasando a través de los casos subsiguientes, ejecutando su código incluso si no se cumple la condición del caso. Esto se conoce como “fall-through” o “caída a través”.
```java
int opcion = 2;
switch

 (opcion) {
    case 1:
        System.out.println("Opción 1 seleccionada");
    case 2:
        System.out.println("Opción 2 seleccionada");
    case 3:
        System.out.println("Opción 3 seleccionada");
    default:
        System.out.println("Opción no válida");
}
```
Si opcion tiene el valor de 2, la salida sería:
```
Opción 2 seleccionada
Opción 3 seleccionada
Opción no válida
```

### Tipos de estructura de Control:
Sentencia IF-Else: Permite ejecutar un bloque de código si se cumple una condición, de lo contrario, ejecuta otro bloque.
Sentencia Switch: Permite elegir entre múltiples bloques de código basados en el valor de una variable. 
Sentencias anidadas: Se refiere a la inclusión de una estructura de control dentro de otra. Por ejemplo, un if dentro de otro if.

### La estructura de Iteración:
La estructura de iteración se utiliza para repetir un bloque de código mientras se cumple una condición.

### Tipos de estructura de iteración:
**Sentencia While:** Ejecuta un bloque de código mientras se cumple una condición.
```java
int contador = 0;
while (contador < 5) {
    System.out.println("Contador: " + contador);
    contador++;
}
```

**Sentencia For: **Ejecuta un bloque de código un número específico de veces.
```java
for (int i = 0; i < 5; i++) {
    System.out.println("Iteración: " + i);
}
```

**Sentencia Do-While:** Similar a while, pero garantiza que el bloque de código se ejecute al menos una vez antes de verificar la condición.
```java
int j = 0;
do {
    System.out.println("Valor de j: " + j);
    j++;
} while (j < 3);
```

**Foreach:** Itera sobre una colección de elementos sin necesidad de un contador o índice explícito.
```java
int[] numeros = {1, 2, 3, 4, 5};
for (int numero : numeros) {
    System.out.println(numero);
}
```

### Operador Ternario en Java
El operador ternario en Java es una forma compacta de escribir una expresión condicional. Tiene la siguiente sintaxis:
```java
condición ? valor_si_verdadero : valor_si_falso;
```

Ejemplo en Java:
```java
int edad = 20;
String mensaje = (edad >= 18) ? “Eres mayor de edad” : “Eres menor de edad”;
System.out.println(mensaje);
```

## Java teoría
Funcionamiento del JDK (Kit de Desarrollo de Java)

El JDK (Java Development Kit) es un conjunto de herramientas necesarias para desarrollar aplicaciones Java. Incluye el compilador de Java (javac), la máquina virtual Java (JVM), bibliotecas Java estándar y otros recursos.

**Compilador de Java (javac):** El compilador de Java convierte el código fuente Java (.java) en bytecode Java (.class), que es ejecutable en cualquier JVM.

**Máquina Virtual Java (JVM):** La JVM interpreta y ejecuta el bytecode generado por el compilador. La JVM es específica de cada sistema operativo y es responsable de administrar la memoria, gestionar el ciclo de vida de los objetos y ejecutar el código Java de manera eficiente.

**Bibliotecas Java Estándar**: El JDK incluye un conjunto de bibliotecas estándar de Java que proporcionan funcionalidades básicas para el desarrollo de aplicaciones, como manipulación de cadenas, entrada/salida, networking, colecciones, etc.

**Herramientas de Desarrollo:** Además del compilador y la JVM, el JDK proporciona varias herramientas de desarrollo útiles, como el depurador (jdb), el generador de documentación (javadoc), el descompilador (javap), entre otros.

El JDK se instala en el sistema operativo del desarrollador y se utiliza para escribir, compilar y ejecutar programas Java en cualquier plataforma compatible. Las aplicaciones desarrolladas con el JDK pueden ejecutarse en cualquier sistema que tenga instalada una JVM compatible, lo que hace que Java sea un lenguaje de programación verdaderamente portátil y multiplataforma.

### Funcionamiento de Compilación en Java
Java utiliza un enfoque de compilación y ejecución separadas. Durante la compilación, el compilador de Java traduce el código fuente (.java) a bytecode (.class), que es un código intermedio ejecutable en cualquier máquina virtual Java (JVM).

Ejemplo de compilación en Java:
```bash
javac MiPrograma.java
```
Esto compila el archivo MiPrograma.java y produce MiPrograma.class, que contiene el bytecode ejecutable.

### Sistemas Operativos en los que Java se Puede Ejecutar
Java es un lenguaje de programación multiplataforma, lo que significa que puede ejecutarse en varios sistemas operativos, incluyendo:
- Windows
- macOS
- Linux/Unix
- Solaris
- Android (basado en Linux)

## Teoría - secuencias

```python
//Contar las palabras de un párrafo
var secuencia, contadorPalabra, charAnterior; 
arr secuencia if cc != marca and cc != “ ”{ contadorPalabra++; } 

while cc =! marca { 
    if (charAnterior→" " and cc != " ") {
        contadorPalabra ++;
    } 
    charAnterior = cc
} 
```

Contar las a de una secuencia
```python
Var secuencia; var contar 
contarA:= 0 escribir (“Ingresar texto”) secuencia:= leer () arrancar while cc != marca { if(cc→"a" or cc ↔ “A” or cc ↔
“Á” or cc ↔ “a”) { contarA:= contarA + 1 } 
av } 
``` 

- Elaborar un algoritmo para carga un arreglo de 50 nombres de 30 caracteres 
```python
real[30] arregloNombres[50] 
for (int i = 0; i < 50 ; i++) { 
    print("Ingresar un nombre")
    arregloNombres[i] = ingresar()
}
```

- Elaborar un algoritmo para eliminar un nombre dado en un arreglo de 50 nombres de 30 caracteres 
```python
real[30] arregloNombres[50] 
metodo llenarAlgoritmo(arregloNombres) { 
    for (int i = 0; i < 50 ; i++) {
        print("Ingresar un nombre")
        arregloNombres[i] = ingresar()
    }
} 
metodo eliminarPorNombre(arregloNombres) { 
    print(“Ingresar nombre a eliminar”); 
    nombreEliminar = ingresar(); 
   

 for(int i = 0; i <50 ; i++) {
        if(arregloNombres[i]→nombreEliminar)
        arregloNombres[i] = " ";
        break;
    }
}

llenarAlgoritmo(arregloNombres) 
eliminarPorNombre(arregloNombres) 
```

- Contar cuántas palabras dentro de un texto tienen un “A” dentro: 
```python
Contar cuántas palabras dentro de un texto tienen un “A” dentro: sec secuencia1 
arr secuencia1 contadorA = 0; 
while (cc != marca) { enPalabra = 0; existeAenPalabra = false; 
    if (ccAnterior→" " and cc != " ") {
        enPalabra = true;
    }
    if (cc ↔ " ") {
        if(enPalabra and existeAenPalabra) {
            contadorA++; 
        } 
        enPalabra = false;
    } 
    if(cc ↔ "a" and enPalabra) {
        existeAenPalabra = true
    } 
} 
```

Intersección de secuencias
```python
Elaborar un algoritmo que dadas dos listas que haga la interesección de las mismas de una tercera.
sec secuencia1, secuencia2, secuencia3; int i = 0; int d = 0; arr secuencia2 arr secuencia1 crear secuencia3;
while (secuencia1[i] != marca){ int b = 0; bool existe = false; while ((secuencia2[b] != marca) and !existe) {
    if(secuencia1[i]→secuencia2[b]) { 
        existe = true 
        secuencia3[d] = secuencia1[i] 
        d++; 
    } 
    b++; 
} 
    i++; 
} 
```

Concatenación de secuencias 
```python
lista1 String arreglo[n]; lista2 String arreglo[m]; lista3 String arreglo[n+m]; i:=0; 
Mientras i <= n lista3[i] = lista1[i]; i:= i +1; FM 
j:= 0; 
Mientras j <= m lista3[i] := lista2[j]; i:= i + 1; j:= j + 1; FM 
```

-  Unión de secuencias 
```python
Elaborar un algoritmo que dadas dos genera una unión en una tercera 
sec secuencia1, secuencia2, secuencia3; arr secuencia1 crear secuencia3; int i = 0 while (secuencia1[i] != marca) {
    secuencia3[i]→secuencia1[i] 
    i++; 
} 
int c = 0 int d = 0; arr secuencia2 while (secuencia2[c] != marca) { 
    bool existe = false; int b = 0;
    while((secuencia3[b] != marca) and !existe) 
        if(secuencia3[b] ↔ secuencia2[c]) { 
            existe = true; 
        } 
        b++
} 
    if(!existe) {
        secuencia3[d + i] = secuencia2[c]
        d++;
    }
    c++;
} 
```
 Diferencia de secuencias
(A v B) - (intersección de A y B)
```python
Elaborar un algoritmo que dadas dos listass permita efecutar la operación de diferencias entre las mismas en una tercera.
sec secuencia1, secuencia2, secuencia3; int i = 0; int d = 0; arr secuencia2 arr secuencia1 crear secuencia3;
while (secuencia1[i] != marca){ int b = 0; bool existe = false; while ((secuencia2[b] != marca) and !existe) {
    if(secuencia1[i]→secuencia2[b]) { 
        existe = true 
    } 
    b++; 
} 
    if(!existe) {
        secuencia3[d] = secuencia1[i]
        d++; 
    }
    i++; 
} 
i = 0; 
while (secuencia2[i] != marca){ int b = 0; bool existe = false; while ((secuencia1[b] != marca) and !existe) {
    if(secuencia2[i] ↔ secuencia1[b]) { 
        existe = true 
    } 
    b++; 
} 
    if(!existe) {
        secuencia3[d] = secuencia2[i]
        d++; 
    }
    i++; 
} 
```


## Registros y Archivos
Un registro, en programación, es un tipo de dato estructurado formado por la unión de varios elementos bajo una misma estructura. Estos elementos pueden ser, o bien datos elementales (entero, real, carácter,...), o bien otras estructuras de datos. A cada uno de esos elementos se le llama campo. Una colección de registros se denomina archivo. 
```java
Cliente Registro Identificador entero Nombre cadena(30) Apellido cadena(20) FRegistro 
```
```java
public class Cliente{ 
    string id; 
    string nombre; 
    string apellido; 
    Public Cliente(String id, String nombre, String apellido){ 
        this.id=id; 
        this.nombre=nombre; 
        this.apellido=apellido; 
    } 
} 
```

Arreglos
Permite representar una secuencia lineal y finita de elementos del mismo tipo. Estos elementos pueden ser de tipo primitivo o de otros tipos. Es posible recuperar cada elemento del arreglo mediante un sub-indice. 
Búsqueda en arreglos
La búsqueda en un arreglo consiste en buscar una dato determinado dentro de la estructura de un arreglo. 
La búsqueda binaria consiste como su nombre lo indica en dividir el arreglo en dos partes de acuerdo a la relación entre el contenido del medio con el valor buscado
Binary search
```java
// Encontrar entre un arreglo ordenado de 100 legajos uno específico con un algorítmo binario 
legajos real arreglo[100] var legajoBuscado, centinela, i, primero, ultimo; centinela := verdadero primero := 0
ultimo:= 99 while centinela and primero > ultimo { i := (primero + ultimo / 2) if ( legajos[i] < legajoBuscado) {
primero := i + 1 } else if (legajos[i] > legajoBuscado) { ultimo:= i - 1 } else if ( legajos[i]→legajoBuscado) {
centinela:= falso print (“Encontrado en posición” + (i + 1))
} 
if (primero > ultimo) {
centinela := falso 
print ("No se encontró en el arreglo")
}
}
```

