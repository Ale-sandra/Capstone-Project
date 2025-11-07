# Capstone-Project
# Analisi RCA 2020–2025
Progetto finale del corso **Data Analyst – Epicode**  
Autrice: **Alessandra Nicastro**

## Obiettivo
Analizzare i dati di rinnovo delle polizze RCA provenienti dal gestionale di agenzia, identificando:
- le tendenze di rinnovo e mancato rinnovo nel periodo 2020–2025;
- le motivazioni dei mancati rinnovi;
- le destinazioni dei clienti che cambiano compagnia;
- il profilo demografico dei clienti più inclini al cambio.

## Dataset e fonti
- **Dati origine:** esportazioni dal gestionale di agenzia (2020–2025)
- **Fonti esterne:** portale ANIA (visure RCA, stato copertura e compagnia)
- **Formati utilizzati:** Excel, CSV e tabelle normalizzate in Power BI

## Workflow tecnico

1. **Estrazione dati**
   - Script `Estrazione file.ipynb`  
     ➤ automatizza il recupero dei file annuali dal gestionale e li separa per anno.

2. **Accesso ai dati ANIA**
   - Consultazione del portale ANIA
     ➤ verifica dello stato di copertura assicurativa dei veicoli non rinnovati.

3. **Pulizia e normalizzazione**
   - Script Pulizia & normalizzazione.ipynb
   ➤ unisce, deduplica e uniforma i dataset;
   ➤ crea chiavi composite e colonne derivate (Anno, Tipo Veicolo, Stato ANIA, Età, Anzianità Contratto);
   ➤ genera le tabelle derivate Compagnie Assicurative, Clienti e Veicoli.

4. **Caricamento e modellazione Power BI**
   - Creazione di schema a **stella** (Fact Rinnovi + Dimensioni Anno, Compagnia, Subagenzia, Cliente)
   - Relazioni 1→N e misure DAX per analisi temporali e percentuali

## Struttura del report Power BI
1. **Pagina 1 – Distribuzione polizze in scadenza**  
   Panoramica generale dei rinnovi e dei mancati rinnovi per tipologia di veicolo e periodo.

2. **Pagina 2 – Mancati rinnovi e impatto economico**  
   Analisi del premio perso nel tempo e relativa incidenza economica.

3. **Pagina 3 – Dove si assicurano altrove**  
   Distribuzione per canale (online, tradizionale, ibrido) e compagnie di destinazione.

4. **Pagina 4 – Profilo clienti che cambiano**  
   Analisi demografica (età, sesso, canale preferito) e profilo dei clienti più inclini al cambio.

---

## Strumenti e linguaggi
- **Python:** pandas, numpy,
- **Power BI:** Power Query, DAX, tooltip, KPI cards, decomposition tree
- **Excel:** Power Query e funzioni di unione e pulizia  
- **GitHub:** documentazione e repository finale

---

## Insight principali
- Crescente incidenza del **canale online** dopo il 2021, con *Prima Assicurazioni* in testa.  
- I **clienti con minore anzianità** mostrano maggiore propensione al cambio.  
- Le **fasce d’età 30–45 anni** e prevalentemente maschili guidano la transizione verso i canali digitali.  
- Le **compagnie tradizionali** restano la principale concorrenza diretta a livello locale.  
- L’impatto economico dei mancati rinnovi è significativo nei primi anni di rapporto, ma più stabile tra i clienti storici.

---

## Autrice
**Alessandra Nicastro** – Data Analyst in formazione, con esperienza pluriennale nel settore assicurativo e passione per l’analisi dei dati e la trasformazione digitale delle agenzie.
