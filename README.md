
# Grünbeck softliQ – Parameterliste für softliQ SC/MC

> **Zugriff:** R = Nur Lesen, R/W = Lesen & Schreiben, R (Code) = Lesen mit Code 005, ? = Unbekannt


## ⚙️ Einstellungen (Schreib- & Lesezugriff)

| Parameter-ID | Bezeichnung | Erwarteter Wert | Zugriff | Kommentar / Werte |
|:---|:---|:---|:---:|:---|
| `D_D_1` | Rohwasserhärte | Double [°dH] | R/W |  |
| `D_D_2` | Sollwert Weichwasserhärte | Double [°dH] | R/W |  |
| `D_A_4_1` | Name Installateur | String | R/W |  |
| `D_A_4_2` | Tel Installateur | String | R/W |  |
| `D_A_4_3` | E-Mail Installateur | String | R/W |  |
| `D_C_1_1` | Sprache | Int | R/W | 0=DE, 1=EN, 2=FR, 3=IT, 4=NL, 5=RU, 6=ES, 7=CN |
| `D_C_2_1` | Härteeinheit | Int | R/W | 0=°dH, 1=°f, 2=°e, 3=ppm, 4=mol/m³ |
| `D_C_4_1` | Regenerationszeitpunkt | Int | R/W | 0=automatisch, 1=fest |
| `D_C_4_2` | Uhrzeit | String (XX:XX) | R/W |  |
| `D_C_4_3` | Startzeit Regeneration 1 | String (XX:XX) | R/W |  |
| `D_C_4_4` | Startzeit Regeneration 2 | String (XX:XX) | R/W | nur softliQ:MC |
| `D_C_4_5` | Startzeit Regeneration 3 | String (XX:XX) | R/W | nur softliQ:MC |
| `D_C_5_1` | Power Modus / Arbeitsweise | Int | R/W | 0=eco, 1=power, 2=comfort (MC), 3=individual (MC) |
| `D_C_5_2` | Datum | String (TT.MM.JJJJ) | R/W |  |
| `D_C_5_3` | Auto Sommer-/Winterzeit | Int | R/W | 0=nein, 1=ja |
| `D_C_6_1` | Aktives Display im Standby | Int | R/W | 0=deaktiviert, 1=aktiviert |
| `D_C_6_3` | Mo Arbeitsweise | Int | R/W | nur bei Arbeitsweise=3 (individual) |
| `D_C_6_4` | Di Arbeitsweise | Int | R/W | nur bei Arbeitsweise=3 (individual) |
| `D_C_6_5` | Mi Arbeitsweise | Int | R/W | nur bei Arbeitsweise=3 (individual) |
| `D_C_6_6` | Do Arbeitsweise | Int | R/W | nur bei Arbeitsweise=3 (individual) |
| `D_C_6_7` | Fr Arbeitsweise | Int | R/W | nur bei Arbeitsweise=3 (individual) |
| `D_C_6_8` | Sa Arbeitsweise | Int | R/W | nur bei Arbeitsweise=3 (individual) |
| `D_C_6_9` | So Arbeitsweise | Int | R/W | nur bei Arbeitsweise=3 (individual) |
| `D_C_7_1` | Soll Service Intervalldauer | Int [Tage] | R/W |  |
| `D_C_8_1` | LED Funktion | Int | R/W | 0=deakt., 1=Störung, 2=Bed.+Stör., 3=Wasser+Bed.+Stör., 4=Dauerhaft (nicht SC18) |
| `D_C_8_2` | LED blinkt bei Salz-Vorwarnung | Int | R/W | 0=nein, 1=ja (nicht SC18) |

## 📧 E-Mail Einstellungen (Base64 verschlüsselt)

| Parameter-ID | Bezeichnung | Erwarteter Wert | Zugriff | Kommentar / Werte |
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
| `D_Y_8_9` | Text Störmeldeweiterleitung | String | R/W |  |
| `D_Y_8_10` | Test-E-Mail versenden | Int | R/W | 0=nein, 1=ja |

