# Masters Thesis: The user perceived performance of route planning APIs

[Extended abstract](https://github.com/Bertware/masterthesis/blob/master/abstract.pdf) (EN)
[Masters thesis](https://github.com/Bertware/masterthesis/blob/master/masterproef%20Bert%20Marcelis.pdf) (NL)

### **abstract (EN)**
For the Web architectures behind route planning applications, Remote Procedure Calls are commonplace, in which a server calculates the routes for all end-users. Linked Connections introduces an alternative architecture following the REST constraints, publishing the raw data in fragments. While benchmarks show a higher cost-efficiency of Linked Connections on the server, it is currently not known how it performs on clients, that now also need to execute the route planning algorithm. 

In this work, we study the user-perceived performance of route planning on the client-side, consuming more bandwidth, versus route planning on the server-side. An isomorphic app was developed with both route planning on the client-side as on the server-side. Both technical performance and user-perceived performance were tested among 17 travellers, and 81 respondents gave insights on their use of travel companions. 

We found that the performance of the client-side Android Linked Connections implementation heavily depends on the type of information, the query and the users device. Linked Connections can be faster or slower than a query answering API based on these parameters. For a majority of the users, the benefit of off-line searches outweighs the slower speed of Linked Connections and even though Linked Connections is slower than the reference API, users consider it as fast as their default application on recent devices.

### **abstract (NL)**
Voor de achterliggende Web-architecturen van routeplanning applicaties worden gebruikelijk Remote Procedure Calls toegepast, waarbij een server de routes voor elke gebruiker berekent. Linked Connections biedt een alternatieve architectuur volgens de REST-constraints, waarbij ruwe data in fragmenten gepubliceerd worden. Terwijl reeds is aangetoond dat de kostenefficiëntie van Linked Connections op servers hoger is, is het op dit moment nog niet bekend hoe Linked Connections presteert op clients, die nu ook zelf het routeplanningsalgoritme moeten uitvoeren. 

In dit werk bestuderen we de door gebruikers ervaren performantie van routeplanning aan de client-side tegenover routeplanning aan de server-side. Een isomorfe applicatie werd ontwikkeld met zowel routeplanning aan client- als server-side. Zowel technische performantie als door gebruikers ervaren performantie werden getest bij 17 reizigers, en 81 respondenten gaven inzichten in hun gebruik van reisapplicaties. 

We ontdekten dat de performantie van client-side Android Linked Connections implementatie hevig afhangt van het type informatie, de opzoekingen en het gebruikte toestel. Linked Connections kan sneller of trager zijn dan een API die vragen beantwoordt op basis van deze parameters. Voor de meerderheid van de gebruikers weegt het voordeel van offline toegang op tegen de tragere snelheid van Linked Connections, en ondanks dat Linked Connections trager is dan de gebruikte referentie RPC API, ervaren gebruikers Linked Connections zo snel als hun huidige applicaties op recente toestellen.
