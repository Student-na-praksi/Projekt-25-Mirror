# Celovita rešitev organizacije pluženja

### Jošt Eržen, Filip Gros, Sebastjan Kordiš, Matevž Vidovič

## 1 Uvod

### Začetni odstavek

Ob novozapadlem snegu se promet skoraj ustavi. Organizacije, ki se ukvarjajo s pluženjem, se na vso moč trudijo, da se situacija ne poslabša do te mere, da bi postala totalen prometni kolaps.
Naš projekt želi biti celovita rešitev organizacije pluženja, da lahko s tem pomagamo pri koordinaciji in nadzorovanju le tega pluženje naredimo učinkovitejše. Poleg tega želimo povezati pravne in fizične osebe, ki potrebujejo pluženje parkirišč in dvorišč, z izvajalci pluženja, kot so kmetje, da lahko zunaj plužne konice omogočimo to storitev, ki koristi obema stranema.
Tako postanejo Vaši stroški pluženja nižji, občani pa so bolj zadovoljni, saj lahko kljub snegu normalno potujejo. Občani bodo zadovolni tudi s spremljanjem pluženja v realnem času, saj bodo tako lahko videli, kdaj je pot, na katero se odpravljajo splužena, in lahko tudi vidijo, da bo do tega tudi prišlo in niso pozabljeni. Največji vpliv pa zna imeti povezovanje pomoči potrebnih in samostojnih plugov, ki skupnosti omogoči, da se s snegom spopade kot celota in ne kot skupek posameznikov.


### 1.1 Izzivi

Člani ekipe se bežno poznamo, ker smo se že nekajkrat videli na faksu, vendar še nikoli nismo med seboj sodelovali na projektu. Iz tega razloga so na začetku največji izziv za ekipo predtavljali medsebojno usklajevanje, torej organizacija časa, čim bolj ustrezna delitev dela in dobra medsebojna komunikacija. Ta izziv smo uspeli nasloviti in premostiti.
Prav tako noben član ekipe še ni sodeloval na projektu, ki bi vseboval ravno te tehnologije, kar je predstavljalo svojevrsten izziv. Večina nas pozna posamezne tehnologije, vendar nam je bilo njihovo povezovanje v celovit sistem precej tuje.
Razvoj algoritma za rešitev problema optimizacije pluženja se je izkazal za zahteven izziv. Predvsem nas je presenetilo potrebno delo za pripravo podatkov v obliko, na kateri lahko izvajamo algoritem, saj se je izkazalo za obsežno nalogo.
Najhujše pa je bilo spoznavanje novih tehnologij, saj smo na področju spletnega programiranja popolnoma neizkušeni in smo vse napake reševali prvič.

### 1.2 Poudarki

V okviru projekta smo ustvarili spletni vmesnik za vpogled in posodabljanje stanja na cestah MOC. Naš sistem podpira posodabljanje stanja na cestah ter dodajanje zahtevkov za pluženje. Zahtevki za pluženje so tisto, kar si lastniki hiš velikokrat pravijo. "Odmetavam sneg iz dvorišča že 3h, medtem ko bi plug, ki pelje mimo potreboval pičle 3 minute." Znotraj naše aplikacije smo omogočili, da bo posameznik ali podjetje lahko oddalo zahtevek, ki bo vseboval naslov, opis ter denarno vsoto, ki jo je pripravljen plačati za storitev pluženja zasebnega zemljišča.

### 1.3 Spremembe

- 28.3. Odločitev za hevristični algoritem določitve optimalnih poti pluženja. Ne bomo iskali popolne rešitve, le eno izmed boljših.
- 5.4. Iz večjega osredotočenja na algoritem organizacije pluženja smo postopoma pozornost v večji meri preusmerili na funkcionalnosti povezane z organizacijo samostojnih plugov za opravljanje dodatnih del.
- 24.4. Namesto izrisa poti navigiranja bomo plugu le izrisali oštevilčene marker-je na križiščih. To olajša rešitev, saj dosedanje rešitve za prikaz poti navigiranja niso delovale dobro. Poleg tega nova zastavitev bolje deluje z našim algoritmom in za uporabnika ne bi smela predstavljati problema.
- 1.5. Opustili bomo CD, ampak bomo ročno vzpostavili novo verzijo projekta vsakič ko bo dovolj napredka, saj tako lahko lažje spremljamo kaj je šlo pri postavitvi narobe in prepustimo to področje le enemu članu ekipe, ker se nam zdi dokaj specifično.

## 2 Potrebe naročnika

Podjetji, ki opravljata pluženje, si želita intuitiven in zanesljiv nadzor nad situacijo pluženja, ter zmanjšane stroške pluženja zaradi višje učinkovitosti.
Občani in lokalna podjetja želijo možnost kontakta s kmeti, ki bi bili pripravljeni pomagati pri pluženju dvorišč in parkirišč, saj je to za večje površine izvajati ročno zelo zahtevno in zamudno, medtem ko kmet s plugom to nalogo opravi zelo hitro. Kmetje s plugom pa si želijo dostopa do nove potencialne storitvene dejavnosti.
Sistem mora vsakemu od deležnikov biti preprost za uporabo, brez nepotrebnih funkcionalnosti, zaradi katerih bi postal zapleten. Sistem mora biti robusten, saj, če se deležniki nanj zanašajo, njegova napaka lahko povzroči prometni kolaps.

### 2.1 Uporabniške zahteve

Kot neregistriran uporabnik želim:
- imeti dostop do zemljevida stanja spluženosti cest, da lahko preverim razmere.
- imeti možnost registracije, da lahko postanem Stranka.

Glede na to, da sem neregistriran uporabnik:
- ko zahtevam možnost registracije, sem preusmerjen na stran ki mi to omogoča.

Kot Administrator želim:
- na zemljevidu videti lokacije Ustaljenih Plugov, da imam pregled nad izvajanjem pluženja.
- ob kliku na Usataljeni Plug dobiti njihovo telefonsko številko, da ga lahko kontaktiram.
- imeti možnost urejanja števila plugov v štartni bazi in lokacije štartnih baz, da se podatki v zaledju spremenijo v realnem času.

Glede na to, da sem admin:
- ko kliknem na Ustaljeni Plug na zemljevidu, dobim njegovo telefonsko številko.
- ko zahtevam urejanje števila plugov v štartni bazi in lokacije štartnih baz, se te podatki posodobijo v roku 1 minute po oddani zahtevi.

Kot Ustaljeni Plug želim:
- da se mi glede na trenuten GPS izpisujejo navodila za nadaljno pot, da sledim optimalni poti pluženja.
- imeti možnost deaktivacije, da se lahko umaknem iz pluženja (zaradi malice, okvare, premora).

Glede na to, da sem Ustaljeni Plug:
- ko zahtevam deaktivacijo, je ta objavljena v roku 30 sekund.


Kot Stranka želim:
- imeti možnost oddaje zahtevka za pluženje, da lahko s tem naročim pluženje snega za zasebnem zemljišču.

Kot Samostojni Plug želim:
- videti trenutno nalogo, da se lahko odpeljem do nje in jo opravim.

Kot Manager želim:
- videti lokacije Samostojnih Plugov in ob kliku na dotičen plug dobiti njegovo telefonsko številko, da ga lahko kontaktiram.
- imeti možnost usmeriti dotičen Samostojni Plug na zemljevidu na določeno opravilo, da se mu posodobi trenutno opravilo.

Glede na to, da sem Manager:
- ko Samostojnemu Plugu spremenim opravilo, je ta o njem obveščen v roku 2 minut.

## 3 Cilji projekta

Projekt bo samodejno organiziral pluženje po približku optimalnega načrta plužnih poti. Poti bo spremenil ob sprotnem dodajanju in odvemanju plugov, kar naročniku omogoča večjo prilagodljivost. Na ta način bo zmanjšal stroške goriva dela, ter občanom izboljšal izkušnjo s prometom na dni sneženja.
Z delom aplikacije, ki samostojnim plugom omogoča povezovanje s pravnimi in fizičnimi osebami za pluženje parkirišč in dvorišč, bomo izboljšali kaotično stanje, ki nastane ob novozapadlem snegu. Tako bo delo lažje organizirano in razporejeno, saj se ne bo vsako podjetje potrebovalo dogovarjati z določenim opravljalcem plužnih storitev, da to poskrbi za njih. Prav tako lahko pomaga šibkejšim članom družbe, naprimer starejšim, ki svojih dvorišč ne morejo očistiti sami, kar povzroča tudi poledico in nevarnost poškodbe zaradi padca.

### 3.1 Primeri uporabe



##### Slovar pojmov

- UI - uporabniški vmesnik (User Interface). Je grafična podoba in osnovno delovanje spletne strani.
- Baza - podatkovna baza, baza podatkov.
- SCRUM master - vodja delovnega procesa skupine.
- Product owner - oseba, ki zajema uporabniške zahteve in jih komunicira ekipi.
- Samostojni plug - plužilec zunaj osnovnega okvira pluženja (npr. kmetje).
- Ustaljeni plug - običajni plug, ki je del sistema (npr. plug družbe Zelenice).
- API - aplikacijski vmesnik. Zunanja storitev, od katere prejmemo podatke.
- frontend - spletna stran in uporabniška izkušnja aplikacije.
- backend - zaledni sistem, kjer se procesirajo podatki in se izvaja poslovna logika.
- hevristični algoritem - algoritem, ki ne išče popolne rešitve, temveč čim boljšo rešitev na osnovi vmesnih približnih ocen prave smeri izvajanja. Je veliko hitrejši od algoritma, ki bi našel najboljšo rešitev. 
- Vite - okolje za razvoj frontend-a.
- Continuous Deploymentu - posodabljanje aplikacije ob vsaki spremembi kode.
- Python - programski jezik, ki ga uporabljamo za backend.
- JavaScript - programski jezik, ki ga uporabljamo za frontend.
- node.js - razširitev jezika JavaScript.
- GitHubCopilot - orodje, ki deluje na podlagi umetne inteligence, pomaga pri pisanju kode.
- programski hrošč ali bug - napaka v kodi.
- refactoring - izboljšava preglednosti sicer delujoče kode.
- penetration tester - oseba, ki obvlada preverjanje ranljivosti vdorov v sistem.
- SQL injection - zlonamerna uporaba vnosnega besedila za spremembo baze.
- PyVRP - algoritem za optimizacijo poti, implementiran v jeziku Python.
- hosting - najem strežnika, od koder je dostopna aplikacija.

#### 3.1.1 Akterji, katere funkcionalnosti imajo na voljo.

Poznamo 6 vrst akterjev.
Neregistriran uporabnik je vsakdo, ki obišče osnovno spletno stran. Vidi lahko zemljevid stanja spluženosti cest in ima možnost registracije, da postane Stranka.
Admin je glavni upravitelj s sistemom. Njegova glavna naloga je upravljanje s štartnimi bazami pluženja in dodajanje novih akterjev (razen teh tipa Stranka).
Ustaljeni plug predstavlja plug znotraj obstoječega sistema pluženja, Samostojni plug pa je neodvisen delavec, ki pomaga pri pluženju, kot so pogosto kmetje, ki jim je pluženje dodatna dejavnost.
Stranka je lahko vsakdo, ki želi oddati zahtevek za pluženje neke površine na področju MOC. To so lahko fizične ali pravne osebe.
Manager pluženja opravlja koordinacijo plugov pri napotitvah na zahtevke za pluženje.

Akterjem je na voljo 12. funkcionalnosti, ki v ozadju uporabljajo še 8 podpornih funkcionalnosti. Določenemu tipu akterja je dostopen določen nabor funkcionalnosti. Ta nabor je predstavljen s terko številk.Oštevilčenost funkcionalnosti je na voljo spodaj.

Neregistriran uporabnik: (1, 2)<br>
Admin: (1, 3, 4, 5, 10, 11, 12)<br>
Ustaljeni plug (3, 6, 7, 9, 12)<br>
Stranka (1, 3, 8, 12)<br>
Samostojni plug (3, 9, 12)<br>
Manager pluženja (1, 3, 4, 10, 12)<br>

Uporabniške funkcionalnosti:
1. Dostop do stanja pluženja 
2. Registracija Stranke
3. Prijava
4. Kontaktiranje pluga
5. Urejanje števila plugov in štartnih baz
6. Aktivacija pluga
7. Deaktivacija pluga
8. Oddaja zahtevka za pluženje
9. Izbira naloge pluženja
10. Usmeritev Samostojnega pluga
11. Registracija osebja
12. Pridobitev pozabljenega gesla

Podporne funkcionalnosti:
13. Poskus registracije
14. Potrditev registracije
15. Posodobitev štartnih baz
16. Potrditev (de)aktivacije
17. Dodajanje zahtevka
18. Izbira zahtevka
19. Dodajanje uporabnika





#### 3.1.2 Primeri uporabe

