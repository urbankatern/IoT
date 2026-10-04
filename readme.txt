--- PRVI SKLOP---
1. Opredelite bistvene razlike med konceptoma IoT in IoE ter pojasnite, kako vkljucitev "procesov" in ljudi spremeni zgolj tehnicno povezavo v poslovno vrednost.
    IoT (Internet of Things) povezuje zgolj naprave in senzorje, medtem ko IoE (Internet of Everything) vkljucuje tudi ljudi, procese in podatke. Naprave zbirajo in med seboj izmenjujejo podatke, ki vplivajo na delovanje procesov in nase odlocitve.

2. Razlozite pomen prehoda z omreznega protokola IPv4 na IPv6 za razvoj masovnega interneta stvari (Massive IoT).
    IPv4 naslovov je hitro zacelo zmanjkovati, zato so presli na IPv6, ki ima vec razlicnih naslovov kot je atomov na povrsju Zemlje.

3. Podrobno s svojimi besedami opisite delovanje 4-nivojske arhitekture IoT sistema na prakticnem primeru pametnega kmetijstva (kot razumete vi).
    1. Nivo - Zaznavanje (na poljih imamo senzor, ki fizicno meri vlaznost)
    2. Nivo - Omrezni (Prenos podatkov do sistema, ki jih bo obdelal s protokolom LoRaWAN)
    3. Nivo - Obdelava (Tu se podatki analizirajo in filtrirajo, sistem primerja trenutno vlaznost z ustrezno in po potrebi poslje signal za namakanje)
    4. Nivo - Aplikacijski (Sistem sprozi namakanje, ce je polje presuho)

4. (Izbira) Zakaj Protokol MQTT v primerjavi s HTTP ponuja bistveno vecjo energijsko ucinkovitost za baterijska senzorska vozlisca?
    A) Ker MQTT deluje izkljucno preko nespremenljivih UDP paketov brez potrjevanja.
    B) Ker ima MQTT minimalno fiksno glavo sporocila (2 bajta) in ohranja odprto TCP sejo (Keep-Alive), kar odpravlja rezijo ponavljajocih se 3-smernih usklajevanj (TCP handshake) in obseznih tekstovnih HTTP glav pri vsaki meritvi.
    C) Ker MQTT samodejno stisne podatke z algoritmom gzip na nivoju mikrokrmilnika.
    D) Ker MQTT ne podpira sifriranja TLS in s tem razbremeni procesor.
    ODG.: B

5. (Povezovanje) Povezi 4 stebre IoE z ustreznim scenarijem delovanja/izvajanja.
    1) Ljudje (People)
    2) Procesi (Processes)
    3) Podatki (Data)
    4) Stvari (Things)
    A) Opticni senzor motnosti vode na cistilni napravi
    B) Algoritem za avtomatsko sprozitev izpiranja filtrov ob dolocenem pragu
    C) upravljalec cistilne naprave, ki prejme alarm na pametno uro
    D) Normaliziran niz casovnih meritev v formatu JSON
    ODG.: 1 => C, 2 => B, 3 => D, 4 => A


--- DRUGI SKLOP ---
1. V katerem letu je Kevin Ashton prvic uporabil termin "Internet of Things" in pri katerem podjetju?
    Leta 1999 pri podjetju P&G

2. Katera je bila prva naprava IoT v zgodovini in kje je bila namescena?
    Prva naprava je bil avtomat za Coca-Colo leta 1982, namescena na univerzi Carnegie Mellon.

3. V katerem letu je stevilo prikljucenih naprav prvic preseglo stevilo ljudi na svetu?
    Leta 2008

4. Zakaj je bil prehod na IPv6 kljucen za razvoj IoT?
    Ker ima IPv6 v primerjavi z IPv4 ogromno stevilo naslovov (2^128)

5. Kateri so 4 nivoji standardnega arhitekturnega modela IoT sistemov?
    1. zaznavni nivo
    2. omrezni nivo
    3. nivo obdelave
    4. aplikacijski nivo

