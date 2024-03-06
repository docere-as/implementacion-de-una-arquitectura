# Implementación de una arquitectura

En esta práctica debes desarrollar una implementación que demuestre la
estructura y funcionamiento del una de las arquitecturas que se
estudian en la materia, a excepción de la arquitectura
cliente/servidor básica.


La funcionalidad del sistema no es relevante, no es necesario
implementar ninguna lógica de negocio concreta.

El proyecto tiene que modelar los componentes propios de la
arquitectura elegida y dichos componentes deben colaborar según lo
definido en la arquitectura. Tanto la implementación de los
componentes como la colaboración entre ellos debe usar los mecanismos
propios del lenguaje de programación _elixir_.


## Pasos

1. Cubre el apartado _Autor_  de este README.

1. Elige una de las arquitecturas estudiadas en la materia,
   distribuída o no. La arquitectura cliente/servidor no es elegible.

2. Cubre los apartados correspondientes de este README.

3. Documenta la arquitectura usando el modelo C4 según se describe en
   el apartado correspondiente de este README.

4. Cubre los apartados correspondientes de este README.

5. Implementa un modelo de la arquitectura elegida y las pruebas
   necesarias para validar dicha implementación.
 
6. Cubre los apartados correspondientes de este README.

7. Sube al moodle la url de este repositorio.


## Requisitos

1. Dado que _elixir_ es un lenguaje orientado a la concurrencia, en
   general, la forma adecuada de representar los componentes de la
   arquitectura es mediante procesos.
   
2. El código fuente tiene que tener el formato dado por `mix format`.

3. Se debe usar la herramienta de construcción estándar: `mix`.

4. Documenta _en línea_ las funciones relevantes del código, usando
   `@doc`, `@spec`, ...


## Uso del repositorio

1. Los usuarios de windows deben configurar el tratamiento de los
   finales de línea.
   
   ```
   % Configuración global (todos los repositorios)
   git config --global core.autocrlf true
   % Configuración lcoal (sólo este repositorio)
   git config --local core.autocrlf true
   ```

2. Las github actions comprueban que el código esté formateado con
   `mix format`. Para mayor comodidad podemos configurar el
   repositorio local para que lo compruebe antes de hacer un commit.
   
   P.e. 
   ```
   ---------------------------
   File: .git/hooks/pre-commit
   ---------------------------
   
   #!/bin/sh
   mix format --check-formatted
   ```
   

# Secciones a cubrir durante el desarrollo de la práctica

## Autor

Nombre, apellidos, login udc


## Presentación de la arquitectura

Nombre de la arquitectura y descripción de la posible variación
elegida.



## Diseño de la arquitectura

Documentación de la arquitectura elegida según el modelo C4. Debe
incluir:

  - Diagramas de contexto, contenedores y componentes.
  
  - Diagrama de código: al menos, diagramas de secuencia.
  

Enlaces a los ficheros en formato PNG o PDF que debem estar en el
directorio `doc/` de este repositorio.


## Testing

Descripción de los tipos de tests implementados.


## Uso

Instrucciones para ejecutar la práctica y los tests asociados.
