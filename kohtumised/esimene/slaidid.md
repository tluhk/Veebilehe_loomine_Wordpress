---
marp: true
theme: default
backgroundImage: url('../../../files/HaapsaluK_est.png')
backgroundPosition: 20px calc(100% - 20px)
backgroundSize: 250px
---

# Veebirakenduste loomine Wordpressi platvormil

Laura Hein, Martti Raavel

---

## Esimene kohtumine

- [Mis on internet?](../teemad/Internet/about.md)
- [Mis on veebileht?](../teemad/Veebileht/about.md)
- [Mis on Wordpress?](../teemad/Wordpress/about.md)
- [Wordpressi kasutamise eelised ja miinused](../teemad/plussidMiinused/about.md)
- [Wordpress.com vs Wordpress.org](../teemad/WordpressVSWordpress/about.md)
- [Wordpressi majutamine](../teemad/WordpressiMajutamine/about.md)

---

## Mis on internet?

Arvutivõrkude võrkude võrk

- Arvutivõrgud
- Serverid ja kliendid
- Domeeninimed ja IP aadressid, DNS
- Protokollid
- ISP
- Ruuterid

---

# Mis on veebileht?

Veebileht on kogum faile, mis on üldjuhul kättesaadavad internetis ühe konkreetse domeeni (näiteks *www.tlu.ee*) all. Need failid võivad sisaldada **teksti**, **pilte**, **videoid**, **helifaile** ja muud meediat, samuti **koodi**, mis määrab, kuidas need elemendid kasutajale esitatakse. Veebilehti näidatakse kasutajale veebilehitseja abil, mis tõlgendab veebilehe koodi ja kuvab selle sisu kasutajaliideses.

---

## HTML

HTML (HyperText Markup Language) on märgendikeel, mida kasutatakse veebilehe ja selle sisu struktureerimiseks.

HTML määrab veebilehe sisu struktuuri.

---

## CSS

Põhimõtteliselt on tegemist keelega, mis kirjeldab seda, kuidas veebileht välja peab nägema - kui HTML kirjeldab sisu, siis CSS kirjeldab välimust.

---

## Javascript

![Kook](./cake.png)

---

## Mis on Wordpress?

Wordpress on avatud lähtekoodiga maailma kõige populaarsem sisuhaldussüsteem (CMS - Content Management System), mida kasutatakse veebilehtede loomiseks. WordPressi enda väitel on 43% veebilehtedest tehtud just WordPressi kasutades.

---

## Mis on sisuhaldussüsteem?

Sisuhaldussüsteem (Content Management System ehk CMS) on tarkvararakendus või -platvorm, mis võimaldab kasutajatel luua, hallata ja avaldada digitaalset sisu, tavaliselt veebisaitide ja blogide jaoks

---

## Wordpress.org vs Wordpress.com

- Wordpress.org tegeleb tarkvara arendamisega
- Wordpress.com pakub majutusteenust

---

## Wordpressi kasutamise eelised ja miinused

---

## Wordpressi kasutamise eelised

- **Lihtne kasutada**: WordPress on kasutajasõbralik ja seda on lihtne õppida.
- **Paindlikkus**: Saab luua igat tüüpi veebisaite, lihtsatest blogidest kuni keerukate e-poodideni.
- **Lai valik teemasid ja pluginad**: On olemas tuhandeid tasuta ja tasulisi teemasid ja pluginad, mis võimaldavad kohandada oma veebisaiti vastavalt vajadusele.
- **Aktiivne kogukond**: Suur ja aktiivne arendajate ja kasutajate kogukond tähendab palju tugimaterjale, foorumeid ja kolmanda osapoole tööriistu.
- **SEO-sõbralik**: WordPress on loodud olema SEO-sõbralik ja paljud pluginad, nagu _Yoast SEO_, pakuvad täiendavaid SEO funktsioone.
- **Täielik kontroll**: WordPress.org pakub täielikku kontrolli veebisaidi üle, alates kohandamisest kuni andmete haldamiseni.
- **Avatud lähtekood**: Võimaldab arendajatel teha vajadusel muudatusi ja kohandusi.

---

## Wordpressi kasutamise miinused

- **Turvalisus**: Populaarsus teeb WordPressi atraktiivseks sihtmärgiks ründajatele.
- **Hooldus**: Kui kasutate WordPress.org versiooni, peate ise hoolitsema veebisaidi uuenduste, varukoopia ja turvalisuse eest.
- **Kvaliteedi varieeruvus**: Kuna teemasid ja pluginaid saab arendada igaüks, võib nende kvaliteet olla ebaühtlane.
- **Kiiruse probleemid**: Mõned teemad ja pluginad võivad veebisaidi aeglaseks muuta, eriti kui need on halvasti kirjutatud.
- **Tehniline oskus**: Kuigi WordPress on kasutajasõbralik, võivad mõned tehnilised ülesanded olla algajatele keerulised.
- **Kulud võivad kuhjuda**: Kuigi WordPressi tarkvara ise on tasuta (WordPress.org puhul), võivad kulud kuhjuda, kui hakkate ostma tasulisi teemasid, pluginad, ja veebimajutust.

---

## Wordpressi majutamine

Kui tahta teha omale Wordpressi abiga veebileht, siis ilmselt on vaja see ka internetis avalikult kättesaadavaks teha. Selleks on vaja leida endale sobiv majutusteenuse pakkuja.

Eestis pakuvad WordPressi majutamise võimalust näiteks:

- [Zone](https://www.zone.ee/)
- [Veebimajutus.ee](https://www.veebimajutus.ee/paketid-ja-hinnad)
- [Hostinger](https://www.hostinger.ee/parim-wordpress-veebimajutus)

---

## Või siis hoopis lokaalne paigaldus

Lokaalne paigaldus tähendab seda, et seame oma arvutisse üles WordPressi keskkonna, kus saame harjutada ja katsetada ilma, et peaksime kohe veebisaiti avalikult kättesaadavaks tegema. See on eriti kasulik siis, kui soovime õppida WordPressi kasutamist või arendada oma veebilehte enne selle avalikustamist.

---

## Dockeri kasutamine

Docker on platvorm, mis võimaldab arendajatel luua, testida ja juurutada rakendusi konteinerites. Docker võimaldab meil luua isoleeritud keskkonna, kus saame paigaldada WordPressi ja selle sõltuvused ilma, et see mõjutaks meie arvuti teisi rakendusi või süsteemi.

---

## Dockeri paigaldamine ja kasutamine

- Docker Desktopi allalaadimine ja paigaldamine
- WordPressi konteineri loomine ja käivitamine Dockeris
- WordPressi veebilehele ligipääs ja selle haldamine

---

## Mis variandid veel on?

Kui hetkel juba mõnda sobivat teenusepakkujat ei ole olemas ja tahaks lihtsalt katsetada ja harjutada, siis saab kasutada näiteks:

## https://byet.host/

---

## Byet kasutaja registreerimine

- Kasutaja registreerimine
- Kasutaja aktiveerimine
- Halduspaneel
- Wordpressi paigaldamine
- Wordpressile ligipääs
