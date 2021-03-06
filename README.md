# Oberlin College Django Project Template

For starting new projects. This template is appropriate for **development** only and *not* **production** or **staging**.

To get started, we generally do something like this (assuming [virtualenvwrapper][] and [pip][] are installed):

```bash
mkvirtualenv <virtualenv_identifier>
pip install django==1.4
django-admin.py startproject <project_name> --template=/path/to/oberlin-project-template/project_template
pip install -r <project_name>/requirements.txt
```

To use `./manage.py` instead of `python manage.py`:

```bash
chmod u+x manage.py
```

When using applications that rely on South, it's best to avoid running migrations at all for the first `syncdb`. The following commands should work:

```bash
./manage.py syncdb --all
./manage.py migrate --fake
```

[virtualenvwrapper]: http://www.doughellmann.com/docs/virtualenvwrapper/
[pip]: http://www.pip-installer.org/