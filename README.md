
# Engeto-pa-3-projekt

Třetí projekt na Python Akademii od Engeta.

## Popis projektu

Tento projekt slouží k extrahování výsledků z parlamentních voleb v roce 2017.  
Vstupem je odkaz na stránku okresu s obcemi (typ `ps32`) na webu volby.cz.  
Výstupem je CSV soubor s počty registrovaných voličů, vydaných obálek, platných hlasů a hlasů pro jednotlivé strany za každou obec.

## Instalace knihoven

Knihovny použité v kódu jsou uvedeny v souboru `requirements.txt`. Doporučeno je použít nové virtuální prostředí a poté spustit:

```bash
python -m venv .venv
# Windows: .venv\Scripts\activate
# macOS/Linux:
source .venv/bin/activate

pip install -r requirements.txt
```

## Spuštění projektu

Spuštění souboru `main.py` v rámci příkazového řádku požaduje dva povinné argumenty:

```bash
python main.py <odkaz-uzemniho-celku> <vysledny-soubor>
```

Následně se vám stáhnou výsledky jako soubor s příponou `.csv`.

## Ukázka projektu

Výsledky hlasování pro okres Prostějov:

1. argument: `https://www.volby.cz/pls/ps2017nss/ps32?xjazyk=CZ&xkraj=12&xnumnuts=7103`  
2. argument: `vysledky_prostejov.csv`

Spuštění programu:

```bash
python main.py "https://www.volby.cz/pls/ps2017nss/ps32?xjazyk=CZ&xkraj=12&xnumnuts=7103" "vysledky_prostejov.csv"
```

Průběh stahování (ukázka výpisu):

```
STAHUJI DATA Z VYBRANEHO URL: https://www.volby.cz/pls/ps2017nss/ps32?xjazyk=CZ&xkraj=12&xnumnuts=7103
UKLADAM DO SOUBORU: vysledky_prostejov.csv
UKONCUJI election-scraper
```

Částečný výstup:

```
code,location,registered,envelopes,valid,...
506761,Alojzov,205,145,144,29,0,0,5,17,4,1,0,0,5,32,0,0,6,0,0,1,1,15,0
589268,Bedihošť,834,527,524,51,0,0,28,1,3,123,2,2,14,1,0,0,6,140,0,0,26,0,0,0,0,82,1
...
```

## Struktura repozitáře

- `main.py` – hlavní skript
- `requirements.txt` – seznam knihoven
- `README.md` – dokumentace
- `vysledky_prostejov.csv` – ukázkový výstup (volitelné)

## Autor

Roman Janotík – janotik.roman@yahoo.com
