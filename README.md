# Masteroppgave 2026 – Six Sigma-analyse av Alnabruterminalen

Dette repositoriet inneholder koden og dataflyten som brukes i Kristian Strøms
masteroppgave i industriell økonomi. Oppgaven undersøker årsaker til
avgangsforsinkelser fra Alnabru godsterminal ved hjelp av en
Six Sigma-/DMAIC-basert analyse av interne prosesser.

Analysen er laget som Jupyter-notebooks og følger hovedsakelig rekkefølgen
Import/transformasjon → Measure → Analyze. En del av koden, variabelnavnene og
kommentarene er på engelsk i stedet for norsk på grunn av personlig vane.

## Filstruktur

```text
├── 00_data_import_and_transformation/
│   └── excelDatasets_import_export.ipynb
├── 01_measure_phase/
│   ├── 01_00_data_exploration_and_experimentation.ipynb
│   └── 01_01_data_quality_analysis.ipynb
├── 02_analyze_phase/
│   └── 02_01_quantitative_analysis.ipynb
├── data/
│   ├── raw/                         # Originale Excel-filer (lokale/rådata)
│   └── cleaned_data/                # Renset datasett til analyse
├── requirements.txt
└── README.md
```

`data/raw/` inneholder originale datakilder og er utelatt fra Git. De må
derfor være tilgjengelige lokalt dersom import-notebooken skal kjøres fra
start.

## Oppsett og kjøring

1. Klon repositoriet og åpne en terminal i prosjektmappen.
2. Opprett og aktiver et virtuelt miljø:

   ```powershell
   python -m venv .venv
   .venv\Scripts\Activate.ps1
   ```

3. Installer avhengighetene:

   ```powershell
   python -m pip install -r requirements.txt
   ```

4. Start Jupyter:

   ```powershell
   jupyter lab
   ```

5. Kjør notebookene i denne rekkefølgen:
   1. `00_data_import_and_transformation/excelDatasets_import_export.ipynb`
   2. `01_measure_phase/01_00_data_exploration_and_experimentation.ipynb`
   3. `01_measure_phase/01_01_data_quality_analysis.ipynb`
   4. `02_analyze_phase/02_01_quantitative_analysis.ipynb`

Velg `.venv` som kernel i Jupyter. Import- og Measure-notebookene oppretter
og oppdaterer datasett i `data/`, inkludert det rensede Parquet-datasettet
som brukes i Analyze-fasen.

## Libraries og verktøy

- **Python** og **Jupyter Notebook/Lab** – utvikling og kjøring av analysen
- **pandas** og **NumPy** – import, strukturering og behandling av data
- **Matplotlib** og **Seaborn** – visualisering
- **SciPy** – statistiske analyser og hypotesetesting
- **openpyxl** og **PyArrow** – lesing av Excel-filer og Parquet-lagring
- **VS Code** – anbefalt editor
- **Git/GitHub** – versjonskontroll

Alle Python-avhengigheter med versjoner er samlet i
[`requirements.txt`](requirements.txt).

## Forfatter

**Kristian Strøm**
