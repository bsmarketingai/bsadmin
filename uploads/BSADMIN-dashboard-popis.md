# BSADMIN – Dashboard (kopie) · kompletní popis stránky

> Zdroj: Claude Design artifact „BSADMIN Dashboard kopie“ (claude.ai/artifact/4kdzFokY6ha54n4emzdHBM).
> Popis je přepsán z vykreslené stránky (1245 × 952 px viewport, desktop). Všechna data níže jsou přesně to, co stránka zobrazuje.
> Barvy a písmo jsou odečtené z obrazovky – hodnoty ber jako velmi blízký odhad, ne jako tokeny ze zdrojáku.
> Přiložené soubory: `bsadmin-dashboard-full.png` (celá obrazovka), `bsadmin-sidebar-top.png`, `bsadmin-sidebar-bottom.png`, `bsadmin-logo.png`.

---

## 1. Celkový koncept

- **Typ stránky:** úvodní dashboard administrace e-shopové platformy **BSSHOP** („bsadmin“) pro jednu účetní jednotku, která provozuje 26 e-shopů v různých zemích.
- **Vizuální styl:** tmavý „tech“ styl. Pozadí celé stránky je **černé s ostrými červenými laserovými paprsky / světelnými čarami**, které se protínají pod různými úhly (glow efekt). Přes pozadí leží **4 velké panely ve stylu glassmorphism** – poloprůhledná šedá výplň s rozostřením pozadí (backdrop blur), jemný světlý okraj, zaoblené rohy (~14–16 px). Červené paprsky prosvítají panely jako rozmazané růžovo-červené skvrny.
- **Layout:** fixní levý sidebar (~220 px, bez panelu – text přímo na černém pozadí) + obsahová mřížka **2 × 2 panely** (každý ~488 px široký, horní řada ~400 px vysoká, dolní řada ~480 px). Mezery mezi panely ~12 px. Celé se to vejde do jednoho viewportu, stránka sama nescrolluje – scrollují jen seznamy uvnitř panelů (tenký šedý scrollbar vpravo).
- **Jazyk UI:** čeština.

## 2. Barvy (odhad)

| Role | Hodnota | Použití |
|---|---|---|
| Pozadí stránky | `#050505`–`#0B0B0D` + červené laserové čáry | celé pozadí |
| Akcentní červená | `#E0262B` (≈ `#DC2626`) | aktivní taby (text + rámeček), primární tlačítka, badge s počtem, řádek „Celkem“, linie grafu, záporné % |
| Tmavě červená (text v aktivním tabu) | `#B91C1C` | text aktivního filtru na světlém podkladu |
| Panel (glass) | ≈ `rgba(160,160,160,0.55)` + `backdrop-filter: blur(~20px)` | 4 hlavní panely – na obrazovce působí jako `#6E6E6E`–`#7A7A7A` |
| Okraj panelu | ≈ `rgba(255,255,255,0.35)` 1 px | panely, řádky, pilulky |
| Řádek seznamu | o stupeň světlejší než panel (≈ `rgba(255,255,255,0.12)`), radius ~8 px, okraj 1 px světlý | tabulky e-shopů, úloh, kontrol |
| Neaktivní tab / pilulka | světle šedá `#B5B5B5`–`#C4C4C4`, text tmavě šedý `#2B2B35`, radius ~6 px | taby, filtry, tagy služeb |
| Text na panelech | bílá `#FFFFFF` (nadpisy, názvy), tmavě šedá `#1F1F2A` (podnadpisy typu „19 kontrol“) | |
| Tmavé tlačítko | `#1E1E2A` / navy-černá, bílý text | „Otevřít“, „Vzdálená podpora“ |
| Stav OK | zelená tečka `#22C55E` | Aktivní / Spuštěna |
| Stav chyba | červená tečka `#EF4444` | Zastavena |
| Šedé labely v sidebaru | `#9CA3AF` | nadpisy sekcí („VYBRANÁ ÚČETNÍ JEDNOTKA“…) |
| Nadpis „NOVINKY“ | světle červená / lososová `#F87171` | |
| Graf – aktuální období | červená `#E0262B`, 2 px, s malými body | |
| Graf – porovnání | bílá `#FFFFFF`, 2 px | |