6. Zakaj je MQTT boljsa izbira od HTTP za IoT naprave z baterijo?
    Saj ima le 2-bitno glavo sporocila in omogoca dolgotrajno odprto TCP povezavo (Keep-Alive)

7. Kateri so 4 stebri IoE (Internet vsega) in kako se razlikuje od IoT?
    Stvari, podatki, procesi, ljudje. Od IoT se razlikuje v tem, da je to bolj kocept kot pa zgolj fizicne naprave in senzorji.

8. Navedite 3 konkretne prednosti pametnih mest, ki jih omogoca IoT.
    Pametna ulicna razsvetljava, pametno locevanje odpadkov, pametna prometna signalizacija (za odpravljanje zastojev)

9. Koliko IoT naprav je napovedanih do leta 2030 in kaj bo pospesilo to rast?
    41.1 miljard, rast naj bi pospesil IPv6, 5G itd.

10. Katera kibernetska varnostna groznja je leta 2016 razgalila rannljivosti IoT naprav in kako?
    Mirai Botnet je okuzil priblizno 100.000 kamer z odprtimi telnet gesli.

11. Kaj je LoRaWAN Class A in zakaj je idealen za baterijske senzorje?
    Je protokol, pri katerem naprava vecino casa spi (baterija zdrzi dlje), ko odda podatke odpre dve kratki okni za sprejem podatkov, katerih interval lahko definiramo.

12. Razlozite razliko med robnim, meglenim in oblacnim racunalnistvom v IoT kontekstu.
    * Robno - podatki se obdelujejo neposredno na napravi
    * Megleno - obdelava poteka na vmesnih napravah med IoT napravami in oblakom
    * Oblacno - podatki so poslani vb oddaljene podatkovne centre, kjer so obdelani in shranjeni

13. Kateri komunikacijski protokol bi izbrali za pametno kmetijstvo in zakaj?
    LoRaWAN, ker omogoca velik doseg, vecjo energijsko ucinkovitost in povezovanje velikega stevila senzorjev.

14. Kaksna je razlika med IoT in IoE v poslovni vrednosti?
    IoT povezuje le naprave in procese (avtomatizacija procesov), medtem ko IoE zraven doda se cloveski faktor, kar omogoca visjo poslovno vrednost (optimizacija procesov)

15. Katera bistvena arhitekturna lastnost loci tehnologijo LoRaWAN od tehnologije NB-IoT?
    A) LoRaWAN deluje v nelicenciranem spektru (npr. 868 MHz v EU) z modulacijo Chip Spread Spectrum (CSS) in omogoca postavitev zasebnih baznih postaj, medtem ko NB-IoT deluje v licenciranem spektru mobilnih operaterjev na osnovi standarda LTE.
    B) LoRaWAN omogoca prenos videoposnetkov v realnem casu, NB-IoT pa le tekstovnih nizov.
    C) NB-IoT ima doseg le do 10 metrov, LoRaWAN pa do 100 kilometrov.
    D) LoRaWAN zahteva neposredno opticno vidljivost med oddajnikom in sprejemnikom.
    ODG.: A

16. Povezi nivoje 4-nivojske IoT arhitekture z njihovo primarno tehnologijo/napravo.
    1) Zaznavni nivo (Perception)
    2) Omrezni nivo (Network)
    3) Nivo obdelave (Edge/Cloud)
    4) Aplikacijski nivo (Application)
    A) LoRaWAN Gateway in usmerjevalnik
    B) Grafana nadzorna plosca in ERP sistem
    C) Digitalni senzor BME280 in A/D pretvornik
    D) Casovna podatkovna baza InfluxDB in Docker kontejner
    ODG.: 1 => E, 2 => A, 3 => D, 4 => B

