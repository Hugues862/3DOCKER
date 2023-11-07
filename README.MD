# Guide de déploiement de l'application de vote

## Démarrage

1. Décompressez l'archive ZIP de l'application de vote dans un dossier de votre choix sur votre machine.

2. Construisez et lancez les conteneurs avec Docker Compose :

   ```bash
   docker-compose up -d --build
   ```

   L'option `-d` vous permet de lancer les conteneurs en mode détaché elle est optionnelle.

## Accès aux applications

Une fois que les conteneurs sont lancés, vous pouvez accéder aux applications Vote et Résultat via votre navigateur web :

- **Application de Vote :** Ouvrez votre navigateur web et allez sur `http://localhost:5001`. Vous devriez voir l'interface de vote.

- **Application de Résultat :** Pour voir les résultats des votes, allez sur `http://localhost:3000` dans votre navigateur web.

## Arrêter les applications

Pour arrêter et supprimer les conteneurs et les réseaux créés par `docker-compose up`, exécutez la commande suivante :

```bash
docker-compose down
```

