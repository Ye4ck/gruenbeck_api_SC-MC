# Grünbeck softliQ:SC – Vollständige Parameterliste

> **Zugriff:** `R` = Nur Lesen · `R/W` = Lesen & Schreiben · `R/W (Code)` = Code-geschützt · `?` = Unbekannt

<details>
<summary> API-Referenz </summary>
  
```
POST http://[IP]/mux_http/
Content-Type: application/x-www-form-urlencoded

Wert lesen:
id=0000&show=D_D_1~

Mehrere Werte lesen (max 1000 Byte Request+Response):
id=0000&show=D_D_1|D_A_1_1|D_Y_5~

Wert schreiben + lesen:
id=0000&edit=D_D_1>20&show=D_D_1~

Mit Zugangscode:
id=0000&code=005&show=D_A_1_1~
```

</details>

<details>
<summary> Codes </summary>

**Codes:** 
- 005 = Austauscher-Details & Ein-/Ausgang  
- 121 = Hydraulische Werte
- 142 = Kontrollparameter
- 189 = Fehlerspeicher Reset
- 245 = Fehlerspeicher & Zählerstände lesen
- 290 = Impulsraten & Anlagen-Datensatz
- 302 = Schrittabstände

</details>
## ⚙️ Einstellungen (Schreib- & Lesezugriff)

| Parameter-ID | Bezeichnung | Einheit | Zugriff | Kommentar / Werte |
|:---|:---|:---|:---:|:---|
| `D_D_1` | Rohwasserhärte | °dH | R/W |  |
| `D_D_2` | Sollwert Weichwasserhärte | °dH | R/W |  |
| `D_A_4_1` | Name Installateur | String | R/W |  |
| `D_A_4_2` | Tel Installateur | String | R/W |  |
| `D_A_4_3` | E-Mail Installateur | String | R/W |  |
| `D_C_1_1` | Sprache | Int | R/W | 0=DE, 1=EN, 2=FR, 3=IT, 4=NL, 5=RU, 6=ES, 7=CN |
| `D_C_2_1` | Härteeinheit | Int | R/W | 0=°dH, 1=°f, 2=°e, 3=ppm, 4=mol/m³ |
| `D_C_4_1` | Regenerationszeitpunkt | Int | R/W | 0=automatisch, 1=fest |
| `D_C_4_2` | Uhrzeit | HH:MM | R/W |  |
| `D_C_4_3` | Startzeit Regeneration 1 | HH:MM | R/W |  |
| `D_C_4_4` | Startzeit Regeneration 2 | HH:MM | R/W | nur MC |
| `D_C_4_5` | Startzeit Regeneration 3 | HH:MM | R/W | nur MC |
| `D_C_5_1` | Power Modus / Arbeitsweise | Int | R/W | 0=eco, 1=power, 2=comfort (MC), 3=individual (MC) |
| `D_C_5_2` | Datum | TT.MM.JJJJ | R/W |  |
| `D_C_5_3` | Auto Sommer-/Winterzeit | Int | R/W | 0=nein, 1=ja |
| `D_C_6_1` | Aktives Display im Standby | Int | R/W | 0=deaktiviert, 1=aktiviert |
| `D_C_6_3` | Mo Arbeitsweise | Int | R/W | nur bei Arbeitsweise=3 |
| `D_C_6_4` | Di Arbeitsweise | Int | R/W | nur bei Arbeitsweise=3 |
| `D_C_6_5` | Mi Arbeitsweise | Int | R/W | nur bei Arbeitsweise=3 |
| `D_C_6_6` | Do Arbeitsweise | Int | R/W | nur bei Arbeitsweise=3 |
| `D_C_6_7` | Fr Arbeitsweise | Int | R/W | nur bei Arbeitsweise=3 |
| `D_C_6_8` | Sa Arbeitsweise | Int | R/W | nur bei Arbeitsweise=3 |
| `D_C_6_9` | So Arbeitsweise | Int | R/W | nur bei Arbeitsweise=3 |
| `D_C_7_1` | Soll Service Intervalldauer | d | R/W |  |
| `D_C_8_1` | LED Funktion | Int | R/W | 0=deakt., 1=Störung, 2=Bed.+Stör., 3=Wasser+Bed.+Stör., 4=Dauerhaft (nicht SC18) |
| `D_C_8_2` | LED blinkt bei Salz-Vorwarnung | Int | R/W | 0=nein, 1=ja (nicht SC18) |