## 🔧 Aktionen

| Parameter-ID | Bezeichnung | Erwarteter Wert | Zugriff | Kommentar / Werte |
|:---|:---|:---|:---:|:---|
| `D_B_1` | Starten der Regeneration / Regeneration aktiv |  | R/W |  |
| `D_M_3_3` | Fehlerspeicher zurücksetzen |  | R/W | Code 189 erforderlich |

## 📊 Allgemeine Sensoren (Lesezugriff)

| Parameter-ID | Bezeichnung | Erwarteter Wert | Zugriff | Kommentar / Werte |
|:---|:---|:---|:---:|:---|
| `D_A_1_7` | Gesamtdurchfluss Anlage | Double [m³/h] | R | MC: 0°Wasser + Verschneidung |
| `D_A_1_6` | Ist-/Sollwert Weichwasserhärte | Double [°dH] | R | Istwert bei Durchfluss>0, Sollwert bei =0 |
| `D_A_2_2` | Tage bis zur nächsten Wartung | Int | R |  |
| `D_A_2_3` | Salzreichweite | Int [Tage] | R | nur SC23 |
| `D_Y_1` | Wasserverbrauch gestern | Int [l] | R |  |
| `D_Y_3` | Salzverbrauch pro Jahr | Int [kg] | R |  |
| `D_Y_5` | Aktueller Regenerationsschritt | Int | R | 0=keine, 1=Soletank, 2=Besalzen, 3=Verdrängen, 4=Rückspülen, 5=Erstfiltrat |
| `D_Y_6` | Software-Version | String | R |  |
| `D_Y_7` | Inbetriebnahme-Datum | String (TT.MM.JJJJ) | R |  |
| `D_Y_8_11` | Ergebnis letzter E-Mail Versand | Int | R | 0=keine, 1=OK, 2=Daten fehlerhaft, 3=kein Internet |
| `D_Y_10_1` | Aktuelle Restkapazität AT1 | Int [%] | R |  |
| `D_Y_10_2` | Aktuelle Restkapazität AT2 | Int [%] | R | nicht bei softliQ:SC |
| `D_Y_13` | Austauscher in Betrieb | Int | R | SC: 0=gestört,1=OK / MC: 0=beide gestört,1=AT1,2=AT2,3=beide |
| `D_Y_14` | Voraussichtl. nächste Regeneration | String (TT.MM.JJJJ HH:MM) | R |  |
| `D_K_1` | Zähler Regenerationen | Int | R |  |
| `D_K_2` | Zähler Weichwassermenge | Int [m³] | R | 0°dH Wasser |

## 📊 Zusätzliche Sensoren 

| Parameter-ID | Bezeichnung | Erwarteter Wert | Zugriff | Kommentar / Werte |
|:---|:---|:---|:---:|:---|
| `D_E_1` | D_E_1 |  | R | Bezeichnung unbekannt |
| `D_Y_9` | D_Y_9 |  | R | Bezeichnung unbekannt |
| `D_Y_9_8` | D_Y_9_8 |  | R | evtl. Verbrauch letzte 8h? |
| `D_Y_9_24` | D_Y_9_24 |  | R | evtl. Verbrauch letzte 24h? |

## 📈 Wasserverbrauch Historie (D_Y_2_x)

