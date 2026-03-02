---
marp: true
theme: default
backgroundImage: url('../../files/HaapsaluK_est.png')
backgroundPosition: 20px calc(100% - 20px)
backgroundSize: 250px
---

# Veebirakenduste loomine Wordpressi platvormil

Laura Hein, Martti Raavel

---

## Teine kohtumine

- Veendume, et kõigil on võimalus Wordpressi kasutada
- Wordpressi halduspaneel
- Postitus vs Lehekülg
- Mallid
- Kuidas WP otsustab, millist malli kasutada?
- Plokid ja plokimustrid
- Teemad

---

---

## Wordpressi halduspaneeli kasutajaliides

![height:450](admin-panel.png)

---

# Postitus vs Lehekülg

Vaikimis on Wordpressis kahte erinevat tüüpi sisu: **postitused** ja **leheküljed**.

Postitused on ajas muutuvad, leheküljed on aga staatilised. Postitusi kasutatakse näiteks blogi pidamiseks, lehekülgi aga näiteks kontaktinfo, teenuste ja toodete tutvustamiseks.

---

## Postitus (Post)

1. **Ajalisus**: Postitused on ajastatud ja kuvatakse tavaliselt kronoloogilises järjekorras, kusjuures uusimad postitused ilmuvad esilehel või postituste lehel kõige ees.

2. **Kategooriad ja Sildid**: Postitusi saab liigitada kategooriate ja siltide järgi, mis aitavad organiseerida ja kategoriseerida blogi sisu.

3. **Kommentaarid**: Tavaliselt on postitustel võimalus lugejatel kommenteerida.

4. **Arhiiv**: WordPress loob automaatselt arhiivid postituste jaoks, mis põhinevad kuupäevadel, kategooriatel ja siltidel.

5. **Dünaamiline**: Postitusi kasutatakse sageli ajakohase sisu jaoks, näiteks blogipostitused, uudised, pressiteated jne.

---

## Lehekülg (Page)

1. **Staatiline sisu**: Leheküljed on mõeldud staatilise sisu jaoks, mis ei muutu sageli. Näiteid on "Kontakt", "Meist", "KKK" jne.

2. **Hierarhia**: Lehekülgedel on hierarhiline struktuur, mis tähendab, et saate luua alamlehti. Näiteks võib "Teenused" lehekülje all olla alamlehti nagu "Konsultatsioon", "Disain" jne.

3. **Ei kuulu kategooriatesse ega siltidesse**: Erinevalt postitustest ei liigitata lehekülgi kategooriate ega siltide alla.

4. **Kommentaarid**: Vaikimisi ei ole lehekülgedel kommentaaride osa, kuigi seda saab sõltuvalt teemast ja vajadusest lubada.

5. **Ei ole ajastatud**: Lehekülgedel puudub avaldamiskuupäev või aeg, ehkki need on loomulikult dateeritud sisemiselt.

---

## Postitus vs Leht

| Omadus                | Postitus (Post) | Leht (Page)    |
| --------------------- | --------------- | -------------- |
| Ajalisus              | Jah             | Ei             |
| Kategooriad ja Sildid | Jah             | Ei             |
| Kommentaarid          | Jah (vaikimisi) | Ei (vaikimisi) |
| Arhiiv                | Jah             | Ei             |
| RSS-voog              | Jah             | Ei             |
| Hierarhia             | Ei              | Jah            |

---
