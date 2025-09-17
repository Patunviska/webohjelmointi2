Kurssin Web-ohjelmointi 2 DT10047-3002 ensimmäinen tehtävä
Tehtävässä piti tehdä yksinkertainen REST API sanakirjaa varten.
Sanakirja tallennetaan tekstitiedostoon sanakirja.txt, jossa jokaisella rivillä on sanapari: suomenkielinen sana ja sen vastine englanniksi.

Asennus ja käynnistys:

1. Kloonaa projekti omalle koneelle
2. Asenna riippuvuudet: npm install
3. Käynnistä palvelin: npm start
4. Palvelin käynnistyy osoitteeseen http://localhost:3000

5. GET /words palauttaa koko sanakirjan: GET http://localhost:3000/words
6. GET /translate?fi=<suomenkielinen sana> hakee englanninkielisen vastineen sanalle: GET http://localhost:3000/translate?fi=auto
7. POST /words lisää uuden sanaparin tiedoston loppuun. Body pitää lähettää JSON-muodossa:

POST http://localhost:3000/words
Content-Type: application/json

{
"fin": "koira",
"eng": "dog"
}

Käytettyjä tekniikoita:

- Node.js
- Express
- fs-moduuli tiedoston käsittelyyn: readFileSync ja appendFileSync
