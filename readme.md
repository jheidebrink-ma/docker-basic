# Deze ReadMe heeft twee onderdelen, bovenaan de Docker setup en onderaan een stuk over dit project.

<hr>

# Docker setup
Deze uitleg gaat over een Docker setup met een container voor NGINX, PHP en MariaDB. Deze setup is zo in te stellen dat je een virtuele ontwikkel omgeving hebt die je kunt gebruiken voor alle ontwikkel opdrachten.
Zo kun je als het nodig is een andere versie van PHP installeren of een andere database engine gebruiken.

<hr>

## Onderdelen
### Public
In deze structuur zit vind je een public folder, hier komen straks alle php documenten te staan die publiekelijk zijn. Je library of config bestanden zul je in een folder buiten de public moeten plaatsen.
### YML
Het docker-compose.yml is het moeder bestand waar in staat wat er gebeurd en welke acties er uitgevoerd moeten worden tijdens het opstarten van het project.  
### Docker folder
In deze folder kom je alle bestanden tegen die nodig zijn voor een specifieke Docker omgeving, zoals de reverse proxy NGINX. 

<hr>

## Setup
### 1 Download
Download deze repository en plaats hem ergens op je computer.  
Zorg ervoor dat hij is uitgepakt én niet in een httpdocs folder staat. Maar op een duidelijke plek waar je vanaf nu aan je project gaat werken.

### 2 Dependecies
Zorg ervoor dat je Docker desktop hebt draaien.  
Download eventueel hier: [https://www.docker.com](url)  
En volg de installatie stappen van Docker.

### 3 Port available
Het kan zijn dat er een andere Docker omgeving aan staat, zet die dan eerst uit. Je hebt als het goed is nu geen XAMP / MAMP / LAMP / WAMP / of docker container draaien.

### 4 Start de docker container
Ga nu via de commandline ( CMD of Terminal ) naar de folder waar je docker-compose.yml file staat en start docker met het volgende commando:  
```
docker-compose up
```
<br>
Wil je deze container in de achtergrond draaien, dus dat je terminal scherm niet vol loopt met tekst, voer dan het volgende commando uit: 
```
docker-compose up -d
```

### 5 Bestanden in public
In de public folder kom je een index.php file tegen, die kun je als voorbeeld gebruiken om te kijken of alles werkt.  
Pas hier wat aan en voeg wat php code of iets anders toe.  
Het `test.php` bestand is een voorbeeld dat je kunt aanroepen in de browser [http://localhost:88/test.php](url) waar je kunt zien welke php er is geïnstalleerd.  

### 6 Test je website
Ga nu naar de volgende url en geniet van je virtuele omgeving met PHP:
[http://localhost:88](url)

### 7 Database beheer
In deze docker setup zit ook een phpmyadmin container. Daarmee kun je je database beheren, zie:
[http://localhost:1088](url)

Veel plezier met ontwikkelen van je applicatie!