| Parameter-ID | Bezeichnung | Erwarteter Wert | Zugriff | Kommentar / Werte |
|:---|:---|:---|:---:|:---|
| `D_Y_2_1` | Wasserverbrauch vor 01 Tag | Int [l] | R |  |
| `D_Y_2_2` | Wasserverbrauch vor 02 Tagen | Int [l] | R |  |
| `D_Y_2_3` | Wasserverbrauch vor 03 Tagen | Int [l] | R |  |
| `D_Y_2_4` | Wasserverbrauch vor 04 Tagen | Int [l] | R |  |
| `D_Y_2_5` | Wasserverbrauch vor 05 Tagen | Int [l] | R |  |
| `D_Y_2_6` | Wasserverbrauch vor 06 Tagen | Int [l] | R |  |
| `D_Y_2_7` | Wasserverbrauch vor 07 Tagen | Int [l] | R |  |
| `D_Y_2_8` | Wasserverbrauch vor 08 Tagen | Int [l] | R |  |
| `D_Y_2_9` | Wasserverbrauch vor 09 Tagen | Int [l] | R |  |
| `D_Y_2_10` | Wasserverbrauch vor 10 Tagen | Int [l] | R |  |
| `D_Y_2_11` | Wasserverbrauch vor 11 Tagen | Int [l] | R |  |
| `D_Y_2_12` | Wasserverbrauch vor 12 Tagen | Int [l] | R |  |
| `D_Y_2_13` | Wasserverbrauch vor 13 Tagen | Int [l] | R |  |
| `D_Y_2_14` | Wasserverbrauch vor 14 Tagen | Int [l] | R |  |
| `D_Y_2_15` | Wasserverbrauch vor 15 Tagen | Int [l] | R |  |
| `D_Y_2_16` | Wasserverbrauch vor 16 Tagen | Int [l] | R |  |
| `D_Y_2_17` | Wasserverbrauch vor 17 Tagen | Int [l] | R |  |
| `D_Y_2_18` | Wasserverbrauch vor 18 Tagen | Int [l] | R |  |
| `D_Y_2_19` | Wasserverbrauch vor 19 Tagen | Int [l] | R |  |
| `D_Y_2_20` | Wasserverbrauch vor 20 Tagen | Int [l] | R |  |
| `D_Y_2_21` | Wasserverbrauch vor 21 Tagen | Int [l] | R |  |
| `D_Y_2_22` | Wasserverbrauch vor 22 Tagen | Int [l] | R |  |
| `D_Y_2_23` | Wasserverbrauch vor 23 Tagen | Int [l] | R |  |
| `D_Y_2_24` | Wasserverbrauch vor 24 Tagen | Int [l] | R |  |
| `D_Y_2_25` | Wasserverbrauch vor 25 Tagen | Int [l] | R |  |
| `D_Y_2_26` | Wasserverbrauch vor 26 Tagen | Int [l] | R |  |
| `D_Y_2_27` | Wasserverbrauch vor 27 Tagen | Int [l] | R |  |

## 📈 Salzverbrauch Historie (D_Y_3_x)

| Parameter-ID | Bezeichnung | Erwarteter Wert | Zugriff | Kommentar / Werte |
|:---|:---|:---|:---:|:---|
| `D_Y_3_1` | Salzverbrauch vor 1 Tag | Double [kg] | R |  |
| `D_Y_3_2` | Salzverbrauch vor 2 Tagen | Double [kg] | R |  |
| `D_Y_3_3` | Salzverbrauch vor 3 Tagen | Double [kg] | R |  |
| `D_Y_3_4` | Salzverbrauch vor 4 Tagen | Double [kg] | R |  |
| `D_Y_3_5` | Salzverbrauch vor 5 Tagen | Double [kg] | R |  |
| `D_Y_3_6` | Salzverbrauch vor 6 Tagen | Double [kg] | R |  |
| `D_Y_3_7` | Salzverbrauch vor 7 Tagen | Double [kg] | R |  |
| `D_Y_3_8` | Salzverbrauch vor 8 Tagen | Double [kg] | R |  |
| `D_Y_3_9` | Salzverbrauch vor 9 Tagen | Double [kg] | R |  |
| `D_Y_3_10` | Salzverbrauch vor 10 Tagen | Double [kg] | R |  |
| `D_Y_3_11` | Salzverbrauch vor 11 Tagen | Double [kg] | R |  |
| `D_Y_3_12` | Salzverbrauch vor 12 Tagen | Double [kg] | R |  |
| `D_Y_3_13` | Salzverbrauch vor 13 Tagen | Double [kg] | R |  |
| `D_Y_3_14` | Salzverbrauch vor 14 Tagen | Double [kg] | R |  |

