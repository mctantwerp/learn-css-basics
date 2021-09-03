# Basis syntax

### Basics

CSS schrijven gebeurt eigenlijk altijd op dezelfde manier. Dat ziet er ongeveer zo uit:

```css
p {
    color: red;
}
```

In dit voorbeeld zien we drie elementen:

1. Het _element_ dat je wil vormgeven \(**selector\)**: p
2. een _eigenschap_ die je wil veranderen \(**property\)**: color
3. wat de _waarde_ van die eigenschap moet zijn \(**value**\): red

Met deze eenvoudige regel zeg je tegen een browser dat alle paragrafen \(&lt;p&gt;\) in de pagina, een rode tekstkleur moeten krijgen.

Natuurlijk hoef je niet voor elke property opnieuw een selector aanduiden, je kan meerdere properties tegelijk aanpassen. Een selector verzamelt één of meerdere properties binnen accolades \({ }\). Properties en values worden door middel van een dubbelpunt \(:\) gescheiden, en een regel wordt altijd afgesloten met een puntkomma \(;\).

```css
p {
    color: red;
    font-size: 18px;
}
```

Daarnaast kan je als selector ook specifieker elementen selecteren, door middel van een id, classes, attributen of pseudo-classes.

### ID selector

In dit voorbeeld zien we het gebruik van een **id selector** \(\#\). Als er in HTML _één bepaald element_ \(een id mag maar 1x per pagina gebruikt worden\) het id 'green' heeft, dan zal dit stukje CSS geactiveerd worden.

{% tabs %}
{% tab title="CSS" %}
```css
#green {
    color: green;
}
```
{% endtab %}

{% tab title="HTML" %}
```markup
<p id="green">This text will have a green color</p>
```
{% endtab %}
{% endtabs %}

### Class selector

In dit voorbeeld zien we het gebruik van een **class selector** \(.\). Als er in HTML _één of meerdere elementen_ \(classes kunnen meerdere keren gebruikt worden op een pagina\) de class 'bold' gebruiken, dan zal dit stukje CSS voor elk van die elementen geactiveerd worden.

{% tabs %}
{% tab title="CSS" %}
```css
.bold {
    font-weight: bold;
}
```
{% endtab %}

{% tab title="HTML" %}
```markup
<p class="bold">This text will be bold</p>
<p>But here, only the word <span class="bold">bold</span> is <span class="bold">bold</span>
```
{% endtab %}
{% endtabs %}

### Attribute selector

Naast het selecteren van een element via een tag selector, id selector of class selector, kan je ook elementen selecteren aan de hand van attributen. Attributen zijn waardes die je op je HTML tag zet. Denk bijvoorbeeld aan een knop \(button\), waarop je een attribuut _disabled_ kan gebruiken om de button te deactiveren. Als je een disabled button specifiek wil vormgeven in css, kan je dus gebruik maken van zo'n 'attribute selector' door gebruik te maken van vierkante haakjes \(\[ \]\) met daarin het attribuut en eventueel een specifieke waarde.

{% tabs %}
{% tab title="CSS" %}
```css
button {
  color: blue;
}
/* enkel het attribuut */
button[disabled] {
  color: grey;
}

/* het attribuut met een specifieke w */
button[type="submit"] {
  color: fuchsia;
}
```
{% endtab %}

{% tab title="HTML" %}
```markup
<button>I'm a normal button</button>
<button disabled>I'm disabled</button>
<button type="submit">I'm a submit button</button>
```
{% endtab %}
{% endtabs %}

### Pseudo-class selector

Een pseudo class kan worden gebruikt om bepaalde states van je element vorm te geven. Elk element heeft standaard verschillende states waarin het zich kan bevinden. Een eenvoudig voorbeeld van zo'n state is bijvoorbeeld de _hover_, welke activeert als je met je muiscursor over een element beweegt. Als je muiscursor boven een element zweeft \(hovered\), dan activeert je browser de _hover_ state van dat element. Om deze state te kunnen vorm geven, maak je gebruik van een specifieke notatie, namelijk `:[state]` \(waarbij \[state\] vervangen wordt door de state die je wil vormgeven, bijvoorbeeld hover\).

{% tabs %}
{% tab title="CSS" %}
```css
a:hover {
    font-weight: bold;
}
```
{% endtab %}

{% tab title="HTML" %}
```markup
<a href="#">This is a link</a>
```
{% endtab %}
{% endtabs %}

### Meer info

Deze voorbeeldjes kan je terugvinden op onderstaande codepen, waarbij je zelf kan gaan spelen met de selectors.

{% embed url="https://codepen.io/TroTi13/pen/KKqgPWV" caption="https://codepen.io/TroTi13/pen/KKqgPWV" %}



