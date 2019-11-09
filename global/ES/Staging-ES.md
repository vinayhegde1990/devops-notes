<h1>Empezando</h1>
<h4> Este documento le mostrará cómo crear un entorno de ensayo para trabajar con Sphinx y leer los documentos </h4>

1. Suponiendo que ya tiene Python, instale Sphinx:

```bash
sudo pip install sphinx sphinx-autobuild
```

2. Crea un directorio dentro de tu proyecto para guardar tus documentos:

```bash
cd /path/to/project
mkdir docs
```

3. Ejecute sphinx-quickstart allí:

```bash
cd docs
sphinx-quickstart
```

4. Esto lo guiará a través de la creación de la configuración básica; en la mayoría de los casos, solo puede aceptar los valores predeterminados. Cuando termine, tendrá un *index.rst*, un *conf.py* y algunos otros archivos. Agregue estos al control de revisión. Ahora, edite su *index.rst* y agregue información sobre su proyecto. Incluye tantos detalles como quieras. Construirlos para ver cómo se ven:

```
make html
```

**Nota:** *Puede usar sphinx-autobuild para recargar automáticamente sus documentos. Ejecute sphinx-autobuild. _build / html en su lugar*

5. Para publicar solo archivos de código relevantes pero NO compilar directorios _static y _templates - agregue un .gitignore en el directorio raíz. Una muestra está debajo

```python
#Folders to ignore
build
_templates
_static

#Extensions to ignore
*.pyc
*.diff
*.err
*.orig
*.rej
*.swo
*.swp
*.vi
*.cache
*.egg-info
*~
*#

#Logs and database files to be ignored
*.log
*.sql
*.sqlite

#OS or Editor folders
.DS_Store
Thumbs.db
.cache
.project
.settings
.tmproj
*.esproj
nbproject
*.sublime-project
```

6. Edite sus archivos para reconstruir hasta que le guste lo que ve, luego confirme los cambios y envíelos a su repositorio público. Una vez que tenga la documentación de **Sphinx** en un repositorio público, puede comenzar a usar **Leer los documentos**