17. Kaj predstavlja mehanizem "Last Will and Testament" (LWT) v protokolu MQTT?
    A) Varnostno kopijo baze podatkov ob izpadu streznika.
    B) Vnaprej definirano sporocilo, ki ga odjemalec ob prijavi shrani na posredniku (Brokerju), posrednik pa ga samodejno objavi na doloceni temi, ce odjemalec nepricakovano izgbi povezavo (npr. odpoved napajanja).
    C) Sifrirni kljuc, ki se unici ob zaznanem napadu na mikrokrmilnik.
    D) Ukaz za ponovni zagon mikrokrmilnika po koncanem prenosu podatkov.
    ODG.: B

18. Povezi varnostno tveganje v IoT z ustreznim protiukrepom
	1) Prisluškovanje in prestrezanje telemetrije na omrežju (Man-in-the-Middle)
	2) Vdor v napravo prek privzetih tovarniških poverilnic (npr. Mirai botnet)
	3) Nalaganje zlonamerne prirejene strojne kode (Firmware modification)
	4) Fizično odčitavanje šifrirnih ključev iz pomnilnika naprave
    A) Uveljavitev varnega zagona (Secure Boot) s preverjanjem kriptografskega podpisa
    B) Sifriranje prometa s protokolom TLS/DTLS
    C) Uporaba namenskega strojnega varnostnega cipa (Secure Element) z zascito pred odpiranjem
    D) Onemogocitev privzetih gesel in uveljavitev unikatnih avtentikacijskih zetonov za vsako napravo
    ODG.: 1 => B, 2 => D, 3 => A, 4 => C

19. Kakšna je bistvena razlika med pasivnim in aktivnim senzorjem?
	A) Pasivni senzorji delujejo le podnevi, aktivni pa ponoči.
	B) Pasivni senzorji ne potrebujejo zunanjega vira električnega napajanja za generiranje signala (npr. termočlen, piezoelektrični kristal), medtem ko aktivni senzorji zahtevajo zunanje napajanje za vzbujanje in merjenje spremembe (npr. fotoupor v delilniku napetosti, radarski senzor).
	C) Pasivni senzorji oddajajo digitalni signal, aktivni pa analogni.
	D) Aktivni senzorji nimajo mikrokrmilniškega vmesnika.
    ODG.: B

20. Povezi mersko fizikalno velicino z ustreznim tipom senzorskega elementa.
    1) Relativna vlaznost zraka
    2) Osvetljenost okolja (vidna svetloba)
    3) Kotna hitrost / orientacija v prostoru
    4) Zracni tlak (atmosferski)
    A) Piezouporovni menbranski senzor
    B) Kapacitivni polimerni senzorski element
    C) MEMS ziroskop s Coriolisovim pospeskom
    D) Fotoupor (LDR) na osnovi kadmijevega sulfida ali fotodioda
    ODG.: 1 => B, 2 => D, 3 => C, 4 => A

21. Zakaj v baterijsko napajanih LoRaWAN omrezjih uporabljamo razred naprav "Class A" namesto "Class C"?
    B) Ker so naprave Class A vecino casa v nacinu globokega spanja (Deep Sleep) in odprejo dve kratki sprejemni okni (RX1 in RX2) le takoj po oddaji svojega paketa (Uplink), medtem ko imajo naprave Class C sprejemnik neprekinjeno vklopljen

22. Povezi koncept obdelave podatkov z njegovo glavno prednostjo.
    1) Robno racunanje (Cloud computing)
    2) Megleno racunanje (Fog computing)
    3) Racunalnistvo v oblaku (Cloud Computing)
    A) Globalna agregacija podatkov, neomejena procesorska moc za strojno ucenje in dolgorocni arhivi
    B) Ultra nizka zakasnitev, neodvisnost od interneta in maksimalna zasebnost lokalnih podatkov
    C) Vmesni nivo lokalnega omrezja, ki agregira podatke vec robnih vozlisc pred posiljanjem v oblak
    ODG.: 1 => B, 2 => C, 3 => B

