### 79. ¿Cómo identificaste el comando necesario cuando la práctica no lo proporcionó?
Analicé la acción que debía realizar (por ejemplo, crear un entorno, inicializar Git o registrar un cambio) y busqué el comando correspondiente en la documentación oficial o en la ayuda de la terminal usando `--help`. Esto me permitió comprender la función antes de ejecutarla.

### 80. ¿Qué diferencia existe entre preparar un archivo para un commit y crear el commit?
Preparar un archivo (`git add`) significa incluirlo en el área de preparación para registrar sus cambios. Crear el commit (`git commit`) guarda definitivamente esos cambios en el historial del repositorio con un mensaje descriptivo.

### 81. ¿Cómo puedes comprobar en qué rama estás trabajando?
Con el comando:
```bash
git branch
```
La rama activa aparece marcada con un asterisco (*). También puede verse en la barra inferior de Visual Studio Code.

### 82. ¿Cómo puedes determinar qué archivos fueron modificados antes de registrarlos?
Usando:
```bash
git status
```
Este comando muestra los archivos nuevos, modificados o eliminados que aún no han sido preparados para commit.

### 83. ¿Cómo puedes observar exactamente qué cambió dentro de un archivo?
Con:
```bash
git diff
```
Este comando muestra línea por línea las diferencias entre la versión anterior y la actual del archivo.

### 84. ¿Por qué debe reconstruirse .venv después de obtener un repositorio?
Porque el entorno virtual no se comparte en GitHub (está en `.gitignore`). Cada colaborador debe crear su propio entorno local y usar `requirements.txt` para instalar las mismas dependencias.

### 85. ¿Qué relación existe entre requirements.txt y .gitignore?
`requirements.txt` registra las dependencias necesarias del proyecto, mientras que `.gitignore` evita subir el entorno virtual que las contiene. Así se comparte solo la lista de paquetes, no los archivos del entorno.

### 86. ¿Por qué la colaboración se realiza desde una rama y no directamente desde main?
Para mantener la estabilidad del proyecto principal. Las ramas permiten desarrollar y probar cambios sin afectar la versión oficial hasta que se revisen y aprueben mediante un Pull Request.

### 87. ¿Por qué una solicitud de cambios no requiere crear un Pull Request nuevo?
Porque los cambios se realizan en la misma rama del Pull Request existente. Al actualizar esa rama, GitHub refleja automáticamente las nuevas modificaciones en la solicitud original.

### 88. Después de realizar el merge en GitHub, ¿por qué todavía es necesario actualizar el repositorio local?
Porque el merge ocurre en el repositorio remoto. Para tener la versión más reciente en la computadora local, se debe ejecutar:
```bash