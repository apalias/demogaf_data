# Analýza populačních trendů v Praze a Moravskoslezském kraji (2000-2023)

## Popis projektu

Tento projekt analyzuje vývoj vybraných demografických ukazatelů v Hlavním městě Praze a Moravskoslezském kraji v letech 2000 až 2023. Cílem bylo identifikovat hlavní trendy, porovnat vývoj mezi kraji a zjistit, jaký vliv měla přirozená měna a migrace na celkový populační vývoj.

## Data

* **Zdroj:** Data pocházejí z veřejných datových sad [(https://data.gov.cz/datová-sada?iri=https%3A%2F%2Fdata.gov.cz%2Fzdroj%2Fdatové-sady%2F00025593%2F6795807bcf25ae041ee00d15b5b5ce8b)]. Soubor `OBY01BHVD.csv` obsahuje data pro více krajů a ukazatelů.
* **Analyzované ukazatele:**
    * Přirozený přírůstek/úbytek na 1 000 obyvatel
    * Přírůstek/úbytek stěhováním na 1 000 obyvatel
    * Celkový přírůstek/úbytek na 1 000 obyvatel
* **Časové období:** 2000 - 2023
* **Regiony:** Hlavní město Praha, Moravskoslezský kraj, Královéhradecký kraj

## Použité technologie

* Python 3.x
* Pandas - pro manipulaci a analýzu dat
* Matplotlib - pro základní vizualizace
* Seaborn - pro pokročilejší a estetičtější vizualizace
* Jupyter Notebook - pro interaktivní analýzu a prezentaci

## Klíčové závěry a vizualizace

* **Praha:** Většinou vykazovala celkový přírůstek obyvatel, tažený jak přirozeným přírůstkem (zejména v letech cca 2006-2019), tak migrací. Trend přirozeného přírůstku je v posledních letech klesající.
* **Moravskoslezský kraj:** Dlouhodobě čelí přirozenému úbytku obyvatel, který byl v posledních letech (zejména 2020-2021) výrazný. Migrační saldo bylo často záporné, s výjimkou výrazného kladného výkyvu v roce 2022.
* **Královéhradecký kraj:** Velmi podobná situace jako v Moravskoslezského kraji, propad přiřozeného přírůstku byl strmý podobně jako MSK. Oboji lze zřejmě vysvětlit COVIDovou pandemié (která nicméně v Praze neměla tak drastický dopad)
* **Rok 2022:** V všech třech krajích je patrný výrazný nárůst migračního salda, který pravděpodobně souvisí s příchodem uprchlíků z Ukrajiny po ruské agresi. Tento rok představuje významný zlom v datech o migraci.
* **Dominantní složka:** Zatímco v Praze měly obě složky (přirozená měna a migrace) vliv, v MSK byl často dominantní přirozený úbytek, vyrovnávaný či prohlubovaný migrací (s výjimkou roku 2022).

![Porovnání přirozeného přírůstku](viz složka plots se všemi vizualizacemi) ## Struktura repozitáře

* `notebooks/por_ukol.ipynb`: Hlavní Jupyter Notebook s analýzou a vizualizacemi.
* `data/OBY01BHVD.csv`: Zdrojová data.
* `plots/`: Složka s vygenerovanými grafy (pokud je ukládáš zvlášť).
* `README.md`: Tento soubor - popis projektu.
* `requirements.txt`: Seznam potřebných Python knihoven.
* `.gitignore`: Specifikace souborů ignorovaných Gitem.

## Jak spustit projekt

1.  **Naklonujte repozitář:**
    ```bash
    git clone [(https://github.com/apalias/demogaf_data.git)](https://github.com/apalias/demogaf_data.git)
    cd [demograf_data]
    ```
2.  **(Doporučeno)** Vytvořte a aktivujte virtuální prostředí:
    ```bash
    python -m venv venv
    source venv/bin/activate  # macOS/Linux
    # nebo
    .\venv\Scripts\activate  # Windows
    ```
3.  **Nainstalujte závislosti:**
    ```bash
    pip install -r requirements.txt
    ```
4.  **Spusťte Jupyter Notebook:**
    ```bash
    jupyter notebook notebooks/por_ukol.ipynb
    # nebo pokud používáte Jupyter Lab:
    # jupyter lab notebooks/por_ukol.ipynb
    ```