23. Primerjajte prednosti in slabosti centralizirane obdelave v oblaku (Cloud) v primerjavi z robnim racunanjem (Edge Computing). Navedite primer, kjer je robna obdelava nujna.
    Cloud prednosti in slabosti:
        + veliki racunalniki in pomnilniska zmogljivost
        + enostavno shranjevanje velikih kolicin podatkov
        + enostavne upravljanje vecjega st. naprav
        + dostop do podatkov kjer koli
        - odvisnost od internetne povezave
        - zakasnitev pri prenosu podatkov
        - vecji promet po omrezju
    Edge prednosti in slabosti:
        + zelo majhna zakasnitev
        + hitrejse lokalno odlocanje
        + deluje brez internetne povezave
        - omejene procesorske in pomnilniske zmoglivosti
        - zahtevnejse vzdrzevanje velikega stevila naprav
    Robna obdelava je nujna pro avtonomnih vozilih, kjer mora avto podatke obdelati brez opazne zakasnitve.

24. Opisite arhitekturo protokola MQTT ter podrobno razlozite vloge komponent: Broker, Publisher, Subscriber.
    Je lahek komunikacijski protokol.
    Publisher:
        - naprava ali aplikacija, ki posilja podatke
        - podatke objavi na doloceno temo (npr. senzor za temperaturo objavi 24* na temo hisa/temperatura)
    Broker:
        - osrednja komponenta
        - sprejema sporocila publisherja
        - preveri kateri Subscriberji so naroceni na doloceno temo
        - sporocilo posreduje vsem ustreznim
        - skrbi za povezave
    Subscriber:
        - naprava ali aplikacija, ki se naroci na eno ali vec tem
        - broker ji posreduje sporocila iz teh tem
    Potek: senzor => publisher => broker => subscriber

25. Podrobno primerjajte nivoje kakovosti storitve QoS 0, QoS 1 in QoS 2 v protokolu MQTT. Kdaj uporabimo posameznega?
    
26. Razlozite tehnologijno LoRaa in omrezno plast LoRaWAN. Kako modulacija Chirp Spread Spectrum (CSS) omogoca dolg doseg?

27. Analizirajte varnostne ranljivosti, ki so omogocile napad botneta Mirai in opisite ukrepe za zascito sodobnih IoT naprav.
    Mirai je botnet, ki je izkoriscal slabo zascito IoT naprav, kot so IP-kamere. Njihove glavne ranljivosti so sibka privzeta gesla, ki jih uporabniki pogosto niso spreminjali in neposredna dostopnost preko interneta. Ukrepi proti takim ranljivostim so sprememba gesel po prvi uporabi, uporaba dolgih in edinstvenih gesel in redno namescanje varnostnih posodobitev.

28. Opisite zgradbo in delovanje pametnega domacega termostata kot celovitega sistema (od senzorja do oblaka in uporabnika), kot ga sami razumete.
    Senzor: meri temperaturo, vlaznost, itd.
    Mikrokrmilnik: obdela meritve in jih primerja z nastavljeno temperaturo
    Aktuator: na podlagi odlocitve vklopi ali izklopi ogrevanje
    Oblak: shranjuje podatke o gretju, omogoca analizo
    Uporabnik: preko telefona spreminja in nadzoruje nastavitve temperature

29. Razlozite pojem "Digitalni dvojcek" (Digital twin) v industrijskem internetu stvari (IIoT) in navedite primer njegove uporabe.
    Digitalni dvojcek je digitalen model fizicnega objekta, stroja ali procesa, ki se s pomocjo podatkov iz senzorjev cim bolj sproti posodablja glede na stanje fizicnega sistema.
    Primer: industrijski motor ima senzorje za merjenje njegovega delovanja, senzorji posljejo podatke v informacijski sistem, kjer njegov digitalni dvojcek prikazuje trenutno stanje motorja.

