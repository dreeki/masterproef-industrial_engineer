# Masters Thesis: The user perceived performance of route planning APIs

<!-- [Extended abstract](https://github.com/Bertware/masterthesis/blob/master/abstract.pdf) (EN) -->
<!-- [Masters thesis](https://github.com/Bertware/masterthesis/blob/master/masterproef%20Bert%20Marcelis.pdf) (NL) -->

### **abstract (EN)**
On the internet as it's currently known, users can easily understand pages of websites. This is not the case for computers, they need to do a lot of effort to substract both meaning and context from sentences. The web, as it is today, is not build to be interpreted by machines. Thanks to the Semantic Web, which is an extension to the current web, it is possible for machines to understand the pages of websites.

It is currently possible to query for linked data to limited amount of data sources, because very few data sources support linked data. Theses queries are executed with SPARQL, which has different working implementations. For geographical queries, GeoSPARQL is needed. However, there are only few implementations of GeoSPARQL and most of these implementations are working incorrect.

In this work, a limited implementation of GeoSPARQL is made in order to request data in RDF format and calculate the topological relations in this data. With this implementation, it has been tested for which interfaces these topological relations can be calculated on the client-side. This paper gives new insights about handling geographical queries on the client-side.

Like this, it appeared to be very simple to calculate the topological relations on the client-side when the data source is a TPF-interface. However, when the source is a SPARQL-endpoint, this is harder to achieve, but still possible. It's also possible to detect whether the source is a GeoSPARQL-endpoint. If this is the case, the entire query can be handled at the source.

The conclusion can be made that handling these kind of queries is better on the client-side. like this, the entire query can be processed, even when the source doesn't fully support it. This scription is mostly useful for computer scientists who are developing the web, or if they want to start doing so. But it can also be used by enthousiasts for receiving a better understanding of the Semantic Web and it's possibilities.

### **abstract (NL)**
Op het internet zoals het nu gekend is, kunnen gebruikers makkelijk pagina's van websites begrijpen. Voor computers is dit echter niet het geval, hier moet enorm veel moeite gedaan worden om betekenis en context uit de zinnen te onleden. Het web zoals het nu is, is niet gebouwd om begrepen te worden door machines. Dankzij het semantische web, wat een uitbreiding op het huidige web is, is het wel mogelijk voor machines om de pagina's van websites te begrijpen.
    
Momenteel is het reeds mogelijk om opzoekingen naar gelinkte data te doen over een beperkt aantal gegevensbronnen, omdat weinig gegevensbronnen gelinkte data ondersteunen. Deze opzoekingen gebeuren aan de hand van SPARQL, waar verschillende werkende implementaties van zijn. Om geografische opvragingen te doen wordt GeoSPARQL gebruikt. Hiervan zijn echter weinig implementaties gemaakt en deze implementaties hebben in vele gevallen incorrecte gedragingen.

In dit werk is een beperkte implementatie van GeoSPARQL gemaakt om zo de informatie in RDF formaat op te halen en topologische relaties uit te rekenen. Hierbij is getest bij welk soorten interfaces deze topologische relaties op de client-side kunnen berekent worden. Deze paper geeft nieuwe inzichten over het afhandelen van deze geografische opvragingen op de client-side.

Zo bleek dat het zeer eenvoudig is om topologische relaties te berekenen op de client-side wanneer de bron een TPF-interface is. Wanneer de bron echter een SPARQL-endpoint is, is dit moeilijker maar nog steeds mogelijk. Ook is het mogelijk te detecteren of de bron een GeoSPARQL-endpoint is, dan kan het geheel afgehandelt worden door de bron.

Zo kan geconcludeerd worden dat het afhandelen van deze opvragingen veel beter op de client-side gedaan kan worden. Zo kan het geheel van de opvraging weergegeven worden, zelfs wanneer de bron dit zelf niet ondersteund. Deze scriptie is vooral nuttig voor computerwetenschappers die mee werken aan de ontwikkeling van het web of dit wensen te doen, maar kan ook gebruikt worden door geïnteresseerden voor het verkrijgen van een beter begrip van het semantische web en zijn mogelijkheden.