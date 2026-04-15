============================================================
README: METEO-APP SPRING BOOT ADVANCED
============================================================

------------------------------------------------------------
1. TASK (Compito)
------------------------------------------------------------
L'obiettivo di questo documento è fornire una guida tecnica 
chiara e concisa per configurare, compilare ed eseguire 
l'applicazione "Meteo-App" in un ambiente di sviluppo locale. 
Il documento serve a garantire che ogni sviluppatore possa 
rendere il servizio operativo senza ambiguità.

------------------------------------------------------------
2. ROLE (Ruolo)
------------------------------------------------------------
Questo file è redatto in qualità di Technical Writer del 
team di sviluppo. Le istruzioni sono scritte con un tono 
professionale e tecnico, focalizzato sull'efficienza operativa.

------------------------------------------------------------
3. AUDIENCE (Pubblico)
------------------------------------------------------------
Il destinatario di questo documento è il nuovo sviluppatore 
Java che si unisce al progetto. Si richiede la conoscenza di:
- Java JDK 17 o superiore
- Apache Maven
- Fondamenti di Spring Boot e REST API

------------------------------------------------------------
4. CONTEXT (Creazione/Formato)
------------------------------------------------------------
Il codice sorgente analizzato è un'applicazione Web Java basata 
su Spring Boot 3.2.5. Il sistema integra l'API di OpenWeatherMap, 
implementa un sistema di cache tramite HashMap e fornisce una 
documentazione interattiva tramite Swagger UI. Il presente 
documento è fornito in formato testo semplice (.txt) per la 
massima compatibilità.

------------------------------------------------------------
5. INTENT (Intento/Obiettivo)
------------------------------------------------------------
Fornire istruzioni step-by-step per l'installazione, la 
configurazione della chiave API e l'utilizzo dei principali 
endpoint del servizio.

------------------------------------------------------------
6. ISTRUZIONI DI INSTALLAZIONE E AVVIO
------------------------------------------------------------

FASE 1: Clonazione ed estrazione
Estrai il contenuto del file .zip o clona il repository nella 
tua cartella di lavoro.

FASE 2: Configurazione Variabile d'Ambiente (CRITICO)
L'applicazione richiede una chiave API valida di OpenWeatherMap.
Impostala come variabile d'ambiente:
- Su Windows (PowerShell): $env:WEATHER_API_KEY="la_tua_key"
- Su Linux/macOS: export WEATHER_API_KEY=la_tua_key

FASE 3: Compilazione ed Esecuzione
Apri il terminale nella root del progetto (dove si trova il 
file pom.xml) ed esegui:
> mvn clean install
> mvn spring-boot:run

L'applicazione sarà disponibile all'indirizzo: 
http://localhost:8080

------------------------------------------------------------
7. ESEMPI DI UTILIZZO
------------------------------------------------------------

- Richiesta Meteo via Browser/CURL:
  GET http://localhost:8080/weather/{nome_citta}
  Esempio: http://localhost:8080/weather/Milano

- Documentazione Swagger (Interfaccia Grafica):
  Visita: http://localhost:8080/swagger-ui.html

- Esecuzione Test Unitari:
  Esegui il comando: mvn test

------------------------------------------------------------
8. CONTATTI E SUPPORTO
------------------------------------------------------------
In caso di errori durante il parsing JSON o problemi di 
connessione all'API, verificare la validità della 
WEATHER_API_KEY e lo stato dei servizi OpenWeatherMap.
============================================================