## 📈 Regenerationszeit Historie (D_Y_4_x)

| Parameter-ID | Bezeichnung | Erwarteter Wert | Zugriff | Kommentar / Werte |
|:---|:---|:---|:---:|:---|
| `D_Y_4_1` | Zeit letzte Regeneration 01 Tag vor aktueller |  | R |  |
| `D_Y_4_2` | Zeit letzte Regeneration 02 Tage vor aktueller |  | R |  |
| `D_Y_4_3` | Zeit letzte Regeneration 03 Tage vor aktueller |  | R |  |
| `D_Y_4_4` | Zeit letzte Regeneration 04 Tage vor aktueller |  | R |  |
| `D_Y_4_5` | Zeit letzte Regeneration 05 Tage vor aktueller |  | R |  |
| `D_Y_4_6` | Zeit letzte Regeneration 06 Tage vor aktueller |  | R |  |
| `D_Y_4_7` | Zeit letzte Regeneration 07 Tage vor aktueller |  | R |  |
| `D_Y_4_8` | Zeit letzte Regeneration 08 Tage vor aktueller |  | R |  |
| `D_Y_4_9` | Zeit letzte Regeneration 09 Tage vor aktueller |  | R |  |
| `D_Y_4_10` | Zeit letzte Regeneration 10 Tage vor aktueller |  | R |  |
| `D_Y_4_11` | Zeit letzte Regeneration 11 Tage vor aktueller |  | R |  |
| `D_Y_4_12` | Zeit letzte Regeneration 12 Tage vor aktueller |  | R |  |
| `D_Y_4_13` | Zeit letzte Regeneration 13 Tage vor aktueller |  | R |  |
| `D_Y_4_14` | Zeit letzte Regeneration 14 Tage vor aktueller |  | R |  |

## 📈 Regeneration Restkapazitäten (D_A_3_x)

| Parameter-ID | Bezeichnung | Erwarteter Wert | Zugriff | Kommentar / Werte |
|:---|:---|:---|:---:|:---|
| `D_A_3_1` | Letzte Regeneration AT1 | String (TT.MM.JJJ HH:MM) | R |  |
| `D_A_3_2` | Letzte Regeneration AT1 übrig | Int [%] | R |  |
| `D_A_3_2_1` | Regeneration 1 – Restkapazität | Int [%] | R |  |
| `D_A_3_2_2` | Regeneration 2 – Restkapazität | Int [%] | R |  |
| `D_A_3_2_3` | Regeneration 3 – Restkapazität | Int [%] | R |  |
| `D_A_3_2_4` | Regeneration 4 – Restkapazität | Int [%] | R |  |
| `D_A_3_2_5` | Regeneration 5 – Restkapazität | Int [%] | R |  |
| `D_A_3_2_6` | Regeneration 6 – Restkapazität | Int [%] | R |  |
| `D_A_3_2_7` | Regeneration 7 – Restkapazität | Int [%] | R |  |
| `D_A_3_2_8` | Regeneration 8 – Restkapazität | Int [%] | R |  |
| `D_A_3_2_9` | Regeneration 9 – Restkapazität | Int [%] | R |  |
| `D_A_3_2_10` | Regeneration 10 – Restkapazität | Int [%] | R |  |
| `D_A_3_2_11` | Regeneration 11 – Restkapazität | Int [%] | R |  |
| `D_A_3_2_12` | Regeneration 12 – Restkapazität | Int [%] | R |  |
| `D_A_3_2_13` | Regeneration 13 – Restkapazität | Int [%] | R |  |
| `D_A_3_2_14` | Regeneration 14 – Restkapazität | Int [%] | R |  |
| `D_A_3_4` | Letzte Regeneration AT2 | String (TT.MM.JJJ HH:MM) | R | nur MC32 |
| `D_A_3_5` | Letzte Regeneration AT2 übrig | Int [%] | R | nur MC32 |

