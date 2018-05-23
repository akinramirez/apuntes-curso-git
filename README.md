## Curso Git desde cero
Sistema de control de versiones para el
mantenimiento eficiente y confiable de archivos.

### Zonas de Git
1. Directorio de trabajo
2. Area de preparacion
3. Directorio Git

### Flujo de trabajo basico en Git
1. Modificas una serie de archivos en tu directorio de trabajo.
2. Preparas los archivos, añadiéndolos a tu área de preparación.
3. Confirmas los cambios, lo que toma los archivos tal y como están en el
área de preparación y almacena esa copia instantánea de manera
permanente en tu directorio de Git.

### Configurando Git por primera vez
```
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
git config --global core.editor nano
git config --list
```

### Sitio de patrones para .gitignore
https://www.gitignore.io/

Esta linea fue creada en la rama master.

## Varios repositorios remotos
Podemos configurar un mismo proyecto para sincronizar cambios con varios repositorios remotos.

## Cliente para Git / Github / Bitbucket / Gitlab
https://www.gitkraken.com/

## Cliente Git / Github
https://desktop.github.com

## Documentacion en español sobre Git
https://git-scm.com/book/es/v2

## Configuración SSH en Windows

Usando Git Bash seguimos los siguiente pasos:

Creamos una carpeta llamada llaves-ssh en el disco C para evitar problemas de rutas.

Ejecutamos el comando ssh-keygen -t rsa -C "mi-correo@ejemplo.com". El correo debe ser el mismo con el que nos registramos en Github para evitar posibles problemas. Dejamos el passphrase vacío y damos enter. Cuando nos pida la ruta escribimos /c/llaves-ssh/github_rsa.

Iniciamos ssh-agent en background ejecutando el comando eval "$(ssh-agent -s)".

Agregamos la llave ssh generada a ssh-agent ejecutando el comando ssh-add /c/llaves-ssh/github_rsa.

Usar el comando cat /c/llaves-ssh/github_rsa.pub. Con este comando vemos el contenido del archivo, copiamos todo el texto que nos muestra.

Ir a las configuración de nuestro perfil de Github y agregar una nueva llave SSH con el contenido que hemos copiado de github_rsa.pub.

Desde ahora podemos hacer pull y push sin que Github nos esté pidiendo los datos de acceso.