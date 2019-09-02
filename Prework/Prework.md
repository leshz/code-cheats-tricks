# Plugin de Git en zsh

Al instalar [Zsh](https://ohmyz.sh), por defecto nos trae el plugin de **GIT**, este plugin contiene una serie de alias o formas abreviadas para ejecutar git por la consola.

Si queremos ver cuantos alias nos ofrece , en la consola escribimos

```bash
alias
```

y buscamos las que apliquen para GIT

---

Los alias de **GIT** que más utilizo son :

```bash
g = git
gco = git checkout
gp = git push de la rama actual
gl  = git pull de la rama actual
gm = git merge
gma = git merge --abort
gm - = git merge de la rama anterior a la actual
glg = git log con informacion de archivos modificados
glgg = git log con graph de ramas
```

# Agregrando nuestros propios Alias

Podemos crear nuestros propios Alias para para reducir la cantidad de comandos que digitamos a diario, para crearlos tenemos que ir al archivo de configuracion de ZSH que esta en ~/.zshrc.

y agregamos:

ALIAS [nuestro_alias]=[comando_a_ejecutar]

Aqui algunos ejemplos:

```bash

alias editAlias="code ~/.zshrc"
alias gu="gulp"
alias c="clear"

```

Tambien podemos unir la ejecuccion de los comando conectandolos con el operador && , este operador ejecuta el comando siguiente , cuando el anterior termine de ejecutarse.

Un ejemplo :

```bash
alias dev="git checkout dev  && git pull origin dev"
```

# Formato del archivo al guardar

Con la instalaccion de [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) en VisualStudio Code nos ayuda a mantener el formato de los archivos, pero aveces este paso no es automatico por lo que nos lleva a hacer 2 click para lograr el formato _( o un atajo de teclado)_ para hacer este proceso automatico, agreganmos la opcion de formatOnsave **true** en el archivo de configuracion de VSCode.

```json
"editor.formatOnSave": true,
```
