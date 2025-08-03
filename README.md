# Projekt_3
# Elections Scraper
Úkolem bylo vytvořit scraper výsledků voleb z roku 2017, který vytáhne data přímo z webu.

**Třetí projekt do Engeto Akademie Tester s Pythonem.**

## Popis projektu
Tento skript slouží pro získání dat z oficiálních webových stránek [Voleb do Poslanecké sněmovny Parlamentu České republiky konaných ve dnech 20. 10. – 21. 10. 2017](https://volby.cz/pls/ps2017nss/ps3?xjazyk=CZ).

## Instalace knihoven
Knihovny použité v tomto skriptu jsou uvedeny v souboru `requirements.txt`. 
Pro instalaci doporučuji použít nové virtuální prostředí a Package installer for Python (PIP).
```
$ pip3 --version
$ pip3 install -r requirements.txt
```

## Spuštění projektu

Pro správné spuštění skriptu je třeba spustit soubor `main.py` se dvěma povinnými argumenty.

`python main.py <odkaz-uzemniho-celku> <vysledny-soubor>`

Následně se stáhnou data ze zadaného odkazu a uloží se do souboru s příponou `.csv`.

## Ukázka projektu

Výsledky hlasování pro kraj Moravskoslezský okres Frýdek-Místek:

1. argument: `[https://www.volby.cz/pls/ps2017nss/ps32?xjazyk=CZ&xkraj=14&xnumnuts=8102]`
2. argument: `volby_2017_vysledky_Frydek_Mistek`

Spuštění programu:

`python main.py "[https://www.volby.cz/pls/ps2017nss/ps32?xjazyk=CZ&xkraj=14&xnumnuts=8102]" "volby_2017_vysledky_Frydek_Mistek"`

Průběh programu:
```
Stahuji data z adresy https://www.volby.cz/pls/ps2017nss/ps32?xjazyk=CZ&xkraj=14&xnumnuts=8102
Exportuji do souboru volby_2017_vysledky_Frydek_Mistek.csv
Dokončeno.
```

Částečný výstup:
```
obec_kod,obec_nazev,volici_pocet,obalky_vydane,hlasy_platne,strana_1,strana_2, ... 598011,Baška,3093,2065,2053,175,1,1,124,1,49,192,21,12,21,1,0,216,0,0,44,665,2,9,194,1,16,7,3,293,5 598020,Bílá,285,178,178,19,0,0,14,0,10,21,3,1,0,1,0,12,1,0,3,52,0,0,15,0,3,0,0,23,0 511633,Bocanovice,358,197,197,20,0,0,32,0,3,13,3,1,0,0,0,18,0,1,1,45,0,0,43,0,0,0,0,17,0
...