## 3. Typografie

- Bezpatkové, humanistické písmo, podle tvarů pravděpodobně **Trebuchet MS** (případně podobný systémový sans). Čísla nejsou tabulková monospace.
- Nadpisy panelů: VERSALKY, bold, ~15–16 px, bílé (např. „VAŠE E-SHOPY“).
- Nadpisy sekcí v sidebaru a pod-sekcí v panelech: VERSALKY, bold, ~11 px, s mírným prostrkáním, šedé (sidebar) nebo bílé (panely).
- Tělo / řádky: ~11–12 px; názvy e-shopů a hodnoty bold.
- Velká čísla v KPI kartách: ~15–16 px bold.

## 4. Logo

- Vlevo nahoře v sidebaru, na střed, ~140 × 45 px.
- **Značka:** červený zaoblený čtverec (`#E0262B`, radius ~6 px), v něm bílé kurzívou psané / kaligrafické „**bs**“ s dlouhou vodorovnou čárou vybíhající doleva, v levém horním rohu malé tmavé kolečko (jako „díra na visačce“).
- **Wordmark:** vpravo od značky bílé bold „**admin**“ (velké, ~26 px), pod ním menší „**bs**shop“ – „bs“ červeně, „shop“ bíle, zarovnané doprava pod „admin“.
- Soubor: `bsadmin-logo.png` (výřez z obrazovky – pro produkci použij originální vektor BSSHOP).

---

## 5. Levý sidebar (shora dolů)

Sekce jsou odděleny tenkou šedou vodorovnou linkou.

### 5.1 Logo
viz výše.

### 5.2 VYBRANÁ ÚČETNÍ JEDNOTKA
- **STREFA s.r.o.** (bold, bílá)
- V Aleji 151
- 541 01 Trutnov
- IČ: 28780965 · DIČ: CZ28780965

### 5.3 PŘIHLÁŠENÝ UŽIVATEL
- Label a hodnota na jednom řádku: „PŘIHLÁŠENÝ UŽIVATEL“ + **Super Admin**

### 5.4 PODPORA
- **+420 499 944 955** (bold, větší)
- po - pá 8:00 - 16:00 (šedá)
- **podpora@bsshop.cz** (bold)
- Primární tlačítko na celou šířku: **Zákaznické centrum** (červené, bílý bold text, radius ~6 px, výška ~28 px)
- Pod ním 3 čtvercové ikonové tlačítka (tmavé, světlý okraj, radius ~8 px): **Instagram**, **Facebook**, **LinkedIn**

### 5.5 NOVINKY (nadpis lososově červený)
Karty s tmavým průhledným pozadím a jemným okrajem, v každé: název (bold) + datum (šedé) + tmavé tlačítko **Otevřít** vpravo.
| Novinka | Datum |
|---|---|
| Cloudflare | 2. 9. 2026 |
| Revolut | 28. 8. 2026 |
| Basileus | 20. 8. 2026 |

### 5.6 SLUŽBA A FRONTY ÚLOH
Karty (tmavé, okraj), název vlevo bold, stav vpravo s barevnou tečkou:
| Položka | Stav |
|---|---|
| Služba BSSHOP | ● Aktivní (zelená) |
| Fronta úloh A | ● Spuštěna (zelená) |
| Fronta úloh B | ● Spuštěna (zelená) |
| Fronta úloh C | ● Zastavena (červená) |

### 5.7 SYSTÉM
Dvousloupcový seznam, label vlevo šedý, hodnota vpravo bílá bold:
| Label | Hodnota |
|---|---|
| Aktualizováno | 4.9.2026 v 14:46 |
| Verze BSADMIN | 20260000.33 |
| Verze IS | 14625 / 13900.81 SQL |
| POHODA | (18.12.2024) |
| Datum databáze | 4. 9. 2026 v 0:06 |

