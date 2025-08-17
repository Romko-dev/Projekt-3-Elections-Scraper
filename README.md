# Engeto-pa-3-projekt

Tretí projekt na Python Akadémii od Engeta.

## Popis projektu

Tento projekt slúži na extrahovanie výsledkov z parlamentných volieb v roku 2017.  
Vstupom je odkaz na stránku okresu s obcami na webe volby.cz  
Výstupom je CSV súbor s počtami registrovaných voličov, vydaných obálok, platných hlasov a hlasov pre jednotlivé strany za každú obec.

## Inštalácia knižníc

Knižnice, ktoré sú použité v kóde, sú uložené v súbore `requirements.txt`. Na inštaláciu odporúčam použiť nové virtuálne prostredie a s nainštalovaným manažérom spustiť nasledovne:

$ pip3 –version                    # overím verziu manažéra

$ pip3 install -r requirements.txt  # nainštalujeme knižnice

## Spustenie projektu

Spustenie súboru `main.py` v rámci príkazového riadku vyžaduje dva povinné argumenty:
bash
python main.py <odkaz-uzemneho-celku> <vysledny-subor>

## Ukážka projektu

Výsledky hlasovania pre okres Prostějov:
	1.	argument: https://www.volby.cz/pls/ps2017nss/ps32?xjazyk=CZ&xkraj=12&xnumnuts=7103
	2.	argument: vysledky_prostejov.csv

## Spustenie programu:

python main.py "https://www.volby.cz/pls/ps2017nss/ps32?xjazyk=CZ&xkraj=12&xnumnuts=7103" "vysledky_prostejov.csv"

## Priebeh sťahovania (ukážka výpisu):
STAHUJI DATA Z VYBRANEHO URL: https://www.volby.cz/pls/ps2017nss/ps32?xjazyk=CZ&xkraj=12&xnumnuts=7103
UKLADAM DO SOUBORU: vysledky_prostejov.csv
UKONCUJEM election-scraper

##  Čiastočný výstup:
code,location,registered,envelopes,valid,...
506761,Alojzov,205,145,144,29,0,0,5,17,4,1,0,0,5,32,0,0,6,0,0,1,1,15,0
589268,Bedihošť,834,527,524,51,0,0,28,1,3,123,2,2,14,1,0,0,6,140,0,0,26,0,0,0,0,82,1
...

##  Štruktúra repozitára
	•	main.py – hlavný skript
	•	requirements.txt – zoznam knižníc
	•	README.md – dokumentácia
	•	vysledky_prostejov.csv