## 📧 E-Mail Einstellungen (Base64 verschlüsselt)

| Parameter-ID | Bezeichnung | Einheit | Zugriff | Kommentar / Werte |
|:---|:---|:---|:---:|:---|
| `D_Y_8_1_1` | E-Mail Adresse 1 (Meldung) | String | R/W | Base64 |
| `D_Y_8_1_2` | E-Mail Adresse 2 (Meldung) | String | R/W | Base64 |
| `D_Y_8_1_3` | E-Mail Adresse 3 (Meldung) | String | R/W | Base64 |
| `D_Y_8_2` | SMTP-Server | String | R/W | Base64 |
| `D_Y_8_3` | Port-Nr. | Int | R/W |  |
| `D_Y_8_4` | Benutzername | String | R/W | Base64 |
| `D_Y_8_5` | Passwort | String | R/W | Base64 |
| `D_Y_8_6` | E-Mail-Adresse | String | R/W | Base64 |
| `D_Y_8_7` | Telefonnummer | String | R/W | Base64 |
| `D_Y_8_8` | Nachname | String | R/W | Base64 |
| `D_Y_8_9` | Text Störmeldeweiterleitung | String | R/W | Base64 |
| `D_Y_8_10` | Test-E-Mail versenden | Int | R/W | 0=nein, 1=ja (Button) |
| `D_Y_8_11` | Ergebnis letzter E-Mail Versand | Int | R | 0=keine, 1=OK, 2=Daten fehlerhaft, 3=kein Internet |
| `D_Y_8_12` | Zeitpunkt letzter Mail-Sendeversuch |  | R |

## 🔧 Aktionen

| Parameter-ID | Bezeichnung | Einheit | Zugriff | Kommentar / Werte |
|:---|:---|:---|:---:|:---|
| `D_B_1` | Manuelle Regeneration starten / Regeneration aktiv |  | R/W | Button |
| `D_E_1` | Inbetriebnahme starten |  | R/W | Button |
| `D_M_3_3` | Fehlerspeicher zurücksetzen |  | R/W | Code 189 · Button |
| `D_Y_12` | Reset Netzwerkparameter |  | R/W | Button |

## 📊 Allgemeine Sensoren (Lesezugriff)

| Parameter-ID | Bezeichnung | Einheit | Zugriff | Kommentar / Werte |
|:---|:---|:---|:---:|:---|
| `D_A_1_1` | Aktueller Durchfluss | m³/h | R | Aktualwerte (auto-refresh 2s) |
| `D_A_1_2` | Restkapazität | m³ | R |  |
| `D_A_1_3` | Aktuelle Anlagenkapazität | m³×°dH | R |  |
| `D_A_1_6` | Ist-/Sollwert Weichwasserhärte | °dH | R | Istwert bei Durchfluss>0, Sollwert bei =0 |
| `D_A_1_7` | Gesamtdurchfluss Anlage | m³/h | R | MC: 0°Wasser + Verschneidung |
| `D_A_2_1` | Restdauer/-menge akt. Reg.Schritt |  | R |  |
| `D_A_2_2` | Restdauer Wartungsintervall | d | R |  |
| `D_A_2_3` | Salzreichweite | d | R | nur SC23 |  |
| `D_A_3_1` | Zeit seit letzter Regeneration | h | R |  |
| `D_A_3_2` | Prozentsatz laufende Regeneration | % | R |  |
| `D_Y_1` | Wasserverbrauch pro Tag | l | R |  |
| `D_Y_3` | Salzverbrauch pro Jahr | kg | R |  |
| `D_Y_5` | Aktueller Regenerationsschritt | Int | R | 0=keine, 1=Soletank, 2=Besalzen, 3=Verdrängen, 4=Rückspülen, 5=Auswaschen |
| `D_Y_6` | Software-Version | String | R |  |
| `D_Y_7` | Inbetriebnahme-Datum | TT.MM.JJJJ | R |  |
| `D_Y_9` | Aktueller Index Inbetriebnahme-Programm |  | R |
| `D_Y_9_8` | Countdown Zeit Entlüftungsprogramm |  | R |
| `D_Y_9_24` | Restdauer Testregeneration |  | R | |
| `D_Y_10_1` | Aktuelle Restkapazität AT1 | % | R |  |
| `D_Y_10_2` | Aktuelle Restkapazität AT2 | % | R | nicht bei SC |
| `D_Y_13` | Austauscher in Betrieb | Int | R | SC: 0=gestört,1=OK / MC: 0=beide gestört,1=AT1,2=AT2,3=beide |
| `D_Y_14` | Voraussichtl. nächste Regeneration | TT.MM.JJJJ HH:MM | R |  |
| `D_K_1` | Zähler Regenerationen | Int | R |  |
| `D_K_2` | Zähler Weichwassermenge | m³ | R |  |