Poznámka pod tím (šedá, menší): „Stáří Pohoda databáze StwPhCZ_28419600 je v požadovaném intervalu.“

---

## 6. Panel 1 (vlevo nahoře) – VAŠE E-SHOPY

- **Hlavička:** „VAŠE E-SHOPY“ + tmavě šedý podtitul „26 e-shopů · 31. 8. – 4. 9. 2026“
- **Taby období** (pilulky): Včera · Dnes · **Tento týden** (aktivní – světle růžové pozadí, červený rámeček a text) · Minulý týden · Tento kvartál · Tento rok · Vlastní
- **Druhý řádek:** dvě bílá date-pole s ikonou kalendáře `28.08.2026` – `03.09.2026`; vpravo dva červené toggle-chipy **s DPH** a **včetně storen** (obrys + červený text = zapnuto)
- **Tabulka** – sloupce: E-SHOP · OBJED. · HODNOTA · PRŮM. (hlavička velkými písmeny, bílá, tenká linka pod ní)
- **Řádek „Celkem“** (připnutý nahoře, světle růžovo-šedé pozadí, červený levý okraj ~3 px, veškerý text červený bold): **895 · 1 009 178 Kč · 1 128 Kč**
- Ostatní řádky: název bold bílý, počet objednávek regular, hodnota bold, průměr regular (menší). Scrolluje se, viditelných ~10 řádků.

| E-shop | Objed. | Hodnota | Prům. |
|---|---:|---:|---:|
| strefa.cz | 191 | 129 294 Kč | 678 Kč |
| e-prefa.cz | 48 | 39 750 Kč | 829 Kč |
| strefa.de | 14 | 11 962 Kč | 829 Kč |
| strefa.hr | 45 | 42 655 Kč | 938 Kč |
| strefa.hu | 12 | 10 346 Kč | 873 Kč |
| strefa.ro | 38 | 34 934 Kč | 924 Kč |
| strefa.fr | 14 | 14 021 Kč | 1 038 Kč |
| strefa.es | 39 | 37 609 Kč | 962 Kč |
| strefa.pt | 14 | 15 082 Kč | 1 095 Kč |
| strefa.ee | 40 | 44 222 Kč | 1 092 Kč |
| strefa.fi | 13 | 15 008 Kč | 1 119 Kč |
| strefa.lv | 45 | 54 050 Kč | 1 208 Kč |
| strefa.si | 11 | 13 423 Kč | 1 251 Kč |
| strefa.bg | 44 | 60 814 Kč | 1 386 Kč |
| strefa.be | 12 | 15 848 Kč | 1 327 Kč |
| strefa.lu | 40 | 57 724 Kč | 1 450 Kč |
| strefa.sk | 13 | 18 765 Kč | 1 457 Kč |
| stref.pl | 45 | 69 361 Kč | 1 546 Kč |
| strefa.at | 15 | 23 604 Kč | 1 610 Kč |
| strefa.gr | 43 | 68 542 Kč | 1 591 Kč |
| strefa.dk | 12 | 20 341 Kč | 1 720 Kč |
| stref.it | 40 | 62 066 Kč | 1 571 Kč |
| stref.lt | 12 | 20 857 Kč | 1 710 Kč |
| stref.se | 40 | 72 726 Kč | 1 814 Kč |
| stref.nl | 13 | 24 459 Kč | 1 896 Kč |
| stref.com | 43 | 31 716 Kč | 737 Kč |

> Pozn.: názvy „stref.pl / .it / .lt / .se / .nl / .com“ jsou v originále opravdu bez „a“ – převzato 1:1. Součet řádků v mockupu přesně nesedí na „Celkem“ (jde o demo data).

---

## 7. Panel 2 (vpravo nahoře) – CELKEM OBJEDNÁVKY

