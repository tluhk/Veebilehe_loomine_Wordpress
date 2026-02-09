# Mall

## Mis on WordPressi mall?

WordPressis viitavad "mallid" ("templates" inglise keeles) failidele, mis määravad kindlaks, kuidas teie veebisaidi sisu kuvatakse brauseris. Mallid on WordPressi teemade lahutamatu osa ja võimaldavad luua erineva kujundusega postitusi, lehekülgi ja muid sisutüüpe.

**Klassikaliste** teemade puhul on need PHP-failid, mis sisaldavad HTML-i, mallisiltide ja PHP-koodi segu.

**Plokiteemade** puhul on need HTML-failid, mis sisaldavad plokke esindavaid HTML-i märgistusi.

Teema loomisel kasutatakse mallifaile, et mõjutada veebisaidi erinevate osade paigutust ja kujundust. Näiteks kasutatakse päise loomiseks päisemalli või malliosa.

Kui keegi külastab teie veebisaidi lehte, laadib WordPress päringu alusel malli. Mallifailis kuvatava sisu tüüp määratakse mallifailiga seotud postituse tüübi järgi. Mallihierarhia kirjeldab, millist mallifaili WordPress laadib, lähtudes päringu tüübist ja sellest, kas mall on teemas olemas. Seejärel parsib server mallis oleva koodi ja tagastab külastajale HTML-i.

Kõige kriitilisem mallifail on **index**, mis on kõikehõlmav mall, kui malli hierarhiast ei leita täpsemat malli. Kuigi teema vajab ainult index-malli, sisaldavad teemad tavaliselt palju malle erinevate sisutüüpide ja kontekstide kuvamiseks.

Lühidalt on WordPressi mallid viis, kuidas kontrollida, kuidas teie veebisaidi sisu kuvatakse. Kui soovite muuta saidi kujundust või funktsionaalsust, peate tõenäoliselt muutma või looma uusi malle oma aktiivses teemas.

## Malli osad

Malliosa on osa mallist, mis sisaldub mõne teise malli osana, näiteks saidi päises. Malli osa saab manustada mitmesse malli, mis lihtsustab teema loomist. Tavalised malliosad hõlmavad järgmist:
- header.php või header.html saidi päise loomiseks
- footer.php või footer.html jaluse genereerimiseks
- sidebar.php või sidebar.html külgriba loomiseks

Kuigi ülaltoodud mallifailid on WordPressis erijuhtumid ja kehtivad ainult ühele lehe osale, saab luua suvalise arvu malliosasid ja lisada need teistesse mallifailidesse.

## Levinud WordPressi mallifailid

Allpool on loetelu põhilistest teemamallidest ja -failidest, mille WordPress tunneb.

