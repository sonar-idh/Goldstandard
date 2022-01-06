# Datengrundlage OCR-Evaluation

Alle Dateien sind im TSV-Format.

Die Ordner mit Präfix "01_original_files" beinhalten die Datengrundlage auf der die intellektuelle Verbesserung durchgeführt wurde.
Die Ordner mit Präfix "02_ocr_corrected" beinhalten die intellektuell verbesserten Daten (Gold-Standard).
Die Ordner mit Suffix "-EL-NER" enthalten die Dateien nach eine (erneuten) Durchlauf der automatischen Entitätserkennung und -verlinkung auf Basis des Systems zum Stand September 2021 auf Basis der unverbesserten (01) bzw. verbesserten (02) Daten.

## Aufbau

| Spaltenbezeichnung | Beschreibung des Inhalts                                                                                         | Leerstellenmarkierung |
| :----------------- | :--------------------------------------------------------------------------------------------------------------- | :-------------------- |
| No.                | Nummerierung von Tokens in Sätzen. Intern genutzt von [neat](https://github.com/qurator-spk/neat).               | 0                     |
| TOKEN              | Das erkannte oder intellektuell verbesserte Token.                                                               |                       |
| NE-TAG             | Named-Entity-Tag. Beginn- bzw. Fortführungsmarkierung einer Zuweisung einer Named-Entity-Kategorie erster Stufe. | O                     |
| NE-EMB             | Embedded Named-Entity-Tag. Wie NE-TAG, nur Sub-Tag eines Teils eines NE-TAGs.                                    | O                     |
| ID                 | Liste der Q-IDs aus Wikipedia, die erkannt / vergeben wurden.  Trennungssymbol ist "\| "                         | -                     |
| url_id             | nicht genutzt                                                                                                    | 0                     |
| left               | Koordinate für Bildausschnitt in [neat](https://github.com/qurator-spk/neat)                                     |                       |
| right              | Koordinate für Bildausschnitt in [neat](https://github.com/qurator-spk/neat)                                     |                       |
| top                | Koordinate für Bildausschnitt in [neat](https://github.com/qurator-spk/neat)                                     |                       |
| bottom             | Koordinate für Bildausschnitt in [neat](https://github.com/qurator-spk/neat)                                     |                       |
| conf               | Liste der Konfidenzen je erkannter Q-ID (in Spalte ID). Komma-separiert. Nicht in allen Dateien vorhanden.       |                       |

## Zeitungsseiten
| Dateinamenpräfix                  | Zeitung                    | Datum      | Seite | Bemerkung                      |
| :-------------------------------- | :------------------------- | :--------- | ----: | :----------------------------- |
| 11614109_1882-05-01_1_1_001       | Neueste Mittheilungen      | 1882-05-01 |     1 |                                |
| 11614109_1886-06-22_5_67_001      | Neueste Mittheilungen      | 1886-06-22 |     1 |                                |
| 2436020X_1879-08-11_0_370_008     | Berliner Boersenzeitung    | 1879-08-11 |     8 | Abend-Ausgabe                  |
| 2436020X_1897-05-07_0_212_002     | Berliner Boersenzeitung    | 1897-05-07 |     2 | Abend-Ausgabe                  |
| 2436020X_1908-09-22_0_445_002     | Berliner Boersenzeitung    | 1908-09-22 |     2 |                                |
| 2436020X_1914-02-21_0_87_018      | Berliner Boersenzeitung    | 1914-02-21 |    18 |                                |
| 25128437_1882-09-23_0_0_002       | Teltower Kreisblat         | 1882-09-23 |     2 |                                |
| 25128437_1896-03-11_0_0_001       | Teltower Kreisblat         | 1896-03-11 |     1 |                                |
| 27058621_1936-09-11_0016_001      | Deutsches Nachrichtenbuero | 1936-09-11 |     1 | Mittags-und Nachmittagsausgabe |
| 27058621_1937-12-28_1748_001      | Deutsches Nachrichtenbuero | 1937-12-28 |     1 |                                |
| 27112366_1874-08-25_000_197_0_006 | Vossische Zeitung          | 1874-08-25 |     6 | Morgen-Ausgabe                 |
| 27112366_1903-05-07_000_211_1_013 | Vossische Zeitung          | 1903-05-07 |    13 | Morgen-Ausgabe                 |
| 27112366_1905-05-10_000_218_2_011 | Vossische Zeitung          | 1905-05-10 |    11 | Abend-Ausgabe                  |
| 27112366_1906-01-25_000_040_1_012 | Vossische Zeitung          | 1906-01-25 |    12 | Morgen-Ausgabe                 |
| 27646518_1888-10-28_17_550_015    | Berliner Tageblatt         | 1888-10-28 |    15 |                                |
| 27646518_1892-07-05_21_335_005    | Berliner Tageblatt         | 1892-07-05 |     5 | Abend-Ausgabe                  |
| 27646518_1897-05-05_26_225_020    | Berliner Tageblatt         | 1897-05-05 |    20 |                                |
| 27646518_1899-04-07_28_175_003    | Berliner Tageblatt         | 1899-04-07 |     3 |                                |
| 9838247_1868-02-19_0_0_001        | Provinzial Correspondenz   | 1868-02-19 |     1 |                                |
| 9838247_1876-12-06_0_0_001        | Provinzial Correspondenz   | 1876-12-06 |     1 |                                |