## 📈 Wasserverbrauch Historie (D_Y_2_x)

| Parameter-ID | Bezeichnung | Einheit | Zugriff | Kommentar / Werte |
|:---|:---|:---|:---:|:---|
| `D_Y_2_1` | Wasserverbrauch vor 01 Tag | l | R |  |
| `D_Y_2_2` | Wasserverbrauch vor 02 Tagen | l | R |  |
| `D_Y_2_3` | Wasserverbrauch vor 03 Tagen | l | R |  |
| `D_Y_2_4` | Wasserverbrauch vor 04 Tagen | l | R |  |
| `D_Y_2_5` | Wasserverbrauch vor 05 Tagen | l | R |  |
| `D_Y_2_6` | Wasserverbrauch vor 06 Tagen | l | R |  |
| `D_Y_2_7` | Wasserverbrauch vor 07 Tagen | l | R |  |
| `D_Y_2_8` | Wasserverbrauch vor 08 Tagen | l | R |  |
| `D_Y_2_9` | Wasserverbrauch vor 09 Tagen | l | R |  |
| `D_Y_2_10` | Wasserverbrauch vor 10 Tagen | l | R |  |
| `D_Y_2_11` | Wasserverbrauch vor 11 Tagen | l | R |  |
| `D_Y_2_12` | Wasserverbrauch vor 12 Tagen | l | R |  |
| `D_Y_2_13` | Wasserverbrauch vor 13 Tagen | l | R |  |
| `D_Y_2_14` | Wasserverbrauch vor 14 Tagen | l | R |  |
| `D_Y_2_15` | Wasserverbrauch vor 15 Tagen | l | R |  |
| `D_Y_2_16` | Wasserverbrauch vor 16 Tagen | l | R |  |
| `D_Y_2_17` | Wasserverbrauch vor 17 Tagen | l | R |  |
| `D_Y_2_18` | Wasserverbrauch vor 18 Tagen | l | R |  |
| `D_Y_2_19` | Wasserverbrauch vor 19 Tagen | l | R |  |
| `D_Y_2_20` | Wasserverbrauch vor 20 Tagen | l | R |  |
| `D_Y_2_21` | Wasserverbrauch vor 21 Tagen | l | R |  |
| `D_Y_2_22` | Wasserverbrauch vor 22 Tagen | l | R |  |
| `D_Y_2_23` | Wasserverbrauch vor 23 Tagen | l | R |  |
| `D_Y_2_24` | Wasserverbrauch vor 24 Tagen | l | R |  |
| `D_Y_2_25` | Wasserverbrauch vor 25 Tagen | l | R |  |
| `D_Y_2_26` | Wasserverbrauch vor 26 Tagen | l | R |  |
| `D_Y_2_27` | Wasserverbrauch vor 27 Tagen | l | R |  |

## 📈 Salzverbrauch Historie (D_Y_3_x)

| Parameter-ID | Bezeichnung | Einheit | Zugriff | Kommentar / Werte |
|:---|:---|:---|:---:|:---|
| `D_Y_3_1` | Salzverbrauch vor 1 Tag | kg | R |  |
| `D_Y_3_2` | Salzverbrauch vor 2 Tagen | kg | R |  |
| `D_Y_3_3` | Salzverbrauch vor 3 Tagen | kg | R |  |
| `D_Y_3_4` | Salzverbrauch vor 4 Tagen | kg | R |  |
| `D_Y_3_5` | Salzverbrauch vor 5 Tagen | kg | R |  |
| `D_Y_3_6` | Salzverbrauch vor 6 Tagen | kg | R |  |
| `D_Y_3_7` | Salzverbrauch vor 7 Tagen | kg | R |  |
| `D_Y_3_8` | Salzverbrauch vor 8 Tagen | kg | R |  |
| `D_Y_3_9` | Salzverbrauch vor 9 Tagen | kg | R |  |
| `D_Y_3_10` | Salzverbrauch vor 10 Tagen | kg | R |  |
| `D_Y_3_11` | Salzverbrauch vor 11 Tagen | kg | R |  |
| `D_Y_3_12` | Salzverbrauch vor 12 Tagen | kg | R |  |
| `D_Y_3_13` | Salzverbrauch vor 13 Tagen | kg | R |  |
| `D_Y_3_14` | Salzverbrauch vor 14 Tagen | kg | R |  |

