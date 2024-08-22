Crear scripts en el símbolo del sistema de Windows (cmd) es una manera efectiva de automatizar tareas repetitivas y realizar operaciones rápidas. Los scripts en cmd suelen escribirse como archivos batch con la extensión `.bat` o `.cmd`.

### **¿Cómo crear un script en el símbolo del sistema de Windows?**

1. **Abrir un editor de texto**:
   - Abre el **Bloc de notas** o cualquier editor de texto simple.

2. **Escribir comandos**:
   - Escribe los comandos que quieres ejecutar. Cada comando debe estar en una nueva línea.

3. **Guardar el archivo**:
   - Guarda el archivo con la extensión `.bat` o `.cmd`. Por ejemplo, puedes nombrarlo `mi_script.bat`.

4. **Ejecutar el script**:
   - Ve al directorio donde guardaste el archivo batch, abre el símbolo del sistema, y ejecuta el script escribiendo su nombre:
     ```cmd
     mi_script.bat
     ```

### **Comandos básicos para incluir en scripts batch**

#### **1. Crear un directorio**
   - Comando:
     ```cmd
     mkdir nombre_del_directorio
     ```
   - Ejemplo de script:
     ```cmd
     @echo off
     mkdir C:\MisDocumentos\NuevoDirectorio
     echo Directorio creado exitosamente.
     ```

#### **2. Navegar entre directorios**
   - Comando:
     ```cmd
     cd [ruta_del_directorio]
     ```
   - Ejemplo de script:
     ```cmd
     @echo off
     cd C:\MisDocumentos
     echo Ahora estás en MisDocumentos.
     ```

#### **3. Crear un archivo de texto**
   - Comando:
     ```cmd
     echo texto > nombre_del_archivo.txt
     ```
   - Ejemplo de script:
     ```cmd
     @echo off
     echo Esto es una prueba > prueba.txt
     echo Archivo de texto creado.
     ```

#### **4. Mover archivos entre directorios**
   - Comando:
     ```cmd
     move [archivo_origen] [directorio_destino]
     ```
   - Ejemplo de script:
     ```cmd
     @echo off
     move C:\MisDocumentos\prueba.txt C:\MisDocumentos\Archivos
     echo Archivo movido a la carpeta Archivos.
     ```

#### **5. Eliminar archivos o directorios**
   - Comando:
     - Para archivos:
       ```cmd
       del nombre_del_archivo.txt
       ```
     - Para directorios:
       ```cmd
       rmdir nombre_del_directorio
       ```
   - Ejemplo de script:
     ```cmd
     @echo off
     del prueba.txt
     echo Archivo eliminado.
     rmdir C:\MisDocumentos\Archivos
     echo Directorio Archivos eliminado.
     ```

#### **6. Ejecutar un programa o abrir un archivo**
   - Comando:
     ```cmd
     start nombre_del_programa.exe
     ```
   - Ejemplo de script:
     ```cmd
     @echo off
     start notepad.exe prueba.txt
     echo Bloc de notas abierto con el archivo prueba.txt.
     ```

### **Ejemplos de scripts básicos**

#### **1. Organizar archivos por tipo**
Este script moverá todos los archivos de un tipo específico (por ejemplo, .txt) a una carpeta dedicada.

```cmd
@echo off
mkdir C:\MisDocumentos\TextFiles
move C:\MisDocumentos\*.txt C:\MisDocumentos\TextFiles
echo Todos los archivos .txt han sido movidos a la carpeta TextFiles.
```

#### **2. Backup de archivos**
Este script copiará todos los archivos de un directorio a un directorio de respaldo.

```cmd
@echo off
mkdir C:\MisDocumentos\Backup
xcopy C:\MisDocumentos\*.* C:\MisDocumentos\Backup /s /i
echo Archivos copiados a la carpeta de Backup.
```

#### **3. Ejecutar una serie de comandos de mantenimiento**
Este script realizará tareas comunes de mantenimiento, como limpiar archivos temporales y vaciar la papelera de reciclaje.

```cmd
@echo off
echo Limpiando archivos temporales...
del /s /q C:\Windows\Temp\*.*
echo Archivos temporales eliminados.

echo Vaciando papelera de reciclaje...
rd /s /q C:\$Recycle.Bin
echo Papelera vaciada.

echo Mantenimiento completado.
pause
```

### **Consejos para escribir scripts**
- **`@echo off`**: Evita que los comandos se muestren en pantalla cuando se ejecutan, manteniendo el script limpio.
- **Comentarios**: Usa `rem` para agregar comentarios que no serán ejecutados, por ejemplo:
  ```cmd
  rem Esto es un comentario.
  ```
- **Variables**: Puedes usar variables para almacenar datos que se reutilizarán en el script. Por ejemplo:
  ```cmd
  set nombre=Juan
  echo Hola, %nombre%
  ```

Estos scripts simples te permiten automatizar una variedad de tareas en Windows, y pueden ser un punto de partida para desarrollar scripts más complejos y útiles.
