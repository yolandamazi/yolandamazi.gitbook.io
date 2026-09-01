# Cómo subir proyectos a GitHub

#### 1. Crea un repositorio en GitHub

En GitHub crea un repositorio nuevo. Importante: si tu proyecto ya existe localmente, crea el repositorio vacío (sin README, .gitignore ni licencia)

#### 2. Abre una terminal dentro de tu proyecto

```
cd ruta/de/tu/proyecto
```

#### 3. Inicializa Git

```
git init
```

#### 4. Añade tus archivos y crea el primer commit

```
git add .
git commit -m "Primer commit" 
```

#### 5. Conecta tu proyecto con GitHub

GitHub te dará una URL parecida a: https://github.com/TU\_USUARIO/mi-proyecto.git

Ejecuta:

```
git remote add origin https://github.com/TU_USUARIO/mi-proyecto.git
```

Puedes comprobar que quedó conectado con:

```
git remote -v
```

#### 6. Sube el proyecto

```
git branch -M main git push -u origin main
```

Y listo. Tu proyecto local estará en GitHub.

#### 7. Cada vez que modifiques el proyecto

```
cd ruta/de/tu/proyecto
git init
git add .
git commit -m "Descripción de los cambios"
git push
```