- **Hlavička:** „CELKEM OBJEDNÁVKY“, podtitul „Hodnota · s DPH · včetně storen“
- **Přepínač metriky:** Počet · **Hodnota** (aktivní) · Prům.
- **Řádek „Porovnat s:“** + taby: **Předchozí** (aktivní) · Před rokem · Vlastní · Nic
- **3 KPI karty** vedle sebe (světlejší glass, okraj, radius ~8 px):
  1. ■ červený čtvereček + „TENTO TÝDEN“ → **1 009 178 Kč** (tmavý text)
  2. □ bílý čtvereček + „POROVNÁNÍ“ → **1 277 419 Kč** (bílý text)
  3. „ROZDÍL“ → **-21,0 %** (červený bold)
- Popisek pod kartami: „Předchozí · 30. 8. – 24. 8. 2026“
- **Spojnicový graf** (bez osy Y, bez mřížky, jen spodní osa X se dny): Po · Út · St · Čt · Pá · So · Ne
  - **Červená linie (tento týden)** s malými body: Po vysoko → Út mírně výš → St nejvýš → Čt mírný pokles → Pá pokles → **So a Ne propad téměř na nulu** (vodorovně u osy X; víkend ještě neproběhl / bez dat).
  - **Bílá linie (porovnání)**: Po nejvýš → Út → St mírný pokles → Čt vrchol → Pá mírně níž → So výrazný pokles → Ne další pokles (na ~polovinu výšky).
  - Přibližné relativní hodnoty (0 = osa X, 100 = vrchol grafu): červená Po 92, Út 93, St 97, Čt 88, Pá 84, So 4, Ne 4; bílá Po 96, Út 90, St 87, Čt 95, Pá 87, So 68, Ne 57.

---

## 8. Panel 3 (vlevo dole) – DŮLEŽITÉ

- **Hlavička:** „DŮLEŽITÉ“ + „19 kontrol, **17 s nálezem**“; vpravo sekundární tlačítko **Skrýt bez nálezu** (světlý obrys, bílý text).
- **Sekce „VYŽADUJE POZORNOST“** – řádky na celou šířku; řádky s nálezem mají **světle červený / růžový rámeček**, počet je v **červeném badge** (bílý bold text, radius ~4 px). U dvou řádků je před badge malá ikonka ozubeného kola ⚙ (nastavení kontroly). Řádek s 0 má šedý badge a neutrální rámeček.

| Kontrola | Počet | Pozn. |
|---|---:|---|
| Položky na e-shopu s nulovou cenou | 3 | ⚙ |
| Master produkty bez variant | 0 | šedý badge |
| Variantní produkty bez masterů | 5 | |
| Prodejní cena pod nákupní cenou | 2 | |
| Produkty s podezřele vysokou marží | 8 | ⚙ |

- **Sekce „DOPORUČENO OPRAVIT“** – mřížka 2 sloupce, menší řádky (regular text, počet vpravo bold tmavý, bez badge). Dlouhé názvy se ořezávají „…“. Nula je zobrazena světle šedě (utlumeně).

| Levý sloupec | # | Pravý sloupec | # |
|---|---:|---|---:|
| Produkty na e-shopu bez obrázku | 34 | Produkty s překročenou velikostí obrázku | 6 |
| Produkty na internetu bez popisu | 23 | Produkty bez povinných parametrů | 47 |
| Produkty s chybějícími E1 parametry | 156 | Produkty bez příznaků | 17 |
| Produkty bez EAN | 89 | Duplicity produktů podle EAN | 6 |
| Duplicity produktů podle kódu | 3 | Produkty skladem v koši | 12 |
| Aktivní master produkt se všemi varianta… | 0 | Aktivní varianty produktů s masterem v koši | 5 |
| Skladové produkty v kategorii, která se ne… | 4 | Kategorie bez produktů | 9 |

---

## 9. Panel 4 (vpravo dole) – ZÁKAZNICKÉ CENTRUM

