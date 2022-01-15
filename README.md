# Sistema di registrazione e autenticazione completa

- Registrazione user semlpice con username(unique) e password,nel database c'è anche il ruolo che però non è gestito in fase di registrazione
- Login con username e password
- Possibilità di creare dei recordi fittizi tramite data fixture in massa e in modo veloce
## Installazione

1-Cloniamo il progetto e rinominiamo il progetto come preferiamo
```bash

git clone git@github.com:eddya92/auth.git "nuovoNomeProgetto"

```



2-Installazione delle dipendenze con composer
```bash

composer install

```
Se non ci permette di fare questo perchè non abbiamo PHP 8 allora usiamo docker

Assicurati di aver installato [Docker](https://docs.docker.com/engine/installation/ "Install Docker") e [Docker Compose](https://docs.docker.com/compose/install/ "Install Docker Compose").

```bash
docker run --rm -it --volume $(pwd):/app prooph/composer:8.0 install
```
3-Cambiare .ENV e docker-compose.yaml per i valori del db

4-Avviamo Docker per adminer e db
```bash
docker-compose up -d
```

5-Avviamo il server di symfony 
```bash
symfony server:start -d
```