## 📈 Regenerationszeit Historie (D_Y_4_x)

| Parameter-ID | Bezeichnung | Einheit | Zugriff | Kommentar / Werte |
|:---|:---|:---|:---:|:---|
| `D_Y_4_1` | Letzte Regeneration 1 (neueste Regeneration) |  | R |  |
| `D_Y_4_2` | Letzte Regeneration 2 |  | R |  |
| `D_Y_4_3` | Letzte Regeneration 3 |  | R |  |
| `D_Y_4_4` | Letzte Regeneration 4 |  | R |  |
| `D_Y_4_5` | Letzte Regeneration 5 |  | R |  |
| `D_Y_4_6` | Letzte Regeneration 6 |  | R |  |
| `D_Y_4_7` | Letzte Regeneration 7 |  | R |  |
| `D_Y_4_8` | Letzte Regeneration 8 |  | R |  |
| `D_Y_4_9` | Letzte Regeneration 9 |  | R |  |
| `D_Y_4_10` | Letzte Regeneration 10 |  | R |  |
| `D_Y_4_11` | Letzte Regeneration 11 |  | R |  |
| `D_Y_4_12` | Letzte Regeneration 12 |  | R |  |
| `D_Y_4_13` | Letzte Regeneration 13 |  | R |  |
| `D_Y_4_14` | Letzte Regeneration 14 (älteste Regeneration) |  | R |  |

## 📈 Regeneration Restkapazitäten (D_A_3_2_x)

| Parameter-ID | Bezeichnung | Einheit | Zugriff | Kommentar / Werte |
|:---|:---|:---|:---:|:---|
| `D_A_3_2_1` | Regeneration 1 – Restkapazität | % | R |  |
| `D_A_3_2_2` | Regeneration 2 – Restkapazität | % | R |  |
| `D_A_3_2_3` | Regeneration 3 – Restkapazität | % | R |  |
| `D_A_3_2_4` | Regeneration 4 – Restkapazität | % | R |  |
| `D_A_3_2_5` | Regeneration 5 – Restkapazität | % | R |  |
| `D_A_3_2_6` | Regeneration 6 – Restkapazität | % | R |  |
| `D_A_3_2_7` | Regeneration 7 – Restkapazität | % | R |  |
| `D_A_3_2_8` | Regeneration 8 – Restkapazität | % | R |  |
| `D_A_3_2_9` | Regeneration 9 – Restkapazität | % | R |  |
| `D_A_3_2_10` | Regeneration 10 – Restkapazität | % | R |  |
| `D_A_3_2_11` | Regeneration 11 – Restkapazität | % | R |  |
| `D_A_3_2_12` | Regeneration 12 – Restkapazität | % | R |  |
| `D_A_3_2_13` | Regeneration 13 – Restkapazität | % | R |  |
| `D_A_3_2_14` | Regeneration 14 – Restkapazität | % | R |  |
| `D_A_3_4` | Letzte Regeneration AT2 | TT.MM.JJJ HH:MM | R | nur MC32 |
| `D_A_3_5` | Letzte Regeneration AT2 übrig | % | R | nur MC32 |

## 🌐 Netzwerk

