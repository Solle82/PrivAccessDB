# 1. Integrationer
Regular text

  ## 1.1 Virusscan
  Scanner indkommende blanketter for virus efter de er gemt i databasen. Grundet vedhæftninger gemmes i databasen i base64 format, er der ingen risici for at disse inficerer serveren.
  Integrationen er synkron, hvilket betyder at denne integration skal gennemføres, før andre integrationer kan udføres.
  ## 1.2 SKAT
  Transformere og validerer indkommende blanketter i SKAT's XML format (begrebsmodel).
  Integrationen er synkron, hvilket betyder at denne integration skal gennemføres, før andre integrationer kan udføres.
  ## 1.3 Kundeoverblik (KOB)
  Transformerer blankettens SKAT XML til KOB's XML format, og sender resultatet til KOB endepunktet.
  ## 1.4 Datawarehouse (DWH)
  Transformerer blankettens SKAT XML til DWH's XML format, hvor XML-filen uploades til en FTP-server - skiftes til SFTP. Herefter sendes en anmodning til DWH endepunktet der påbegynder protokollen "Styret Fil Overførsel". Når DWH melder tilbage til Blanketfordeleren, slettes filerne fra FTP-serveren igen, og integrationen markeres som udført.
  ## 1.5 Captia (CAP)
  Transformerer blankettens SKAT XML til Captia-XML som sendes til en JAVA komponent. Denne komponent kommunikerer med Captia SOAP-webservicen for sagsoprettelse i Workzone.

.

# 2. Blanketter
## 2.1 tst.01
### 2.1.1 Formål og integrationer
### 2.1.2 Tilpasninger


## 2.2 04.063
### 2.2.1 Formål og integrationer
### 2.2.2 Tilpasninger


## 2.3 06.013
### 2.3.1 Formål og integrationer
### 2.3.2 Tilpasninger


## 2.4 Statsstøtte
### 2.4.1 Formål og integrationer
### 2.4.2 Tilpasninger


## 2.5 Moms20
### 2.5.1 Formål og integrationer
### 2.5.2 Tilpasninger









## Header 2
> Quoted
> - Quoted list item

### Header 3
`var inline_code = true`

```
if (display == code){
  return true
}
```

#### Header 4
*This text will be italic*
_This will also be italic_

**This text will be bold**
__This will also be bold__

_You **can** combine them_

~~this text is linethrough~~

##### Header 5
* Unordered Item 1
* Unordered Item 2
  * Unordered Item 2a
  * Unordered Item 2b

1. Ordered Item 1
1. Ordered Item 2
1. Ordered Item 3
   1. Ordered Item 3a
   1. Ordered Item 3b

###### Header 6
![GitHub Logo](/images/logo.png)
Format: ![Alt Text](url)

- [x] @mentions, #refs, [links](), **formatting**, and <del>tags</del> supported
- [x] list syntax required (any unordered or ordered list supported)
- [x] this is a complete item
- [ ] this is an incomplete item
If you include a task list in the first com

tables too...

First Header | Second Header
------------ | -------------
Content from cell 1 | Content from cell 2
Content in the first column | Content in the second column
