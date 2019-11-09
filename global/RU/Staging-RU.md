<h1> Начиная </h1>
<h4> Этот документ покажет вам, как создать промежуточную среду для работы со Sphinx и прочитать документы. </h4>

1. Если у вас уже есть Python, установите Sphinx:

```bash
sudo pip install sphinx sphinx-autobuild
```

2. Создайте каталог внутри вашего проекта для хранения ваших документов:

```bash
cd /path/to/project
mkdir docs
```

3. Запустите там sphinx-quickstart:

```bash
cd docs
sphinx-quickstart
```

4. Это поможет вам создать базовую конфигурацию; в большинстве случаев вы можете просто принять значения по умолчанию. Когда это будет сделано, у вас будут *index.rst*, *conf.py* и некоторые другие файлы. Добавьте их в контроль версий. Теперь отредактируйте ваш *index.rst* и добавьте некоторую информацию о вашем проекте. Включите столько деталей, сколько хотите. Построить их, чтобы увидеть, как они выглядят:

```
make html
```

**Примечание:** *Вы можете использовать sphinx-autobuild для автоматической перезагрузки ваших документов. Запустите sphinx-autobuild. Вместо этого _build / html.*

5. Чтобы публиковать только соответствующие файлы кода, но НЕ создавать каталоги _static & _templates - добавьте .gitignore в корневой каталог. Образец ниже

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

6. Отредактируйте свои файлы, чтобы перестроить, пока вам не понравится то, что вы видите, затем зафиксируйте ваши изменения и отправьте их в ваш публичный репозиторий. Как только вы получите **Sphinx** документацию в публичном хранилище, вы можете начать использовать **Read Docs**.
