# FUNDAMENTOS PROGRAMACION ORIENTADA A OBJETOS
*Ejemplos y conceptos especificamente dados para C#*


# Paradigmas
## Imperativo: Se deben dar instrucciones exactas de lo que debe hacer. 
*C#, Java*
  - Procedimental: 
  - Orientado a Objetos: Clases
  - Procesamiento Paralelo
## Declarativo: Indicar que se quiere hacer y el resultado que se desea
*Prolog*
  - Logico
  - Funcional / Flujo de Datos: Funciones
  - Base de datos
  
Material de ayuda [Fundamentos C#](https://github.com/Repositorios-de-Estudio/FundamentosCsharp)

***

# Fundamentos Progrmacion Orientada a Objetos

## ¿Que es POO?
Es un tipo de paradigma de progrmación (estilo) imperativo que se basa en los conceptos de clase y objeto, donde se utilizan piezas (clases) simples y reutilizables para su estrctura. Cada clase tiene restricciones de transferencia indirecta de control, cada clase tiene sus propias caracteristicas que interactuan entre si. Como principio de desarrollo se suele usar DRY (Dont Repeat Yourself) para mantener el programa eficiente.

## Caracteristicas
- Programación estructurada: Flujo de control mediante: bulces, subrutinas y condicionales.
- Programación Procedimental: Busca reutilizar el codigo ya existente cada que se necesite.
- Programación Modular: Dividir un programa en modulos o subprogramas para resolver problemas complejos.

## Clase
Es un modelo o plantilla/prototipo que define métodos (funciones) y atributos (propiedades) de datos de cualquier objeto dado. Los objetos son la instancia de cada clase. Ej: Animal {nombre, raza ... caminar(), comer()}.

## Objeto
Una entidad del mundo real claramente identificable. Los campos de datos con los valores actuales representan el estado del objeto.


## Principios de POO

## Encapsulamiento
(C# namespaces)
Ocultar el estado interno y la funcionalidad de un objeto y permitir solo el acceso a través de un conjunto público de funciones.

## Abstracción
(C#: Clase Abstracta, Metodos y Propieades Abstractos)
Modelar los atributos e interacciones pertinentes de las entidades como clases para definir una representación abstracta de un sistema.

*Clase Abstracta*
Las clases abstractas nos permiten tener una clase base con cierta funcionalidad común ya implementada, sobre la que podemos heredar y especificar algunos métodos.
- La clase abstracta puede funcionar si cumple una de estas dos:
	- La clase que hereda implementa todas los metodos y propiedades abstractos
	- Se vuelva así misma una clase abstracta
- Se pueden definir metodos y propiedades abstractos y no abstractos
- Las clases abstractas pueden heredas de otra clase abstracta
- No son instanciables (no se pueden crear objetos)
- Declara metodos que se deben sobreescribir en la clase que herede de esta
	- Se pueden crear metodos no abstractos
- Cuando se tienen varias clases que comparten metodos y propiedades que funcionan diferente

## Herencia
(C# : Clase, Clase Abstracta, Interface)
Es una característica de los lenguajes de programación orientados a objetos que permite definir una clase base, que proporciona funcionalidad específica (datos y comportamiento), así como clases derivadas, que heredan o invalidan esa funcionalidad.

- Una nueva clase toma los mismos atributos y metodos de otra clase
	- Empleado Hereda de Persona, Empleado hereda los mismos atributos y metodos de Persona
	- Esto evita declarar atributos y metodos que son comunes con la clase Persona
- La clase principal es llamada _superclase_ y la que hereda es llamada _subclase_
- Cada _subclase_ puede convertirse es una _superclase_  
	- De esta manera se puede tener un arbol de herencia: Animal <- Mamifero <- Felino <- Leon
- C# solo soporta herencia simple, cada clase solo puede heredas de una sola clase
	- 	La herencia multiple se tratar con Interfaces

*Interfaz*
A diferencia de las clases abstractas, una interfaz por sí sola no aporta funcionalidad, sino que fija un contrato que pueden implementar de manera distinta otras clases.
- Define metodos y propiedades abstractos
- Todos los metodos y propiedades deben ser abstractos
- Todos los metodos y propiedades deben ser implementados por la clase que hereda
- Una interfaz es como un molde rigido para una clase
- Una clase puede implementar varias interfaces
- Las interfaces deben empezar con I mayuscula: Interfaz Encendible = IEncencible
- Upcasting: Moldea/castea un objeto del tipo _subclase_ al tipo de una de su _superclase_
	- Array de tipo Mueble, silla de tipo Silla: `array[0]= silla;` // implicitamente se castea a tipo Mueble
- Downcasting: Moldea/castea un objeto del tipo _superclase_ al tipo de una _subclase_
	- Array de tipo Mueble, silla de tipo Silla: `Circulo otraSilla = array[0] as Circulo;`

## Polimorfismo
Capacidad de implementar las mismas propiedades y métodos heredados a una clase, sin embargo, se implementan de diferente forma por lo que funcionan de diferente forma, esto logra que objetos de varios tipos tengan las mismas funciones.

- Habilidad de poder realizar operaciones con objetos de distinto tipo
	- ej: objetos distinto tipo TV, auto, Lampara se pueden "Encender"
- Permite crear sistemas escalables
- Objetos de distinto tipo se comportan como uno solo
- Reuso de codigo
- Se aplica con Interfaces y Herencia

***

# Buenas Practicas
-  DRY (Dont Repeat Yourself)
-  SOLID (Single, Open/Closed, Liskov subs, Interface, Dependedi)

***

# PATRONES DE DISEÑO
Son una solución general, reutilizable y aplicable a diferentes problemas de diseño de software. Se trata de plantillas que identifican problemas y proporcionan soluciones apropiadas a problemas generales a los que se han enfrentado los desarrolladores. 

- Ahorran tiempo en el diseño
- Ayudan a estar seguro de la validez del codigo
- Ayuda a tener una metodologia en comun al trabajar en equipo
- Hace que sean menos propenso a tener errores

## Tipos de patrones de diseño

### 1. Patrones creacionales
Simplifican la creación de objetos, desacoplando la manera de como se crean del resto de la implementación: Encapsulan y ocultan su funcionamiento. Normalmente hace uso de Interfaces. (mas comunes en negrita)

- **Abstract Factory**
- **Builder Patterns**
- **Factory Method**
- **Prototype**
- **Singleton**

### 2. Patrones estructurales
Permiten la creación de la estructura especificando la forma en que las clases se relacionan con otras. El concepto de herencia se utiliza para componer interfaces y definir formas de componer objetos para obtener nuevas funcionalidades.

- **Adapter**
- **Bridge**
- **Composite**
- **Decorator**
- **Facade/Fachada**
- **Flyweight**
- **Proxy**

### 3. Patrones de comportamiento
El patrón de comportamiento se ocupa de la comunicación entre objetos de clase. Se utilizan para detectar la presencia de patrones de comunicación ya presentes y pueden manipular estos patrones.

- Chain of responsibility
- Command
- Interpreter
- Iterator
- Mediator
- Memento
- Observer
- State
- Strategy
- Template method
- Visitor

## 1. Patrones creacionales

### Abstract Factory
Provee una interfaz que delega la creación de un conjunto de objetos con caracteristicas similares sin necesidad de conocer como crealos.

### Builder Patterns
Separa el proceso de creación del objeto para poder crear representaciones distintas.

### Factory Method
Similar a *Abstrac Factory* con la diferencia de que provee un metodo que las subclases deben implementar.

### Prototype
Permite la creación de objetos en plantillas de tal forma que para crear un objeto se clona uno ya existente. Se utiliza para restringir las operaciones de memoria / base de datos manteniendo la modificación al mínimo utilizando copias de objetos.

### Singleton
Restringe la creación de instancias a un solo objeto y proporciona acceso global al objeto.

## 2. Patrones estructurales

### Adapter
Permite a dos interfaces que no son compatibles comunicarse entre ellas, mediante un objeto intermedio que permite su comunicacion.

### Bridge
Desacopla una extracción (interfaz) de su implementación (clase) y permite desarrollar a las clases de manera independiente utilizando una interfaz como puente.

### Composite
Se usa para agrupar objetos como un solo objeto. Permite componer objetos en estructuras de árbol y luego trabajar con estas estructuras como si fueran objetos individuales.

### Decorator
Permite agrega una nueva funcionalidad extra a un objeto sin necesidad de cambiar el comportamiento de los demas objetos del mismo tipo. La clase inicial permanece inalterada mientras que una clase decorator proporciona capacidades adicionales.

### Facade/Fachada
Proporciona una interfaz simplificada y solamente dejar acccesible lo que se va a utilizar (ej. libreria externa).

### Flyweight
Permite que una gran cantidad de objetos comparten un unico objeto para realizar una tarea, reduciendo el uso de memoria y mejorar el rendimiento al reducir la creación de objetos. El patrón busca objetos similares que ya existen para reutilizarlo en lugar de crear otros nuevos que sean similares.

### Proxy
Se utiliza como una interfaz hacia cualquier otra cosa que se encarga de realizar una tarea que puede ser costosa o no duplicable. (ej. conexiona internet, archivo). Utilizada para crear objetos que pueden representar funciones de otras clases u objetos y la interfaz se utiliza para acceder a estas funcionalidades

## 3. Patrones de comportamiento

### Chain of responsibility
Desacopla el emisor del receptor de tal forma que en una cadena de elementos, cada elemento decide lo proceso o lo delega al siguiente objeto de la cadena.

### Command
Encapsula una accion y define los parametros necesarios para ejecutarla.

### Interpreter
Define una repsentación de una gramatica asi como el mecanismo para procesarla. El arbol de sintaxis se suele interpretar mediante el patron composite.

### Iterator
Permite iterar a los elementos un objeto de colección sin necesidad de conocer como esta organizo o su estructura.

### Mediator
Encapsula como otros objetos se comunican entre ellos, través de su clase que permite la comunicación para varias clases.

### Memento
Otorna la habilidad a un objeto de volver a un estado anterior.

### Observer
Permite definir un mecanismo de suscripción para notificar a varios objetos sobre cualquier evento que le suceda al objeto que está siendo observado.

### State
En el patrón state, el comportamiento de una clase varía con su estado y, por lo tanto, está representado por el objeto de contexto.

### Strategy
Permite seleccionar el comportamiento del objeto en tiempo de ejecución segun factores.

### Template method
Se usa con componentes que tienen similitud donde se puede implementar una plantilla del código para probar ambos componentes. El código se puede cambiar con pequeñas modificaciones.

### Visitor
El propósito de un patrón Visitor es definir una nueva operación sin introducir las modificaciones a una estructura de objeto existente.

***