| Parameter-ID | Bezeichnung | Einheit | Zugriff | Kommentar / Werte |
|:---|:---|:---|:---:|:---|
| `D_C_3_1` | WLAN deaktivieren |  | R/W | Button |
| `D_C_3_2` | WLAN suchen |  | R/W | Button |
| `D_C_3_6_1` | WLAN IP-Adresse | String | R |  |
| `D_C_3_6_2` | Default Gateway | String | R |  |
| `D_C_3_6_3` | Primary DNS | String | R |  |
| `D_C_3_6_4` | Secondary DNS | String | R |  |
| `D_C_3_6_5` | WLAN Status | Int | R | 0=nicht verbunden, 1=verbunden |
| `D_C_3_7_1` | Access Point IP-Adresse | String | R |  |
| `D_C_3_7_2` | Access Point SSID | String | R |  |
| `D_C_3_7_3` | Access Point Status | Int | R | 0=nicht verbunden, 1=verbunden |

## 🔌 Programmierbarer Ein-/Ausgang (Code 005)

| Parameter-ID | Bezeichnung | Einheit | Zugriff | Kommentar / Werte |
|:---|:---|:---|:---:|:---|
| `D_G_1` | Funktion potentialfreier Kontakt | Int | R/W (Code) | 0=N.C., 1=N.O., 2=Reg.-Meldung, 3=Reg. Wasserförderpumpe, 4=Freigabe Resthärtekontrolle, 5=Störmeldeweiterleitung |
| `D_G_2` | Verzögerung Resthärtekontrolle | Min. | R/W (Code) |  |
| `D_G_3` | Funktion Programmierbarer Eingang | Int | R/W (Code) | 0=Reg. Auslösung, 1=Reg. Sperre, 2=Störmeldeweiterleitung |

## 🛡️ Kontrollparameter (Code 142)

| Parameter-ID | Bezeichnung | Einheit | Zugriff | Kommentar / Werte |
|:---|:---|:---|:---:|:---|
| `D_H_2` | Reaktion auf Netzausfall | Int | R/W (Code) | 0=keine, 2=Meldetext+Störmeldekontakt, 3=+Regeneration |
| `D_H_3` | Anlage überlastet | Int | R/W (Code) | 0=keine Meldung, 1=Meldetext+Störmeldekontakt |
| `D_H_4` | Überwachung Desinfektion |  | R/W (Code) | Button |
| `D_H_5` | Chlorzelle |  | R/W (Code) | Button aktivieren/deaktivieren |
| `D_H_6` | Überwachungszeit WZ Regeneration | Min. | R/W (Code) |  |
| `D_H_7` | Überwachungszeit Besalzen | Min. | R/W (Code) |  |
| `D_H_8` | Tagesabstand Zwangsregeneration | d | R/W (Code) |  |
| `D_H_9` | Überwachung Nenndurchfluss |  | R/W (Code) | Button |
| `D_H_10` | Reg.zeitpunkt & Kapazität über | d | R/W (Code) |  |
| `D_H_11` | Restkapazität-Grenzwert | % | R/W (Code) |  |

## 📋 Anlagen-Datensatz (Code 005 & 290)

| Parameter-ID | Bezeichnung | Einheit | Zugriff | Kommentar / Werte |
|:---|:---|:---|:---:|:---|
| `D_F_1` | Regenerationszeitpunkt (erweitert) | Int | R/W (Code) | 0=Auto, 1=Fest, 2=Wochenzeitschaltuhr |
| `D_F_2` | Wochentag | Int | R/W (Code) | 1=Mo, 2=Di, 3=Mi, 4=Do, 5=Fr, 6=Sa, 7=So |
| `D_F_3_1` | Wochenzeitschaltuhr Montag |  | R/W (Code) |  |
| `D_F_3_2` | Wochenzeitschaltuhr Dienstag |  | R/W (Code) |  |
| `D_F_3_3` | Wochenzeitschaltuhr Mittwoch |  | R/W (Code) |  |
| `D_F_3_4` | Wochenzeitschaltuhr Donnerstag |  | R/W (Code) |  |
| `D_F_3_5` | Wochenzeitschaltuhr Freitag |  | R/W (Code) |  |
| `D_F_3_6` | Wochenzeitschaltuhr Samstag |  | R/W (Code) |  |
| `D_F_3_7` | Wochenzeitschaltuhr Sonntag |  | R/W (Code) |  |
| `D_F_4` | Anlagentyp | Int | R/W (Code) | 0=Einzelanlage frei, 1=SC18, 2=SC23 Code 290|
| `D_F_5` | WZ Weichwasser Impulsrate | l/Imp | R (Code) | Code 290 |
| `D_F_6` | WZ Regeneration Impulsrate | l/Imp | R (Code) | Code 290 |
| `D_F_8` | Referenzposition Transferventil suchen |  | R/W (Code) | Button |
| `D_F_9` | Referenzposition Regenerationsventil suchen |  | R/W (Code) | Button |

