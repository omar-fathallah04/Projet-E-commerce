# Application e-commerce Django

C'est une application web développée avec Django pour gérer des produits et des catégories.
La base de données que j'ai utilisé est PostgreSQL.

---

## Installation

```bash
python3 -m venv env
source env/bin/activate
pip install django pillow psycopg2-binary
```

---

## Configuration de la base de données (PostgreSQL)

Créer la base de données :

```bash
psql -d postgres -c "CREATE DATABASE ecommerce_db;"
```

Dans `ecommerce/settings.py`, renseigner vos informations :

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'ecommerce_db',
        'USER': 'votre_utilisateur',
        'PASSWORD': '',
        'HOST': '',
        'PORT': '',
    }
}
```

---

## Lancement

```bash
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```

---

## Pages disponibles

| Adresse | Description |
|---|---|
| /products/ | liste des produits |
| /products/<id> | detail d'un produit |
| /products/categories/ | liste des categories |
| /products/category/<id>/ | produits d'une categorie |
| /admin/ | interface d'administration |

---

## Remarque

A chaque modification des modeles, relancer :

```bash
python manage.py makemigrations
python manage.py migrate
```
