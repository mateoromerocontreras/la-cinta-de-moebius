---
layout: post
title:  "Navegación con la línea de comandos en Windows"
date:   2024-08-19 23:50:52 -0300
categories: Sistemas operativos
background: '/img/posts/simbolo-sistema-Windows.jpg'
---
# Navegar entre Directorios
## Actividad nº1 de sistemas operativos

Descripción: Los estudiantes aprenderán a moverse entre diferentes directorios utilizando la línea de comandos.
La siguiente tarea esta pensada para familiarizarse con la navegación en la línea de comandos de Windows. 
Mediante la línea de comandos de windows deberán navegar en la estructura de directorios del sistema operativo.

### Actividad 1: Navegar entre Directorios
Abrir el Símbolo del sistema (cmd.exe): 
* Presionar Win + R, escribir cmd y presionar Enter. 

Cambiar el directorio actual: 
* Comando: cd [nombre_del_directorio] 

**Ejemplo**: Navegar al escritorio con cd Desktop. 
* Comando: cd Desktop

#### Navegar desde el directorio raíz (C:) hasta el directorio Documentos.

Para ir aun directorio superior en el arbol de directorios se utiliza el comando 
`cd ..`

Para ir al directorio raíz se utiliza el comando `cd ..` hasta llegar al directorio raíz: C:\.
A continuación, para llegar al directorio Documentos se debe navegar a través de los siguientes directorios:
* `cd Users`
* `cd [nombre_de_usuario]`
* `cd Documents`

Puede variar según la configuración del sistema operativo y el nombre de usuario.

#### Mostrar la ruta completa del directorio actual. 
Comando: cd 
Tarea: 
Mostrar la ruta del directorio actual y escribirla en un archivo de texto. 


### Actividad 2: Crear Archivos y Directorios

Descripción: Los estudiantes practicarán la creación de archivos y directorios, así como su organización.
Crear un nuevo directorio: 
Comando: mkdir [nombre_del_directorio] 
Ejemplo: mkdir Ejercicio 
Tarea: 
Crear un directorio llamado Proyectos en el escritorio. 
Crear un nuevo archivo de texto: 
Comando: echo [texto] > [nombre_del_archivo.txt] 
Ejemplo: echo Hola Mundo > hola.txt 
Tarea: 
Crear un archivo llamado lista.txt dentro del directorio Proyectos con el texto "Tareas pendientes". 
Crear un archivo vacío: 
Comando: type nul > [nombre_del_archivo.txt] 
Ejemplo: type nul > nuevo.txt 
Tarea: 
Crear un archivo vacío llamado notas.txt en el directorio Proyectos. 
### Atividad 3: Listar el Contenido de Directorios
Descripción: Los estudiantes aprenderán a visualizar y organizar el contenido de los directorios.
Listar los archivos y carpetas en el directorio actual: 
Comando: dir 
Tarea: 
Listar el contenido del directorio Proyectos que crearon previamente. 
Listar archivos y directorios con detalles adicionales: 
Comando: dir /w (lista en formato ancho) o dir /p (lista página por página) 
Tarea:
Listar el contenido de C:\Windows y anotar cuántos archivos y carpetas hay. 
Listar solo archivos de un tipo específico (por ejemplo, archivos .txt): 
Comando: dir *.txt 
Tarea: 
Listar solo los archivos .txt en el directorio Proyectos. 

### Actividad 4: Mover y Copiar Archivos
Descripción: Los estudiantes practicarán mover y copiar archivos de un directorio a otro utilizando la línea de comandos.
Copiar un archivo: 
Comando: copy [ruta_origen] [ruta_destino] 
Ejemplo: copy hola.txt C:\Users\[usuario]\Desktop\Proyectos 
Tarea: 
Copiar hola.txt desde C:\ al directorio Proyectos. 
Mover un archivo: 
Comando: move [ruta_origen] [ruta_destino] 
Ejemplo: move hola.txt C:\Users\[usuario]\Desktop\Proyectos 
Tarea: 
Mover notas.txt del directorio Proyectos al escritorio. 

### Actividad 5: Ejecutar Scripts Básicos

Descripción: Los estudiantes aprenderán a crear y ejecutar scripts básicos en la línea de comandos para
automatizar tareas sencillas.
Crear un script batch: 
Comando: Usar echo para escribir comandos en un archivo .bat 
Ejemplo: echo echo "Hola, mundo!" > script.bat 
Tarea: 
Crear un script organizar.bat que mueva todos los archivos .txt del escritorio al directorio Proyectos. 
Ejecutar el script: 
Comando: nombre_del_script.bat 
Ejemplo: script.bat 
Tarea: 
Ejecutar el script organizar.bat y verificar que los archivos .txt fueron movidos. 

### Actividad 6: Borrar Archivos y Directorios

Descripción: Los estudiantes aprenderán a eliminar archivos y directorios de manera segura.
Eliminar un archivo: 
Comando: del [nombre_del_archivo] 
Ejemplo: del hola.txt 
Tarea: 
Eliminar notas.txt del escritorio. 
Eliminar un directorio vacío: 
Comando: rmdir [nombre_del_directorio] 
Ejemplo: rmdir Ejercicio 
Tarea: 
Eliminar el directorio vacío Proyectos. 
Eliminar un directorio con contenido: 
Comando: rmdir /s [nombre_del_directorio] 
Tarea: 
Crear un directorio llamado Temp con algunos archivos dentro, y luego 
eliminarlo junto con su contenido. 

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
