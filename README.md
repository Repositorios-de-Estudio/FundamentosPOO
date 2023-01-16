# FundamentosPOO 
Ejemplos en C#


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

# Fundamentos Progrmacion Orientada a Objetos

## ¿Que es POO?
Es un tipo de paradigma de progrmación (estilo) imperativo que se basa en los conceptos de clase y objeto, donde se utilizan piezas (clases) simples y reutilizables para su estrctura. Cada clase tiene restricciones de transferencia indirecta de control, cada clase tiene sus propias caracteristicas que interactuan entre si. Como principio de desarrollo se suele usar DRY (Dont Repeat Yourself) para mantener el programa eficiente.

## Caracteristicas
- Programación estructurada: Flujo de control mediante: bulces, subrutinas y condicionales.
- Programación Procedimental: Busca reutilizar el codigo ya existente cada que se necesite.
- Programación Modular: Dividir un programa en modulos o subprogramas para resolver problemas complejos.

##Clase
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