Business value ocenjujemo na skali od 1 do 10, kjer 1 pomeni “zelo majhna poslovna vrednost” in 10 pomeni “ogromna poslovna vrednost”.
Pogostost uporabe ocenjujemo na skali od 1 do 10, kjer 1 pomeni “skoraj nikoli uporabljeno” in 10 pomeni “uporabljeno ves čas”.

##### 1. Dostop do stanja pluženja (MUST HAVE)
Dostop do stanja pluženja uporabniku izriše zemljevid pluženja, kjer so cest pobarvane glede na zasneženost oziroma čas od zadnjega pluženja, ter so vidne trenutne lokacije plugov.
Business value: 8
Pogostost uporabe: 10

Osnovni tok:
1. Uporabnik dostopa do začetne spletne strani sistema.
2. Zaslonska maska kliče GoogleMaps API in pridobi zemljevid območja.
3. Zaslonska maska od zalednega sistema pridobi stanje cest.
4. Kot del strani se izriše zemljevid stanja pluženja.


##### 2. Registracija Stranke (SHOULD HAVE)
Neregistriran uporabnik se lahko registrira v sistem in tako postane Stranka.
Business value: 6
Pogostost uporabe: 2

Osnovni tok:
1. Uporabnik dostopa do začetne spletne strani sistema.
2. Uporabnik klikne na gumb “Registracija”.
2. Izriše se registracijsko okno.
3. Uporabnik vnese svoje podatke (e-poštni naslov, uporabniško ime, geslo), pri čemer geslo vnese dvakrat, ter klikne na gumb “Registriraj me”.
4. Sproži se tok dogodkov primera uporabe “Poskus registracije”.
5. Primer uporabe “Poskus registracije” vrne sporočilo o uspešnosti.
6. Uporabnik je preusmerjen na začetno spletno stran sistema.
7. Sproži se tok dogodkov primera uporabe “Potrditev registracije”

Predpogoj: Uporabnik še ni registriran v sistem kot Stranka.
Popogoj: Uporabnik prejme e-poštno sporočilo, kjer lahko potrdi prijavo.

Alternativni tok:
Če na koraku 5 “Poskus registracije” vrne sporočilo, da registracija ni uspešna, uporabnika obvesti o napaki. (Primer: “Uporabnik s tem e-poštnim naslovom že obstaja). Tok se zaključi.



##### 3. Prijava (MUST HAVE)
Prijava obstoječim uporabnikom omogoči vstop v sistem in dostop do funkcionalnosti, ki so namenjene njihovemu tipu uporabnika.
Business value: 10
Pogostost uporabe: 8

Osnovni tok:
1. Uporabnik dostopa do začetne spletne strani sistema.
2. Kot del strani se izriše prijavno okno.
3. Uporabnik vnese prijavne podatke ter klikne na gumb “Prijava”.
4. Zalednemu sistemu je poslan zahtevek za prijavo.
5. Zaledni sistem vrne sporočilo o sprejetju prijave.
6. Uporabnik je preusmerjen na spletno stran, ki je primerna njegovemu tipu uporabnika.

Predpogoj: Uporabnik je potrjeno registriran.
Popogoj: Uporabnik lahko uporablja funkcionalnosti, ki so na voljo njegovemu tipu uporabnika.

Alternativni tok:
Če je koraku 5 vrnjeno sporočilo o zavrnitvi prijave, se o tem izpiše obvestilo. (Primer: “V podanem uporabniškem imenu ali geslu je prisotna napaka.”) Tok se zaključi.



##### 4. Kontaktiranje pluga (COULD HAVE)
Admin in Manager preko uporabe Kontaktiranje pluga pridobita kontaktne podatke izbranega pluga.
Business value: 2
Pogostost uporabe: 2

Osnovni tok:
1. Admin/Manager na strani Admin UI/Manager UI klikne na enega od plugov na zemljevidu ali enega od plugov v tabeli deaktiviranih plugov.
2. Odpre se okno s kontaktnimi podatki izbranega pluga.

Predpogoji:
Uporabnik je prijavljen kot Admin ali Manager.



##### 5. Urejanje števila plugov in štartnih baz (COULD HAVE)
Primer uporabe omogoča Admin-u, da spremeni lokacije štartnih baz in število plugov, ki posamezni bazi pripadajo. Tako vpliva na algoritem izbire najboljših poti.
Business value: 4
Pogostost uporabe: 2


Osnovni tok:
1. Admin na strani Admin UI klikne na gumb “Uredi štartne baze”.
2. Izriše se okno s tabelo štartnih baz, njihovih lokacij ter njihovo številčnostjo pripadajočih plugov.
3. Admin v oknu ureja podatke in klikne na gumb “Shrani”.
4. Izrisano okno s tabelo štartnih baz se zapre. 
5. Sproži se tok dogodkov primera uporabe “Posodobitev štartnih baz”.
6. Primer uporabe “Posodobitev štartnih baz” vrne sporočilo o uspešnosti, ki se uporabniku izpiše.

Predpogoj: Uporabnik je prijavljen kot Admin.
Popogoj: Podatki štartnih baz so posodobljeni.






##### 6. Aktivacija pluga (SHOULD HAVE)
Ustaljeni plug preko Aktivacija pluga svoj plug vrne v med aktivne pluge v stanju pluženja, če je bil predhodno deaktiviran.
Business value: 4
Pogostost uporabe: 3

Osnovni tok:
1. Ustaljeni plug na Plug UI klikne na gumb “Aktivacija”.
2. Sproži se tok dogodkov primera uporabe “Potrditev (de)aktivacije”.
3. Primer uporabe “Potrditev (de)aktivacije” vrne sporočilo o uspešnosti, ki se uporabniku izpiše.
4. Gumb “Aktivacija” se spremeni v gumb “Deaktivacija”

Predpogoji:
Uporabnik je prijavljen kot Ustaljeni plug.
Ustaljeni plug je deaktiviran.

Popogoj: Ustaljeni plug je dodan na seznam aktivnih plugov.

Alternativni tok:
Če na koraku 3 “Potrditev (de)aktivacije” vrne sporočilo, da aktivacija ni uspešna, se o tem izpiše obvestilo. Tok se zaključi.




##### 7. Deaktivacija pluga (SHOULD HAVE)
Ustaljeni plug izvzame svoj plug vrne iz stanja pluženja.
Business value: 4
Pogostost uporabe: 2

Osnovni tok:
1. Ustaljeni plug na Plug UI klikne na gumb “Deaktivacija”.
2. Sproži se tok dogodkov primera uporabe “Potrditev (de)aktivacije”.
3. Primer uporabe “Potrditev (de)aktivacije” vrne sporočilo o uspešnosti, ki se uporabniku izpiše.
4. Gumb “Deaktivacija” se spremeni v gumb “Aktivacija”

Predpogoji:
Uporabnik je prijavljen kot Ustaljeni plug.
Ustaljeni plug je aktiviran.

Popogoj: Ustaljeni plug je odstranjen iz seznama aktivnih plugov.

Alternativni tok:
Če na koraku 3 “Potrditev (de)aktivacije” vrne sporočilo, da deaktivacija ni uspešna, se o tem izpiše obvestilo. Tok se zaključi.





##### 8. Oddaja zahtevka za pluženje (SHOULD HAVE)
Primer uporabe omogoči Stranki, da je njihov zahtevek dodan v bazo trenutnih zahtevkov.
Business value: 6
Pogostost uporabe: 5

Osnovni tok:
1. Stranka na Stranka UI v okno zahtevka vnese podatke zahtevka ter klikne na gumb “Oddaj zahtevek”.
2. Sproži se tok dogodkov primera uporabe “Dodajanje zahtevka”.
3. Primer uporabe “Dodajanje zahtevka” vrne sporočilo o uspešnosti, ki se uporabniku izpiše.

Predpogoj: Uporabnik je prijavljen kot Stranka.
Popogoj: Zahtevek je dodan med trenutne zahtevke.





##### 9. Izbira naloge pluženja (SHOULD HAVE)

Samostojni plug ali Ustaljeni plug prevzame opravljanje zahtevka pluženja, ki je odstranjen iz baze trenutnih zahtevkov.
Business value: 6
Pogostost uporabe: 3

Osnovni tok:
1. Samostojni plug ali Ustaljeni plug klikne na gumb “Izberi nalogo”.
2. Odpre se okno z nalogami, ki so na voljo, in so uporabniku blizu po geolokaciji.
3. Uporabnik označi nalogo in klikne na gumb “Izberi”.
4. Okno z nalogami se zapre.
5. Sproži se tok dogodkov primera uporabe “Izbira zahtevka”.
6. Primer uporabe “Izbira zahtevka” vrne sporočilo o uspešnosti, ki se uporabniku izpiše.

Predpogoj: Uporabnik je prijavljen kot Samostojni plug ali Ustaljeni plug.

Popogoj: Zahtevek je odstranjen iz trenutnih zahtevkov.



##### 10. Usmeritev Samostojnega pluga (COULD HAVE)
Admin ali Manager lahko napotita Samostojni plug na nalogo iz množice trenutnih zahtevkov, če opazita, da je ta res nujna.
Business value: 1
Pogostost uporabe: 2

Osnovni tok:
1. Uporabnik klikne na plug na izrisanem zemljevidu.
2. Poleg kontaktnih podatkov se pojavi gumb “Usmeri”, ki ga klikne.
3. Izbranemu plugu je na njegov UI dodano rdeče obvestilo o usmeritvi z gumbom “Sprejmi”. Klikne ga takoj, ko lahko.
4. Sproži se tok dogodkov primera uporabe “Izbira zahtevka”.
5. Primer uporabe “Izbira zahtevka” vrne sporočilo o uspešnosti, ki se izbranemu plugu izpiše.
6. Izbranemu plugu se iz UI odstrani rdeče obvestilo.

Predpogoj: Uporabnik je prijavljen kot Admin ali Manager in izbrani plug je prijavljen kot Samostojni plug ali Ustaljeni plug.

Popogoj: Zahtevek je odstranjen iz trenutnih zahtevkov.



##### 11. Registracija osebja (MUST HAVE)
Admin lahko v sistem doda kateregakoli od akterjev.
Business value: 10
Pogostost uporabe: 2

Osnovni tok:
1. Admin klikne na gumb “Dodaj uporabnika”.
2. Izriše se okno v katerem lahko izbere tip uporabnika in vnese njegove podatke. Klikne na gumb “Dodaj”.
3. Sproži se tok dogodkov primera uporabe “Dodajanje uporabnika”.
4. Primer uporabe “Dodajanje uporabnika” vrne sporočilo o uspešnosti, ki se izpiše.

Predpogoj: Uporabnik je prijavljen kot Admin.
Popogoj: Uporabniški profil je dodan v sistem.

Alternativni tok:
Če na koraku 3 “Dodajanje uporabnika” vrne sporočilo, da dodajanje ni uspešno, se le-to izpiše.


##### 12. Pridobitev pozabljenega gesla (MUST HAVE)
Če uporabnik pozabi geslo ga lahko pridobi preko e-pošte.
Business value: 10
Pogostost uporabe: 4

Osnovni tok:
1. Uporabnik klikne na gumb “Pozabil sem geslo”.
2. Izriše se okno za vnos e-poštnega naslova. Uporabnik klikne na gumb “Potrdi”.
3. Sproži se tok dogodkov primera uporabe “Pozabljeno geslo”.
4. Primer uporabe “Pozabljeno geslo” vrne sporočilo o uspešnosti, ki se izpiše.

Predpogoj: Uporabnik je predhodno že bil dodan v bazo uporabnikov.
Popogoj: Uporabnik je prejel e-pošto z geslom.





 Podporne funkcionalnosti:

##### 13. Poskus registracije (SHOULD HAVE)
Poskus registracije uporabnika pripravi, da lahko potrdi svojo registracijo.
Business value: 6
Pogostost uporabe: 2

Osnovni tok:
1. Dobimo zahtevek za registracijo s podatki o uporabniku.
2. Preverimo, če uporabnik s tem e-poštnim naslovom že obstaja.
3. Dodamo ga v bazo še nepotrjenih uporabnikov.
4. Vrnemo sporočilo o uspešnem vpisu.

Popogoj: Uporabnik je vpisan v bazo nepotrjenih uporabnikov.

Alternativni tok:
Če v koraku 2 ugotovimo, da je uporabnik že v naši bazi, vrnemo sporočilo o neuspelem vpisu.


##### 14. Potrditev registracije (SHOULD HAVE)
Potrditev registracije zaključi registracijo uporabnika po tem, ko jo je potrdil na prejetem e-poštnem sporočilu.
Business value: 6
Pogostost uporabe: 2

Osnovni tok:
1. Zaledni sistem pošlje e-poštni naslov uporabnika.
2. Preverimo, če je uporabnik s takšnim e-pošnim naslovom prisoten v bazi nepotrjenih uporabnikov, ter pridobimo njegove ostale podatke.
3. Sproži se tok dogodkov primera uporabe “Dodajanje uporabnika”.
4. Primer uporabe “Dodajanje uporabnika” vrne sporočilo o uspešnosti.
5. Uporabnika odstranimo iz baze še nepotrjenih uporabnikov.
6. O uspešni prijavi ga obvestimo na e-poštni naslov.

