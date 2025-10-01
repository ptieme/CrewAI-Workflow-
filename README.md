# CrewAI-Workflow-
Ein mehrstufiger CrewAi- Workflow (Analyst- Texter- Revisor) erstellt aus wenigen Eingaben (Unternehmens- URL, Kurzbeschreibung , Rollenanforderung, Benefits) fertige, Markenkonforme Stellenanazeigen.

Im Notebook werden die Eingaben interaktiv abgefragt und anschließend mit super/websiteSearchTool recherchiert und zu einer hochwertigen Anzeige verdichtet
Technik: crewai , crewai[tools], SerperDevTool, optional Stramlit
Keys: SERPER_API_kEY (pflicht) optional OPENAI_API_KEY(oder anderes LLM gemäß CrewAI-Doku)


# Kurz gesagt
Du gibst die wichtigen Eckdaten ein - der *crew* analysiert die Firmenkultur, ermittelt die ANforderungen und erstellt eine ansprechende, fehlerfreie Anzeige im Corporate-Ton.

# Features

- **3-Agenten‑Pipeline**: Analyst → Texter → Revisor (Qualitätssicherung)
- **Websuche integriert** (Serper/WebsiteSearchTool) zur Recherche von Firmenkultur & Branchenkontext
- **Geführter Dialog** (Notebook) oder **Web‑UI (Streamlit)**
- **Klares, strukturiertes Ergebnis** als Markdown (leicht kopierbar in ATS/Jobboards)
- **Mehrsprachig erweiterbar** (DE/EN/FR)
- **Konfigurierbar** (Rollenanzahl, Iterationen, Prompt‑Vorlagen)

 # TECH-STACK
 - **Python**, **Jupyter Notebook** (`.ipynb`)
- **CrewAI** (`crewai`, `crewai[tools]`)
- **SerperDevTool** (Google/Serper API), **WebsiteSearchTool**
- Optional: **Streamlit** für eine klickbare Web‑App
- Benötigte Keys (als Umgebungsvariablen):  
  - `SERPER_API_KEY` (Pflicht für Websuche)  
  - `OPENAI_API_KEY` *(oder anderes LLM gemäß CrewAI‑Doku)*
 

# Funktionsweise (Pipeline)
1. **Eingaben**: Unternehmens‑URL, Kurzbeschreibung, Rolle, Anforderungen, Benefits
2. **Analyst**: Prüft Website & Beschreibung → extrahiert Kultur, Werte, Mission, Besonderheiten
3. **Branchenanalyse**: Trends/Chancen/Herausforderungen – Kontext für das Wording
4. **Rollen‑Anforderungen**: Muss/Soll‑Kriterien, Aufgaben, Impact
5. **Texter**: Erstellt die Anzeige (Titel, Intro, Aufgaben, Profil, Benefits, Call‑to‑Action)
6. **Revisor**: Prüft Stil, Rechtschreibung, Konsistenz, Arbeitgeber‑Marke → Endfassung