30. Pojasnite razliko med pasivnimi in aktivnimi RFID sistemi ter opisite delovanje NFC tehnologije.
    Pasivni RFID nima lastne baterije, napaja se z elektro magnetskim poljem citalnika, ima krajsi domet in manjso ceno. Aktivni RFID ima lastno baterijo, vecji domet in je posledicno tudi drazji.
    NFC je tehnologija za komunikacijo na zelo kratke razdalje, deluje pri 13,56 MHz in omogoca komunikacijo med napravami, prva naprava prebere podatke druge, lahko tudi dvosmerno.

31. Razlozite pomen energetske optimizacije pri baterijskih IoT napravah in opisite tehnike spanja (Sleep Modes) pri mikrokrmilnikih (hint Class-A).
    Pri IoT napravah je poraba energije zelo pomembna, obicajno porabi najvec energije aktivno delovanje mikrokrmilnika in senzorjev ter komunikacija med napravami. Da bi porabo znizali, lahko definiramo casovni interval: ko se naprava zbudi opravi meritve in poslje podatke, nato pa preklopi v nacin spanja, kjer je poraba energije zelo majhna.

32. Analizirajte in argumentirajte eticne in pravne vidike zajema podatkov v sistemih pametnih mest z vidika Splosne uredbe o varstvu podatkov (GDPR).
    Eticno vprasanje je predvsem ravnotezje med koristijo za mesto in zasebnost prebivalcev, npr. sistem kamer, ki lahko pomaga pri upravljanju prometa, vendar hkratni omogoca mnozicno spremljanje gibanja ljudi. Zato je potrebno, da se pri takih sistemih ureja anonimizacija, omejitev dostopa, sifriranje ipd.

33. Opisite zgradbo in delovanje pametnega sistema za ravmamke z odpadki v pametnem mestu (Smart Waste Management).
    1. Senzor v zabojniku meri napolnjenost zabojnikov ter druge parametre
    2. Mikrokrmilnik / IoT naprava obdela meritev
    3. Brezzicna povezava - s pomocjo protokola LoRaWAN mikrokrmilnik poslje obdelane podatke na oblak (Cloud)
    4. Cloud - meritve se shranijo in analizirajo
    5. uporabnik - delavcu na komunali digitalni dvojcek prikazuje podatke, delavec se odloci ali je potrebno poslati ljudi, da zabojnike spraznijo ali preverijo
    6. Odvoz - vozila dobijo optimalno pot glede na napolnjenost zabojnikov

34. Kaj je tehnologija Bluetooth Mesh in kako se razlikuje od tradicionalnega prenosa Bluetooth tocka-tocka?
    Bluetooth Mesh je omrezna tehnologija, pri kateri lahko vec Bluetooth naprav sodeluje v mrezni (mesh) topologiji.
    Pri Bluetooth komunikaciji imamo povezavo A <=> B, pri Bluetooth mesh tehnologiji pa lahko sporocilo potuje preko vecih naprav (A => B => C => D)
    Naprave v omrezju lahko sporocilo posredujejo naprej, zato komunikacija ni omejena na neposredno povezane naprave.

35. Razlozite, kaj je "Man-in-the-Middle" (MITM) napad na nezasciteno IoT omrezje in kako ga preprecimo..
    MITM napad se zgodi, ko napadalec prestreze komunikacijo med dvema napravama in se postavi med njiju, napadalec nato poskusa prestrezti ali spremeniti komunikacijo. (Namesto BT naprava <=> streznik pride do IoT naprava <=> napadalec <=> streznik)
    Preprecujemo ga z sifriranjem komunikacije, medsebojno preverjanje identitete naprave in mocno avtentikacijo.

36. Opredelite pomen standardizacije v IoT in vlogo organizacij (IEEE, IETF, ITU, 3GPP) pri zagotavlanju interoperabilnosti.
    Standardizacija zagotavlja, da lahko naprave razlicnih proizvajalcev med seboj komunicirajo. S tem omogocamo povezovanje IoT naprav razlicnih proizvajalcev. Vloga organizacij je ustvarjanje standardov in pravil, ki se jih proizvajalci drzijo, kar omogoca interoperabilnost (kompatibilnost naprav razlicnih prozivajalcev).
