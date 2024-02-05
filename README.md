# PROYECTO GIT 



Esta trabajando en un proyecto Git colaborativo con varias ramas y commits. Tu tarea es
utilizar el comando git log con algunas opciones específicas para obtener un resumen
gráfico de los últimos 5 commits en todas las ramas.

```
$ git config alias.a "log --all --graph --oneline -n 5"
```

   **`"log --all --graph --oneline -n 5"`**: Esto especifica el comando que el alias "a" representará.

- `log`: Este comando muestra el historial de commits.
- `--all`: Muestra todos los commits, no solo los de la rama actual.
- `--graph`: Muestra una representación gráfica del historial de commits.
- `--oneline`: Muestra cada commit en una sola línea.
- `-n 5`: Limita la salida a los últimos 5 commits.

2.Esta trabajando en un proyecto Git colaborativo con varias ramas y commits. Tu tarea es
utilizar el comando git log con algunas opciones específicas para obtener un resumen
gráfico de los últimos 5 commits en todas las ramas.

1. Esta trabajando en un proyecto Git colaborativo y necesitas obtener una visión gráfica y
   detallada del historial de commits. Tu tarea es utilizar el comando git log con opciones
   específicas para personalizar el formato y presentación de la salida. La salida debe tener
   las siguientes especificaciones:

1. Muestra una representación gráfica del historial de commits

1. Muestra el hash corto del commit en color rojo

1. Muestra las referencias (ramas o tags) en las que está involucrado el commit en color
   amarillo

1. Muestra el mensaje del commit.

1. Muestra la fecha relativa del commit en color verde.

