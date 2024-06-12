<h1> Commencer </h1>
<h4> Ce document vous montrera comment créer un environnement intermédiaire pour travailler avec Sphinx & Read the Docs </h4>

1. En supposant que vous ayez déjà Python, installez Sphinx:

```bash
pip3 install sphinx sphinx-autobuild
```

2. Créez un répertoire dans votre projet pour contenir vos documents:

```bash
cd /path/to/project
mkdir docs
```

3. Exécuter `sphinx-quickstart` là-bas:

```bash
cd docs
sphinx-quickstart
```

4. Cela vous guidera à travers la création de la configuration de base; dans la plupart des cas, vous pouvez simplement accepter les valeurs par défaut. Quand c'est fait, vous aurez un *index.rst*, un *conf.py* et quelques autres fichiers. Ajoutez-les au contrôle de révision. Maintenant, éditez votre *index.rst* et ajoutez des informations sur votre projet. Inclure autant de détails que vous le souhaitez. Construisez-les pour voir à quoi ils ressemblent:

```
make html
```

**Remarque:** *Vous pouvez utiliser sphinx-autobuild pour recharger automatiquement vos documents. Exécutez sphinx-autobuild. _build / html à la place.*

5. Pour publier uniquement les fichiers de code pertinents, mais PAS les répertoires `build`, `_static` & `_templates`, veuillez ajouter un .gitignore dans le répertoire racine. Un échantillon est ci-dessous

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

6. Modifiez vos fichiers pour reconstruire jusqu'à ce que vous souhaitiez voir ce que vous voyez, puis validez vos modifications et transmettez-les à votre référentiel public. Une fois que vous avez la documentation **Sphinx** dans un référentiel public, vous pouvez commencer à utiliser **Lire la documentation**.
