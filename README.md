# Masters Thesis: Client-side evaluatie van GeoSPARQL opvragingen over heterogene gegevensbronnen

<!-- [Extended abstract](https://github.com/Bertware/masterthesis/blob/master/abstract.pdf) (EN) -->
<!-- [Masters thesis](https://github.com/Bertware/masterthesis/blob/master/masterproef%20Bert%20Marcelis.pdf) (NL) -->

### **abstract (EN)**
On the Web as it's currently known, users can easily understand pages of websites. This is not the case for computers, they need to do a lot of effort to substract both meaning and context from sentences. The Web, as it is today, is not build to be interpreted by machines. Thanks to the Semantic Web, which is an extension to the current Web, it is possible for machines to understand the pages of websites.

It is currently possible to query for linked data to a limited amount of data sources, because very few data sources support linked data. These data sources can be heterogeneous, which means they can be different types of data sources. Theses queries are executed with SPARQL, which has multiple working implementations. For geographical queries, GeoSPARQL is needed. However, there are only few implementations of GeoSPARQL and most of these implementations are working incorrect.

In this work, a limited implementation of GeoSPARQL is made in order to request data in RDF format and calculate the topological relations in this data. With this implementation, it has been tested for which interfaces these topological relations can be calculated on the client-side. Doing this on the client-side is important for many reasons. The major reason is that many of these calculations would cripple a server, while these calculations for only one user on the client-side is very possible. In other words, doing this on the client-side is an effective way of spreading the load. This paper gives new insights about handling geographical queries on the client-side.

Like this, it seems to be very simple to calculate the topological relations on the client-side when the data source is a data dump. Hereby, the client wil have to download the entire data set. It's also possible to calculate topological relations when the source is a TPF interface. The interface will already provide several optimizations by only returning the necessary data. However, when the source is a SPARQL endpoint, this is more difficult. However, this is also possible by iterating over the different RDF triples and by counting the amount of matching results. Like this, the smallest pattern can be formed and retrieved from the SPARQL endpoint. This prevents the retrieval of unnecessary data.

The conclusion can be made that handling these kind of queries can be handled better on the client-side. Like this, the entire query can be processed, even when the source doesn't fully support it. This master's thesis is mostly useful for computer scientists who are true experts about Semantic Web, but it can also be used by enthousiasts who want to receive a better understanding of the Semantic Web and it's possibilities.

### **abstract (NL)**
Op het Web zoals het nu gekend is, kunnen gebruikers makkelijk pagina's van websites begrijpen. Voor computers is dit echter niet het geval, hier moet enorm veel moeite gedaan worden om betekenis en context uit de zinnen te ontleden. Het Web zoals het nu is, is niet gebouwd om begrepen te worden door machines. Dankzij het Semantische Web, wat een uitbreiding op het huidige Web is, is het wel mogelijk voor machines om de pagina's van websites te begrijpen.
    
Momenteel is het reeds mogelijk om opzoekingen naar gelinkte data te doen over een beperkt aantal gegevensbronnen, omdat weinig gegevensbronnen gelinkte data ondersteunen. Deze gegevensbronnen kunnen ook heterogeen zijn, wat betekent dat het andere types van bronnen kunnen zijn. Deze opzoekingen gebeuren aan de hand van SPARQL, waar verschillende werkende implementaties van zijn. Om geografische opvragingen te doen wordt GeoSPARQL gebruikt. Hiervan zijn echter weinig implementaties gemaakt en deze implementaties hebben in vele gevallen incorrecte gedragingen.

In dit werk is een beperkte implementatie van GeoSPARQL gemaakt om zo de informatie in RDF formaat op te halen en topologische relaties uit te rekenen. Hierbij is getest bij welk soorten interfaces deze topologische relaties op de client-side kunnen worden berekend. Dit op de client-side doen is belangrijk voor vele redenen. Eén van de belangrijkste redenen is dat deze berekeningen een server zouden kunnen verlammen, terwijl deze berekeningen voor slechts één gebruiker op de client-side zeer goed mogelijk zijn. In andere woorden, dit op de client-side doen is een effectieve manier om de belasting te verspreiden. Deze paper geeft nieuwe inzichten over het afhandelen van deze geografische opvragingen op de client-side.

Zo blijkt dat het zeer eenvoudig is om topologische relaties te berekenen op de client-side wanneer de bron een ``data dump'' is. Hierbij zal de client de volledige dataset moeten downloaden. Daarnaast is het mogelijk om de topologische relaties te berekenen wanneer de bron een ``TPF interface'' is. Deze zal zelf al optimalisaties voorzien door enkel de benodigde gegevens terug te geven. Wanneer de bron echter een SPARQL-endpoint is, is dit moeilijker. Dit wordt echter mogelijk gemaakt door de verschillende RDF triples te overlopen en te tellen hoeveel resultaten overeenkomen. Hierbij kan zo het kleinste patroon gevormd worden om te voorkomen dat meer data opgehaald worden dan noodzakelijk is.

Zo kan geconcludeerd worden dat het afhandelen van deze opvragingen veel beter op de client-side gedaan kan worden. Zo kan het geheel van de opvraging weergegeven worden, zelfs wanneer de bron dit zelf niet ondersteund. Deze masterproef is vooral nuttig voor computerwetenschappers die echte experts zijn van het Semantische Web, maar kan ook gebruikt worden door geïnteresseerden voor het verkrijgen van een beter begrip van het Semantische Web en zijn mogelijkheden.


# Setup

1. Installeer LaTeX: [https://www.latex-project.org/get/](https://www.latex-project.org/get/)
2. Clone deze git repo
3. Installeer de plugin `LaTeX Workshop`
4. Open `settings.json`: ⌘ + Shift + P en zoek op `Open Settings (JSON)` (Windows users: waarschijnlijk `F1`)
5. Voeg onderstaand JSON-fragment onderaan het bestand toe (onder de laatste key)
```json
    "latex-workshop.latex.recipes":[
        {
            "name": "lualatex ➞ bibtex ➞ lualatex x 2",
            "tools": [
                "lualatex",
                "bibtex",
                "lualatex",
                "lualatex"
            ]
        },
        {
            "name": "lualatex ➞ bibtex ➞ makeglossaries ➞ lualatex x 2",
            "tools": [
                "lualatex",
                "bibtex",
                "makeglossaries",
                "lualatex",
                "lualatex"
            ]
        },
        {
            "name": "lualatex (zonder bibliografie)",
            "tools": [
                "lualatex"
            ]
        }
    ],
    "latex-workshop.latex.tools":[
        {
            "name": "bibtex",
            "command": "bibtex",
            "args": [
                "%DOCFILE%"
            ],
            "env": {}
        },
        {
            "name": "makeglossaries",
            "command": "makeglossaries",
            "args": [
              "%DOCFILE%"
            ]
        },
        {
            "name": "lualatex",
            "command": "lualatex",
            "args": [
                "-interaction=nonstopmode",
                "--shell-escape",
                "%DOC%"
            ],
            "env": {}
        }
    ],
    "latex-workshop.latex.autoBuild.run": "onFileChange",
    "latex-workshop.latex.recipe.default": "lastUsed",
    "latex-workshop.view.pdf.viewer": "tab",
    "latex-workshop.latex.clean.fileTypes": [
        "**/*.aux",
        "**/*.bbl",
        "**/*.blg",
        "**/*.idx",
        "**/*.ind",
        "**/*.lof",
        "**/*.lot",
        "**/*.out",
        "**/*.toc",
        "**/*.acn",
        "**/*.acr",
        "**/*.alg",
        "**/*.glg",
        "**/*.glo",
        "**/*.gls",
        "**/*.fls",
        "**/*.fdb_latexmk",
        "**/*.snm",
        "**/*.synctex(busy)",
        "**/*.synctex.gz(busy)",
        "**/*.nav",
        "**/*.lol",
        "**/*.dvi",
        "**/*.lop",
        "**/*.tdo",
        "**/*.ist",
        "_minted-main/*",
        "_minted-main"
    ],
    "latex-workshop.latex.autoClean.run": "onBuilt",
    "editor.wordWrap": "on"
```
4. Herlaad het VS Code venster: ⌘ + Shift + P en zoek op 'Reload window' (Windows users: waarschijnlijk `F1`)
5. Als je nu `main.tex` opent, zou er een icoon `TeX` moeten bijkomen links in het venster
6. Klik op dat icoon en voer het commando `Build LaTeX project` -> `Recipe: lualatex -> bibtext -> makeglossaries -> lualatex x 2` uit
7. Je zou nu een `main.pdf` moeten hebben en alle build files zouden weg moeten zijn (met uitzondering van het log-bestand om eventueel te debuggen)