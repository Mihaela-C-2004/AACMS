# Tema Docker Compose - WordPress + MySQL

## Cerinta
Ruleaza un WordPress functional si o baza de date MySQL prin Docker Compose, folosind doua servicii.

## Pornire
1. Instaleaza Docker Desktop si porneste-l.
2. Deschide un terminal in folderul ce contine `compose.yaml`.
3. Ruleaza `docker compose up -d`.
4. Verifica cu `docker compose ps`.
5. Deschide http://localhost:8080, alege limba, numele site-ului, contul administratorului si parola administratorului.
6. Verifica pagina de administrare la http://localhost:8080/wp-admin.

## Configurarea bazei de date
WordPress primeste automat valorile din `compose.yaml`:
- host: db
- baza de date: sdlda
- utilizator: sdlda
- parola: sdlda

Contul de administrator WordPress se alege separat, in browser.

## Comenzi
- `docker compose ps` - starea containerelor
- `docker compose logs -f` - jurnale (Ctrl+C pentru iesire)
- `docker compose down` - oprire si eliminare containere, dar volumele se pastreaza
- `docker compose up -d` - repornire
- `docker compose down -v` - resetare COMPLETA, sterge datele din volume!