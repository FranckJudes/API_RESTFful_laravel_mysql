

# Laravel RESTful API

Cette application Laravel est une API RESTful simple pour gérer les articles (CRUD).

## Prérequis

- PHP >= 7.3
- Composer
- MySQL (ou toute autre base de données supportée par Laravel)

## Installation

1. Clonez le dépôt :
    ```sh
    git clone https://github.com/votre-utilisateur/votre-repo.git
    cd votre-repo
    ```

2. Installez les dépendances :
    ```sh
    composer install
    ```

3. Configurez votre fichier `.env` :
    ```plaintext
    cp .env.example .env
    ```
    Mettez à jour les informations de votre base de données dans le fichier `.env`.

4. Générez la clé d'application :
    ```sh
    php artisan key:generate
    ```

5. Exécutez les migrations de la base de données :
    ```sh
    php artisan migrate
    ```

## Utilisation

Démarrez le serveur de développement :
```sh
php artisan serve
```

L'API sera accessible à l'adresse `http://localhost:8000`.

### Routes de l'API

| Méthode | URI                | Action        | Description                         |
|---------|--------------------|---------------|-------------------------------------|
| GET     | /api/articles      | index         | Récupère tous les articles          |
| POST    | /api/articles      | store         | Crée un nouvel article              |
| GET     | /api/articles/{id} | show          | Récupère un article par ID          |
| PUT     | /api/articles/{id} | update        | Met à jour un article par ID        |
| DELETE  | /api/articles/{id} | destroy       | Supprime un article par ID          |

### Exemples de Requêtes

- **GET** `/api/articles`
    ```sh
    curl -X GET http://localhost:8000/api/articles
    ```

- **POST** `/api/articles`
    ```sh
    curl -X POST http://localhost:8000/api/articles \
    -H "Content-Type: application/json" \
    -d '{"title": "Mon Titre", "body": "Mon contenu"}'
    ```

- **GET** `/api/articles/{id}`
    ```sh
    curl -X GET http://localhost:8000/api/articles/1
    ```

- **PUT** `/api/articles/{id}`
    ```sh
    curl -X PUT http://localhost:8000/api/articles/1 \
    -H "Content-Type: application/json" \
    -d '{"title": "Titre mis à jour", "body": "Contenu mis à jour"}'
    ```

- **DELETE** `/api/articles/{id}`
    ```sh
    curl -X DELETE http://localhost:8000/api/articles/1
    ```

## Tests

Pour exécuter les tests, utilisez la commande suivante :
```sh
php artisan test
```

## Contribuer

Les contributions sont les bienvenues ! Veuillez soumettre une pull request ou ouvrir une issue pour discuter des changements que vous souhaitez apporter.

## Licence

Ce projet est sous licence MIT. Voir le fichier [LICENSE](LICENSE) pour plus de détails.