1. Muestra el hash del commit como un identificador abreviado.

   ```
   $ git config  alias.e "log --graph --abbrev-commit --decorate --format=format:'%C(red)%h%C(reset) %C(yellow)%d%C(reset)         %C(white)%s%C(reset) %C(green) (%ar)%C(reset)' --all"
   ```

   **`"log --graph --abbrev-commit --decorate --format=format:'%C(red)%h%C(reset) %C(yellow)%d%C(reset) %C(white)%s%C(reset) %C(green) (%ar)%C(reset)' --all"`**: Este es el comando que se ejecutará cuando escribas `git e`. Aquí está desglosado:

   - `log`: Muestra el historial de commits.

   - `--graph`: Muestra una representación gráfica del historial de commits.

   - `--abbrev-commit`: Muestra los identificadores de commit abreviados.

   - `--decorate`: Añade decoraciones como las etiquetas de las ramas o las cabeceras de los commits.

   - ```
     --format=format:'%C(red)%h%C(reset) %C(yellow)%d%C(reset) %C(white)%s%C(reset) %C(green) (%ar)%C(reset)'
     ```

     : Define un formato personalizado para la salida del registro. Este formato está configurado con códigos de color para resaltar diferentes partes de la salida:

     - `%C(red)%h%C(reset)`: Muestra el hash abreviado del commit en rojo.
     - `%C(yellow)%d%C(reset)`: Muestra las referencias de ramas y etiquetas en amarillo.
     - `%C(white)%s%C(reset)`: Muestra el mensaje del commit en blanco.
     - `%C(green) (%ar)%C(reset)`: Muestra la fecha relativa del commit en verde.

   - `--all`: Muestra todos los commits, no solo los de la rama actual.

   3.Estas trabajas frecuentemente con el comando git log -1 HEAD para obtener detalles sobre
   el último commit en la rama actual. Sin embargo, encuentras que escribir este comando
   completo es un poco tedioso. Quieres simplificarlo creando un alias personalizado.

   Tu tarea es utilizar el comando git config para crear un alias llamado last que represente el
   comando git log -1 HEAD.

   ```
   $ git config --global alias.last "log -1 HEAD"
   ```

   1. **`git config --global`**: Este comando se utiliza para configurar opciones globales de Git que afectarán a todos los repositorios en tu sistema. La opción `--global` indica que la configuración se aplicará a nivel global en lugar de sólo en el repositorio actual.
   2. **`alias.last`**: Aquí estás creando un alias llamado "last". Este alias te proporcionará un atajo para un comando específico de Git.
   3. **`"log -1 HEAD"`**: Esto define el comando que se ejecutará cuando escribas `git last`. Aquí está desglosado:
      - `log`: Este comando muestra el historial de commits.
      - `-1`: Esta opción indica que sólo se mostrará un único commit.
      - `HEAD`: Se refiere al commit más reciente en la rama actual en la que te encuentras.

   Entonces, en resumen, este alias "last" te proporciona una forma rápida de ver el último commit en la rama actual. Cuando ejecutas `git last`, verás los detalles del commit más reciente.

   4.Imagina que deseas simplificar el proceso de editar la configuración global de Git. Tu tarea
   es utilizar el comando git config para crear un alias que te permita abrir fácilmente la
   configuración global en tu editor de texto preferido. Ejecuta el comando para crear un alias
   llamado ec que cumpla con la especificación dada.

   ```
   $ git config --global alias.c "config --global -e"
   ```

   1. **`git config --global`**: Indica que estamos configurando una opción a nivel global en Git. Esto significa que la configuración se aplicará a todos los repositorios en tu sistema.
   2. **`alias.c`**: Aquí estás creando un alias llamado "c". Este alias te proporcionará un atajo para un comando específico de Git.
   3. **`"config --global -e"`**: Define el comando que se ejecutará cuando escribas `git c`. Aquí está desglosado:
      - `config`: Es el comando para acceder a la configuración de Git.
      - `--global`: Indica que estamos accediendo a la configuración global de Git.
      - `-e`: Esta opción abre el archivo de configuración en tu editor de texto predeterminado para que puedas editarlo directamente.

   5.Imagina que estás trabajando en un proyecto Git colaborativo con múltiples colaboradores
   y ramas. Tu tarea es utilizar el comando git log con opciones específicas para personalizar
   la salida del historial de commits y resaltar información clave. El resultado de la ejecución
   del comando se debe ve como el ejemplo siguiente:

   ```
   $ git config  alias.d "log --graph --abbrev-commit --decorate --format=format:'%C(bold yellow)%h%C(reset)  %C(red)%d%C(reset) %C(red)\ %C(white)%s%C(reset) %C(blue)\ %C(blue)[ %C(blue)%an%C(reset) %C(blue)]' --all"
   ```

   

1. **`git config`**: Es el comando principal para configurar opciones en Git.
2. **`alias.d`**: Con esta parte del comando, estás creando un alias llamado "d".
3. **`"log --graph --abbrev-commit --decorate --format=format:'%C(bold yellow)%h%C(reset) %C(red)%d%C(reset) %C(red)\ %C(white)%s%C(reset) %C(blue)\ %C(blue)[ %C(blue)%an%C(reset) %C(blue)]' --all"`**:
   - **`log`**: Este subcomando muestra el historial de commits.
   - **`--graph`**: Muestra una representación gráfica del historial de commits.
   - **`--abbrev-commit`**: Muestra los identificadores de commit abreviados.
   - **`--decorate`**: Añade decoraciones como las etiquetas de las ramas o las cabeceras de los commits.
   - **`--format=format:'...'`**: Define un formato personalizado para la salida del registro. Este formato incluye una serie de códigos de color y variables para formatear la salida de la manera deseada:
     - `%C(bold yellow)%h%C(reset)`: Muestra el hash abreviado del commit en negrita y amarillo.
     - `%C(red)%d%C(reset)`: Muestra las referencias de ramas y etiquetas en rojo.
     - `%C(white)%s%C(reset)`: Muestra el mensaje del commit en blanco.
     - `%C(blue)[ %C(blue)%an%C(reset) %C(blue)]`: Muestra el nombre del autor del commit entre corchetes y en azul.
   - **`--all`**: Muestra todos los commits, no solo los de la rama actual.