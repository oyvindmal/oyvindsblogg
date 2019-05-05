+++
date = "2019-05-05T17:44:03+02:00"
frontimage = "https://picsum.photos/1920/300?q=83594583949839"
summary = "Enkel blogg med hugo"
title = "Bygg en statisk blogg - Del 1"

+++
Denne bloggen er basert på Hugo

Jeg kommer ikke til å gå igjennom hvordan man installerer Hugo og Go, da dette varierer fra maskin til maskin. Det finnes en god guide på dette [her](https://gohugo.io/getting-started/installing/)

## Opprette nettsiden

## Opprette tema

Det finnes mange [ferdige temaer](https://themes.gohugo.io/) du kan bruke eller ta utgangspunkt i, men i dette tilfellet ønsker jeg å bruke 

## Konfigurasjonsendringer

{{< highlight toml "linenos=table, linenostart=1" >}}

  
baseURL = "https://blogg.oyvindmal.no/"  
languageCode = "en-us"  
title = "blogg.oyvindmal.no"  
theme = "blogg"  
{{< / highlight >}}