---
layout: post
tittle: "Formulaires Javascript"
date: 2023-08-08 11:33:35 +0200
categories: javascript
---

## Récupérer valeur écrite dans le HTML
```html
<body>
    <form>
        <!--Champ nom avec input texte-->
        <label for="nom">Nom : </label>
        <input type="text" id ="nom" name="nom" value="David">

        <!--Champ conditions avec checkbox-->
        <label for="conditions">Acceptez vous les conditions : </label>
        <input type="checkbox" id="conditions" name="conditions" checked>

        <!--Champ residence avec boutons radio : France, UE, hors UE-->
        <label for="residence">Résidence</label>

        <input type="radio" id="france" name="residence" value="france" checked>
        <label for="france">France</label>
        <input type="radio" id="eu" name="residence" value="eu">
        <label for="eu">Europe</label>
        <input type="radio" id="hors-eu" name="residence" value="hors-eu">
        <label for="hors-eu">Hors Europe</label>
    </form>
</body>
```

```js
//Champ nom avec input texte
let nom = document.getElementById("nom")
console.log(nom.value)

//Champ conditions avec checkbox
let condition = document.getElementById("conditions")
console.log(conditions.checked)

//Champ residence avec boutons radio
let listBtnRadio = doacument.querySelectorAll("input[type=radio]")
for (let i = 0; i < listBtnRadio.length; i++) {
    if (listBtnRadio[i].checked) {
        console.log(listBtnRadio[i].value)
    }
}
```

[source vidéo](https://openclassrooms.com/fr/courses/7696886-apprenez-a-programmer-avec-javascript/8206488-recuperez-la-valeur-d-un-champ-de-formulaire#/id/video_Player_2)

Pour réagir de manière dynamique, il faut écouter les événements qui sont sur ces bouton, exemple sur le "nom", pour voir en direct les changements (sur l'événement "change").

__Cela fonctionne avec tout les type de champs__

```js
//
nom.addEventListener("change", () => {
    console.log(nom.value)
})
```

---

```js
let form = document.querySelector("form")

form.addEventListener("submit", (event) => {
    event.preventDefault()
    let nom = document.getElementById("nom")
    console.log(nom.value)
})
```

__Une pop-up apparait et affiche un formulaire__

[code pop_up](https://github.com/OpenClassrooms-Student-Center/7696886-javascript/blob/P4-C2---Soumettez-un-formulaire---Base/scripts/popup.js)