- **index.php** - Peamine mallifail. See on nõutav kõigi teemade puhul.
- **style.css** - Peamine stiilileht. See on nõutav kõigi teemade puhul ja sisaldab teema teabepäist.
- **rtl.css** - Paremalt vasakule laaditav laaditabel kaasatakse automaatselt, kui veebisaidi keele teksti suund on paremalt vasakule.
- **front-page.php** (klassikaline teema) või **front-page.html** (plokiteema) - Esilehe malli kasutatakse alati saidi esilehena, kui see on olemas, olenemata sellest, millised seaded jaotises Administraator > Seaded > Lugemine.
- **home.php** (klassikaline teema) või **home.html** (plokiteema) - Avalehe mall on vaikimisi esileht. Kui te ei määra WordPressi staatilist esilehte kasutama, kasutatakse viimaste postituste kuvamiseks seda malli.
- **singular.php** (klassikaline teema) või **singular.html** (plokiteema) - Ainsuse malli kasutatakse postituste jaoks, kui faili single.php ei leitud, või lehtede jaoks, kui lehekülge page.php ei leita. Kui ainsus.php-d ei leita, kasutatakse faili index.php.
- **single.php** (klassikaline teema) või **single.html** (plokiteema) - Ühe postituse malli kasutatakse siis, kui külastaja taotleb ühte postitust.
- **single-{post-type}.php** (klassikaline teema) või **single-{post-type}.html** (plokiteema) - Ühe postituse mall, mida kasutatakse siis, kui külastaja taotleb kohandatud postituse tüübist üksikut postitust. Näiteks single-book.php kasutatakse üksikute postituste kuvamiseks kohandatud postitustüübist nimega raamat.
- **archive-{post-type}.php** (klassikaline teema) või **archive-{post-type}.html** (plokiteema) - Arhiivi postituse tüübi malli kasutatakse siis, kui külastajad taotlevad kohandatud postitustüübi arhiivi. Näiteks faili archive-books.php kasutatakse kohandatud postituste tüübist nimega raamatud pärinevate postituste arhiivi kuvamiseks. Arhiivimalli faili kasutatakse juhul, kui archive-{post-type} malli pole.
- **page.php** (klassikaline teema) või** page.html** (plokiteema) - Lehemalli kasutatakse siis, kui külastajad taotlevad üksikuid lehti, mis on sisseehitatud mall.
- **page-{slug}.php** (klassikaline teema) või **archive-{post-type}.html** (plokiteema) - Lehe slug malli kasutatakse siis, kui külastajad taotlevad konkreetset lehte, näiteks lehte, millel on slug „teave” (page-about.php).
- **category.php** (klassikaline teema) või **category.html** (plokiteema) - Kategooriamalli kasutatakse siis, kui külastajad taotlevad postitusi kategooriate kaupa.
- **tag.php** (klassikaline teema) või **tag.html** (plokiteema) - Sildi malli kasutatakse siis, kui külastajad taotlevad postitusi sildi järgi.
- **taxonomy.php** (klassikaline teema) või **taxonomy.html** (plokiteema) - Taksonoomia termini malli kasutatakse siis, kui külastaja taotleb kohandatud taksonoomias terminit.
- **author.php** (klassikaline teema) või **author.html** (plokiteema) - Autorilehe malli kasutatakse alati, kui külastaja laadib autorilehe.
- **date.php** (klassikaline teema) või **date.html** (plokiteema) - Kuupäeva/kellaaja malli kasutatakse siis, kui postitusi taotletakse kuupäeva või kellaaja järgi. Näiteks nende slug-idega loodud lehed:
  - http://example.com/blog/2014/
  - http://example.com/blog/2014/05/
  - http://example.com/blog/2014/05/26/
- **archive.php** (klassikaline teema) või **archive.html** (plokiteema) - Arhiivimalli kasutatakse siis, kui külastajad taotlevad postitusi kategooria, autori või kuupäeva järgi. Märkus. See mall alistatakse, kui on olemas täpsemad mallid, nagu kategooria.php, autor.php ja date.php.
- **search.php** (klassikaline teema) või **search.html** (plokiteema) - Otsingutulemuste malli kasutatakse külastaja otsingutulemuste kuvamiseks.
- **attachment.php** (klassikaline teema) või **attachment.html** (plokiteema) - Manusemalli kasutatakse üksiku manuse (nt pildi, pdf-i või muu meediumifaili) vaatamisel.
- **image.php** (klassikaline teema) või **image.html** (plokiteema) - Pildimanuse mall on faili attachment.php spetsiifilisem versioon ja seda kasutatakse üksiku pildimanuse vaatamisel. Kui seda pole, kasutab WordPress selle asemel attachment.php-d.
- **404.php** (klassikaline teema) või **404.html** (plokiteema) - Malli 404 kasutatakse siis, kui WordPress ei leia postitust, lehte või muud sisu, mis vastaks külastaja soovile.
- **kommentaarid.php** - Klassikaliste teemade kommentaaride mall. Plokiteemade puhul kasutatakse selle asemel plokke.

## Wordpressi malli hierarhia

https://developer.wordpress.org/files/2014/10/Screenshot-2019-01-23-00.20.04.png
