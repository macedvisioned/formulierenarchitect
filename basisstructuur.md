# <h1>Basisstructuur ontwerp html formulieren in Elementor Pro</h1>

# Voorbeeldformulier
![](https://i.imgur.com/EW9vmj3.png)


In de kop van het formulier het logo met skiplink
```
<!--Skiplink-->
Added to issue [https://github.com/nl-design-system/backlog/issues/74](url)
<h2>Skiplink to go to the maincontent</h2>
<a href="#subheader" class="bypass" tabindex="0">Ga direct naar inhoud</a>
<!--end main-->

<a class="skiplink" href="#example_content">
        <span class="skiplink__text">Ga direct naar inhoud</span>
    </a>
```
# <h2>Formuliernaam</h2>
Bij voorkeur de H1 tag mits het een stand alone html pagina is anders een H2 tag als dit embedded is in een html pagina.
Hieronder een stuk voorbeeldcode met Figma design tokens.
<b>Voorbeeld zoals gemaakt in get NL Design systeem.</b>
de token $utrecht is hier gerelateerd aan een van de gemeentes. Wijzig de tekst als het dollarteken in jouw projectnaam
```
      "heading-1": {
        "value": {
          "fontFamily": "$utrecht.typography.sans-serif.font-family",
          "fontWeight": "$utrecht.typography.weight-scale.bold",
          "lineHeight": "$utrecht.typography.line-height.sm",
          "fontSize": "$utrecht.typography.scale.3xl",
          "letterSpacing": "$utrecht.typography.letter-spacing.normal",
          "paragraphSpacing": "0",
          "textDecoration": "none",
          "textCase": "none"
        },
        "description": "Header h1 layout",
        "type": "typography"
      },
```
# <h2>Header van het formulier</h2>
Sectie kop is altijd de H2 tag met attribuut en bladwijzers om een navigatie in het formulier te creëren. Dit is handig voor een meerstappen formulier.

In de header van het formulier staan:
* een korte instructie 
* een sectie NAW of gebruikersgegevens, dus wie de invuller is van het formulier
* In de header staan dan ook de componenten om in te vullen van wie het formulier afkomstig is.
* een navigatie (bladwijzers), de stappen in het proces, bij voorkeur horizontaal.
```
<div id="header" role="header"> <!--add formfields and instructions here...-->

```

# <h2>De formulierinhoud</h2>
# <h3>Secties binnen een formulier</h3> 
Let op: H3 binnen de h2 sectie.
In deze sectie komt het daadwerkelijke formulier met daarin de vragen.
Hieronder vallen dan tussensecties met de H4 tag waar zich meestal conditionele inhoud bevindt.
Nadere uitleg van de componenten in het volgende hoofdstuk:
```
<div id="main" role="main"> <!--add formfields here...-->


```

# <h2>Footer gedeelte </h2>
De footer is expliciet voor:
* parafenroute
* ondertekening
* instructie voor verzending 
```
<div id="footer" role="footer"> <!--add formfields and additional information here...-->


```


---


# <h2>Hulp bij het ontwerpproces van een formulier</h2>
[https://www.visioned.net/checklist-hoe-maak-ik-een-toegankelijk-formulier/](https://)
