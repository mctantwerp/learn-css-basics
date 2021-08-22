# Syntax basics

CSS schrijven gebeurt eigenlijk altijd op dezelfde manier. Dat ziet er ongeveer zo uit:

```css
p {
    color: red;
}
```

In dit voorbeeld zien we drie elementen:

1. Het element dat je wil vormgeven \(**selector\)**: p
2. een eigenschap die je wil veranderen \(**property\)**: color
3. wat de waarde van die eigenschap moet zijn \(**value**\): red

Met deze eenvoudige regel zeg je tegen een browser dat alle paragrafen \(&lt;p&gt;\) in de pagina, een rode tekstkleur moeten krijgen.

Natuurlijk hoef je niet voor elke property opnieuw een selector aanduiden, je kan meerdere properties tegelijk aanpassen:

```css
p {
    color: red;
    font-size: 18px;
}
```

Daarnaast kan je als selector ook specifieker elementen selecteren, door middel van een id, of classes:

```css
#green {
    color: green;
}
```

In dit voorbeeld zien we het gebruik van een **id selector** \(\#\). Als er in HTML een bepaald element het id 'green' heeft, dan zal dit stukje CSS geactiveerd worden.

```css
.bold {
    font-weight: bold;
}
```

In dit voorbeeld zien we het gebruik van een **class selector** \(.\). Als er in HTML één of meerdere elementen de class 'bold' gebruiken, dan zal dit stukje CSS voor elk van die elementen geactiveerd worden.