Predpogoji:
Uporabnik je vpisan v bazo nepotrjenih uporabnikov.
Uporabnik še ni vpisan v bazo uporabnikov.

Popogoj: Uporabnik je vpisan v bazo uporabnikov.

Alternativni tokovi:
Če v koraku 2 ugotovimo, da uporabnik še ni v naši bazi uporabnikov, ga na e-poštni naslov opozorimo o nenavadnem delovanju. Tok se ustavi.
Če v koraku 4 dobimo sporočilo o neuspešnem dodajanju, uporabniku na e-pošto posredujemo vzrok napake. Tok je zaključen.

##### 15. Posodobitev štartnih baz (COULD HAVE)
V zaledju se spremenijo podatki o štartnih bazah.
Business value: 4
Pogostost uporabe: 2


Osnovni tok:
1. Dobimo podatke o željeni spremembi podatkov o štartnih bazah.
2. V bazi spremenimo podatke.
3. Vrnemo sporočilo o uspešnosti.

Popogoj: Podatki o štartnih bazah so posodobljeni.

Alternativni tokovi:
Če je sprememba podatkov v koraku 2 neuspešna, vrnemo sporočilo o neupešni spremembi.


##### 16. Potrditev (de)aktivacije (SHOULD HAVE)
Sprememba stanja aktivnosti pluga.
Business value: 4
Pogostost uporabe: 5

Osnovni tok:
1. Dobimo zahtevek za spremembo, ki vsebuje šifro pluga in željeno stanje (aktiviran/deaktiviran).
2. Preverimo trenutno stanje pluga.
3. Spremenimo stanje pluga.
4. Vrnemo sporočilo o uspešni spremembi.

Predpogoj: Plug je že zaveden v bazi.
Popogoj: Stanje pluga je enako kot v zahtevku.

Alternativni tokovi:
Če v koraku 2 ugotovimo, da je trenutno stanje že enako željenemu stanju, vrnemo sporočilo o uspehu, ter sporočilu dodamo, da se stanje ni spremenilo.
Če v koraku 2 ugotovimo, da plug ni zaveden v bazi, vrnemo sporočilo o neuspehu ter povemo, da pluga ni v bazi.
Če v koraku 3 ne uspemo spremeniti stanja pluga, vrnemo sporočilo o neupehu, kjer dodamo, da je prišlo do neznane napake in naj uporabnik poskusi kasneje.



##### 17. Dodajanje zahtevka (SHOULD HAVE)
Zahtevek za pluženje je dodan med trenutne zahtevke.
Business value: 6
Pogostost uporabe: 5

Osnovni tok:
1. Dobimo podatke zahtevka.
2. Preverimo, da uporabnik, ki je zaveden na zahtevku, res obstaja.
3. Zahtevek dodamo na seznam trenutnih zahtevkov.
4. Vrnemo sporočilo o uspehu.

Predpogoj: Uporabnik v podatkih zahtevka je vpisan v bazo Strank.
Popogoj: Zahtevek je dodan med trenutne zahtevke.

Alternativni tokovi:
Če v koraku 2 ugotovimo, da uporabnik še ni v naši bazi Strank, ali v koraku 3 ne moremo dodati zahtevka na seznam trenutnih zahtevkov, vrnemo sporočilo o neuspetju. Tok se ustavi.



##### 18. Izbira zahtevka (SHOULD HAVE)
Plug je izbral zahtevek, zato zahtevek ne bo več na voljo.
Business value: 6
Pogostost uporabe: 3

Osnovni tok:
1. Dobimo identifikator zahtevka in podatke o plugu.
2. Preverimo, da je zahtevek na seznamu trenutnih zahtevkov in da plug res obstaja.
3. Z namenom deaktivacije se sproži tok dogodkov primera uporabe “Potrditev (de)aktivacije”.
4. Primer uporabe “Potrditev (de)aktivacije” vrne sporočilo o uspešnosti.
5. Preverimo, da je zahtevek še vedno na seznamu trenutnih zahtevkov.
6. Zahtevek odstranimo iz trenutnih zahtevkov.
7. Zahtevek dodelimo plugu.
8. Vrnemo sporočilo o uspešnosti.

Predpogoji:
Zahtevek je na seznamu trenutnih zahtevkov.
Plug je v bazi plugov.

Popogoji:
Zahtevek ni več med trenutnimi zahtevki.
Plug je deaktiviran.

Alternativni tokovi:
Če v koraku 2 odkrijemo napako, vrnemo sporočilo o neuspešnosti z navedenim razlogom.
Če v koraku 3 dobimo sporočilo o neuspešnosti, vrnemo sporočilo o neuspešnosti z navedenim razlogom.
Če v koraku 5 ugotovimo, da zahtevek ni več na voljo, vrnemo sporočilo o neuspešnosti in opozorimo plug, da je morda bil deaktiviran kljub neuspetju pridobitve zahtevka.


##### 19. Dodajanje uporabnika (MUST HAVE)
Admin lahko dodaja vse vrste uporabnikov.
Business value: 10
Pogostost uporabe: 2

Osnovni tok:
1. Dobimo zahtevek za dodajanje uporabnika.
2. Uporabnika dodamo v bazo.
3. Vrnemo sporočilo o uspešnosti.

Popogoj: Novi uporabnik je prisoten v bazi uporabnikov.

Alternativni tokovi:
Če v koraku 2 ugotovimo, da je uporabnik že prisoten, uspešnemu sporočil dodamo obvestilo, da je uporabnik že predhodno obstajal.


##### 20. Pozabljeno geslo (MUST HAVE)
Pošiljanje pozabljenega gesla na e-pošto uporabnika.
Business value: 10
Pogostost uporabe: 4

Osnovni tok:
1. Dobimo zahtevek o pozabljenem geslu z e-pošto uporabnika.
2. Dobimo geslo iz baze uporabnikov.
3. Pošljemo geslo in uporabniško ime na e-poštni naslov.
4. Vrnemo sporočilo o uspešnosti.

Popogoj: Uporabnik s takšno e-pošto obstaja v bazi uporabnikov.

Alternativni tokovi:
Če v koraku 2 ugotovimo, da takšnega uporabnika ni, prekinemo tok.









#### 3.1.3 Sprejemni testi
![Sprejemni testi 1](gradivo/img/Strategije1.PNG)
![Sprejemni testi 2](gradivo/img/Strategije2.PNG)

















### 3.1.4 Diagram primerov uporabe

