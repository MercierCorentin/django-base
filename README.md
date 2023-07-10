# Tuto Open classroom sur Django

Lien du tuto: https://openclassrooms.com/fr/courses/7172076-debutez-avec-le-framework-django

## Démarer le projet

Avec Docker:

```bash
# Construire l'image
sudo docker compose build
# Lancer le projet
sudo docker compose up -d
```

**Ou** avec un environnement virtuel:

```bash
python3 -m venv env
source env/bin/activate
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
```

## Gestion de la DB

```bash
# Création des tables dans la db
docker compose exec web python manage.py migrate
# Création d'un super user
docker compose exec web python manage.py createsuperuser
```