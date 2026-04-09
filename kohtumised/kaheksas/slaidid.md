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

## Kaheksas kohtumine

- Vahepeal tekkinud küsimused

---

## Lisatööriistad blokkide stiilide valikutes

Lisa `theme.json` faili "settings" jaotisesse:

```json
"appearanceTools": true,
```

Osaline faili sisu peaks nägema välja midagi sellist:

```json
"$schema": "https://schemas.wp.org/trunk/theme.json",
"version": 2,
"settings": {
  "appearanceTools": true,
  "position": {
    "sticky": true
  },
  ...
}
```

---

## Menüü elementide vahe

```css
.wp-block-navigation__container {
  gap: 24px;
}
```

---

## Slider bloks

---