![DPU3_1_1](https://teaching.lavbic.net/plantuml/png/VLDDZzem4BtdLrZqaEN0IejKgUfXfR1f4GTOYvGBLGycTaD8i2FROIlQ_fZ-aTxsV-tO9XyEj1V4l7dpPkPveegSLqII8zgHjCYag3bDHIaaqf9m1Id6TQ1Q5cNVILtgB-o7ZieyuqT8enH-cEonQiLIeXZw6Q2UxfFLVTddcXbSICgamzwz_ppxyEa9K2AbU77WheJAu7TFbgHQo5clpb66X9iD0vj3enMJBCkLbZdiX-fAIBBZUJ52KO9McuQ5opgpq0OtK68CAOX5amQS2v6LR4ag5U752165viiWR2h8KIWj3Zn7LQENu3QD1IMw42TEmAEp4yQp890irOI3B2Z0eEo8Aa5XJcPKNlyoVgX7rjd6vL5isbI82gIWya1QeXEDO-ZQew-T0IJDWUhMOfQuJleqB25_kipLJqI5pa-kskpb6957YHcvHOezqZEb1D9dijViL9W_xU1kdkVjrYjOd7VmQeYJKcHiiEHYXGV3Kx63Xp-1UsUoAm-CiuoWZAdoiXAUGq7OLGXLr0h9pXmt15u_37XQKYjyWpeTIefcYjS_caZDyxrvRCTEPlyGlgDitFftaOuZZnmBunqOrThd3Dw67ktYcCTP33YTLFirNCGsyFK5uGQZILrDVZsQurrjq8IA5pvvH7VchiOUiax6WQ4tCVR3Q13748Sn05_tEQMCVxiapDE4rp2SPtIDmaq1_meszz3l1V5WDZmVtwmqLuU2PBZdEhbkRJwin5kt5naT3x0TmyJtnulja3x3rXXZqRt1xWssVXYZZoZdQLbJTfsT-baxHvUFjxrq27ahrpMSZIqslOrrCXk_o_Q_Cy3vzlI02vWPn6lXZ6wn-V8D)

![DPU3_1_2](https://teaching.lavbic.net/plantuml/png/RLExZjim4Epr5GkboBbm6I3L0Rv7d8DWd637LP1YBUt9b2MkG59sS4a-9Z-IxluhIyesHE4QYpixC_iWRGzATsYmXHqMXyfmhyk26pRW36ehAT8kiLTMII_OD-uR_NIBHbMwbJGKyaDcnEej5MW9VYKmyhqFlgUzSkHnDYMP0VlmwSlTvyTxGT4OFWtWhX5bycTaYuLZSpVI3PGfuTs2YUEAt9wCD1Lea2xALkaK5XjONA0LQgo4qpNzsp_IDORqAh_abynLGolix29_IW4jB5VIOcAeSAWb1Ub6MKSjT5nsREZgrATX6vVDf0zi7NTGCbXHrZWf-V2moSVqtAWQZqCkIcIi7HwSajkgGxLg86KHQske3eItluwEgWdbAZw2qXv2uxJQorMz1krsap_5vRUs9IDhFC86MzzvhQd2KRbjp5zJ9MimM4ZNm9Psvx7MpvEXIju5suvVSTVK56mhiirvr7oPYE8ZV5LbIHeArbfMhLXRS0pedw3t0sze_JJkn21Fo8hg9f_1_Fi-A7_CuIRBPzxBVoDy_Unn_udWOGk3v7oEylwAWZ0SfjAhBix8G3F_O1Omxxlvxrl_jkHSyadFRtt7uoYBmqj38yYtFWg7bc9958VooIgFAex3R18FZcDaEmK6pyiM6dfnWihV8bh_cUpXx5tyFm00)




#### 3.1.5 Nefunkcionalne zahteve

Sistem mora delovati za simultano organizacijo do 100 plugov.
Plug pa je avtomatsko voden v smeri njemu začrtanega pluženja. Posodabljanje informacij se dogaja v realnem času, torej se za potrebe pluženja mora posodobiti v največ eni minuti od zadnje spremembe stanja plugov na cestah in sprememb informacij o štartnih bazah.
Zemljevid stanja na cestah je na voljo tudi neregistriranim uporabnikom in prikazuje stanje za največ 5 minut nazaj.
V okviru organizacije opravljanja zahtevkov za pluženje moramo v primeru MOC omogočati hranjenje vsaj 30.000 zahtevkov naenkrat.
Omogočati moramo registriranost za vsaj 70.000 strank, ter hkratno prijavljenost za vsaj 5000 strank.

### 3.2 Merila uspeha

Naročnik je izražil željo za algoritmično podprto določitev poti plugov, spremljanje dela plugov, ter za dodatne funkcionalnosti, ki izboljšajo izkušnjo občanov v okviru pluženja.
To smo uspeli zagotoviti s svojim algoritmom ter podprtjem ideje zahtevkov za pluženje dvorišč in parkirišč, na katere se lahko prijavijo kmetje in prosti plugi.

## 4 Opis sistema

![Opis sistema](https://teaching.lavbic.net/plantuml/png/ZLNDRXen4BxxAKPSQ0zGgSUeQeKsbH8f5CG6L8NaCB2ZhTcrlV9wgKALHyWhzTI-L-tzPrb8EI3ccx_FCvzD6d6Pe4O1MoKI9KaQtpp719c8FpA6MwCq3DJcpolA0M0A2wy29MhrvrNoACUzkLyvzkfWKKZYBCJSvy-l6r-mG-Vw-riIy8CWIHy4IWn9vx5JVrx5OY1uqNJ2XYLso2JA7OUJ7W-hEMCiG8CRJ0a6AqssTXfnI9H58_uetrMO9Q1IWvQ8H_6EtW_W5mFxMU-xIK_ifLtqWOIDt_E0rochcVTK_7gWc2JVKcbEPnu8J0fhkBucWpoc0AOEEwgwJ4cdHS7r98uXSxQBIN0RsS70m9Vg9ynZ-xLGcI6O9OOBVa33bGJ_EJKaNBujKASiRskADqeGp2rQChjJ8PVbxssM6klMiBmjaN8P3H1elc_R4xUMnbnGo2q1xSmNHs42ez7dJjU5rmDQMVIWLW0zg9KNZCV7g8M7qwL_3pUJrTSXEpffKQBDxSHPZe7L4odWvhXmTIIpLc3Ef3Ke6rbQtMhri6n8hcVBHwEJSkgOYPEgxONOdFgIGQgCveRshOHFUOT6CUrjbEqRf_Cw2Nt3FGyBvM0SAblpXt2bHjRlT3QJ2uM1lRIazqxD0En810NDyvMk85OHRlaEEtcknSMyH1dMrbTnXBCPdTYJKRJtSxcIw-tUGB8JPgsh2wCiSObzO-aeAZzSx_Yku52z6l0emMYIcP4K8jWdI1PJgf-EgkF5Gxidvxy2U_daJ7iUkdpFG_zcjhoxRcvKUuZruhaCOQQ3Qj17aZqNr87ULf4ArCREIfLNWCSgl_1UpGz64DcLxGWYPI1mvv3L7mFlhcSyXlKz5tJFuzXrdMWdpFQMCesTf9pYvQGem1ri57o7DFzF8_d55RcKb5CvfwWt4y_l-uNz0m00 "Opis sistema")
*P.S. s črtkano črto so označene neobvezne ali pa priporočljive razširitve sistema

Predstavitev sistema glede na diagram:
Na zgornjem diagramu je površinsko predstavljen sistem, ki ga želimo implementirati. Sistem lahko razdelimo na “Front-End”, ki je predstavljen v paketu UI, ter “Back-end”, ki obsega 2 glavna modula.
- SnowOnRoads Service predstavlja podatke, ki na zemljevid mestne občine Celje proecira višino snežne odejo na vsaki izmed cest. Upošteva, kdaj se je nazadnje peljal mimo plug, kjer ob njegovem mimohodu ponastavimo višino snega na 0 cm.
- Plow navigation algorithm pa je srce našega problema. Na podlagi stanja snega, prestavljenega z zgoraj opisanim servisom, izračuna najoptimalenjšo pot pluženja za vsakega voznika podjetja VOC in Zelenice. Izračunano pot pošlje vozniku. Le administrator lahko vpliva na parametre algoritma (predstavljene v manager UI). Algoritem upošteva vnaprej določeno prioritetno lestvico cest, kar v grobem pomeni da bodo državne, regionalne in medkrajvne ceste prej splužene kot stranske ulice. Ob intenzivnem sneženju se lahko zgodi, da bodo te ceste splužene večkrat, medtem ko bodo nekatere stranske ulice ostale nedotaknjene.
- Plowing orders so ena izmed možnih razširitev sistema, ki jih sistem po našem mnenju naj bi vseboval (Should have). Občan, ki se je registriral, lahko postane naročnik storitev pluženja. Ko se odloči, pošlje povpraševanje po storitvi. V najkrajšem možnem času mu vodja plužne izmene (manager)odobri ali zavrne storitev. Če je povpraševanje odobreno, se vključi v Plow navigation Algorithm, ali pa se direktno dodeli vozniku pluga, če ta nima trenutno aktivne poti pluženja. 
- TimeTillPlowArrive Service implementira funkcijonalnost povpraševanja po času, kdaj se željena ulica spluži. To ugotovimo na podlagi oddaljenosti plugov od ulice in njihovih plužnih poti. Je ena izmed opcijskih razširitev sistema (Could Have). 


Sistem je v osnovi zastavljen, da zadosti štirim ciljnim množicam.
- Občan predstavlja “navadnega” uporabnika (regular user). Ima dostop do zemljevida, na katerem je predstavljena trenutna snežna odeja na cestnem sistemu MOC
- Naročnik je vsak občan, ki se je registriral. Lahko oddaja povpraševanja po storitvi pluženja. 
vodja plužne izmene ali manager povpraševanja odobri ali pa jih zavrne. Ima pregled nad strenutnin stanjem, vključno z lokacijami plugov. Ob kliku na vsak plug, se mu razširi njegova entita. Tam so prikazani vsi koristni podatki o plugu in vozniku. 
- Voznik pluga je zaposleni pri podjetju VOC ali Zelenice. Ob možni nadgradnji sistema je lahko to tudi kateri izmed lokalnih - - kmetov ali drugih oseb, ki imajo v privatni lasti mehanizacijo zmožno pluženja. Njigova glavna naloga je da plužijo po zagrtani poti.
- Admin predstavlja le en administrativni profil, ki ima vso moč nad sistemom.

### 4.1 Pregled sistema


MVC uporabljamo, ker nam omogoča učinkovito komunikacijo s frontend-om in urejen dostop do baze.
Za upravljanje z bazo uporabljamo Mediator, saj olajša kode strežnika, ker se ni treba ukvarjati s podrobnostmi baze.
Za dostop do baze uporabljamo Singleton, saj je najbolj smiselna ureditev dostopa.

ARSO API nam omogoča ažurne podatke o vremenu, ki jih preberemo na nek časovni interval. Iz njega dobimo količino zapadlega snega v časovnem obdobju, prek česar lahko posodobimo stanje cest glede na prejšnje stanje in vmesno pluženje.

GoogleMapsAPI nam omogoča pridobitev zemljevida območja in postavitev položajev plugov.

### 4.2 Osrednji arhitekturni pogledi

  #### Arhitekturni elementi
  - ReactApp (skrbnik: Sebastjan)
  - FlaskApp (skrbnik: Jošt)
  - Database (skrbnik: Filip)
  - AlgorithmHandling (skrbnik: Matevž)

    - #### **Komponenti diagram**
  ![Komponenti diagram](https://teaching.lavbic.net/plantuml/svg/RLBBRi8m4BpxAqQvf3tm0pqWWP1e3eYe22vj3oRPW9NWZMmJf5JzzveqF1ousJipkpDhnvXHeJH1QKUca1bP56n0CjiZuqFDchGJLnHHSo2hLObMVcbCPIjJpgKhkOaWBMRJv4Az5wqJd6XhEIl9sOwuJfuIjuPFbWpcwGhsMDTiN4VtzuubH7nnV7LdnVKO6191tO_M-OfCSsvo0vQrKmVLIiScPQV4FRRsu-LMArkgJP_wHm2VFatgZNrZ5CJu5NT8pYSz6kDbphohQ25hEqcJLzz-CB1d1eiBp6A8tG8Ee2TsBpPkwnlqxl67BGneuo3eOmOVTFAnMk8_Oun9dYCdcndbcQojY3KxWb6xlGCNmJFX3T6xaLgX8bWdA_-sTOTH93fPHKMd6exrmetnR3xNUvrJ_bks4eqboDAfvbojZZkA_W00 "Komponenti diagram")

  - #### **Deployment diagram**
  ![Deployment diagram](https://teaching.lavbic.net/plantuml/svg/RP11Ri9034NtSmelmu8S8L8gKTG5AaeeYnQ4tC64OGPxD9EcQgiUeRVgmPg42X74xjko_t_wMevUcBY69oy1Nzb4QvP7YcmiV2c0bu9Gru3UhzifIOcRKISQKzD62-zCbHwYSB_qg2rMzBzGt-g6wNWhxppE89cAL8vcw6C-VsYlbJwptBK-nDkIGaFXX77lCDeE0rQS59DoqMepMl62Vdy8667dFb8ZwRgB7VwV4_EYV8HJs2smR9Wx8CfT9PSuqu1-FqDBeQzbxju-YG-qUIP7R3IbSU_x1gvPiWihfVu0)
 - #### **Diagram zaporedja**
 ![Diagram zaporedja](https://teaching.lavbic.net/plantuml/svg/dPBTRjf048Nlzob6z8PAZL0iZAeeGYBfZo9LZGMbLxqPsmCic1rtl3Ofxz2toeDrR4Cn3RreBuo0_SuvSsQziYd1Wjd7_6HCiR4kHy4jn9XibiAbInFEMC0BkaAFoFaEbT82oyn_eIS_oUpIRVKO4lqWwL2OU9OxbfJalZ6BCtL_0VnERA7TodhgGYAyw-W1EeS5VI_99VJ9BlHnr4rx5NwuU_l-_W8TeNYRs1oT_tV1nN5DKmLwyy9ZjYPd8S_APGycCvXVm-rjSpmU6vEVdA0tQ24iO1eg5DUkA3-KEyFgI7AfJYCLISi7oYVil73s9_wOUxkrUwm7ojdRLZ3yks0odJt297femT7v94qrMw4dRMAqpDLOfxs1TrnnPg7CMJ1c-1ZDJk0qD5ge1eCR7Q7Wb6EhH5-VrnqiCDgZneQAYQsfY7q_AKNcMlRDDrVxLWMj8bqKLrtjq6YbMZkg8rBq6_jLI5z4x9zZf-yZe-Mk3dc30UmnTMjxL6iOwryvfXdfpJjQbYQbhhhxQsYE-Uhri1Ty_bcwPjrduHSaXxLe_cSiCgf7M448MvGDoPegdMEFSDp12uUWTGZ_po5eBaODvjS70zXHNB2-O1uuhgZmxI8Er-4hU_8rlm00)


- #### **Diagram aktivnosti**
  ![Diagram aktivnosti](https://teaching.lavbic.net/plantuml/svg/NP8xRiCm341tdOB8b5mX7dg0ea2NBaKN6c9i-aCPakp1HO_WG_GWxUJSgtJY-5DD0YK-yb4A4NqqvlpME8-fS0dEMeGUyqWTbRg1fcglloG59URy_eWN1A7nL51CJAC8Zkm43jSVxgg299G8rgKFK8a7-3IWw_nQjHa32xoWO4P-mIC41oxjwFez3YGCxf7S9hTKli3nsJhWFYLFJoU8EGaS9-0SWu3rwNPtBgI4SH227YnLhhvpg0e4nqtvh8KFqNOhDmwygEz1whlsfgtDjsF7CrGiN-w6ouoqZ8wenb98-Tnhe1Ui4R2Ct0dd6fqLNGSrMN2DHvqV2YLcNzk6w57VOE9ecajv7B0God0pG9tgT3P35fCjwtQeaalXUigQA2vwEyjiViC_xnLFGlNoG9EUG7GBvMl_LNRjhvQSh_w9CI6wvWy0)


- #### **Razredni diagram**
  ![Razredni diagram](https://teaching.lavbic.net/plantuml/svg/TLHDRnen4BtpAonwA2aGaLCbRfIqYQBGef3sL6bbl9F5mTXRsvi4HVptZhrhhu7DOLUQUJFpvjDCxKebGLgo-3Cdxpqcg37a1_wtix8adzQKRQU25nkx5XMyzmWPqZpFIg5U1nTJibPAE9rG1PTEyQ9uxXGQ2cuiw5H7cUKlr8BphegDW-vMltuwA8SEC0Glm3RQJ2X6BLSozJKWWDcCPXh-LM1iwcggzOv_W34iNG0oTgAEL2kQcvIgpUHCBU7DXZXdu4Vw9mrm5h1twFLAR3ijW5nJIzVKG3E81yXnHkZDujXMN1POXPB43QSUN_2QAocnDKfxZ90ngnNOG2yF6zbHprFeuByZdWNad8PGnpIt84e874EiLE-_lm4Rj6nf-17n5fdTbp0bAwknW16XkZ1JSisPRHUcpkBGxEI3Mv5s9s-mTNNDGwaiVzeFs8RA0lACQg0XS0Y6nSITxb_rn-F-rUNbbtv7fwQaCc0IwuapF7DeQZwpzh6zIqpOaSU1Fj8rhcipH5_NRmFQHEd1hLoKbdXc2TPiaT-GaqIQelg1e4ci9VwcAfbJlP-xK63QATvJcMEdbcWKTRDyn-MHPa4bYlf8vp8_KLWgda7ofQYE0wxeJXchdXFeq8iJJRkMfjDbqARMXQPfTk4nvMxmDFqkguvIaZRFHA4qjvjRB4DW7VMvn2kQgzqEaUI8dCETKTBCPBxaR2l0X4lQqIrapmxBdfIkNwE_CkCItrKpyEA8rDA8E35ZIYXjBeukEBAiGB_4C_qyB9MsK_9rCfdKRFWUZSFpwX-Z-o0qBrOIxaRJShF0zEBL6_yoLWKVN2J9UqtsIlUbmZnDm8fWt49PKHfCN-cyjah8LfAMZyeTHYH3JOPzt7ilgtnh6ZTqJ8gDPv5at9n6eebM2LKueDDdev_qyWFmP9nkFVu3)


## 5 Končno stanje ter linki do dodatnih repozitorijev

Izdelan imamo algoritem določitve poti pluženja. Njegovo pravilnost smo preverjali z izrisom grafa cest in križišč, kjer so križišča pravilno obarvana glede na njihovo pomembnost v dani situaciji, kar nam omogoča navigiranje plugov.

Trenutno uspešno prikazujemo spletni vmesnik za neregistrirane stranke,

![Glavna stran](gradivo/img/homepage_rg.png)
**Glavna stran**

spletni vmesnik za registrirane stranke,

![Stranka stran](gradivo/img/homepage_user_rg.png)
**Stran stranke**

spletni vmesnik za administratorje,

![Admin stran](gradivo/img/homepage_admin_rg.png)
**Stran administratorja**

spletni vmesnik za pluge,

![Plug stran](gradivo/img/homepage_plow_rg.png)
**Stran voznika pluga**

ter delujeta prijava in registracija uporabnika in pa voznika pluga.

![Prijava registracija](gradivo/img/login_registration.png)
**Prijavna stran**

### 5.1 Opis sistema

Izziv nam je predstavljala izbira primernega ogrodja ter orodij za razvijanje frontend dela, prav tako pa smo imeli nekaj problemov s pretvarjanjem podatkov o cestah, da so bili primerni za prikaz na zemljevidu. Težave smo imeli tudi s povezovanjem frontend dela aplikacije z zaledjem, ki smo jih rešili z preusmerjanjem api klicev iz node.js strežnika na flask (python) strežnik.

![Opis sistema](https://teaching.lavbic.net/plantuml/png/RLF1Rfmm4BtxAqPxINiWXnwhAD9s4tKZXO2MaaEJ72RB27d1DhBDHjagdz2_weVLni2o6n12dZVFu-TvWwcuR52ZWAqIZP8aRMRVQu9MrDyOmwrL6XOFfAdancgkKKBRA8slabSBG0Fvm-RsPpOmC-iO5NQP4KphjWpST81Yb5YIxj1u09U5uBA3bcCz5CfOjPCScg5AbZB66jnMhe9ZIFK6QUq-6zLQWgInNF03MguaPE_6abZ07yO0nYtvdKV0FKzh9GXIXxw4-5wLNFRh_YwGt_L0B_e8-8iTeqx-CTnqBIFjmm_MOGLQV4NZLNV2RdwCGd93slGx7vDLl_fDDKc-7TJ5oGe4Dg4YW7kN44NNPzS8ZimbqXamcmFZEI9SNfvY3ho8y-mNh9UFjnVif9sXmBG7dv9zhzdOzW0FJONli5S7DsQTypYXTJecPZYc2D5vhT4IHq6_zaECVhACroK-LPruxhP8rEhVNo_1A3VyblOJ_fK_OBJjUDLmSfzWqxc0qns3cn2rZSjyyPESo8t2miquwRtp_UjPtwwYQ9xdn1v8r3lQymAU9LXDihMIIWHZKUumZ8jtB5id-VrDxva7LcCC4LI2x8wWKXOAvURL_NZ11Su-_WC0 "Opis sistema")

Trenutno stranke lahko dostopajo do glavne strani, kjer s pomočjo google maps API-ja ter podatkov MOC izrišemo zemljevid. Neprijavljene in neregistrirane stranke imajo dostop do prijave ter registracije.
Celotna aplikacija, skupaj s konfiguracijskimi datotekami se nahaja v repozitoriju https://github.com/Student-na-praksi/Projekt-25-Mirror.git. Kot je že v samem imenu namignjeno, je to mirror ing originalnega repozitorija. Zakaj? Noben iz ekipe še nikoli ni postavil full-stack aplikacije na nekem gosotvanem servisu, zato smo se odločili, da kreiramo nov repozitorij, na katerem si lahko prosto eksperimentiramo brez strahu, da bomo kako pokvarili trenutno (lokalno delujočo) kodo.

Izvedli smo test registracije, test prijave, test dodajanja pluga, test prikaza zemljevida ter test prikaza cest na zemljevidu.
Vse teste smo izvajali na drugem repozitoriju (https://github.com/Student-na-praksi/SnowPlowNavigationSystem.git). S strani profesorja smo bili
opozorjeni, da imamo na repozitoriju znotraj organizacije na voljo le določeno število minut za testiranje, medtem ko jih ima novo ustvarjeni repozitorij, ki se ne nahaja znotraj organizacije neomejeno.

Trenutno naša koda obsega približno 2100 vrstic kode (brez praznih vrstic).

## 6 Vodenje projekta

#### Dnevnik sprememb:
- 29.2. Začetni nabor idej za možne funkcionalnosti. Začetek projekta.
- 7.3. Omejitev idej, ki jih želimo podpirati.
- 13.3. Ob stoječem sestanku smo dokončno razjasnili želje uporabniške zgodbe in arhitekturo. Sedaj definiramo potrebovane funkcionalnosti.
- 29.2. Začetni nabor idej za možne funkcionalnosti. Začetek projekta.
- 7.3. Omejitev idej, ki jih želimo podpirati. Želeli smo utrditi svojo vizijo projekta s povečanjem fokusa na manj idej. Napredovali smo hitreje.
- 13.3. Ob stoječem sestanku smo dokončno razjasnili željene uporabniške zgodbe in arhitekturo. Želeli smo pojmovanja sistema združiti na enem mestu. Sedaj lahko definiramo potrebovane funkcionalnosti.
- 27.3. Odločitev za dodato uporabo Google Maps in delitev razvijalskih vlog za specifične dele sistema. Želeli smo si olajšati delo navigacije na kratkih razdaljah, saj bi težko dosegli raven uporabnosti, ki ga že ponuja Google Maps. To nam bo omogočilo lažje napredovanje s projektom.
- 28.3. Odločitev za hevristični algoritem. Sprva smo želeli napisati algoritem, ki bi iskal optimalne poti pluženja, a smo ugotovili, da je to prekompleksna naloga. V nadaljevanju bomo poskusili uporabiti hevristike, ki bodo našle dobre rešitve pluženja, četudi te ne bodo optimalne.
- 3.4. Odločitev za kasnejši razvoj algoritma. Ker se je uporabniška zgodba uvedbe samostojnih plugov zdela dobro sprejeta in nas razlikuje od ostalih ekip, smo se odločili, da damo poudarek na njen razvoj. Razvili jo bomo preden začnemo razvijati algoritem.
- 17.4. Dogovorili smo se, da bomo znotraj obstoječega repozitorija imeli povezavo na nov repozitorij, od koder se bo naša spletna aplikacija avtomatsko deploy-ala.
- 18.4. Za frontend bomo namesto create-react-app uporabljali Vite, saj omogoča delo s Shadcn in je bolj splošno uporabljano, zato zanj obstaja več pomoči na forumih. 
- 24.4. Namesto izrisa poti navigiranja bomo plugu le izrisali oštevilčene marker-je na križiščih. To olajša rešitev, saj dosedanje rešitve za prikaz poti navigiranja niso delovale dobro. Poleg tega nova zastavitev bolje deluje z našim algoritmom in za uporabnika ne bi smela predstavljati problema.
- 3.5. Stanje cest v največ 7 barvah. Sprva smo stanje cest želeli prikazovati z barvo na zvezen način, a se je izkazalo, da brskalnik to težko podpira in začne delati bolj počasi. Iz tega razloga se omejimo na 7 barv.
- 9.5. Namesto prvotne ideje izdelave algoritma s konvolucijo slike cest in plugov smo se odločili za izvedbo algoritma s pomočjo grafa, ki predstavlja kričišča in ceste, ter vključuje pluge preko križišč, ob katerih se nahajajo.
- 21.5. Namesto vmesnih idej za deployment smo se odločili za fly.io, saj nam edini omogoča vzpostavitev aplikacije zaradi njenih posebnosti v smislu ločenega serverja za frontend in za backend.


#### Izvajani procesi in prakse
Uporabljali smo SCRUM in Extreme Programing.
Tedensko smo se dobivali na stoječih sestankih ob tabli pred enem izmed laboratorijev, ki imajo tablo. Začeli smo z naslovitvijo težav zadnjega tedna ter kako daleč je vsak posameznik prišel, potem pa skupaj zasnovali delo naslednjega tedna. SCRUM master je razdelil naloge.

V naslednji iteraciji želimo zgraditi glavno stran z zemljevidom, ki prikazuje trenutno snežno stanje na cestah ter osnovno delovanje algoritma. Podpirati želimo začeti osnovne pluge in administratorske dožnosti.

### 6.1 Usklajevanje ekipe


Sestajali smo se vsako sredo po predavanjih ter komunicirali preko Discord-a.
Po potrebi smo se sestali tudi v četrtek pred vajami.
Med sestanki smo pregledali stanje projekta, ocenili napredek od zadnjega sestanka ter razdelili naloge, ki naj bi jih člani ekipe morali opraviti do naslednjega sestanka. Pogovorili smo se o problemih, ki so se pojavili v preteklem tednu in jih poskusili nasloviti. Začrtali smo delovanje nadaljnjih funkcionalnosti ter definirali njihovo arhitekturo.



### 6.2 Projektni načrt

**SEZNAM IZDELKOV**
Spodaj je naveden seznam vseh izdelkov, ki smo jih tekom semestra izdelali v okviru projekta. Zaradi preglednosti so ločeni po iteracijah. Večina jih je v digitalni pisni obliki (kode ali zapiskov), ostali pa so v papirnati obliki.

1. iteracija (21 dni)
- Pregledani podatki in začetna vizualizacija (1 dni)
- Zapisnik snovanja idej pristopa k algoritmu (2 dni)
- Zapisnik pregled obstoječih rešitev (2 dni)
- Definiranje uporabniških zgodb in funkcionalnih zahtev (2 dni)
- Skica predloge projekta (4 dni)
2. iteracija (21 dni)
- Izvedba okrnjenega algoritma planiranja s pomočjo PyVRP (10 dni)
- Izdelava simulacije naključnega nabora voženj po mestu - kot merilo uspešnosti algoritma pluženja (8 dni)
- Obdelane .shp datotek kot predpriprava za izvajanje algoritma (1 dni)
- Home page UI: vsebuje zemljevid stanja cest, login (2 dni)
- Avtentikacija Admin-a in Ustaljenih Plugov (1 dni)
- Admin UI - lokacije plugov, št plogov v bazah... (8 dni)
- Ustaljeni Plug GPS sharing - vsi aktivni Ustaljeni plugi delijo svojo lokacijo z Adminom. (3 dni)
- Ustaljeni Plug UI - glede na trenuten GPS se mu izpisujejo navodila za nadaljno pot, možnost deaktivacije/pavze (3 dni)
- Testi enot (2 dni)
3. iteracija (28 dni)
- Vključitev kmetov v pluženje z VOC in Zelenice (4 dni)
- Razvoj svojega algoritma organizacije pluženja (14 dni)
- Ročno testiranje sistema kot celote (4 dni)
- Izdelava dokumentacije sistema kot celote (2 dni)
4. iteracija (28 dni)
- Načrtovanje poti neregirstrianim uporabnikom (8 dni)
- Nadaljnji razvoj algoritma organizacije pluženja.
- Posodobitev pomembnosti posameznih cest glede na njihovo priljubljenost. (1 dni)
- Ročni testi za testiranje sistema kot celote. (4 dni)
- Integracijsko testiranje tretje iteracije s prejšnjima (4 dni)
- Vsi testi enot. (4 dni)
- Celotna dokumentacija kode s popravki (2 dni)


![Ganttov diagram](https://teaching.lavbic.net/plantuml/png/dLdTRgD65BxtKupQYswZhhjnicfQLLLPcpXi7MFX7tMtggoncTXZOCQ2WJQk-WXvY7sHNYNlrJC3XW4JuqI950UO-Rxpyvrp6FyQ2HoA5MP2eA_wyWzFa4lnAiJ1LwtMpv6uzyalBVL0BxsC_caX96X0VCg8-WUX0NpiSf-7wEkxZlnHLwyv4-bLM7SFb_wLAt7aPQi-uAMt2ddCt6mjkRfxV-TMTtn__U7Ax6RBuHU78V_h4BZqM41z4WcU4tmDrDBd4N6Vsw3MJf-krY8tzj_Mpzzd3cn57cLRBDstgEmaGimYk4MOQAsfIz0TvsB1_sxvcArYl28eybkjRSWtP2cGYbU4n9gWyn_56l4xT4qMOOp3UzHvrxbiHLZ4eOll8_0JoMneHO1MkTJwu-ni519t6z9jY1DoTeRU_81SHh_z4-48_J5opDwVoCSHeC5rMAsMdBSH5IJ4Ixh1PsTlEkVQ4cjYEkVxDHVeBq8yW6JkdZGMsRRVH8Z0PRcVjLlG42Ewsz44_Z34iBp0DWI1BpQILGdYymVBCVOOvoYrwbc8pCYL3t7SSXSB3z8RG7RuyO48Xb52Tp7swIwpfmm66_K7XHVgqJ961TwOyIJdZy2za8TRZ3o4_HKFgGXYYTFHSCP3UsOCFvfxeCvpPYasXvRn1K1ioEC3NQEGF7s102LLZ6prt377vl3ZIv7682RCF8fSSaUPYWz6J_yHVqD0OYbccaAw_yRcU68CVxCQmwKpAq1xEHP1yPQ7UC7eqnSFZDojkBkGSRoBcRUad66VoSjuNMDvpxosXX2YHWVdT3KFWmOp1Wn7u6iLrop_oO6F1yP9G3gZmsYwt8i3A0Rr49cpUdRtDHZMpYK-1g5jGVa-NyaFa3cUKBb_MH9QpnmOirngbqTZ9-deA0bn5nZoGeGysiBsDAcuJKyJnvmuTYb73ZMMaIam7B8ZOS8W8p4xsD3wV7Ix533RIsxMAHKrT5ZLEWrLBQryfRAMke1x8PCQ0K_lvGy-tsSLHX6KfO0_Fcmu6jtFd94ovPqUy4zmDRVcNNq9qj0b-EUqkb4Kubt2DsfnXG8FeQMdPOy0dnYqBEb0HOGowUCLHMkIoD95lMeATgVZYNqxDmPzsx4cDxSDjKJnrtoTfs14WzXF2J3i-PluyK6HX0O0MaS9Lvo03mgW-iJeBVAuWCyXzJcA8QsUlZ0E14kEpGoHdA_qIcJTJWV6nBA7UxPN9tdINcHasz5w2oi45yHJFBP5wyHGUA219NYZ2aLEvw0Stepc89XHGp-fKBZX0KH8ZW5JwoUKH6GH0yYE151x4wgMoiWjmKVV8P0qPTM0tTYtvdnaz1kgKXNOI0HK8UefLI333IXxgphq51R9mWyLT-J7AvvK3JMcanjpEB6w9O_NcrkGqv0b5fWB-xu5axmyIm7hE_Jq1RmFXa8dJs2OWgBVRhVBuJPwjzPmFhME5wyApG8_Dr3PX_gZCOhMEAHi1NoI239ELZIuNJmeoSdkw5DGSWIYutlY7ErIv_6WBHrreV64dUVZ6yEnXlsYmDHItHlqBCcf1Tna_v1gWfcIi1Z2bt8dA8WXGRSqWjG1GWmdtAM-obk6NTY6ST0Pv4y0efEY0akKZShptszniYDLxgF1jA-v-6JU4qZKhAKInaMxcgtJeJMPJw0L7y_MWogapGrP0yrGFEwITZL5ktRFr9jeVN8MN4fjEWv9AdLedlADAF9I5FGc97TuARXCbMyFB7FCQwCxiVLelzYsve6at3rW8faFpTydn-tKcRseZLUx-0bO1IMjALnK6_1LfG5V559-jW5tDEwpjA78IHXv0H6gMEpR0vHFDBExifPz9Zv8Q4cguy-ruToQplXu0Qc2EccxbV8_fTkgQ5tMTzRSXvSlpH07fWcGioXa5a4R9y12jgqbyQ65LQqTVnfFpDkIwXfnwwRAqkZw36xd4BTncDNvlKWBvtLQcFTcvl4SrNWroG4ghTWq3RSATjOvKHYAdoQEooPnN5R5KPUe5vefGnWGGv6zfaBXfuWHUFkWOIH22auDylSjZmVLMKfhMlFf45u0caUgChPgE9jyEcsIYQoZcIYd3dHiPzupPxahVtX9ml28ktoXYWACtIHOf0FabaSu83ivqCWngcYZm7BD4ovVug6SB6IxXGK7pSInZTvyP8zWn0GrVZeUPjq8BSYdoBPzHBTpUsOwnc1mNBzLfbfsCq5MAiSYhqIZck3obGNw7mpV6neSlZOE9sRVKGFL2UNaUJfrKy9btPGmltWjHCsOSF2gaqq91KZd-9mmlpXnKZXzL7WTjbr8gNZ7Lp3lIwS9zaUp2xdZQ32D8q89w8GXuQAs7BuAKBLsy9zqwKWxkL3wW57uyG57kRaPvCpkQTtqX4F9_HaZZT2I-nnYwCfHmI5WS7uaM7UpECSxiZG_WQlT8JyngxjREicgXT0Ee8vHK0stxe7YrAVkRdPGKtjB7hdKGgRd5tMt3WyI6fvwncVwy5BtGAbjr9Alrky6cABMrdkffDtwE9HqL_U8ojhAZO7yTg4V4i9QlqAggYzb_WS0 "Ganttov diagram")

**Ganttov diagram**

![PERT diagram12](https://teaching.lavbic.net/plantuml/png/jLZRSjiu4dtdLtHD7cQtod4iIhuaut8LOz4sDxQaeYHlZMkgL908oH0fGilRxcWodv2Fo8_CK_9Vsm0l8aZAaJAL5qewe823HgFxT8SkyzSa82kOafcx27ZiEzVSum540V537A9-f7bq7a748M2BvmWS5j1PnBYlQU6CU1HEZYyqxJACVlVebHP69A9THXPYqZyq0184_B_o6y0zysaw_TJ3zH3xK_jJktoJ_LSB2pf3COtyr_iAiLVqOduwTyG83nmQPEZfpViBynfdAqtYq3c9lMX4_nSP7bluAzmCpF110-tdqcjh1lg9bbA7dovdOiPtjm6b_jKWI0WGDsA9pyFeyeqSk_e9I0W3s-mER6jW6uy6l9hFwHaz-yN37RvpIE06r85tS9dXHzddrKSuXuzm0lBpD_-ZiCh95gbmUE_5zAfr30mPanbR4eM0DJBjbhgo-4FpidehNG7q2sNX76hSlRMPie00ssmOce7vu1C1-4iApA5BbStJUyisykD9wSXP99yKFSe-aKzEfyvc5vb1G1SUMdND7HAvF15yDkJB9nhv11AsYOd7DdKhuJ7TtflTWuWX1NYh4CkGHc93doU5JM0Ti33YQm8k46_10nQjOeNGiDT_D7h_ClTcfAThGwkbKCgX5ut5fqXcIRzyOiyGqA-VqPEI9lDC1lskCVhGV_oXh8OKKTzbucOoNteIWQz_KMz9VPhnIwXgBNCuCdeVh8FEhoKVkaAim1gPTGj25E8r3yZKPry_ksYrpO8xK-5hyzXtPnZsYESBc3nNJTarRwmUte53pxOb7nsLROurdwv7Sh8-2V6SfVTbGKArt-3U-2vE7V4uKpdbs8iUvt0t5e6sWKhcQjt-zG_cOcqSwX4CMMiCmnvVY2zu2zoe4a2VkkQzZDvxiiaNnNIXiicnflXjRHBgJ0cwTnJmS4r5CjbrMhOvill3WVbXP3qQ4skqTtXlPGHad2ynAx0cPZRTq23nyJeIlqBZoRIhMUqRYyk7UkKAh6bn_QMqfX-KriGIq6chQ-TOPUrhlDjUSIRS3NmHUz13yc2DlfBVBW8XPfiL__9foM7m-wCzKFtvLqHKedBs7KOgMBNrEjEsleFfKvhX60Haa_0bU2ICAdnvi432ClLH91zZG1NSCIjYglJ8Wi4pJKHMOgx2_tey7FKV9iRzRTyQtJsWk-bxxoRd36qrRXNOo_SoPAlOImdxnFMMyPTFSbEeBt1DIBZS0_A75QQC6Ce9mNeOtniZgz_R-zfU55O-QR3yoGwo_Mb6zZXyNkCLYNX4NN1v9ACAflbr84OtGXybP2cZSN4eQWwx6qnkh7jpEC4GE3WeaqcAUeDhw-qTjE_u2hs0B2YChNUGX7GQ8x4DNM6IJPW38WEZTypGhaU0iP6fL_-k_s1E1iRjOUaYfTHfeBdB5OmamYJ1N7d_mN1Mp7yj9UOOtnPw07Fim8iNNCsnndXqP_P6rlLX7j3Ag81-gdBCiMQEWXMQ4LwZeTpYVY6d8_Zw6Vq0pOSwDC7Y2UN0yV6nIhNxOFKcO-kWx2AuWAvgpm9h95dOIveBRWT329z9mFm5qav2bbKlR6jOkGUXmJo6SIt4gCBp_N7Of6V1L-fcSDh9yCwmhTxjtljfPxHh0UzjSy1ht8-qlayIxZ1FNhOrNa0XD4Jam2gL-d7aI_x7Hx32k27gDDoRtBKyiZThacogecXyUyZ9VDzEHdZ5CfL6VQuMZ-EUDPgCKDl2gsbxFf-sgnnIz2Zxp2EkS96sgeGAhCB1-4zCjW5tjogxxdTD8Sd63tYlvAtA4m5fdsM9GCoLvG417icvqribLeQsMimMs2wX60SqZPSeoqIZ87Gf1bOyqdy4MBBF8YxSzv_75KroOroF-ga7_Y2RVPUwHdErzmz49vbfe5EnMOvLADdK-LiAifBIxLrjYLQsF7JKYhp0cZHS-oKDrzvRmrraIy2vUam5rdXCZwbk41Kjk2iQoKYSon_CUF28TGR6xoVgOJIPgMQwCUm7qnuU59ibdLEzJl5qbtYpKyqcGkm-acsNEbDPRbLPtRiw6HiuKorPO8sMj57XOWoDjl4gHBL8aQTGEpFgeV9H1Sslmv7vS5ZywcGCu5mLOGMsV_pQavwiC_SCO-Uo-wJMJWNMvFgTbro_Sv3hYoNWhPhp2-p5MhlKgQ0lXFZnqBHJQ-nvLgsSmRbUPtMkVuCLHdAU7r4zrTZcesN-UsygxMBPJWELpZVS1gz_MQXpno52yb1KE2GGMSSdgE6g7IVKROQD8dXWslixaF3lSrLT5fYcAStYrw-lqkQjbhPmvM_PFjMoBgf0idQ9bZSm1PRt3XMmsiBJQZqz-TUiaQOL_KSLpVji0YrrihHoLqkkLZIKwaFR1ezMRlQa-qjxBLhHT15ehTzHiaZMXD1A7QpSSBgMDWdaeg8AroebbXXeA6-RNjlMawL9rVTA0qLvLCBKcaIhb2ZoZQmKq8gQGA0bJQqEPF9KIniCk_RILBwBTmjfgPLAvSf0tGpRmMq5gE8D-zeEbki3TIJNsYgwrR_fKHVQJYlhlDpVXCIg3TIKJksDPcch5Q8jTwUsbkeLyJiJ1YMaPESIMag1vPEeZPLJPMbCN95IcigPTBGqVKXZPL6x19K2Q0bL0fPM3hBrqI8Lr8R-3m00 "PERT diagram12")

![PERT diagram34](https://teaching.lavbic.net/plantuml/png/bPJjRjem58R_-ogErh_qY-zsA1AbQOLKHXLefqsJa24dcS7Op35iO_GIUX6xaVrgxsjs4b02Q6L_yl4U-VZ9UrudcZ0neufEOKX7ar39kV1Raai5Mb4HcH8AJJW66hG4nSAl6docSAIP58H48yeHpaxgX3GY_PEZGo9DDLup6jgclmW0LKf-Zvy0xfZ0fFsGc_sCzaIUIECqNKkY3KxFjebNNMs17M4zg0I-hKZbeqhLoirLtMsPRfacFWPqpdKVV-WcPw6Oce-1aRcW8Wael6kCxFhBApv7ftG2pDJeY8rfupGkEE-0Hj3kkru9Ze80grXzpyrNn0lW4XgfM4ZlpWgATLX1sLvgLLXz4IlxvMTPRMllMuKedCS97yzVdWt00YPJr7812vZn-UiV56E49JnsMy04V4QEWeqm1tZJz3gkrrkRao36VMF6H2saTyDONkDKYhk8Ljj2R4b5kUFHvKAE8J8N32bG7ah5z9I2L24LR6cDmmrptiBMGw_VxGoQTxVTF6NSUZ_bUJcbWMhUoOssrqbFlZmB2HeZpKoA3LB48es6SoBj_BdKUVTwdtfzjpFekxq-70rBGJ0iRJkOg8NqdZfe2Q1sbaFRQ5jepMzpwhINFdAweE3BoTocCN7iCBnhCt-JCbggfX6qBTC8Mh4GRs5SIm6WTfuZssZxeb_-L_JB_nLzkmLSNEJtNcjx1tQlCEJemtnciZ0KxFNt1FCMvP0UUgwNk77WhCxN1BNYBbMj-0RLHFfoFQ9yfBlNxi1p7zlknuDHIfjjotjGoc_4nXp_cM8pPP-NvjZvFXqRDfmoGLLaJ1EKot0hFMwd_Q7f3UwRzwvtU81ilckLFEDQ8oJv8HuVE-i_JqR9dFICcZbZ9FilsAvbpsAcPiPDCkV0Lk9aaYIVzdqTYuoKcL16pJb2ibFShMwojblw2m00 "PERT diagram34")

**Graf PERT**

### 6.3 Finančni načrt
Časovno zahtevnost izdelave aplikacije bomo ocenili s pomočjo modela COCOMO 2 za zgodnji model načrta.

Pri tem bomo za izračun uporabili sledečo formulo:

$$ effort_{ČM} = A * size^B * M $$

kjer bomo dobili rezultat v človek-mesecih.

Za parameter A bomo privzeli vrednost 2,94.

#### 6.3.1 Ocena obsega aplikacija
Velikost aplikacije ocenimo tako, da jo razdelimo na funkcionalnosti in vsaki od njih določimo utež glede na njen obseg. Tipi funkcionalnosti so sledeči:
- Zunanji vhod (External Input - EI)
- Zunanja poizvedba (External Query - EQ)
- Zunanji izhod (External Output - EO)
- Notranja logična datoteka (Internal Logical File - ILF)
- Zunanja vmesniška datoteka (External Interface File - EIF)

| Vrsta FP | Ime funkcionalnosti | Obseg | Utež |
|----------|---------------------|-------|------|
| EI       | Prijava v sistem						| LOW | 3
| EI       | Zahteva za predviden čas prihoda		| LOW | 3
| EI       | Zahteva za izračun plužnih poti		| AVG | 4
| EI       | Posodobitev podatkov o voznem parku	| LOW | 3
| EI       | Oddaja naročila za pluženje			| LOW | 4
| EI       | Potrditev naročila za pluženje			| AVG | 3
| EQ       | Prikaz stanja na cestah				| LOW | 3
| EQ       | Izpis podatkov o določenem plugu		| LOW | 3
| EQ       | Izpis naročil za pluženje				| LOW | 3
| EO       | Izračun optimalnih plužnih poti		| AVG | 5
| ILF      | Interna podatkovna baza				| LOW | 7
| EIF      | Baza vremenskih podatkov				| LOW | 5
| EIF      | Baza geografskih podatkov				| LOW | 5
| vsota ||| 51

Pri implementaciji bomo večinoma uporabljali jezik JavaScript, za katerega velja, da ena funkcijska točka ustreza približno 47 vrsticam izvorne kode. Izračunani obseg je torej
$$ size = 51 * 47 = 2.397 KSLOC $$

#### 6.3.2 Parameter B
Parameter B izračunamo iz 5 dejavnikov, ki opisujejo lastnosti projektne skupine.

| Dejavnik | Opis | Vrednost | Utež |
|----------|------|----------|------|
| PREC	   | Stopnja precedenčnosti 			 			 | zelo nizka | 5
| FLEX	   | Stopnja fleksibilnosti zahtev 		 			 | visoka 	  | 2
| RESL	   | Stopnja pripravljenosti na tveganja			 | nominalna  | 3
| TEAM	   | Stopnja uigranosti skupine 					 | nominalna  | 3
| PMAT	   | Zrelostni nivo razvojnega procesa po modelu CMM | zelo nizek | 5
| vsota    |      |			 | 18

Vrednost B je za naš projekt torej enaka
$$ B = 1.01 + 0.01 * 18 = 1.19$$

#### 6.3.3 Parameter M
Parameter M izračunamo iz 7 dejavnikov, ki dodatno vplivajo na trud, ki bo potreben pri razvoju aplikacije.

| Dejavnik | Opis | Vrednost | Razpon uteži | Utež |
|----------|------|----------|--------------|------|
| PERS     | Stopnja usposobljenosti članov ekipe | nominalna | 1.5 - 0.5 | 1.0
| PREX     | Stopnja izkušenosti članov ekipe z uporabljeno tehnologijo | nizka | 1.5 - 0.5 | 1.2
| RCPX     | Ocena kompleksnosti projekta | visoka | 0.5 - 1.5 | 1.2
| RUSE     | Potreba po izdelavi komponent, namenjenih za ponovno uporabo |zelo nizka | 0.5 - 1.5 | 0.5
| PDIF     | Kombinacija spremenljivosti platforme in potrebe po učinkovitosti | nizka | 0.5 - 1.5 | 0.7
| *SCED*   | Krčitev/raztezanje predvidene porabe časa ||| 1.0
| FCIL     | Kombinacija razpoložljivosti razvojnih orodij in komunikacijskih sredstev | zelo visoka | 1.5 - 0.5 | 0.7
| produkt |||| 0.3528

Vrednost M je za naš projekt torej enaka
$$ M = \prod{dejavnik_i} = 0.3528 $$

#### 6.3.4 Končni izračun časovne zahtevnosti

Vrednosti *A*, *size*, *B* in *M* vstavimo v formulo za izračun:
$$ effort_{ČM} = 2.94 * 2.397^{1.19} * 0.3528 = 2.94 ČM $$

Ocena časovne zahtevnosti za naš projekt je torej približno **2,94** človek-mesecev dela.

#### 6.3.5 Finance

| Strošek		     | Cena v € |
|----------------|----------|
| Delo			     | 8400
| Elektrika	     | 250
| Kosila		     | 1400
| Pijače		     | 560
| Kava			     | 200
| Potni stroški	 | 370
| Skupaj         | 11180


## 7 Ekipa


### 7.1 Predznanje

Ekipo sestavljamo štirje študenti 3. letnika univerzitetnega programa Fakultete za računalništvo in informatiko. Izkušenj z realnimi projekti imamo koolektivno bolj malo. Tudi naše znanje spletnega programiranja ni na zavidljivem nivoju. To bomo poskusili nadoknaditi z večjim interesom in zagnanostjo.

- **Matevž Vidovič** je vešč programer v Python-u, s spletnimi tehnologijami pa nima veliko izkušenj. Zanimata ga tako backend kot frontend, zato glede tega nima preferenc. Razvijanje algoritma pluženja se mu zdi zanimiv izziv, za katerega že ima nekaj idej.
- **Filip Gros** je moralni steber naše ekipe. Izkušen programer umetnega zaznavanja v programskemu jeziku Python bo poskrbel za celovito povezanost aplikacije. Poleg Pythona je vešč tudi v jezikih Go, Java, C.
- **Jošt Eržen** je izkušen programer pri večjem projektu v programskemu jeziku Java, prav tako pa ima nekaj znanja v programskih jezikih Python, C in JavaScript ter SQL.
- **Sebastjan Kordiš**, naš strokovnjak matematike, bo poskrbel za optimalne algoritme. Ima izkušnje programiranja v programskih jezikih Python, Go, Java, C ter Javascript.

### 7.2 Vloge

- Kakšne so bile vloge članov ekipe pri projektu?
- Kaj je prispeval vsak član ekipe?
- Za določitev posameznih prispevkov uporabite kataloge elementov.
- Navedite grobo oceno prispevka posameznega člana ekipe v odstotkih.

Vsi člani smo razvijalci izvorne kode. Poleg vloge razvijalca je Matevž Vidovič zaradi njegove predhodne komunikacije z stranko prevzel vlogo lastnika izdelka, Filip Gros pa prevzel vlogo SCRUM master-ja.

Filip je vzpostavil začetno verzijo sistema, vključno s prijavo in lokalno podatkovno bazo.
Veliko časa je namenil Continuous Deploymentu preko repozitorija vsebovanega znotraj trenutnega repozitorija. Tovrsten deployment nam ni uspel, zato je Filip delo nadaljeval še s tremi potencialnimi rešitvami. Rešitev s fly.io je končno uspela.
Vzpostavil je velik del backend-a.

Matevž je izvedel obdelavo podatkov zemljevidov. Ukvarjal se je z Google Maps API-jem, namreč kako naše podatke cest pretvoriti v pravilen format, da jih lahko v React-u prikažemo nad prikazanim Google Maps-om, ter kako prikazati markerje v različne namene.
Vzpostavil je okolje Vite in omogočil delo s Shadcn (po dolgotrajnem neuspelem poskusu s create-react-app) ter osnoval obliko strani z osnovnimi gumbi in pasico. Dodal je prikaz cest in plugov.
Izvedel je obdelavo geografskih podatkov v graf cest ter zasnoval algoritem, ki na grafu skozi iterativno podajanje nujnosti med križišči določi naslednjih k križišč, ki jih mora vsak plug obiskati. Poskusil je vzpostaviti simulacijo plugov in njihovih gps-ov ter tako algoritem integrirati v rešitev za namen prikaza, a se je integracija simulacije izkazala za prezahtevno za trenutno iteracijo. 


Jošt je naredil zaslonske maske, vzporedno z Matevžem se je ukvarjal z Maps API-jem. Delal je na zalednem delu aplikacije ter zasnoval API vmesnike, poskrbel je za povezavo API vmesnikov Vite in Flask strežnika. Prav tako je Filipu malo pomagal z podatkovno bazo.

Sebastjan je poizvedel o integraciji Google Maps. V prvi iteraciji je naredil finančni načrt. Na frontend-u je poskusil dodati funkcionalnost dodajanja zahtevkov in izpolnitve polj.


Groba ocena prispevkov:
Filip 30%
Matevž 30%
Jošt 30%
Sebastjan 10%



## 8 Omejitve in tveganja


### Matrika izpostavljenosti tveganj:
Ustvarjamo aplikacijo, katere nedelovanje lahko povroči popolen prometni kolaps, kar ima velik vpliv na veliko število ljudi. Prav tako je etično problematično, da s tem onemogočimo urgentne zdravstvene prevoze, ki so lahko za ljudi usodni. Do tega ne sme priti, zato usodne napake niso dopustne niti v primerih z zelo nizko verjetnostjo.

Po drugi strani manjše napake v sistemu niso tako hude - nihče ni tako zelo odvisen od podatkov sistema, da bi manjša napaka imela trajne posledice, zato je leva stran tabele lahko bolj zelena.

![Matrika izpostavljenosti tveganj](./gradivo/img/Tabela_tveganj.PNG)


### Družbene, etične, politične in pravne omejitve

- Potrebno se bo pozanimati o zbiranju osebnih podatkov, na primer za lokacijo, ter uporabnike obvestiti o zbiranju ter uporabi teh podatkov pri ponudbi storitve.
- Če v aplikaciji pride do napake in to povzroči prometni kolaps je to lahko etično sporno, sploh recimo v primeru onemogočenih urgentnih zdravstvenih prevozov. Preveriti moramo tudi našo pravno odgovornost v tej situaciji - če je edini razlog za kolaps prav težava v naši aplikaciji, smo morda lahko za to odgovorni.
- Pogledati si moramo, kako bomo obravnavali povezovanje kmetov s strankami - če bo plačilo potekalo preko nas moramo za to pridobiti ustrezna dovoljenja in pravne nastavke. Če prepustimo, da plačilo izvedejo sami, je lahko etično sporno, če je s tem omogočena siva ekonomija.

### Opredelitev tveganj in strategij njihovega obvladovanja

Za opredelitev resnosti tveganj smo uporabili svojo matriko, ki je vidna na zgornji sliki.
Najprej bomo našteli tveganja padajoče po njihovi izpostavljenosti, nato pa jih opisali po kategorijah.



#### Našteta tveganja (padajoče po izpostavljenosti)

##### Visoka izpostavljenost:
- Vdor v sistem (T17)
- SQL injection (T18)

##### Srednjevisoka izpostavljenost:
- Algoritem (T3):
- Geografske datoteke (T4):
- Specifična tehnologija (T9):
- Bolezen (T10):
- Sprememba zahtev (T13):
- Algoritem slabši od trenutnega sistema (T14):
- Precenitev sposobnosti (T15):

##### Srednja izpostavljenost:
- ARSO API (T1)
- SCRUM težave (T7):
- Kljužni razvijalec (T8):
- Cena host-anja (T11):

##### Srednjenizka izpostavljenost:
- Github merging(T6):
- MOC rez v proračunu (T12):
- Scam uporabniki (T16):

##### Nizka izpostavljenost:
- Nepreverjenost PyVRP (T5):





#### Tehnologija:

##### Ime in oznaka: ARSO API (T1)
- Verjetnost: Majhna
- Učinek: Dopusten
- Izpostavljenost: Srednja

- Opis tveganja: Ob izgubi dostopa do podatkov ARSO bi izgubili možnost napovedovanja vremenskih pogojev.

- Vpliva na: Izdelek, Posel

- Strategija obvladovanja: Strategija zmanjševanja.
- Opis obvladovanja: Sistem mora biti na to pripravljen in v tem primeru vseeno delovati, četudi manj precizno. Recimo celotnemu Celju pripisati neko konstantno padanje snega glede na zadnje podatke, ki jih imamo.



##### Okvara transponderja (T2):
- Verjetnost: Visoka
- Učinek: Dopusten
- Izpostavljenost: Srednjevisoka

- Opis tveganja: Obstaja možnost okvare transponderja (recimo da telefonu zmanjka baterije), v temu primeru ne bi imeli informacij o danemu plugu

- Vpliva na: Izdelek

- Strategija obvladovanja: Strategija izogibanja
Opis obvladovanja: Za obvladovanje zahtevamo od uporabnikov, da imajo polne telefone in da imajo na voljo power bank. Morda celo nek poceni rezervni telefon. Če tudi ta ne deluje, naj se vrnejo v bazo.



##### Algoritem (T3):
- Verjetnost: Zmerna
- Učinek: Resen
- Izpostavljenost: Srednjevisoka

- Opis tveganja: Zaradi pomanjkanja znanja o tem tipu algoritmov nismo sposobni razviti približno optimalnega algoritma.

- Vpliva na: Projekt, Izdelek, Posel

- Strategija obvladovanja: Strategija zmanjševanja
- Opis obvladovanja: Izvedli bomo okrnjeno neoptimalno verzijo algoritma, za kar bomo kompenzirali z boljšo spletno aplikacijo in uporabniško izkušnjo. Dodelane ideje za relaksirane vrste algoritma že imamo, zato smo v to opcijo sigurni.

##### Geografske datoteke (T4):
- Verjetnost: Zmerna
- Učinek: Resen
- Izpostavljenost: Srednjevisoka

- Opis tveganja: Nismo še delali z geografskimi datotekami, kar bi lahko povzročilo težave, saj ne vemo, kaj so optimalna orodja zanje - tako bi lahko zašli v suboptimalna orodja, kjer bi že zgradili velik del kode.

- Vpliva na: Izdelek

- Strategija obvladovanja: Strategija izogibanja
- Opis obvladovanja: Že v prvi iteraciji bomo poskusili narediti osnovno rokovanje s temi datotekami in se pozanimati o optimalnih orodjih za delo z njimi. Tako se verjetnost kasnejših težav zmanjša. Dober začetni projekt je vizualizacija podatkov ter njihova pretvorba v človeku berljivo obliko.

##### Nepreverjenost PyVRP (T5):
- Verjetnost: Majhna
- Učinek: Neznaten
- Izpostavljenost: Nizka

- Opis tveganja: Nihče v ekipi še ni delal s knjižnico PyVRP. Izkazalo bi se lahko, a ni preveč uporabna, ali je polna hroščev.

- Vpliva na: Projekt

- Obvladovanje ni potrebno: Ker je knjižnica javna, je pogosto uporabljana in zato verjetno že nekoliko testirana. Poleg tega ni naša edina ideja za izvedbo algoritma in njena neuporabnost ni tako kritična.



#### Orodja:
##### Github merging(T6):
- Verjetnost: Zelo majhna
- Učinek: Dopusten
- Izpostavljenost: Srednjenizka

- Opis tveganja: Ker še nismo sodelovali pri večjih projektnih nismo vešči pri uporabi sistema Git, še posebej ne pri merge-anju v situacijah, kjer smo nespretno delali z Git-om (ne pull-ali pred commitanjem; ne odprli svojega brancha, čeprav bi to bilo potrebno; ustvarili preobsežen commit).

- Vpliva na: Projekt

- Strategija obvladovanja: Krizni načrt
- Opis obvladovanja: V primeru incidenta se bomo takoj obvestili ter priskočili na pomoč. Ker smo majhna ekipa bi to moralo zadostovati za premostitev težav.


##### SCRUM težave (T7):
- Verjetnost: Zmerna
- Učinek: Dopusten
- Izpostavljenost: Srednja

- Opis tveganja: SCRUM ne uspe najbolje in se aktivnost na kritični poti podaljša.

- Vpliva na: Projekt

- Strategija obvladovanja: Strategija izogibanja
- Opis obvladovanja: Developerji bomo glede aktivnosti na kritični poti s SCRUM master-jem pogosteje komunicirali, da lahko ta dodeli dodatno pomoč, če se aktivnost zavleče.



#### Ljudje:

##### Kljužni razvijalec (T8):
- Verjetnost: Zmerna
- Učinek: Dopusten
- Izpostavljenost: Srednja

- Opis tveganja: Jošt zaradi bolezni ali drugega razloga za odsotnost ni na voljo. Kot najbolj izkušen s programiranjem backenda njegova odsotnost pusti velik primankljaj v tej vrsti del, kar vpliva na kritično pot.

- Vpliva na: Projekt

- Strategija obvladovanja: Strategija zmanjševanja
- Opis obvladovanja: Poskusili bomo z deli na backendu opraviti čim prej ter si frontend-ovske aktivnosti pustiti za kasneje. Tako bomo v primeru Joštove odsotnosti imeli blazino aktivnosti, na katerih lahko delamo s polno paro v času odsotnosti in tako ni vpliva na kritično pot.


##### Specifična tehnologija (T9):
- Verjetnost: Majhna
- Učinek: Resen
- Izpostavljenost: Srednjevisoka

- Opis tveganja: Ob razvoju odkrijemo potrebo po uporabi bolj specifične tehnologije, ki pa je ne znamo uporabljati in osebno ne poznamo osebe, ki bi nam lahko svetovala.

- Vpliva na: Projekt

- Strategija obvladovanja: Krizni načrt
- Opis obvladovanja: Pristopimo do profesorja ali asistenta, ki se spozna na to področje ter nas usmeri na učne materiali, s čimer lahko prebrodimo svoj problem.



##### Bolezen (T10):
- Verjetnost: Zmerna
- Učinek: Resen
- Izpostavljenost: Srednjevisoka

- Opis tveganja: Kot ekipa le 4 članov obstaja večja možnost, da zboli večji del ekipe (2 ali 3 bolni predstavlja večjo ustavitev sposobnosti, kot bi pri ekipi 5 članov). To bi lahko močno zamaknilo kritično pot.

- Vpliva na: Projekt

- Strategija obvladovanja: Strategija izogibanja
- Opis obvladovanja: Poskusili bomo čim bolje ohraniti svoje zdravje. V primeru tudi blage bolezni oseba ne bo prišla na sestanek, saj bi okužba še enega člana pomenila ogromen izpad v projektu.


#### Organizacija:

##### Cena host-anja (T11):
- Verjetnost: Zmerna
- Učinek: Dopusten
- Izpostavljenost: Srednja

- Opis tveganja: Za hostanje potrenujemo denar, ki nam ni na voljo, kar oteži izdelavo izdelka.

- Vpliva na: Posel

- Strategija obvladovanja: Krizni načrt
- Opis obvladovanja: Profesor je omenil, da bi se v takšnem primeru dalo prositi za povračilo stroškov. Sicer pa bi lahko poiskali znanca, ki bi nam lahko storitev priskrbel po nizki ceni.


##### MOC rez v proračunu (T12):
- Verjetnost: Zelo majhna
- Učinek: Usoden
- Izpostavljenost: Srednjenizka

- Opis tveganja: MOC zaradi rezov v proračunu prekliče projekt.

- Vpliva na: Posel

- Strategije obvladovanja ne definiramo. Izpostavljenot je zaradi nizke verjetnosti dovolj nizka.



#### Zahteve:

##### Sprememba zahtev (T13):
- Verjetnost: Majhna
- Učinek: Resen
- Izpostavljenost: Srednjevisoka

- Opis tveganja: MOC vmes spremeni zahteve do te mere, da je dotedanja koda neuporabna.

- Vpliva na: Projekt

- Strategija obvladovanja: Strategija izogibanja
- Opis obvladovanja: Že med iteracijami bomo poskusili preveriti, če gremo v pravo smer in če se rešitev ujema z njihovimi zahtevami.

##### Algoritem slabši od trenutnega sistema (T14):
- Verjetnost: Visoka
- Učinek: Resen
- Izpostavljenost: Srednjevisoka

- Opis tveganja: Razvit algoritem je slabši od obstoječega sistema pluženja. To se lahko hitro zgodi, saj je težko modelirati vse majhne dejavnike, ki jih domenski eksperti posedujejo.

- Vpliva na: Posel

- Strategija obvladovanja: Strategija izogibanja
- Opis obvladovanja: Sprogramirali bomo simulacijo vožnje po mestu v določenih razmerah pluženja. Skozi celoten proces bomo primerjali rezultate ob pluženju nastavljenem po metodi ostrega očesa, z rezultati našega trenutnega algoritma. Tako bomo bolje vedeli, da razvijamo v pravi smeri.


#### Ocenjevanje:

##### Precenitev sposobnosti (T15):
- Verjetnost: Majhna
- Učinek: Resen
- Izpostavljenost: Srednjevisoka

- Opis tveganja: Hudo smo precenili trajanje aktivnosti razvoja spletne aplikacije zaradi slabe ocene svojega znanja.

- Vpliva na: Projekt

- Strategija obvladovanja: Krizni načrt
- Opis obvladovanja: Zmanjšali bomo nabor funkcionalnosti, ki jih imamo namen implementirali, ter povečali komunikacijo, saj vsaj nekdo o tej stvari ve nekoliko več.

#### Varnost:

##### Scam uporabniki (T16):
- Verjetnost: Zelo majhna
- Učinek: Dopusten
- Izpostavljenost: Srednjenizka

- Opis tveganja: Registracija ljudi, ki namerno želijo škodovati sistemu z veliko količino zahtevkov.

- Vpliva na: Izdelek

- Strategija obvladovanja: Strategija zmanjševanja
- Opis obvladovanja: Omejimo število zahtevkov, ki jih uporabnik lahko odda.

#### Vdor v sistem (T17)
- Verjetnost: Zelo majhna
- Učinek: Usoden
- Izpostavljenost: Visoka

- Opis tveganja: Zlonameren vdor hekerjev, ki onemogočijo delovanje sistema.

- Vpliva na: Izdelek

- Strategija obvladovanja: Strategija izogibanja
- Opis obvladovanja: Pred uvedbo produkcijske aplikacije, bomo za testiranje varnosti
najeli izkušenega penetration testerja. Obseg dela za našo aplikacijo je majhen, zato cenovno to ni večji problem.


#### SQL injection (T18)
- Verjetnost: Zelo majhna
- Učinek: Usoden
- Izpostavljenost: Visoka

- Opis tveganja: Zlonamerno spreminjanje podatkovne baze po nepredvideni poti.

- Vpliva na: Izdelek

- Strategija obvladovanja: Strategija izogibanja
- Opis obvladovanja: Vsi dostopi do podatkovne baze se izvajajo na backend-u. Poskrbeli bomo za pravilno preverjanje vnosnega besedila v zahtevkih.



## 9 Refleksija

Pri projektu smo se s skupinskim delom naučili kopico mehkih veščin, za katere sploh nismo vedeli, da jih ne zmoremo, kaj šele obvladamo. Naučili smo se sodelovanja pri razvoju programske kode, saj je za to potrebno veliko komunikacije, ko več oseb dela na isti funkcionalnosti in morajo razumeti kodo en drugega, ter zagotoviti, da bo na koncu en del kode deloval z drugim.
Tehnično smo se naučili ogromno, saj nam je bilo pred projektom področje spletnega programiranja povsem tuje. Tako smo se naučili vzpostaviti profesionalno frontend okolje, programiranja v Reactu, vzpostavitve in deployment podatkovne baze, deployment izvorne kode na strežniku, in še veliko podrobnosti.
Komunicirali smo uspešno. Stoječi sestanki so bila naša najboljša praksa, saj smo le tako lahko določili skupno vizijo željene rešitve. Pred prvim stoječim sestankom smo namreč imeli velike probleme s komunikacijo, saj še nismo razvili skupnega jezika za posamezne dele sistema in tega, kako naj se povezujejo.
Tehnično večina stvari ni šla po pričakovanjih. Zaradi neizkušenosti smo za vse dele sistema potrebovali veliko več časa, kot smo si sprva predstavljali. Največje probleme smo imeli z deploymentom in pa tudi integracijo komponent.
Veliko težav smo imeli zudi z vzpostavitvijo frontend okolja, saj so nam vse napake bile nove in smo jih s težavo in počasi odpravljali.
Sedaj nam je jasno, da smo si zadali prevelik zalogaj, sploh za tako neizkušeno ekipo.


### 9.1 Priporočila

Če bi se projekta lotili še enkrat, bi ga zastavili v bolj omejenem obsegu. Uporabljali bi manj napredne tehnologije, ki pa so nam že znane (npr. vanilla JavaScript namesto React-a).
Ostalim ekipam bi svetovali prakso stoječih sestankov, če le te še niso uporabljale. Te so nam namreč najbolj pomagali pri razumevanju stanja projekta in potrebnih nadaljnjih korakov.
Ker smo neizkušena ekipa, bi naročniku priporočili bolj podrobno definirano zastavljen problem. Odprtost problema je bil svojevrsten izziv in nam je dopustil kreativno odločanje o željeni končni rešitvi, a smo zaradi svoje neizkušenosti zašli v preveč idejnih smeri naenkrat.
Poleg tega, bi svetoval prihodnjim ekipam, da takoj, ko se implementira osnovna delujoča osnova vzpostavi CI in CD, saj je to končni rezultat dela celotne ekipe. Tudi lažje je že na začetku razmišljati, kako organizirati samo kodo znotraj projekta, saj smo v našem primeru omejeni, koliko prostora in procesorske moči nam Fly.io zagotavlja brez vložka finančnih sredstev. 