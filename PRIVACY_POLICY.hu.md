# Adatkezelési tájékoztató

**BME Mérnökinformatikus Anyagbázis Bot**  
Discord-alkalmazásazonosító: **1552045664257712288**  
Verzió: 1.0 – tervezet  
Hatálybalépés: **2026.09.22**

> Közzététel előtti tervezet. A hiányzó adatkezelői, tárhely- és megőrzési adatokat ki kell tölteni. A megjelölt jogalapokat az üzemeltetőnek a tényleges működésére tekintettel ellenőriznie kell. A jelenlegi szoftver nem végez általános, időalapú adattörlést; ehhez üzemeltetői eljárás szükséges.

## 1. Ki kezeli az adatokat?

Adatkezelő: **BenceGLG (üzemeltetői név; jogi név: Galgovszki Bence)**  
Kapcsolattartási cím: **bgalgovszki@gmail.com**  
Adatvédelmi megkeresések: **bgalgovszki@gmail.com**  
Adatvédelmi tisztviselő, ha kijelölése alkalmazandó: **Galgovszki Bence**

A tájékoztató a botot üzemeltető személy vagy szervezet adatkezeléséről szól. A Discord a saját szolgáltatásában végzett adatkezelését a [Discord adatvédelmi tájékoztatójában](https://discord.com/privacy) ismerteti. A bot nem az egyetem hivatalos szolgáltatása.

## 2. Milyen adatok kerülnek a bothoz?

Az adatokat a Discord API-ján keresztül, a parancsokat és űrlapokat használó személyektől, valamint jelentések és moderáció esetén a bejelentőktől és a személyzettől kapjuk.

| Adatkör | Példák és cél |
| --- | --- |
| Discord-azonosítók és jogosultsági adatok | Felhasználó-, szerver-, rang-, csatorna- és üzenetazonosítók; jogosultságellenőrzés, rangkezelés, tartalomhoz rendelés |
| Beküldött tananyagok | Cím, leírás, témakör, tantárgy, címkék, URL, csatolt fájl, időpont, jóváhagyási állapot; a könyvtár működtetése |
| Jelentések és ellenőrzések | Jelentő/feltöltő/moderátor azonosítója, indoklás, döntés, időpont; hibák és visszaélések kezelése |
| Moderáció | Figyelmeztetések, időkorlátok, eltávolítások, kitiltások és azok indokai; a közösség védelme |
| Hozzájárulások | Feltöltési és jóváhagyási számok, pontok, kézi korrekciók; profil és toplista |
| Értesítések | Tantárgyi feliratkozás, felhasználóazonosító és kézbesítési nyilvántartás; kért emlékeztetők |
| Technikai és auditnaplók | Műveletek, hibák, kézbesítési próbálkozások, kapcsolódó azonosítók; hibaelhárítás és ellenőrizhetőség |

A bot nem épít általános chatarchívumot, nem használ üzenettartalom- vagy jelenlétfigyelési Gateway-intentet, és nem rögzít hangot. Egyes funkciókhoz azonban lekéri a kapcsolódó Discord-üzeneteket: például a saját tananyagbejegyzését szerkesztéshez, vagy a közelmúlt üzeneteit a személyzet által kért törléshez. A Discord által rendelkezésre bocsátott tag- és rangadatokat is feldolgozza jogosultságellenőrzéskor.

A bot nem kér Discord-jelszót, belépési tokent, fizetési adatot vagy személyazonosító okmányt. Ne tölts fel felesleges személyes adatokat. A fájlok tartalma és a beküldött szöveg is tartalmazhat személyes adatot; ezeket szükség esetén az üzemeltetőnek külön kell felülvizsgálnia.

## 3. Célok és jogalapok

**Az üzemeltető által ellenőrizendő jogalapok:** a tananyagbázis rendszerezéséhez, azonosítható hozzájárulásokhoz, közösségi profilokhoz, moderációhoz és működési naplókhoz a biztonságos, követhető közösségi szolgáltatás fenntartásához fűződő jogos érdek; az önkéntes tantárgyi emlékeztetőkhöz hozzájárulás. Kötelező hatósági megkeresés teljesítése esetén az adott jogi kötelezettség lehet irányadó.

A jogos érdek nem korlátlan felhatalmazás: az üzemeltetőnek mérlegelnie kell az érintettek érdekeit és jogait. A bot használata önmagában nem jelenti, hogy bármilyen adatkezeléshez hozzájárultál.

Az emlékeztetőt az `/ertesitesek` paranccsal kapcsolhatod ki. A visszavonás a jövőbeli értesítéseket állítja le. A feliratkozás nem feltétele a tananyagok böngészésének. Azonosító nélkül a személyhez kötött feltöltési, pontozási és moderációs funkciók nem működtethetők ugyanúgy.

## 4. Ki láthatja az adatokat?

A jóváhagyott tananyagok, leírásaik és a feltöltő Discord-megjelölése az adott csatorna jogosult olvasói számára láthatók. A közösségi profil és toplista más szervertagok által is lekérdezhető; a pontok nem kizárólag személyzeti adatok. A tagság vagy az anyag letöltése lehetővé teheti további példányok készítését.

A jóváhagyásra váró anyagok, jelentések és moderációs naplók a beállított személyzet számára érhetők el. Az üzemeltető és a szükséges technikai hozzáféréssel rendelkező személyek a helyi adatbázishoz, fájlokhoz és naplókhoz is hozzáférhetnek. A hozzáférések helyes beállításáért az üzemeltető felel.

A bot a Discord infrastruktúráját használja az üzenetekhez, csatolmányokhoz és privát értesítésekhez. A jelenlegi kód nem tartalmaz hirdetési, adateladási vagy mesterségesintelligencia-tanítási integrációt.

További tárhely- vagy technikai szolgáltató: **[KITÖLTENDŐ: szolgáltató neve és szerepe; saját gépes üzemeltetés esetén ezt kell jelezni]**. A külső tananyaglinkek megnyitásakor az adott weboldal saját adatkezelése érvényes; a bot nem tölti le automatikusan ezeket az oldalakat.

## 5. Tárolás és nemzetközi adattovábbítás

A bot saját adatai SQLite-adatbázisban, a csatolmányok másolatai pedig az üzemeltető háttértárán találhatók. A Discordon közzétett üzenetek és fájlok emellett a Discord rendszerében is jelen vannak.

A botot futtató gép helye: **Magyarország**. A mentések helye és az esetleges tárhelyszolgáltató: **LOCALHOST**. Ha az üzemeltető EGT-n kívüli szolgáltatót vesz igénybe, itt ismertetni kell az érintett továbbítást és az alkalmazott garanciákat: --. A Discord saját nemzetközi adatkezeléséről annak tájékoztatója ad információt.

## 6. Mennyi ideig őrizzük meg?

A megőrzés a tananyagbázis céljához, az ügy lezárásához, a biztonsági szükséglethez vagy egy tényleges jogi kötelezettséghez igazodik. Az alábbi időszakokat az üzemeltetőnek véglegesítenie és ténylegesen végrehajtania kell; a szoftver önmagában nem biztosítja őket.

| Adatok | Véglegesítendő megőrzési szabály |
| --- | --- |
| Aktív tananyag és feltöltői kapcsolat | A tananyag szükséges és jogszerű szolgáltatásban tartásáig; szükségességi felülvizsgálat: **[KITÖLTENDŐ: gyakoriság]** |
| Elutasított/eltávolított fájlok és metaadatok | **[KITÖLTENDŐ: időtartam és az időszak kezdete]** |
| Lezárt jelentések, figyelmeztetések, auditadatok | **[KITÖLTENDŐ: kategóriánkénti időtartam vagy indokolt felülvizsgálati szabály]** |
| Pontok és profilkapcsolatok | A közösségi hozzájárulás szükséges nyilvántartásáig, illetve az elfogadott törlési/tiltakozási kérelem teljesítéséig |
| Értesítési feliratkozás | Kikapcsolásig vagy elfogadott törlési kérelemig; régi kézbesítési jelölések: **[KITÖLTENDŐ: időtartam]** |
| Technikai naplók | Jelenleg méretalapú rotáció; időalapú felső korlát: **[KITÖLTENDŐ]** |
| Biztonsági mentések | **[KITÖLTENDŐ: mentési ciklus és végleges kivezetési idő]** |

A bot eltávolítása a szerverről vagy a szerver elhagyása nem törli automatikusan a tárolt adatokat. Szükségtelenné vált adatot az üzemeltetőnek törölnie vagy megfelelően anonimizálnia kell. Indokolt megőrzés esetén csak a szükséges adatkör maradhat meg korlátozott hozzáféréssel.

## 7. Törlési kérelem és a jelenlegi technikai korlátok

A fenti kapcsolattartási címen kérhetsz törlést. Add meg a Discord-felhasználóazonosítódat és az érintett adatokat; jelszót vagy bot tokent soha ne küldj. A kérelemhez indokolt, arányos módon ellenőrizhetjük, hogy az érintett fiókhoz tartozol.

Az adminisztrátori törlési funkció eltávolítja a feltöltői/jelentői kapcsolatot a megfelelő adatbázisrekordokból, törli a pontokat és értesítési adatokat, valamint frissíti az aktív tananyagkártyákat. **Nem törli automatikusan** a figyelmeztetéseket, auditnaplókat, jóváhagyói adatokat, történeti személyzeti üzeneteket, mentéseket vagy a feltöltött fájlban szereplő személyes adatokat. Ezeket a kérelem részeként külön kell megvizsgálni és szükség esetén törölni vagy kitakarni. A Discordon vagy más felhasználóknál található másolatok kezelése külön intézkedést igényelhet.

## 8. Érintetti jogok

Az alkalmazandó feltételek szerint kérhetsz hozzáférést, helyesbítést, törlést, korlátozást és adathordozhatóságot; tiltakozhatsz a jogos érdeken alapuló adatkezelés ellen, és visszavonhatod a hozzájárulásodat. A kérelmekre főszabály szerint egy hónapon belül válaszolunk; jogszerű hosszabbításról tájékoztatunk.

Panaszt tehetsz az illetékes felügyeleti hatóságnál, Magyarországon a [Nemzeti Adatvédelmi és Információszabadság Hatóságnál](https://www.naih.hu/), és bírósági jogorvoslatot is igénybe vehetsz.

A bot automatikusan számít pontokat és technikai korlátozásokat alkalmaz, de nem értékel egyetemi teljesítményt. A tartalmi jóváhagyási és moderációs döntéseket személyzet kezdeményezi; felülvizsgálat kérhető.

## 9. Biztonság és változások

A program jogosultságellenőrzéseket, paraméterezett adatbázis-lekérdezéseket, feltöltési korlátokat és auditnaplózást használ. Az üzemeltető feladata a gép, a hozzáférések, a tokenek és mentések védelme. A tájékoztató nem állítja, hogy a helyi adatok automatikusan titkosítottak, vagy hogy a fájlokat vírusellenőrző vizsgálja.

A lényeges adatkezelési változásokat a tájékoztató frissítésével és a szerver tájékoztatási csatornáján jelezzük. Ha új hozzájárulás szükséges, azt külön kérjük.