## 🔒 Austauscher-Details (Code 005)

| Parameter-ID | Bezeichnung | Erwarteter Wert | Zugriff | Kommentar / Werte |
|:---|:---|:---|:---:|:---|
| `D_A_1_1` | Aktueller Durchfluss AT1 | Double [m³] | R (Code) |  |
| `D_A_1_2` | Restkapazität AT1 | Double [m³×°dH] | R (Code) |  |
| `D_A_1_3` | Kapazitätszahl AT1 | Double [m³×°dH] | R (Code) |  |
| `D_A_2_1` | Restzeit/-menge Reg.Schritt AT1 | Double [l oder min] | R (Code) |  |
| `D_A_1_4` | Aktueller Durchfluss AT2 | Double [m³] | R (Code) | nur MC32 |
| `D_A_1_5` | Restkapazität AT2 | Double [m³×°dH] | R (Code) | nur MC32 |
| `D_A_1_8` | Kapazitätszahl AT2 | Double [m³×°dH] | R (Code) | nur MC32 |
| `D_A_2_4` | Restzeit/-menge Reg.Schritt AT2 | Double [l oder min] | R (Code) | nur MC32 |
| `D_A_1_9` | Aktueller Durchfluss Verschneidung | Double [m³] | R (Code) | nur MC32 |

## 🔒 Durchfluss-Details (Code 005)

| Parameter-ID | Bezeichnung | Erwarteter Wert | Zugriff | Kommentar / Werte |
|:---|:---|:---|:---:|:---|
| `D_K_3` | Durchfluss Spitzenwert (Parallel) | Double [m³/h] | R (Code) | nur MC32 |
| `D_K_4` | Zeitzähler Nenndurchfluss überschritten | Double [min] | R (Code) |  |
| `D_K_7` | Schrittanzeige Regenerationsventil |  | R |  |
| `D_K_8` | Verbrauchskapazitätszahl |  | R |  |
| `D_K_9` | Durchschnittsverbrauch letzten 03 Tage |  | R |  |
| `D_K_14` | Spitzenwert AT1 | Double [m³/h] | R (Code) |  |
| `D_K_15` | Überschreitung Nenndurchfluss AT1 | Double [min] | R (Code) |  |
| `D_K_16` | Spitzenwert AT2 | Double [m³/h] | R (Code) | nur MC32 |
| `D_K_17` | Überschreitung Nenndurchfluss AT2 | Double [min] | R (Code) | nur MC32 |

## 🔒 Wassermengen (Code 005)

| Parameter-ID | Bezeichnung | Erwarteter Wert | Zugriff | Kommentar / Werte |
|:---|:---|:---|:---:|:---|
| `D_K_18` | Weichwassermenge AT1 | Double [m³] | R (Code) |  |
| `D_K_19` | Weichwassermenge AT2 | Double [m³] | R (Code) | nur MC32 |
| `D_K_20` | Rohwassermenge Verschneidung | Double [m³] | R (Code) | nur MC32 |
| `D_K_21` | Nachspeisemenge | Double [l] | R (Code) |  |

## 🔒 Impulsraten (Code 290)

| Parameter-ID | Bezeichnung | Erwarteter Wert | Zugriff | Kommentar / Werte |
|:---|:---|:---|:---:|:---|
| `D_F_5` | Wasserzähler Weichwasser Impulsrate |  | R (Code) |  |
| `D_F_6` | Wasserzähler Regeneration Impulsrate |  | R (Code) |  |

## 🌐 Netzwerk

