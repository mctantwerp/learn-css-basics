# Intro

Eenmaal je begint met het bouwen van een website, zal je heel snel bezig zijn met het opbouwen van een layout. Je bouwt als het ware blokjes (boxes) op een pagina. Die blokjes kunnen onder elkaar, of naast elkaar komen te staan.

Zo’n blokje kan ook verschillende eigenschappen hebben:

* Een breedte
* Een hoogte
* Een kleur
* Een afbeelding of tekst

Elk element dat je via CSS kan benaderen, gedraagt zich als zo’n blok. Je kan die blokken eigenlijk opdelen in 2 grote onderdelen: **block** en **inline** blokken. Deze onderdelen omschrijven hoe zo’n blok zich gedraagt in een layout. Er zijn daarin zeer duidelijke verschillen te merken.

Het type block wordt in CSS aangeduid door de **display** property.

### Block

Een **block** element gedraagt zich als een regel in een layout. Het element zal standaard altijd proberen de breedte van zijn omringend (_parent_) element aan te nemen. Het zal zich dus proberen zo breed mogelijk te maken.

Enkele voorbeelden van block elementen: `<p>`, `<h1>`, `<div>`

### Inline

Een **inline** element gedraagt zich als een onderdeel van een regel. Het element zal dus gewoon breder worden naarmate er meer inhoud in het element wordt gezet, en zal als het breder zou worden dan zijn omringend (parent) element, standaard overlopen op een nieuwe regel. Er kunnen dus meerdere inline elementen op 1 regel passen, naast elkaar.

Enkele voorbeelden van inline elementen: `<span>`, `<a>`, `<strong>`

| Block                                                                                                                                                                    | Inline                                                                                                                        |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------- |
| Maakt zich zo breed mogelijk binnen zijn parent element                                                                                                                  | Wordt breder aan de hand van zijn inhoud                                                                                      |
| Kan een breedte en hoogte krijgen met behulp van CSS                                                                                                                     | Kan geen breedte of hoogte krijgen met behulp van CSS                                                                         |
| Zal andere elementen op een nieuwe lijn duwen, ook al is het blok niet de hele breedte van zijn parent element                                                           | Zal andere inline elementen horizontaal wegduwen en kan verder doorlopen op een nieuwe regel                                  |
| Een CSS margin (marge langs de buitenkant van een element) of padding (marge langs de binnenkant van een element) zorgt ervoor dat omringende elementen worden weggeduwd | Enkel horizontale (left & right) margin en padding worden gerespecteerd, en zullen andere inline elementen aan de kant duwen. |