- **Hlavička:** „ZÁKAZNICKÉ CENTRUM“; vpravo dvě tlačítka: **Vzdálená podpora** (tmavé navy) a **Všechny úlohy** (červené).
- Podtitul: „25 aktivních úloh, **10 vyžaduje reakci**“
- **Tabulka úloh** – sloupce ČÍSLO · NÁZEV · CENA · STAV; každý řádek je karta (světlejší glass, okraj, radius ~8 px). Číslo bold, cena vpravo zarovnaná, stav bílý bold zarovnaný vpravo. Seznam scrolluje (viditelných ~9 řádků). Při hoveru se název a cena podtrhnou (viz řádek 159501 na screenshotu).

| Číslo | Název | Cena | Stav |
|---|---|---:|---|
| 154965 | Retino | 42 000,- | Schválit cenu |
| 162076 | Vytváření zálohových faktur | 0,- | Upřesnit |
| 159672 | Opravy 404 stránek ze scanu | 0,- | Upřesnit |
| 159501 | Alza chyba | 0,- | Upřesnit |
| 156575 | ALZA feed | 0,- | Upřesnit |
| 156351 | GoPay – GR, DK, IT, LT, SE, NL | 0,- | Upřesnit |
| 156129 | Google nákupy | 0,- | Upřesnit |
| 154967 | Alza obj 5868472971 | 0,- | Upřesnit |
| 153871 | Chyba v BSadminu OBR | 0,- | Upřesnit |
| 137421 | ALZA – ASM a DSM | 15 000,- | Schválit cenu |
| 156350 | PayPal – GR, IT, LT, NL | 0,- | Vyřízeno |
| 160940 | Nezobrazuje se logo BSshop v Supportboxu | 0,- | Vyřízeno |
| 161744 | Chyba synchronizace atributů | 0,- | Vyřízeno |

- **Podsekce „VYUŽÍVÁTE SLUŽBY“** (vnořený glass box ve spodní části panelu) – tagy/pilulky (světle šedé, tmavý text, radius ~6 px), zalamované do řádků:
  Další jazyková mutace · Cizí měna · Novinky · Bonusy a slevové kupóny · Diskusní fórum · Hodnocení produktů · SmartForm · Looker Studio · Mailkit propojení · Přenos UTM parametrů do Pohody (server side) · DPD ParcelShop · PPL ParcelShop · ČP - Balík na poštu · SP - Balík na poštu · ČP - Balík do balíkovny · ČP - Časová pásma · Slovak Parcel Service (UPS) · GP webpay · Google Analytics 4 · Elasticsearch

---

## 10. Komponenty – shrnutí pro znovupoužití

| Komponenta | Popis |
|---|---|
| Glass panel | poloprůhledná šedá + blur, 1 px světlý okraj, radius 14–16 px, padding ~12 px |
| Tab / pilulka | výška ~20 px, radius 6 px, světle šedá; aktivní = světle růžová výplň + 1 px červený rámeček + červený bold text |
| Toggle chip | obrysový, červený rámeček a text (zapnuto) |
| Řádek seznamu | karta, radius 8 px, 1 px světlý okraj, výška ~24 px |
| Zvýrazněný řádek „Celkem“ | světlejší pozadí, červený levý border 3 px, červený text |
| Badge počtu | červený `#E0262B` / šedý pro 0, bílý bold text, min-width ~28 px |
| Primární tlačítko | červená výplň, bílý bold text, radius 6 px |
| Tmavé tlačítko | navy-černá výplň, bílý bold text |
| Sekundární tlačítko | průhledné, světlý obrys, bílý text |
| Status řádek | tmavá karta s okrajem, tečka 8 px (zelená/červená) + text stavu |
| KPI karta | label s barevným čtverečkem legendy + velké číslo |
| Line chart | 2 série (červená = aktuální, bílá = porovnání), bez gridu, popisky dnů dole |
