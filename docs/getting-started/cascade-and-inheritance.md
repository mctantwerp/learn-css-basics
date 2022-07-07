# Cascade & inheritance

Het meest complexe onderdeel bij het schrijven van CSS is het goed begrijpen van het _cascading_ principe. 

### Cascade

CSS wordt door een browser ingelezen, en zal lijn per lijn worden geïnterpreteerd. Dat wil zeggen dat er een volgorde zit in het toepassen van CSS regels op elementen. Opeenvolgende CSS selectors kunnen elkaar dus beïnvloeden en properties kunnen worden overschreven. Dit is een zeer belangrijk onderdeel van CSS, maar maakt het soms ook best complex. Het _cascading_ ****principe kunnen we illustreren aan de hand van een eenvoudig voorbeeld:

{% tabs %}
{% tab title="CSS" %}
```css
h1 { 
    color: red; 
}
h1 { 
    color: green; 
}
```
{% endtab %}

{% tab title="HTML" %}
```markup
<h1>What color would I be?</h1>
```
{% endtab %}
{% endtabs %}

Indien je deze CSS regels toepast op de titel in HTML, met het lezen van bovenstaande uitleg, welke kleur zou de titel dan krijgen denk je?

Beide selectors hebben dezelfde specificiteit, wat wil zeggen dat ze voor de browser even belangrijk zijn. Maar in dit geval zal de color property uit de eerste selector overschreven worden door de color property van de 2e selector. De titel zal dus een groene kleur krijgen.

Bepaalde selectors zijn specifieker dan anderen. Des te specifieker een selector, des te meer 'gewicht' deze heeft om properties van andere selectors te overschrijven. Meer gedetailleerde informatie hierover komt later nog aan bod, maar een handige vuistregel is de volgende:

{% hint style="info" %}
Een ID selector is specifieker dan een class selector, en een class is specifieker dan een element selector. Een ID zal dus altijd properties van een simpele class selector kunnen overschrijven, ongeacht de volgorde in CSS. Een simpele class selector zal dus ook altijd properties van een simpele element selector kunnen overschrijven, ongeacht de volgorde in CSS.

ID &gt; class &gt; element
{% endhint %}

### Inheritance

Inheritance, of het overerven van properties, wil zeggen dat CSS regels op elementen kunnen worden overgenomen door onderliggende \(child\) componenten. Een heel eenvoudig voorbeeld:

{% tabs %}
{% tab title="CSS" %}
```css
p { color: green; }
```
{% endtab %}

{% tab title="HTML" %}
```markup
<p>This will be green, but <span>this span text will be as well</span> due to inheritance</p>
```
{% endtab %}
{% endtabs %}

In bovenstaande voorbeeld zetten we een groene kleur op elke paragraaf. Zoals je kan zien in de HTML tab, staat in dit voorbeeld een `span` tag in de paragraaf. Als we dit voorbeeld zouden openen in een browser, zien we dat ook de `span` tag groen is. De kleur wordt dus overgenomen \(inherited\) van de paragraaf.

{% embed url="https://developer.mozilla.org/en-US/docs/Learn/CSS/Building\_blocks/Cascade\_and\_inheritance" %}

### Efficiëntie

De combinatie van het _cascading_ principe met _inheritance_ maakt dat we op een vrij efficiënte manier CSS kunnen schrijven. Het basis principe is als volgt:

* Je schrijft heel algemene CSS regels via element selectors, deze wordt overgenomen op alle elementen en zorgt voor een uniforme look & feel.
* Specifieke componenten ga je aanduiden met class selectors. Het voordeel hierbij is dat je deze componenten kan hergebruiken. Met de class selectors ga je op component niveau specifieke CSS regels toepassen. Deze class selectors overschijven delen van de algemene selectors, specifiek voor een bepaalde component.

Op deze manier hoef je niet voor elke component apart alle verschillende CSS regels toe te passen, maar maak je handig gebruikt van het _cascading_ principe \(class &gt; element\) en ook van _inheritance_ \(elementen binnen je class componenten erven CSS regels over\).

