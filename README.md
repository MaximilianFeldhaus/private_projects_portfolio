# Portfolio Privater Projekte

Willkommen zu meiner Sammlung privater Projekte. Dieses Repository dient als Präsentation meiner persönlichen Entwicklungsarbeit, Experimente und Nebenprojekte.

---

# KI-basierter Stichprobenassistent für Wirtschaftsprüfer

**Status:** In Bearbeitung | **Kategorie:** Financial Technology / Prüfungssoftware
**Link zum Repo** Das Repo ist privat. Auf Wunsch gebe ich gerne Zugriff auf den Code.

Ein KI-gestütztes Stichproben-Tool, das die Rechnungsvalidierung durch Verarbeitung von Excel-Stichprobendateien und entsprechenden PDF-Rechnungen mit LLM Technologie automatisiert. Das Tool hilft dabei, manuelle Prüfungsarbeiten zu reduzieren und gleichzeitig Genauigkeit und Compliance-Standards zu gewährleisten.

**Videodemonstration:**

![Demo](assets/demo_ki_stichprobenassistent.gif)

**Hauptfunktionen:**
- Rechnungstext-Extraktion und -Analyse mit LLM-Modellen (Qwen3-14B)
- Automatisierte Validierung von Artikelnummer und -beschreibung gegen Quelldokumente
- Geschäftsjahr-Validierung mit konfigurierbaren Stichtagen
- Betragsvergleich zwischen gebuchten und berechneten Werten
- Audit-Trail mit LLM-Interaktionsprotokollierung
- Multi-Engagement-Dashboard zur Verwaltung verschiedener Prüfungsprojekte
- Verarbeitungsstatus-Anzeige mit Ergebnisvisualisierung

**Technologie-Stack:** React, Material-UI, Flask, Python, Predibase/Ollama LLM Integration, pandas, PDF-Verarbeitung

## Architektur & Workflow

**Frontend:** React mit Material-UI, mit Dashboard für Engagement-Management, Stichprobenverarbeitungsinterface mit Datei-Upload und LLM-Logs-Viewer für Audit-Trail.

**Backend:** Flask mit CORS-Unterstützung, Integration von Predibase/Ollama LLM-Modellen für Dokumentenverarbeitung, pandas für Excel-Verarbeitung und umfassendes Logging-System.

**Kern-Workflow:**
1. Upload von Excel-Stichprobendateien und entsprechenden PDF-Rechnungen
2. Geschäftsjahr-Validierung gegen konfigurierbare Stichtage
3. Textextraktion und Artikel-Matching mit LLM
4. Betragsvalidierung zwischen gebuchten und berechneten Werten
5. Reporting mit Audit-Trail

# DivideMix for noisy text classification

**Status:** Vollständig implementiert | **Kategorie:** Machine Learning / Natural Language Processing  
**Link zum Repo:** https://github.com/LiJunnan1992/DivideMix (Original) | https://github.com/MaximilianFeldhaus/DivideMix-for-noisy-text-classification (Meine Anwendung für Textdaten statt Bilder)

Eine Adaption der DivideMix-Methode für robuste Textklassifizierung in Anwesenheit von noisyLabels. Das Projekt überträgt die ursprünglich für Bildklassifizierung entwickelte DivideMix-Technik auf die Textverarbeitung mittels BERT-Transformern und ermöglicht somit effektives Training trotz unzuverlässiger Trainingslabels. Dieses Projekt entstammt originär aus meinem Seminar Advanced Topics in Machine Learning im Master Information Systems.

**Hauptfunktionen:**
- Robuste Textklassifizierung mit noisy Labels durch DivideMix-Algorithmus
- BERT-basierte Merkmalsextraktion statt CNN-Architekturen
- Textaugmentierung mit WordNet-Synonymen für bessere Generalisierung
- MixUp-Techniken auf Embedding-Ebene für Textdaten
- Automatische Erkennung und Behandlung von Clean/Noisy-Samples
- Unterstützung für symmetrische und asymmetrische Noise-Modi
- Dynamisches Batch-Padding für variable Textlängen

**Technologie-Stack:** Python, PyTorch, Transformers (BERT), NLTK/WordNet, scikit-learn, NumPy

## Architektur & Workflow

**Modellarchitektur:** BERT-Transformer für Sequenzklassifizierung mit angepasster DivideMix-Trainings-Pipeline für Text-spezifische Herausforderungen.

**Datenverarbeitung:** Tokenisierung mit BERT-Tokenizer, dynamisches Padding für Batch-Verarbeitung, WordNet-basierte Textaugmentierung zur Erhöhung der Datenvielfalt.

**Kern-Workflow:**
1. **Warmup-Phase:** Standardtraining auf allen Daten zur Modellinitialisierung
2. **Sample-Auswahl:** Gaussian Mixture Model zur Unterscheidung zwischen Clean- und Noisy-Samples
3. **Co-Training:** Zwei Netzwerke trainieren sich gegenseitig mit unterschiedlichen Datenaufteilungen
4. **MixUp-Regularisierung:** Lineare Interpolation auf Embedding-Ebene für bessere Generalisierung
5. **Semi-Supervised Learning:** Verwendung von Clean-Samples als gelabelte und Noisy-Samples als ungelabelte Daten
