```
git clone git@github.com:helloedvaldo/django-default.git NOME_DO_PROJETO
cd NOME_DO_PROJETO
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
cp contrib/env-sample .env
./contrib/secret_gen.py
```

Edite o arquivo .env conforme necessário:

```
nano .env
```

```
SECRET_KEY=INSIRA_SUA_KEY_GERADA_AQUI
DEBUG=True
ALLOWED_HOSTS=*
DEFAULT_FROM_EMAIL=exemplo@exemplo.com

EMAIL_BACKEND=django.core.mail.backends.console.EmailBackend
EMAIL_HOST=localhost
EMAIL_PORT=25
EMAIL_USE_TLS=False
EMAIL_HOST_USER=
EMAIL_HOST_PASSWORD=
```

```
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```
