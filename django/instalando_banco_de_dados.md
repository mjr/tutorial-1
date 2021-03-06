# Instalação de um banco de dados

Há vários softwares de banco de dados diferentes que pode armazenar dados para o seu site. Nós vamos usar o padrão, `sqlite3`.

Isto já está configurado nesta parte do seu arquivo `AfroPython/settings.py`:

```

DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.sqlite3',
        'NAME': os.path.join(BASE_DIR, 'db.sqlite3'),
    }
}
```

Para criar um banco de dados para o nosso blog, vamos fazer o seguinte no console. Digite:

```
python3 manage.py migrate
```

Precisamos estar no diretório que contém o arquivo `manage.py` dentro da pasta `afropython`.
Se isso der certo, você deve ver algo como isto:

```
...@AfroPython:/mnt/project$ python3 manage.py migrate
Operations to perform:
  Apply all migrations: admin, contenttypes, auth, sessions
Running migrations:
  Applying contenttypes.0001_initial... OK
  Applying auth.0001_initial... OK
  Applying admin.0001_initial... OK
  Applying sessions.0001_initial... OK
```

E está pronto! Hora de iniciar o servidor web e ver se nosso site está funcionando!

Acesse o ícone na lateral esquerda da tela. Uma nova guia/aba vai abrir no seu navegador.

![Abrir o projeto](django/abrir_site.png)

Parabéns! Você criou seu primeiro site e o executou usando um servidor de web! Não é impressionante?

![Site início](django/servidor_rodando.png)

Pronto(a) para o próximo passo? Está na hora de criar algum conteúdo!
