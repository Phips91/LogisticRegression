# LogisticRegression

#Projektname: Logistic Regression

Anleitung zum Betrieb des Codes: 
1. MyBinder über den BinderBatch öffnen
2. Nach dem öffnen des MyBinder, das Notebook

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/Phips91/LogisticRegression.git/HEAD)

Hier ist eine kurze Dokumentation zum gegebenen Code:

**Logistische Regression Projekt - Lösung**

In diesem Projekt wird ein logistisches Regressionsmodell entwickelt, um vorherzusagen, ob ein Nutzer auf eine Werbeanzeige auf einer Webseite geklickt hat oder nicht. Dies geschieht anhand von Nutzereigenschaften, die in einem Datensatz enthalten sind. Der Datensatz enthält die folgenden Merkmale:

- 'Daily Time Spent on Site': Die Zeit, die ein Nutzer täglich auf der Webseite verbringt (in Minuten).
- 'Age': Das Alter des Nutzers (in Jahren).
- 'Area Income': Das durchschnittliche Einkommen der Region des Nutzers.
- 'Daily Internet Usage': Die durchschnittliche tägliche Internetnutzungsdauer des Nutzers (in Minuten).
- 'Ad Topic Line': Die Überschrift der Werbeanzeige.
- 'City': Die Stadt des Nutzers.
- 'Male': Ob der Nutzer männlich ist (1) oder nicht (0).
- 'Country': Das Land des Nutzers.
- 'Timestamp': Die Zeit, zu der der Nutzer auf die Werbeanzeige geklickt oder das Fenster geschlossen hat.
- 'Clicked on Ad': Ob der Nutzer auf die Werbeanzeige geklickt hat (1) oder nicht (0).

**Libraries installieren**

Zuerst werden die erforderlichen Python-Bibliotheken installiert, darunter numpy, pandas, seaborn und scikit-learn. Dies geschieht mithilfe von pip, dem Paketmanager für Python.

**Libraries importieren**

Nach der Installation der Bibliotheken werden sie importiert, um in diesem Projekt verwendet zu werden. Dies umfasst pandas für Datenmanipulation, numpy für numerische Berechnungen, matplotlib und seaborn für die Datenvisualisierung sowie scikit-learn für das Trainieren und Auswerten des logistischen Regressionsmodells.

**Die Daten**

Die advertising.csv-Datei wird eingelesen und in einen DataFrame namens "ad_data" geladen. Ein erster Blick auf die Daten erfolgt mithilfe der Methode "head()", um die ersten Zeilen des DataFrames anzuzeigen. Anschließend werden die Methoden "info()" und "describe()" auf "ad_data" angewendet, um grundlegende Informationen über die Daten und statistische Kennzahlen zu erhalten.

**Explorative Datensanalyse**

In diesem Abschnitt wird die explorative Datenanalyse mithilfe der Seaborn-Bibliothek durchgeführt. Es werden verschiedene Diagramme erstellt, um Beziehungen und Muster in den Daten zu erkunden:

- Ein Histogramm des Alters (Age) wird erstellt, um die Verteilung der Altersgruppen zu visualisieren.
- Ein Jointplot zeigt die Beziehung zwischen "Area Income" und "Age".
- Ein weiteres Jointplot zeigt die Kernel Density Estimation (KDE) der Verteilung von "Daily Time Spent on Site" gegen "Age".
- Ein letztes Jointplot stellt "Daily Time Spent On Site" gegen "Daily Internet Usage" dar, um deren Beziehung zu untersuchen.
- Schließlich wird ein Pairplot erstellt, wobei "Clicked on Ad" als Hue verwendet wird, um die Beziehung zwischen den Merkmalen und der Zielvariable zu visualisieren.

**Logistische Regression**

In diesem Abschnitt werden die Daten in Trainings- und Testsets aufgeteilt, um ein logistisches Regressionsmodell zu trainieren. Die ausgewählten Merkmale (Spalten) sind "Daily Time Spent on Site", "Age", "Area Income", "Daily Internet Usage" und "Male". Die Zielvariable ist "Clicked on Ad".

- Zuerst wird die Methode "train_test_split" aus scikit-learn verwendet, um die Daten aufzuteilen.
- Dann wird ein leeres logistisches Regressionsmodell erstellt und auf das Trainingssatz angepasst.

**Vorhersagen und Auswertung**

Nun werden Vorhersagen für die Testdaten gemacht und ein Klassifizierungsreport für das Modell erstellt, um die Leistung des Modells zu bewerten. Dieser Report enthält Metriken wie Genauigkeit, Präzision, Rückruf und F1-Score für jede Klasse ("geklickt" oder "nicht geklickt"). Die Ausgabe des Klassifizierungsreports wird auf der Konsole angezeigt, um die Modellleistung zu bewerten.

Das Ziel des Projekts ist es, ein Modell zu entwickeln, das anhand von Nutzereigenschaften vorhersagen kann, ob ein Nutzer auf eine Werbeanzeige klicken wird oder nicht. Der Klassifizierungsreport bietet Einblicke in die Leistung des Modells bei dieser Aufgabe.
