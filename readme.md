<p align="center">
  <img src="https://git-scm.com/images/logos/downloads/Git-Icon-1788C.png" alt="Git Logo" width="80" height="80" />
  <img src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png" alt="GitHub Logo" width="80" height="80" />
</p>

# 🚀 Documentación del Flujo Básico de Git y GitHub

## Objetivo del Repositorio

Este repositorio fue creado como parte de una actividad para documentar y aplicar el flujo de trabajo esencial con **Git** y **GitHub** utilizando la terminal. Se incluyen los comandos paso a paso para inicializar un proyecto, gestionarlo localmente y subirlo a un repositorio remoto.

---

## 💻 Flujo de Trabajo Paso a Paso (Comandos de la Terminal)

Aquí se detalla el proceso completo, cumpliendo con las instrucciones 1 a 6 de la actividad.

### 1. Inicialización del Proyecto Local

Se crea la estructura básica del proyecto.

| Paso | Acción | Comando Utilizado |
| :--- | :--- | :--- |
| **1.1** | Crear la carpeta del proyecto | `mkdir mi-proyecto-github` |
| **1.2** | Navegar a la carpeta | `cd mi-proyecto-github` |
| **1.3** | Crear el archivo `index.html` | `touch index.html` |
| **1.4** | Agregar contenido simple a `index.html` | `echo "<h1>¡Mi Primer Repositorio con Git y GitHub!</h1>" > index.html` |

### 2. Configuración e Inicialización de Git

Se convierte la carpeta local en un repositorio de Git.

| Paso | Acción | Comando Utilizado |
| :--- | :--- | :--- |
| **2.1** | Inicializar el repositorio Git | `git init` |

### 3. Primeros Commits (Cumpliendo con 2 Commits Mínimos)

Se preparan y guardan los primeros cambios en el historial local.

| Paso | Acción | Comando Utilizado | Notas |
| :--- | :--- | :--- | :--- |
| **3.1** | Agregar `index.html` al área de *staging* | `git add index.html` | Prepara el archivo para el commit. |
| **3.2** | Realizar el **Primer Commit** | `git commit -m "Commit 1: Estructura inicial del index.html"` | Se guarda el primer estado del proyecto. |
| **3.3** | Agregar contenido adicional | `echo "<p>Este es un párrafo de prueba para el segundo commit.</p>" >> index.html` | Simulación de un cambio posterior. |
| **3.4** | Agregar el cambio al *staging* | `git add .` | Agrega todos los cambios pendientes. |
| **3.5** | Realizar el **Segundo Commit** | `git commit -m "Commit 2: Añadir párrafo de contenido de prueba"` | Se guarda el segundo cambio requerido. |

### 4. Creación de la Rama Principal y Conexión Remota

Se configura la rama principal como `master` y se establece el vínculo con GitHub.

| Paso | Acción | Comando Utilizado | Notas |
| :--- | :--- | :--- | :--- |
| **4.1** | Crear/Renombrar a la rama `master` | `git branch -M master` | Asegura que la rama principal sea `master`. |
| **4.2** | Conectar con el repositorio remoto | `git remote add origin <URL_DEL_REPOSITORIO_DE_GITHUB>` | Reemplazar `<URL_DEL_REPOSITORIO_DE_GITHUB>` con la URL real de tu repositorio. |
| **4.3** | Verificar la conexión remota (Opcional) | `git remote -v` | Muestra los remotos configurados. |

### 5. Subida del Proyecto a GitHub (Push)

Se envían los commits locales al repositorio remoto.

| Paso | Acción | Comando Utilizado | Notas |
| :--- | :--- | :--- | :--- |
| **5.1** | Subir el proyecto a GitHub | `git push -u origin master` | El flag `-u` establece la rama remota de seguimiento. Solo es necesario la primera vez. |

> ✅ **Resultado:** El repositorio está en GitHub, la rama principal es `master`, y se tienen al menos dos commits visibles, además del archivo `index.html` con contenido.

---

## ❓ Preguntas de Reflexión sobre Git

### Comandos Esenciales

| Pregunta | Respuesta |
| :--- | :--- |
| **¿Para qué sirve el comando `git status`?** | Muestra el estado del árbol de trabajo y el área de *staging*. Indica qué archivos han sido modificados, cuáles están listos para ser confirmados (*committed*), y cuáles no están siendo rastreados. |
| **¿Qué hace el comando `git add`?** | Mueve los cambios de uno o más archivos al **área de *staging*** (o índice), preparándolos para ser incluidos en el próximo `git commit`. |
| **¿Cuál es la diferencia entre `git add` y `git commit`?** | **`git add`** *prepara* los cambios para ser guardados (los pasa al área de *staging*). **`git commit`** *guarda* los cambios que están en el área de *staging* de forma permanente en el historial del repositorio local. |
| **¿Para qué se usa `git remote add origin`?** | Se usa para **vincular** el repositorio local de Git con un repositorio remoto, dándole el nombre de `origin` (el nombre estándar para el remoto principal). |
| **¿Qué hace el comando `git push`?** | Sube o envía los *commits* desde la rama local actual al repositorio remoto configurado. |
| **¿Qué hace `git checkout -b` comparado con `git checkout`?** | **`git checkout -b <nueva-rama>`** **crea** una nueva rama y **cambia** a ella inmediatamente. **`git checkout <rama-existente>`** solo **cambia** a una rama existente. |
| **¿Cómo puedes crear una nueva rama y cambiarte a ella al mismo tiempo?** | **`git checkout -b <nombre-de-la-rama>`** o **`git switch -c <nombre-de-la-rama>`**. |

### Conceptos Avanzados y de Inspección

| Pregunta | Comando(s) o Explicación |
| :--- | :--- |
| **¿Por qué es recomendable trabajar con ramas?** | Permite a los desarrolladores trabajar en nuevas características o corregir errores de forma **aislada** de la rama principal (producción), lo que garantiza estabilidad y facilita la revisión de código (Pull Requests) antes de la integración. |
| **¿Qué ocurre si se clona un repositorio que ya existe en tu máquina?** | Si intentas clonar en una carpeta que ya existe y no está vacía, Git te dará un error. Si la carpeta no existe, Git la crea y descarga el repositorio remoto. |
| **¿Cómo puedes ver todas las ramas locales y remotas?** | **`git branch -a`** |
| **¿Qué comando usas para eliminar un archivo del repositorio?** | **`git rm <archivo>`** (Lo elimina del sistema de archivos y del seguimiento de Git, y lo añade al *staging* para el próximo *commit*). |
| **¿Cómo ves el historial de commits en tu repositorio?** | **`git log`** |
| **¿Cómo puedes ver los últimos 3 commits en una sola línea cada uno?** | **`git log -3 --oneline`** |
| **¿Qué comando usas para ver el estado actual de tu repositorio?** | **`git status`** |
| **¿Cómo puedes ver los remotos configurados y sus URLs?** | **`git remote -v`** |
| **¿Qué comando te permite cambiar de rama?** | **`git checkout <nombre-de-la-rama>`** o **`git switch <nombre-de-la-rama>`** |