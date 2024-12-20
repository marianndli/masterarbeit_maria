# Masterarbeit

# Automating Land Cover Classification for Biodiversity Assessment


Dieses Projekt analysiert und segmentiert Projekte von BioValues mit dem Ziel, spezifische Biotopflächenfaktoren zu klassifizieren. Verschiedene Modelle wie FLAIR, U-Net und DeepLabV3+ wurden verwendet, um die Qualität von Labeling und Modellergebnissen zu bewerten. Die Grundlage bilden hochauflösende Orthofotos und zugehörige Vektordaten.

---

## Verzeichnisstruktur

### Daten
- **Ortofotos_KantonZuerich**
  - Enthält Rasterdaten (GeoTIFFs) für die Projektdurchführung.
  - Unterordner:
    - `gemeindeZuerich`: GeoTIFFs der Gemeinde Zürich.
    - `sonstige`: Zusätzliche GeoTIFFs für BioValues-Projekte.
- **ShapefilesLiegenschaften_KantonZuerich**
  - Vektordaten zur Zuschneidung der Rasterdaten entsprechend der Projektgrenzen.
- **FLAIR_output**
  - Gespeicherte Konfigurationen und Ergebnisse der FLAIR-Experimente.
- **FLAIR_data**
  - Eingabedaten für FLAIR-Experimente.
- **Rasterdateien_RGB**
  - Rasterdaten für DeepLabV3+ Experiment D.
- **Rasterdateien_RGBI**
  - Grundlage für U-Net- und DeepLabV3+-Experimente (ohne Experiment D).
- **SegmentationMasks**
  - Masken für die Rasterdateien.
- **Projects_BioValues.xlsx**
  - Projektinformationen und relevante Metadaten.
- **labelmap.txt**
  - Zuordnung der Labels zu den jeweiligen Kategorien.

### Codes
- **Rasterdateien_zuschneiden.ipynb**
  - Schneidet Rasterdateien basierend auf Shapefiles zu.
- **Datenanalyse_Segmentierungsmasken_ProjectinfosBiovalues.ipynb**
  - Analysiert Segmentierungsmasken und liefert Ergebnisse für Kapitel 5.1 der Masterarbeit.
- **FLAIR_Model.ipynb**
  - Experiment FLAIR ohne Trainingsdaten. Ergebnisse in Kapitel 5.2.1.
- **FLAIROutputkonvertieren.ipynb**
  - Konvertiert FLAIR-Ergebnisse in ein CVAT-kompatibles Format (COCO).
- **FLAIR_mitTrainingsdaten.ipynb**
  - FLAIR-Experimente 1 bis 4. Ergebnisse in Kapitel 5.2.2.
- **U-Net.ipynb**
  - Alle U-Net-Experimente. Ergebnisse in Kapitel 5.2.3.
- **DeepLabV3+_BaseModel.ipynb**
  - DeepLabV3+ Experimente 1 bis 11 sowie Erweiterungen 9a-e b. Ergebnisse in Kapitel 5.2.4.1 bis 5.2.4.3.
- **DeepLabV3+_RGBI.ipynb**
  - DeepLabV3+ Experimente A-C. Ergebnisse in Kapitel 5.2.4.4 bis 5.2.4.6.
- **DeepLabV3+_RGB.ipynb**
  - DeepLabV3+ Experiment D. Ergebnisse in Kapitel 5.2.4.7.

---


