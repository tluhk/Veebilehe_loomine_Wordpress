# Worpdressi arenduskeskkond

## Keskkond WordPressi arendamiseks

WordPressi mugavaks arendamiseks on mitmedi võimalusi, mida saab suures plaanis jagada kaheks: oma arvutis või serveris (isiklik või teenusepakkuja oma).

Serveris majutatud WordPressi lehekülje arendamiseks on vaja mingil viisil serverile ligipääsu (näiteks ftp), et oleks võimalik serverisse üles laadida muudetud faile.

Kohalikus arvutis arendades on võimalik seada arenduskeskkond üles nii, et WordPressi failidele on võimalik ka otse ligi pääseda, ilma, et oleks vaja neid kuidagi eraldi liigutada.

Erinevate võimalustest arenduskeskkondade valikust saab lugeda [siit](https://make.wordpress.org/core/handbook/tutorials/installing-a-local-server/).

# Arenduskeskkond Dockeris

Üks väga mugav viis oma arvutis Wordpress tööle saada, on kasutada selleks `Docker`it.

Docker on tarkvara, mis võimaldab luua ja kasutada erinevaid virtuaalseid masinaid. Dockeri abil on võimalik luua erinevaid keskkondi, mis on eraldatud üksteisest ja ei sega üksteise tööd. Näiteks on võimalik luua eraldi keskkond, kus töötab WordPress ja teine keskkond, kus töötab MySQL andmebaas.

Mis on Docker ja kuidas see töötab, saab vaadata näiteks [siit](https://youtu.be/aLipr7tTuA4).

Selleks, et arvutis saaks Dockerit kasutada, tuleks kõigepealt paigaldada `Docker Desktop` rakendus.

> NB! Võib juhtuda, et `Docker Desktop`-i paigaldamisel nõutakse veel mingi lisatarkvara paigaldamist (_WSL2_). Kui see nii on, siis tuleks see ka paigaldada.

Selle saab alla laadida [siit](https://docs.docker.com/desktop/).

Kuna WordPressi arenduskeskkond vajab töötamiseks mitut erinevat teenust (PHP, andmebass, WordPressi kood), siis kõige mugavam on kasutada selleks Dockeri poolt pakutavat tööriista `docker-compose`, mis võimaldab korraga käivitada mitu konteinerit ja võimaldab neil konteineritel omavahel suhelda. Nende konteinerite loomiseks ja omavaheliste seoste seadistamiseks kasutatakse `docker-compose.yml` faili. Õnneks ei ole meil endal vaja sellega väga palju vaeva näha, kuna meie eest on see töö juba ära tehtud ja saame kasutada juba loodud faili, mille saab kopeerida [siit](https://hub.docker.com/_/wordpress).

Fail ise näeb välja selline:

```yml
services:
  wordpress:
    image: wordpress
    restart: always
    ports:
      - 8080:80
    environment:
      WORDPRESS_DB_HOST: db
      WORDPRESS_DB_USER: exampleuser
      WORDPRESS_DB_PASSWORD: examplepass
      WORDPRESS_DB_NAME: exampledb
    volumes:
      - wordpress:/var/www/html

  db:
    image: mysql:8.0
    restart: always
    environment:
      MYSQL_DATABASE: exampledb
      MYSQL_USER: exampleuser
      MYSQL_PASSWORD: examplepass
      MYSQL_RANDOM_ROOT_PASSWORD: "1"
    volumes:
      - db:/var/lib/mysql

volumes:
  wordpress:
  db:
```

Selleks, et WordPress nüüd oma arvutis tööle saada, tuleks eelnevalt kirjeldatud `docker-compose.yml` salvestada oma arvutisse vabalt valitud kausta ja seal kaustas olles käsurealt käivitada käsk: `docker compose up -d`

Seejärel tuleb veebilehitsejas minna aadressile: `http://localhost:8080/` ja järgida juhiseid WordPressi paigaldamiseks.