| Parameter-ID | Bezeichnung | Erwarteter Wert | Zugriff | Kommentar / Werte |
|:---|:---|:---|:---:|:---|
| `D_C_3_6_1` | WLAN IP-Adresse | String | R |  |
| `D_C_3_6_2` | Default Gateway | String | R |  |
| `D_C_3_6_3` | Primary DNS | String | R |  |
| `D_C_3_6_4` | Secondary DNS | String | R |  |
| `D_C_3_6_5` | WLAN Status | Int | R | 1=verbunden |
| `D_C_3_7_1` | Access Point IP-Adresse | String | R |  |
| `D_C_3_7_2` | Access Point SSID | String | R |  |
| `D_C_3_7_3` | Access Point Status | Int | R | 1=verbunden |

## ⚠️ Fehlerspeicher (D_K_10_x, Code 245)

| Parameter-ID | Bezeichnung | Erwarteter Wert | Zugriff | Kommentar / Werte |
|:---|:---|:---|:---:|:---|
| `D_K_10_1` | error 01 |  | R (Code) | Code 245 |
| `D_K_10_2` | error 02 |  | R (Code) | Code 245 |
| `D_K_10_3` | error 03 |  | R (Code) | Code 245 |
| `D_K_10_4` | error 04 |  | R (Code) | Code 245 |
| `D_K_10_5` | error 05 |  | R (Code) | Code 245 |
| `D_K_10_6` | error 06 |  | R (Code) | Code 245 |
| `D_K_10_7` | error 07 |  | R (Code) | Code 245 |
| `D_K_10_8` | error 08 |  | R (Code) | Code 245 |
| `D_K_10_9` | error 09 |  | R (Code) | Code 245 |
| `D_K_10_10` | error 10 |  | R (Code) | Code 245 |
| `D_K_10_11` | error 11 |  | R (Code) | Code 245 |
| `D_K_10_12` | error 12 |  | R (Code) | Code 245 |
| `D_K_10_13` | error 13 |  | R (Code) | Code 245 |
| `D_K_10_14` | error 14 |  | R (Code) | Code 245 |
| `D_K_10_15` | error 15 |  | R (Code) | Code 245 |
| `D_K_10_16` | error 16 |  | R (Code) | Code 245 |

## ❓ Unbekannte Parameter

| Parameter-ID | Bezeichnung | Erwarteter Wert | Zugriff | Kommentar / Werte |
|:---|:---|:---|:---:|:---|
| `DD_C_4_3` | DD_C_4_3 |  | ? |  |
| `D_C_4_1_3` | D_C_4_1_3 |  | ? |  |
| `D_C_6_8_1` | D_C_6_8_1 |  | ? | evtl. Variante von D_C_6_8 |
| `D_C_7_10_1` | D_C_7_10_1 |  | ? |  |
| `D_C_C_8_1` | D_C_C_8_1 |  | ? |  |
| `D_C__10_1` | D_C__10_1 |  | ? |  |
| `D_C__4_3` | D_C__4_3 |  | ? |  |
| `D_A_1_22` | D_A_1_22 |  | ? |  |
| `D_A_1_2_2` | D_A_1_2_2 |  | ? |  |
| `D_A_1_33` | D_A_1_33 |  | ? |  |
| `D_A_2_5` | D_A_2_5 |  | ? |  |
| `D_A__3_1` | D_A__3_1 |  | ? |  |

---

## API-Referenz

```
POST http://[IP]/mux_http/
Content-Type: application/x-www-form-urlencoded

# Wert lesen:
id=0000&show=D_D_1~

# Mehrere Werte lesen (max 1000 Byte Request+Response):
id=0000&show=D_D_1|D_A_1_1|D_Y_5~

# Wert schreiben + lesen:
id=0000&edit=D_D_1>20&show=D_D_1~

# Mit Zugangscode:
id=0000&code=005&show=D_A_1_1~

# Antwort (XML):
# <data><D_D_1>20</D_D_1></data>
```

**Codes:** `005` = Austauscher-Details · `245` = Fehlerspeicher · `189` = Fehlerspeicher Reset · `290` = Impulsraten

**Hinweis:** Min. 15 Sekunden Abstand zwischen Anfragen einhalten.
