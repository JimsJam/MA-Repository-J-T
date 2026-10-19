# MA-Repository-J.-T.
Das Jupyter Notebook dient zur Simulation und Auswertung zweier parallel angeordneter periodischer Lochgitter. Es enthält Funktionen zur Erzeugung synthetischer Kamerabilder sowie zur Parameter- und Identifizierbarkeitsanalyse.

## Erste Schritte
### Voraussetzungen:
Für die Ausführung des Jupyter Notebooks werden folgende Komponenten benötigt:
- Python 3.10 oder neuer
- Jupyter Notebook zur Ausführung und Bearbeitung des Notebooks
- pip zur Installation der benötigten Python-Pakete
  
Folgende Python-Bibliotheken werden für die Simulation und Auswertung verwendet:
- numpy: Numerische Berechnungen und Verarbeitung von Arrays
- scipy: Wissenschaftliche Berechnungen und numerische Methoden
- matplotlib: Visualisierung der Simulationsergebnisse
- pandas: Verarbeitung und Auswertung tabellarischer Daten
- joblib: Unterstützung paralleler Berechnungen
- notebook und ipykernel: Ausführung des Jupyter Notebooks

Die benötigten Python-Pakete sind in der Datei requirements.txt aufgeführt.

### Installation:

1. Repository herunterladen
  
    Das Repository kann über Git geklont oder als ZIP-Datei heruntergeladen werden.
    
    Bei der Verwendung von Git wird das Repository über die Kommandozeile heruntergeladen:
    
    ```
    git clone <Repository-URL>
    cd MA-Repository-J-T
    ```
    
2. Python-Pakete installieren
   
    ```
    python -m pip install -r requirements.txt
    ```
     
3. Jupyter Notebook starten:
   
    ```
    jupyter notebook
    ```
   
Anschließend kann das gewünschte .ipynb-Notebook in der geöffneten Jupyter-Oberfläche ausgewählt und ausgeführt werden.

Die Installation der Pakete sollte in der Python-Umgebung erfolgen, die anschließend auch für das Notebook verwendet wird. Eine vorhandene virtuelle Umgebung kann dafür genutzt werden.

## Hinweise
### Funktionen
- grid_mask(): Erzeugt eine periodische binäre Gittermaske mit kreisförmigen Löchern.
- simulation(): Simuliert das Bild zweier gegeneinander verschobener Gitter. Optional können Gauß-Blur, Poisson- und Gauß-Rauschen sowie eine Gamma-Transformation angewendet werden.
- distance_function(): Berechnet den Bildfehler mit MSE, MAE oder NMSE.
- parallel_grid_search() und grid_search_topk(...): Durchsuchen Parameterkombinationen und liefern K-Kandidaten mit kleinem Bildfehler.
- plot_sensitivity_1d() und plot_sensitivity_2d(...): Visualisieren die Sensitivität gegenüber einzelnen oder mehreren Parametern.
- analyze_coarse_to_fine(): Wertet die Ergebnisse einer Coarse-to-Fine-Suche stufenweise aus.
- ctfs_multiple_runs(), evaluate_ctfs_runs(...) und final_summarize_ctfs_statistics(...): Führen mehrere Suchläufe zusammen und fassen deren Ergebnisse statistisch zusammen.

Die jeweiligen Übergabeparameter sind in den Docstrings der entsprechenden Funktionen erläutert.

### Ergebnisse und Dateien
- Die Funktionen liefern Listen zurück die bei aktiviertem save_csv zusätzlich als CSV-Datei gespeichert werden.
- Die Benennung der CSV-Datei kombiniert den selbst vergebenen Namen mit den jeweiligen Startwerten.
- Die statistischen Auswertungen werden entweder als Plots mit Matplotlib dargestellt oder durch zusätzliche Print-Ausgaben ergänzt.

###

