# Hoe gebruik ik CSS

CSS kan op verschillende manieren gebruikt worden:

* via _inline_ styling, dus rechtstreeks op je HTML elementen
* via een specifieke `<style>` tag die in de `<head>` tag van je HTML pagina leeft
* in een apart bestand \(.css\) dat kan ingeladen worden in je HTML pagina met behulp van een `<link>` tag

### Inline styling

De allereerste manier om elementen in HTML \(of XML\) visueel op te maken  maakte gebruik van inline styling. Deze manier van opmaken wordt ondertussen **niet meer gebruikt**, al kom je het soms nog tegen als we CSS via Javascript gaan aanpassen, maar dat is voor later.

```markup
<p style="color: red">Deze tekst is rood</p>
```

Zoals je kan zien in dit voorbeeld, maken we geen gebruik van een _selector_, maar zetten we eigenlijk rechtstreeks onze _properties_ op het element.

{% hint style="success" %}
Het voordeel van deze manier van werken is dat het in principe sneller is voor de browser. De browser hoeft niet meer te gaan zoeken op de pagina naar een bepaalde _selector_, maar weet eigenlijk meteen welke opmaak hij op dit element moet toepassen aan de hand van het 'style' attribuut.
{% endhint %}

{% hint style="danger" %}
Het grote nadeel van deze methode is dat het niet herbruikbaar is. Als je meerdere paragrafen rood wil kleuren, moet je deze methode op elk element herhalen. Of, stel dat dat het geval is en je wil de kleur aanpassen, moet je weer telkens op elk element een wijziging aanbrengen.
{% endhint %}

### Style tag

Een tweede manier om CSS te gebruiken is via de style tag. Dit is een manier om CSS toe te voegen in je HTML \(of XML, of SVG\) bestand toe te voegen.

```markup
<style>
    p { 
        color: red; 
    }
</style>
```

Deze toepassing zie je nog regelmatig gebruikt worden, omdat het makkelijk is om te gebruiken om kleine stukjes CSS toe te voegen. Ook wordt deze techniek soms gebruikt om de meest kritische css in te laden \(bvb alles wat meteen zichtbaar is als je een pagina inlaad, zoals lettertypes, bepaalde kleuren, een logo\).

{% hint style="success" %}
Een  voordeel van deze techniek is dat de CSS meteen beschikbaar is, en niet moet wachten op het verder inladen van bepaalde bestanden.
{% endhint %}

{% hint style="danger" %}
Ook een groot nadeel bij deze techniek is dat het niet herbruikbaar is. Als je verschillende pagina's hebt, moet je op elke pagina dezelfde style tag inladen om consistentie te garanderen. Als je daarna een wijziging in CSS moet doen, moet je dat dus ook op elke pagina doen.
{% endhint %}

### Link tag

De derde techniek is om je css op te slaan in een apart bestand, een 'css file'. Die bestanden kan je herkennen aan hun extensie, `.css` . Zulke bestanden kan je inladen in je HTML door middel van een link tag. Deze link tag plaats je in de `head` tag van je HTML. **Deze techniek wordt tegenwoordig het meeste gebruikt.**

```markup
<head>
    ...
    <link href="style.css" rel="stylesheet" />
</head>
```

Opgelet, de link tag heeft naast het `href` attribuut ook een `rel` attribuut. Dit specifieke rel attribuut maakt duidelijk aan de browser dat dit bestand bedoelt is om de pagina vorm te geven. Zonder dit attribuut zal de css in de meeste browsers niet geactiveerd worden.

{% hint style="success" %}
Het grote voordeel met deze techniek is dat alle CSS gebundeld zit in een bestand dat je kan hergebruiken op verschillende pagina's. Daarnaast kan dit bestand ook makkelijk _minified_ worden \(geoptimaliseerd dat het zo klein mogelijk is qua bestandsgrootte, zodat het sneller kan ingeladen worden\). Je kan ook een basis css maken met de basis vormgeving, en dan per pagina een extra, kleinere, css file met specifieke styling voor die pagina.
{% endhint %}

{% hint style="danger" %}
Het nadeel aan deze techniek is dat we met een apart bestand werken, dat moet ingeladen worden. Dat kan soms iets langer duren, zeker als je met grote bestanden werkt.
{% endhint %}

