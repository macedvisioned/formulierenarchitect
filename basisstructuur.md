# Basisstructuur ontwerp html formulieren in Elementor Pro

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

## Formuliernaam

Bij voorkeur de H1 tag mits het een stand alone html pagina is anders een H2 tag als dit embedded is in een html pagina.  
Hieronder een stuk voorbeeldcode met Figma design tokens.  
**Voorbeeld zoals gemaakt in get NL Design systeem.**  
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

## Header van het formulier

Sectie kop is altijd de H2 tag met attribuut en bladwijzers om een navigatie in het formulier te creëren. Dit is handig voor een meerstappen formulier.

In de header van het formulier staan:

*   een korte instructie
*   een sectie NAW of gebruikersgegevens, dus wie de invuller is van het formulier
*   In de header staan dan ook de componenten om in te vullen van wie het formulier afkomstig is.
*   een navigatie (bladwijzers), de stappen in het proces, bij voorkeur horizontaal.  
    \`\`\`

```

# <h2>De formulierinhoud</h2>
# <h3>Secties binnen een formulier</h3> 
Let op: H3 binnen de h2 sectie.
In deze sectie komt het daadwerkelijke formulier met daarin de vragen.
Hieronder vallen dan tussensecties met de H4 tag waar zich meestal conditionele inhoud bevindt.
Nadere uitleg van de componenten in het volgende hoofdstuk:
```

```

# <h2>Footer gedeelte </h2>
De footer is expliciet voor:
* parafenroute
* ondertekening
* instructie voor verzending 
```

```
<h2>Tabelweergave in samenvatting formulier</h2>
```

| Homework | Exams | Projects |
| --- | --- | --- |
| 1 | 2 | Final |
| 15% | 15% | 15% |

Semantic Elements to use instead of ARIA's roles

ARIA Role Semantic Element

header h1

header h6

```
<table>
   <tr>
     <th rowspan="2" id="h" tabindex="1">Homework</th>
     <th colspan="3" id="e" tabindex="2">Exams</th>
     <th colspan="3" id="p" tabindex="3">Projects</th>
   </tr>
   <tr>
     <th id="e1" headers="e" tabindex="4">1</th>
     <th id="e2" headers="e" tabindex="5">2</th>
     <th id="ef" headers="e" tabindex="6">Final</th>
     <th id="p1" headers="p" tabindex="7">1</th>
     <th id="p2" headers="p" tabindex="8">2</th>
     <th id="pf" headers="p" tabindex="9">Final</th>
   </tr>
   <tr>
    <td headers="h" tabindex="10">15%</td>
    <td headers="e e1" tabindex="11">15%</td>
    <td headers="e e2" tabindex="12">15%</td>
    <td headers="e ef" tabindex="13">20%</td>
    <td headers="p p1" tabindex="14">10%</td>
    <td headers="p p2" tabindex="15">10%</td>
    <td headers="p pf" tabindex="16">15%</td>
   </tr>
  </table>
  
<!--aria specs
https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/Table_Role	
-->

<div role="table" aria-label="Semantic Elements" aria-describedby="semantic_elements_table_desc" aria-rowcount="81">
  <div id="semantic_elements_table_desc">Semantic Elements to use instead of ARIA's roles</div>
  <div role="rowgroup">
    <div role="row">
      <span role="columnheader" aria-sort="none">ARIA Role</span>
      <span role="columnheader" aria-sort="none">Semantic Element</span>
    </div>
  </div>
  <div role="rowgroup">
    <div role="row" aria-rowindex="11">
      <span role="cell">header</span>
      <span role="cell">h1</span>
    </div>
    <div role="row" aria-rowindex="16">
      <span role="cell">header</span>
      <span role="cell">h6</span>
    </div>
    <div role="row" aria-rowindex="18">
      <span role="cell">rowgroup</span>
      <span role="cell">thead</span>
    </div>
    <div role="row" aria-rowindex="24">
      <span role="cell">term</span>
      <span role="cell">dt</span>
    </div>
  </div>
```

rowgroup thead

term dt

---

## Hulp bij het ontwerpproces van een formulier

[https://www.visioned.net/checklist-hoe-maak-ik-een-toegankelijk-formulier/](https://)
