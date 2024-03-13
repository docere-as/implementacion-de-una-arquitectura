# Implementación de una arquitectura

En esta práctica debes desarrollar una implementación que demuestre la
estructura y funcionamiento de una de las arquitecturas que se
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
   distribuida o no. La arquitectura cliente/servidor no es elegible.

2. Cubre el apartado correspondiente de este README.

3. Documenta la arquitectura usando el modelo C4 según se describe en
   el apartado correspondiente de este README.

4. Cubre los apartados correspondientes de este README.

5. Implementa un modelo de la arquitectura elegida y las pruebas
   necesarias para validar dicha implementación.
 
6. Cubre los apartados correspondientes de este README.

7. Sube al moodle la url de este repositorio.


>[!NOTE]
> Si deseas una revisión intermedia antes de completar el
> desarrollo de la práctica, solicitala directamente al profesor.


## Requisitos

1. Dado que _elixir_ es un lenguaje orientado a la concurrencia, la
   forma adecuada de representar los componentes de la arquitectura es
   mediante procesos.
   
2. El código fuente tiene que tener el formato dado por `mix format`.

3. Se debe usar la herramienta de construcción estándar: `mix`.

4. Documenta _en línea_ las funciones relevantes del código, usando
   `@doc`, `@spec`, ...
   
5. El código debe compilar sin _warnings_.

6. El código debe pasar los tests antes de hacer un _push_ a _github_.


## Uso del repositorio

1. Antes de realizar el primer _push_ es conveniente crear el proyecto
   con `mix new app`.

2. El repositorio inicial contiene una _github action_ que realiza
   comprobaciones automáticas sobre el código del proyecto.
   
   Para que esta acción funcione correctamente puede ser necesario
   configurar los siguientes parámetros:
   
   - Versión de OTP.
   
   - Versión de elixir.
   
   - Ruta al proyecto dentro del repositorio.
   
   Estos parámetros se configuran en el fichero `.config` en la raíz
   del repositorio.
   
   Ejemplo de fichero `.config`:
   
   ```
   OTP_VERSION=25.0.4
   ELIXIR_VERSION=1.14.1
   APP_BASE_PATH=app/
   ```
   
3. Para nuestra comodidad también podemos configurar el repositorio
   local para que realice comprobaciones sobre el proyecto y no nos
   permita hacer un commit si nos hemos olvidado de algo.
   
   Por ejemplo, comprobar que el código compila sin warnings, tiene el
   formato requerido y pasa los tests. En un entorno _unix-like_ una
   opción para hacer esto último es con el siguiente fichero:

   ```
   ---------------------------
   File: .git/hooks/pre-commit
   ---------------------------
   
   #!/bin/sh
   mix compile --warnings-as-errors
   mix format --check-formatted
   mix test
   ```
   
## Entrega de la práctica

Al entregar la práctica para su evaluación debes tener en cuenta lo
siguiente:

- Sube al moodle la url del _commit_ que quieres que se evalúe. Si
  subes la url del repositorio, se evaluará el último commit de la
  rama `main`.
  
- Los commits para los que la _github action_ original no se haya
  ejecutado con éxito se consideran **no entregados** y reciven una
  calificación de **0 puntos**.

- Si quieres una revisión intermedia del proyecto antes de entregarlo,
  ponte en contacto con el profesor.


# Secciones a cubrir durante el desarrollo de la práctica

## Autor

Nombre, apellidos, login udc


## Presentación de la arquitectura

Nombre de la arquitectura.

Breve descripción de la arquitectura y sus posibles variaciones
elegidas.




## Diseño de la arquitectura

Documentación de la arquitectura elegida según el modelo C4. Debe
incluir:

  - Diagramas de contexto, contenedores y componentes.
  
  - Diagrama de código: al menos, diagramas de secuencia.
  

Enlaces a los ficheros en formato PNG o PDF que deben estar en el
directorio `doc/` de este repositorio.


## Testing

Descripción de los tipos de tests implementados.


## Uso

Instrucciones para ejecutar la práctica y los tests asociados.
