# 🛠️ Configuración inicial de Git

En esta sección aprenderás a **instalar y configurar Git** en tu computadora.  
Es el primer paso antes de empezar a trabajar con repositorios.

## 1️⃣ Verificar si ya tienes Git instalado

Abre tu terminal (CMD, PowerShell, Git Bash o terminal de Linux/Mac) y escribe:

```bash
git --version
```

Si ves un número de versión igual o superior (ej: `git version 2.42.0`), ¡ya lo tienes instalado! 🎉  

Si no, sigue con la instalación 👇  

## 2️⃣ Instalar Git

- **Windows**:

Descarga el instalador desde [git-scm.com](https://git-scm.com/)  

- **MacOS**:

```bash
   brew install git
```

- **Linux (Debian/Ubuntu)**:

```bash
   sudo apt update
   sudo apt install git
```

- **Linux (Fedora/RHEL)**:

```bash
   sudo dnf install git
```

## 3️⃣ Configurar Git por primera vez

Después de instalar Git, configura tu nombre y correo (se guardan en cada commit):

```bash
   git config --global user.name "Tu Nombre"
   git config --global user.email "tu@email.com"
```

👉 Usa el mismo correo de tu cuenta de GitHub para que tus commits aparezcan vinculados a tu perfil.

### 📌 Explicación

- **`git config`** → sirve para configurar opciones en Git.  
- **`--global`** → significa que la configuración aplica a **todo tu usuario en el sistema** (todos los repositorios que uses en tu computador).  
- **`user.name`** → define el **nombre de autor** que aparecerá en cada commit que hagas.  
- **`user.email`** → define el **correo electrónico del autor** que quedará registrado en los commits.  

👉 Es importante usar el **mismo correo de tu cuenta de GitHub** para que los commits se asocien correctamente a tu perfil.  

### ✅ En resumen

Estos comandos configuran tu **identidad en Git**.  
Cada vez que hagas un commit, quedará guardado con tu **nombre y correo** para saber quién lo hizo.

## 4️⃣ Comprobar la configuración

Para verificar qué datos configuraste:

```bash
   git config --list
```

### 🔎 ¿Qué hace?

Muestra **todas las configuraciones actuales de Git** que están activas en tu entorno.  

Incluye configuraciones de tres niveles:  

- **Sistema** → afectan a todos los usuarios en el computador.  
- **Global** → afectan solo a tu usuario (todas las carpetas/repositorios).  
- **Local** → afectan únicamente al repositorio en el que estás trabajando.  

### 📌 Ejemplo de salida

```bash
   user.name=Tu Nombre
   user.email=tu@email.com
   color.ui=auto
   core.editor=code --wait
```

### ✅ En resumen

Este comando sirve para ver rápidamente qué valores de configuración tiene Git activos (nombre, correo, colores, editor, etc.).
Es útil para comprobar que configuraste Git correctamente antes de empezar a trabajar.

## 5️⃣ (Opcional) Configurar un editor de texto

Por defecto, Git abre el editor del sistema para los mensajes de commit.
Puedes cambiarlo, por ejemplo, a VS Code:

```bash
   git config --global core.editor "code --wait"
```

Este comando sirve para decirle a Git qué editor de texto usar cuando necesite que escribas algo (como un mensaje de commit, un rebase, un merge, etc.).

👉 Nota: En este tutorial, usamos VS Code.

### 🔎 Desglose del comando**

- **`git config`** → comando para configurar opciones de Git.  
- **`--global`** → significa que la configuración aplica para **todo tu usuario** en el sistema (todos los repositorios que uses).  
  - Si no usas `--global`, solo aplica en el repositorio actual.  
- **`core.editor`** → es la opción que define **qué editor de texto Git debe abrir**.  
- **`"code --wait"`** → le estás diciendo que use **Visual Studio Code** como editor.  
  - `code` = el comando para abrir VS Code desde la terminal.  
  - `--wait` = le dice a Git que **espere a que cierres el editor antes de continuar**.  
    (Si no lo pones, Git podría seguir sin que hayas terminado de escribir el mensaje).  

## 6️⃣ Configurar colores en Git (opcional, pero recomendado)

Esto hace que la terminal se vea más clara al usar Git:

```bash
   git config --global color.ui auto
```

### 🔎 ¿Qué hace?

Ese comando **activa los colores en la salida de Git en la terminal**.  

Git muestra mensajes (como `git status`, `git diff`, `git log`) con partes resaltadas en color.  

Esto hace que sea **más fácil leer y entender** qué es nuevo, qué cambió, qué está agregado o eliminado.  

### 📌 Desglose del comando

- **`git config`** → sirve para configurar Git.  
- **`--global`** → aplica la configuración a **todo tu usuario en el sistema** (todos los repositorios).  
  - Si lo omites, solo aplica al repo actual.  
- **`color.ui`** → define cómo Git usará colores en la terminal.  
- **`auto`** → significa:  
  - Usa colores solo si la salida va a la terminal (no en scripts o redirecciones).  

### 🎨 Ejemplo práctico

Con `color.ui auto`:

- Archivos nuevos se ven en **verde**  
- Archivos eliminados en **rojo**  
- Mensajes de estado en diferentes colores según su tipo  

Sin colores → todo aparece en **blanco/gris**, y es más difícil distinguir cambios.  

## ✅ En resumen

Este comando hace que **Git use colores automáticamente en la terminal**, para que leer los estados, commits y diferencias sea mucho más claro y visual.

✅ ¡Listo! Ya tienes Git instalado y configurado.