## 🔧 Hydraulische Werte (Code 121)

| Parameter-ID | Bezeichnung | Einheit | Zugriff | Kommentar / Werte |
|:---|:---|:---|:---:|:---|
| `D_I_1` | Dauer Reg.Schritt Verdrängen | Min. | R/W (Code) |  |
| `D_I_2` | Menge Reg.Schritt Rückspülen | l | R/W (Code) |  |
| `D_I_3` | Menge Reg.Schritt Erstfiltrat | l | R/W (Code) |  |
| `D_I_4` | Menge Reg.Schritt Auswaschen | l | R/W (Code) |  |
| `D_I_5` | Min. Nachspeise Soletank kl. Kapazität | l | R/W (Code) |  |
| `D_I_6` | Max. Nachspeise Soletank kl. Kapazität | l | R/W (Code) |  |
| `D_I_7` | Min. Nachspeise Soletank gr. Kapazität | l | R/W (Code) |  |
| `D_I_8` | Max. Nachspeise Soletank gr. Kapazität | l | R/W (Code) |  |
| `D_I_9` | Maximaldauer Salztank füllen / Erstfiltrat | Min. | R/W (Code) |  |
| `D_I_10` | Endfrequenz Regenerationsventil | Hz | R/W (Code) |  |
| `D_I_11` | Endfrequenz Transferventil | Hz | R/W (Code) |  |
| `D_I_12` | Endfrequenz Referenzpunktsuche | Hz | R/W (Code) |  |
| `D_I_13` | Kapazitätsreserve Eco | % | R/W (Code) |  |
| `D_I_14` | Kapazitätsreserve Power | % | R/W (Code) |  |
| `D_I_15` | Nenndurchfluss | m³/h | R/W (Code) |  |
| `D_I_16` | WZ Weichwasser Impulsrate | l/Imp | R/W (Code) |  |
| `D_I_17` | WZ Regeneration Impulsrate | l/Imp | R/W (Code) |  |
| `D_I_18` | Chlorstrom Sollwert | mA | R (Code) |  |
| `D_I_20` | Ladung | mAmin | R/W (Code) |  |

## 📐 Schrittabstände (Code 302)

| Parameter-ID | Bezeichnung | Einheit | Zugriff | Kommentar / Werte |
|:---|:---|:---|:---:|:---|
| `D_J_1` | Schritte Referenzpunkt → Auswaschen | Steps | R/W (Code) |  |
| `D_J_3` | Schritte Auswaschen → Betrieb | Steps | R/W (Code) |  |
| `D_J_4` | Schritte Betrieb → Soletank füllen | Steps | R/W (Code) |  |
| `D_J_5` | Schritte Soletank füllen → Besalzen | Steps | R/W (Code) |  |
| `D_J_6` | Schritte Besalzen → Verdrängen | Steps | R/W (Code) |  |
| `D_J_7` | Schritte Verdrängen → Rückspülen | Steps | R/W (Code) |  |
| `D_J_8` | Schritte Rückspülen → Umkehrposition | Steps | R/W (Code) |  |
| `D_J_9` | Schritte Referenzpunktsuche | Steps | R/W (Code) |  |

## 🔒 Zählerstände & Durchfluss-Details (Code 245)

| Parameter-ID | Bezeichnung | Einheit | Zugriff | Kommentar / Werte |
|:---|:---|:---|:---:|:---|
| `D_K_3` | Durchfluss Spitzenwert | m³/h | R (Code) | nur MC32: Parallelbetrieb |
| `D_K_4` | Zeitzähler Nenndurchfluss überschritten | h | R (Code) |  |
| `D_K_5` | Chlorstrom | mA | R (Code) | |
| `D_K_6` | Schrittanzeige Transferventil | Steps | R (Code) | |
| `D_K_7` | Schrittanzeige Regenerationsventil | Steps | R (Code) |  |
| `D_K_8` | Verbrauchskapazitätszahl | m³×°dH | R (Code) |  |
| `D_K_9` | Durchschnittsverbrauch letzten 3 Tage | m³ | R (Code) |  |
| `D_K_11` | Parameter mit letzter Einstellungsänderung |  | R (Code) | |
| `D_K_14` | Spitzenwert AT1 | m³/h | R (Code) |  |
| `D_K_15` | Überschreitung Nenndurchfluss AT1 | Min. | R (Code) |  |
| `D_K_16` | Spitzenwert AT2 | m³/h | R (Code) | nur MC32 |
| `D_K_17` | Überschreitung Nenndurchfluss AT2 | Min. | R (Code) | nur MC32 |

