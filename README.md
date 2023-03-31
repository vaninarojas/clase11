Primero debemos descargar git para luego instalarlo en nuestra pc. 
Recordar tildar la opción de: "git bash here" y seleccionar la opción de use visual s tudio as git defualt editor.
Podemos abrir el git bash o una consola o una terminal desde vsc.
Para abrir la terminal desde vsc tenemos que abrir el root en el IDE, luego tocamos sobre el botón "terminal" y luego tocamos sobre el select que esta a lado del "+" y seleccionamos la opción "git bash". Al tocarlo, se nos abre el bash en la terminal.
Paso seguido necesitamos configurar nuestro usuario por única vez con los siguientes comandos:
git config --global user.name "nombreUsuario"
git config --global user.email emailSuyo@gmail.com
Luego de esto podemos corroborar si la configuración quedo impactada con los siguientes comandos:
git config user.name
git config user.email
-----------------
Luego de tener todo configurado e instalado necesito pararme sobre mi root y decirle: 
"che root vamos a trabajar con git" ¿como hago esto?
Para hacer esto necesitamos estar posicionado sobre mi root y usar el comando (por primera y unica vez): 
git init
Luego de ejecutar el git init ya estamos parados sobre el estado "working directory" que es donde generamos todas las lineas de codigo
Cuando completo mi tarea, paso todo lo trabajado del "working directory" -> "staging area" ¿cómo hago esto? Para hacerlo necesitamos el comando:
git add . (comando por lote)
git add nombreArchivo (manual archivo o directorio)
Luego de pasar todo al "staging area" instantaneamente pasamos todo al "repositoty" con el comando:
git commit -m "comentario breve y descriptivo de lo que se estuvo trabajando"
Al terminar de commitear, se nos genera una version nueva y nos posiciona en el "working directory" automaticamente. 
¿cómo controlo los estados de mis archivos/directorios? Con el siguiente comando:
git status
-------------
RAMAS
Las ramas nos sirven para generar una copia fiel de nuestro proyecto. Esto nos permite modificar la rama sin miedo a romper todo. ¿cómo hago para generar una rama? Con el siguinte comando:
git branch nombreRama
Para corroborar las ramas que tenemos creadas usamos el comando:
git branch -l
Para movernos entre las ramas usamos el comando:
git checkout nombreRama
Es importante que cuando nos movemos a una rama y trabajamos sobre la misma, hagamos el pasaje de estado que ya conocemos (working directory -> staging area -> repo)
A partir de entender que el código generado en nuestra rama es el correcto voy a necesitar agregar esta rama a mi master, ¿cómo hacemos este agregado de nuestra rama al master? Antes de ejecutar el comando es necesario estar posicionado sobre el master para ahí, ejecutar el siguiente comando: 
git merge nombreRama
Luego de mergear, podemos eliminar la rama con el siguinte comando:
git branch -D nombreRama
