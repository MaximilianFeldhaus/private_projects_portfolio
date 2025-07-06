# Portfolio Privater Projekte

Willkommen zu meiner Sammlung privater Projekte. Dieses Repository dient als Präsentation meiner persönlichen Entwicklungsarbeit, Experimente und Nebenprojekte.

---

# Stichprobenassistent für Wirtschaftsprüfer

**Status:** In Bearbeitung | **Kategorie:** Financial Technology / Prüfungssoftware

Ein KI-gestütztes Stichproben-Tool, das die Rechnungsvalidierung durch Verarbeitung von Excel-Stichprobendateien und entsprechenden PDF-Rechnungen mit LLM Technologie automatisiert. Das Tool hilft dabei, manuelle Prüfungsarbeiten zu reduzieren und gleichzeitig Genauigkeit und Compliance-Standards zu gewährleisten.

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