ZAP Security Report
1. Johdanto

Raportin tarkoitus ja laajuus

Tämän raportin tarkoituksena on dokumentoida penetraatiotestauksen tulokset, jotka kohdistuivat sovelluksen rekisteröitymissivuun. Testauksen tavoitteena oli tunnistaa poikkeamat ja haavoittuvuudet, jotka voivat vaarantaa järjestelmän tietoturvan.

Testauksen aikataulu ja testausympäristö

Aikataulu: [Testauksen ajankohta]

Testausympäristö: Kali Linux, Docker, OWASP ZAP

Sovelluksen URL: http://localhost:8000/register

Testauksen laajuus

Testaus keskittyi rekisteröintisivuun ja siihen liittyviin turvallisuusnäkökulmiin, kuten syötteen validointiin, istuntojen hallintaan ja tietoturvakonfiguraatioihin.

Käytetyt testausmenetelmät ja työkalut

Työkalut: OWASP ZAP, Burp Suite

Metodologia: Harmaa laatikko -testaus

2. Yhteenveto

Keskeiset löydökset ja suositukset

Puuttuva Content Security Policy (CSP): Sovelluksesta puuttuu CSP, mikä altistaa sen XSS- ja data-injektiohyökkäyksille. Suositus: Määritä tiukka CSP käytettäväksi kaikilla sivuilla.

SQL-injektio haavoittuvuus: Parametrien käsittelyssä havaittiin puutteita, jotka mahdollistavat SQL-injektion. Suositus: Käytä valmiita kyselyjä (Prepared Statements) ja parametrisoituja kyselyjä SQL-tietokantakutsuihin.

Puuttuvat anti-clickjacking- ja MIME-sniffing-headerit: X-Frame-Options ja X-Content-Type-Options -otsikot puuttuvat, mikä mahdollistaa ClickJacking- ja MIME-sniffing-hyökkäykset. Suositus: Lisää asianmukaiset turvaotsikot palvelimen konfiguraatioon.

Yleinen arvio tietoturvan tilasta

Testauksen perusteella sovelluksessa on useita kriittisiä ja keskitasoisia haavoittuvuuksia, jotka voivat johtaa tietovuotoihin tai järjestelmän kompromisoitumiseen. Parannukset CSP:n, syötteen validoinnin ja tietoturvaotsikoiden osalta ovat ensisijaisia toimenpiteitä.

3. Löydökset ja löydöksien kategoriointi

Punainen (Kriittinen)

SQL-injektio: Havaittiin, että sovellus ei suodata syötteitä kunnolla, mahdollistaen SQL-injektion hyödyntämisen (esim. käyttäjätietojen kaappaaminen tai tietokannan manipulointi).

Path Traversal: Sovellus altistuu polkujen manipuloinnille, mikä voi johtaa arkaluonteisten tiedostojen lataamiseen tai suorittamiseen.

Keltainen (Keskitaso)

Puuttuva Content Security Policy (CSP): Ilman CSP:tä sovellus on alttiina XSS-hyökkäyksille, mikä mahdollistaa haitallisten skriptien suorittamisen käyttäjän selaimessa.

Puuttuvat turvallisuusotsikot: X-Frame-Options ja X-Content-Type-Options puuttuvat, mikä altistaa sovelluksen ClickJackingille ja MIME-sniffingille.

Sovelluksen virheilmoitukset paljastavat liikaa tietoa: Palvelinvirheilmoitukset voivat paljastaa sovelluksen rakenteeseen liittyviä tietoja hyökkääjille.

Vihreä (Matala)

User Agent Fuzzer -testaus osoitti erilaista käyttäytymistä eri käyttäjäagenteilla: Tämä voi paljastaa tietoa sovelluksen eri versioista tai eri käyttäjäryhmille suunnatuista ominaisuuksista.

Mahdollinen formaattivirhe: Testauksen aikana havaittiin virheviesti / %s, joka voi viitata epävarmaan merkkijonon muotoiluun koodissa.
