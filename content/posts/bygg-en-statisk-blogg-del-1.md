+++
date = "2019-05-05T17:44:03+02:00"
frontimage = "https://picsum.photos/1920/300?q=83594583949839"
summary = "Enkel blogg med hugo"
title = "Bygg en statisk blogg - Del 1"

+++
Denne bloggen er basert på Hugo

Jeg kommer ikke til å gå igjennom hvordan man installerer Hugo og Go, da dette varierer på ulike operativsystemer. Det finnes en god guide på dette [her](https://gohugo.io/getting-started/installing/)

Hugo benytter Markdown for å strukturere innholdet. Markdown er ett enkelt markup språk for å definere formatering av innhold. Github har en fin guide som gir en introduksjon til Markdown. Kanskje jeg på ett eller annet tidspunkt skriver en introduksjon til dette på norsk.

[https://guides.github.com/features/mastering-markdown/](https://guides.github.com/features/mastering-markdown/ "https://guides.github.com/features/mastering-markdown/")

I senere deler av denne guiden skal jeg gå igjennom hvordan man kan knytte denne opp mot [Forestry.io](https://www.forestry.io) for å få et redigeringsgrensesnitt i nettleseren.

## Opprette nettsiden

{{< highlight Bash >}}

hugo new site <Ditt navn>

{{< / highlight >}}

## Opprette tema

Det finnes mange [ferdige temaer](https://themes.gohugo.io/) du kan bruke eller ta utgangspunkt i, men i dette tilfellet ønsker jeg å lage mitt eget tema. Jeg kommer ikke til å gå igjennom hvordan temaet på denne bloggen er bygget opp konkret men heller bare gå igjennom hva du får ut av boksen.

{{< highlight Bash>}}

hugo new theme <Ditt tema>

{{< / highlight >}}

## Konfigurasjonsendringer

Konfigurajsonen finner du i config.toml. Denne inneholder noen enklere innstillinger for hvordan nettsiden din skal genereres. Som standard inneholder den nesten alt som skal til for å få nettstedet til å fungere, men vi er nødt til å gjøre noen endringer for at alt skal fungere som det skal.

Under "baseURL" skriver du inn adressen nettsiden din skal ha. I mitt tilfelle er dette https://blogg.oyvindmal.no men det vil variere ut fra hvor du skal hoste din nettside.

"languageCode" definerer hvilket språk nettsiden din er på. 

"title" definerer tittelen på nettsiden din. Denne kan du senere gjenbruke i maler. Jeg pleier ikke å bruke denne

Til slutt må du legge til en linje for å definere hvilket tema som skal benyttes. Skriv inn det samme som du gjorde når du opprettet temaet i forrige steg. I mitt tilfelle "blogg"

Den ferdige konfigurasjonsfilen vil da se ut omtrent som dette.

{{< highlight toml "linenos=table, linenostart=1" >}}
baseURL = "https://blogg.oyvindmal.no/"  
languageCode = "en-us"  
title = "blogg.oyvindmal.no"  
theme = "blogg"  
{{< / highlight >}}

## Temaets oppbygging

blabla mappenavn

blabla lookup

blabla baseof

blabla partials

## Archetypes

Archetyper er rett og slett definisjoner av hvordan en bestemt type innhold skal genereres. Denne inneholder all data du ønsker at skal predefineres

## {{< highlight markdown "linenos=table, linenostart=1" >}}

title: "{{ replace .Name "-" " " | title }}"
date: {{ .Date }}
draft: true
summary: "Lorem ipsum"
frontimage: "http://placekitten.com/800/800"

***

{{< / highlight >}}

## Innhold

{{< highlight Bash>}}

hugo new posts/min-nye-post.md

{{< / highlight >}}

## Statiske filer

Blabla mapper

blabla både på tema og selve siden

blablabla filbane