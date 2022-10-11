## Docker - comenzi utile

#### Listari diverse

- Listare containere active

```shell
$ docker ps
```

- Listarea tuturor containerelor (active + inactive)

```bash
$ docker ps -a
```

- Listare imagini conectate de un container

```bash
$ docker image ls
```

- Listarea tuturor imaginilor (conectate sau neconectate de un container)

```bash
$ docker image ls -a
```

#### Creare imagini

```bash
$ docker build -t nume-imagine:tag .
```

#### Rulare containere

- Rulare container in fundal

```bash
$ docker run -d --name nume-container nume-imagine:tag
```
- Rulare container temporar (dupa inchidere containerul va fi sters)

```bash
$ docker run --rm --name nume-container nume-imagine:tag
```

- Rulare container temporar cu variabila

```bash
$ docker run -e nrs=1 --rm --name nume-container nume-imagine:tag
```

#### Stergere obiecte

- Sterge imagini neconectate de nici un container

```bash
$ docker image prune --filter "dangling=true"
```

- Sterge imagini mai vechi de un numar de ore

```bash
$ docker image prune --filter "until=3600h"
```

#### Diverse

- Conectare la terminalul unui container

```bash
$ docker exec -it nume-container bash
```

- Listare loguri container

```bash
$ docker logs -f nume-container
```