## 🔒 Wassermengen (Code 005)

| Parameter-ID | Bezeichnung | Einheit | Zugriff | Kommentar / Werte |
|:---|:---|:---|:---:|:---|
| `D_K_18` | Weichwassermenge AT1 | m³ | R (Code) |  |
| `D_K_19` | Weichwassermenge AT2 | m³ | R (Code) | nur MC32 |
| `D_K_20` | Rohwassermenge Verschneidung | m³ | R (Code) | nur MC32 |
| `D_K_21` | Nachspeisemenge | l | R (Code) |  |

## 🔒 Austauscher 2 Details – nur MC32 (Code 005)

| Parameter-ID | Bezeichnung | Einheit | Zugriff | Kommentar / Werte |
|:---|:---|:---|:---:|:---|
| `D_A_1_4` | Aktueller Durchfluss AT2 | m³ | R (Code) |  |
| `D_A_1_5` | Restkapazität AT2 | m³×°dH | R (Code) |  |
| `D_A_1_8` | Kapazitätszahl AT2 | m³×°dH | R (Code) |  |
| `D_A_1_9` | Aktueller Durchfluss Verschneidung | m³ | R (Code) |  |
| `D_A_2_4` | Restzeit/-menge Reg.Schritt AT2 | l oder min | R (Code) |  |

## ⚠️ Fehlerspeicher (D_K_10_x, Code 245)

| Parameter-ID | Bezeichnung | Einheit | Zugriff | Kommentar / Werte |
|:---|:---|:---|:---:|:---|
| `D_K_10_1` | Fehlerspeicher (1) |  | R (Code) | 0=kein Fehler |
| `D_K_10_2` | Fehlerspeicher (2) |  | R (Code) | 0=kein Fehler |
| `D_K_10_3` | Fehlerspeicher (3) |  | R (Code) | 0=kein Fehler |
| `D_K_10_4` | Fehlerspeicher (4) |  | R (Code) | 0=kein Fehler |
| `D_K_10_5` | Fehlerspeicher (5) |  | R (Code) | 0=kein Fehler |
| `D_K_10_6` | Fehlerspeicher (6) |  | R (Code) | 0=kein Fehler |
| `D_K_10_7` | Fehlerspeicher (7) |  | R (Code) | 0=kein Fehler |
| `D_K_10_8` | Fehlerspeicher (8) |  | R (Code) | 0=kein Fehler |
| `D_K_10_9` | Fehlerspeicher (9) |  | R (Code) | 0=kein Fehler |
| `D_K_10_10` | Fehlerspeicher (10) |  | R (Code) | 0=kein Fehler |
| `D_K_10_11` | Fehlerspeicher (11) |  | R (Code) | 0=kein Fehler |
| `D_K_10_12` | Fehlerspeicher (12) |  | R (Code) | 0=kein Fehler |
| `D_K_10_13` | Fehlerspeicher (13) |  | R (Code) | 0=kein Fehler |
| `D_K_10_14` | Fehlerspeicher (14) |  | R (Code) | 0=kein Fehler |
| `D_K_10_15` | Fehlerspeicher (15) |  | R (Code) | 0=kein Fehler |
| `D_K_10_16` | Fehlerspeicher (16) |  | R (Code) | 0=kein Fehler |




**Bekannte Codes:** 005 = Austauscher-Details & Ein-/Ausgang · 121 = Hydraulische Werte · 142 = Kontrollparameter · 189 = Fehlerspeicher Reset · 245 = Fehlerspeicher & Zählerstände lesen · 290 = Impulsraten & Anlagen-Datensatz · 302 = Schrittabstände

**Hinweis:** Min. 15 Sekunden Abstand zwischen Anfragen. Max 1000 Byte pro Request+Response.
