# 🇮🇹 Grünbeck softliQ:SC – Elenco completo dei parametri
*Italiano · Firmware v01.13*

> **Accesso:** `R` = Solo lettura · `R/W` = Lettura & Scrittura · `R/W (Code)` = Protetto da codice

<details>
<summary> Riferimento API </summary>

```
POST http://[IP]/mux_http/
Content-Type: application/x-www-form-urlencoded

id=0000&show=D_D_1~
id=0000&show=D_D_1|D_A_1_1|D_Y_5~
id=0000&edit=D_D_1>20&show=D_D_1~
id=0000&code=005&show=D_A_1_1~
```
</details>

<details>
<summary> Codici </summary>

| Code | Descrizione |
|:---:|:---|
| `005` | Dettagli scambiatore & I/O |
| `121` | Valori idraulici |
| `142` | Parametri di controllo |
| `189` | Reset memoria guasti |
| `245` | Memoria guasti & contatori |
| `290` | Tassi di impulsi & record dati |
| `302` | Incrementi |

</details>

---

## ⚙️ Impostazioni (Lettura & Scrittura)

| ID Parametro | Descrizione | Unità | Accesso |
|:---|:---|:---:|:---:|
| `D_D_1` | Durezza dell‘acqua grezza | °dH | R/W |
| `D_D_2` | Valore nominale durezza acqua dolce | °dH | R/W |
| `D_A_4_1` | Nome installatore | String | R/W |
| `D_A_4_2` | Tel. installatore | String | R/W |
| `D_A_4_3` | E-mail installatore | String | R/W |
| `D_C_1_1` | Lingua | Int | R/W |
| `D_C_2_1` | Unità di durezza | Int | R/W |
| `D_C_4_1` | Seleziona istante di rigenerazione: | Int | R/W |
| `D_C_4_2` | Ora | HH:MM | R/W |
| `D_C_4_3` | Istante di rigenerazione quotidiano | HH:MM | R/W |
| `D_C_4_4` | Ora avvio rigenerazione 2 (solo MC) | HH:MM | R/W |
| `D_C_4_5` | Ora avvio rigenerazione 3 (solo MC) | HH:MM | R/W |
| `D_C_5_1` | Modalità Power | Int | R/W |
| `D_C_5_2` | Data | TT.MM.JJJJ | R/W |
| `D_C_5_3` | Ora legale/solare automatica | Int | R/W |
| `D_C_6_1` | Display attivo in stand-by | Int | R/W |
| `D_C_6_3` | Modalità funzionamento lun | Int | R/W |
| `D_C_6_4` | Modalità funzionamento mar | Int | R/W |
| `D_C_6_5` | Modalità funzionamento mer | Int | R/W |
| `D_C_6_6` | Modalità funzionamento gio | Int | R/W |
| `D_C_6_7` | Modalità funzionamento ven | Int | R/W |
| `D_C_6_8` | Modalità funzionamento sab | Int | R/W |
| `D_C_6_9` | Modalità funzionamento dom | Int | R/W |
| `D_C_7_1` | Impostazione intervallo di manutenzione | d | R/W |
| `D_C_8_1` | Anello luminoso a LED funzione (solo con softliQ:SC23) | Int | R/W |
| `D_C_8_2` | L‘anello luminoso a LED lampeggia in caso di preallarme sale (solo con softliQ:SC23) | Int | R/W |

## 📧 Impostazioni e-mail

| ID Parametro | Descrizione | Unità | Accesso |
|:---|:---|:---:|:---:|
| `D_Y_8_1_1` | Indirizzo e-mail 1 per inoltro | String | R/W |
| `D_Y_8_1_2` | Indirizzo e-mail 2 per inoltro | String | R/W |
| `D_Y_8_1_3` | Indirizzo e-mail 3 per inoltro | String | R/W |
| `D_Y_8_2` | Server SMTP | String | R/W |
| `D_Y_8_3` | N. porta | Int | R/W |
| `D_Y_8_4` | Nome dell‘utente | String | R/W |
| `D_Y_8_5` | Password | String | R/W |
| `D_Y_8_6` | Indirizzo e-mail | String | R/W |
| `D_Y_8_7` | Telefono | String | R/W |
| `D_Y_8_8` | Cognome | String | R/W |
| `D_Y_8_9` | Testo della e-mail di inoltro delle segnalazioni di guasto | String | R/W |
| `D_Y_8_10` | Invia e-mail di prova | Int | R/W |
| `D_Y_8_11` | Stato invio e-mail | Int | R |
| `D_Y_8_12` | Ora dell'ultimo tentativo di invio dell'email |  | R |

## 🔧 Azioni / Pulsanti

| ID Parametro | Descrizione | Unità | Accesso |
|:---|:---|:---:|:---:|
| `D_B_1` | Avviare la rigenerazione manuale |  | R/W |
| `D_E_1` | Avvio messa in servizio |  | R/W |
| `D_M_3_3` | Cancella memoria guasti |  | R/W (Code 189) |
| `D_Y_12` | Reset parametri rete |  | R/W |

## 📊 Sensori generali (Solo lettura)

| ID Parametro | Descrizione | Unità | Accesso |
|:---|:---|:---:|:---:|
| `D_A_1_1` | Portata corrente | m³/h | R |
| `D_A_1_2` | Capacità residua | m³ | R |
| `D_A_1_3` | Capacità corrente dell‘impianto | m³×°dH | R |
| `D_A_1_6` | Valore reale/nominale durezza acqua dolce | °dH | R |
| `D_A_1_7` | Portata totale impianto | m³/h | R |
| `D_A_2_1` | Durata/quantità residua fase di rigenerazione corrente |  | R |
| `D_A_2_2` | Durata residua intervallo di manutenzione | d | R |
| `D_A_2_3` | Autonomia sale (solo con softliQ:SC23) | d | R |
| `D_A_3_1` | Tempo dall‘ultima rigenerazione | h | R |
| `D_A_3_2` | Percentuale della rigenerazione corrente | % | R |
| `D_Y_1` | Consumo d‘acqua al giorno | l | R |
| `D_Y_3` | Consumo sale all'anno | kg | R |
| `D_Y_5` | Fase attuale della rigenerazione: | Int | R |
| `D_Y_6` | Versione software | String | R |
| `D_Y_7` | Data di messa in servizio | TT.MM.JJJJ | R |
| `D_Y_9` | Indice attuale programma di messa in servizio |  | R |
| `D_Y_9_8` | Conto alla rovescia programma di spurgo |  | R |
| `D_Y_9_24` | Durata residua generazione di prova |  | R |
| `D_Y_10_1` | Capacità residua attuale AT1 | % | R |
| `D_Y_10_2` | Capacità residua attuale AT2 | % | R |
| `D_Y_13` | Scambiatore in servizio | Int | R |
| `D_Y_14` | Prossima rigenerazione prevista | TT.MM.JJJJ HH:MM | R |
| `D_K_1` | Contatore rigenerazione | Int | R |
| `D_K_2` | Contatore quantità d‘acqua dolce | m³ | R |

## 🌐 Rete

| ID Parametro | Descrizione | Unità | Accesso |
|:---|:---|:---:|:---:|
| `D_C_3_1` | Disattiva WLAN |  | R/W |
| `D_C_3_2` | Cerca WLAN |  | R/W |
| `D_C_3_6_1` | Indirizzo IP WLAN | String | R |
| `D_C_3_6_2` | Gateway predefinito | String | R |
| `D_C_3_6_3` | DNS primario | String | R |
| `D_C_3_6_4` | DNS secondario | String | R |
| `D_C_3_6_5` | Stato WLAN | Int | R |
| `D_C_3_7_1` | Indirizzo IP | String | R |
| `D_C_3_7_2` | SSID | String | R |
| `D_C_3_7_3` | Stato: | Int | R |

## 🔌 Ingresso/Uscita programmabile (Code 005)

| ID Parametro | Descrizione | Unità | Accesso |
|:---|:---|:---:|:---:|
| `D_G_1` | Funzione contatto senza potenziale | Int | R/W (Code 005) |
| `D_G_2` | Ritardo controllo durezza residua | Min. | R/W (Code 005) |
| `D_G_3` | Funzione ingresso prog. | Int | R/W (Code 005) |

## 🛡️ Parametri di controllo (Code 142)

| ID Parametro | Descrizione | Unità | Accesso |
|:---|:---|:---:|:---:|
| `D_H_2` | Reazione al black-out di rete | Int | R/W (Code 142) |
| `D_H_3` | Impianto in sovraccarico | Int | R/W (Code 142) |
| `D_H_4` | Monitoraggio disinfezione |  | R/W (Code 142) |
| `D_H_5` | Cella del cloro |  | R/W (Code 142) |
| `D_H_6` | Tempo di monitoraggio contatore dell‘acqua rigenerazione | Min. | R/W (Code 142) |
| `D_H_7` | Tempo di monitoraggio aggiunta sale | Min. | R/W (Code 142) |
| `D_H_8` | Intervallo in giorni della rigenerazione forzata | d | R/W (Code 142) |
| `D_H_9` | Monitoraggio portata nominale |  | R/W (Code 142) |
| `D_H_10` | Istante di rigenerazione e capacità impianto sopra | d | R/W (Code 142) |
| `D_H_11` | Valore limite capacità residua | % | R/W (Code 142) |

## 📋 Record dati impianto (Code 005 & 290)

| ID Parametro | Descrizione | Unità | Accesso |
|:---|:---|:---:|:---:|
| `D_F_1` | Seleziona istante di rigenerazione | Int | R/W (Code) |
| `D_F_2` | Giorno della settimana | Int | R/W (Code) |
| `D_F_3_1` | Lunedì |  | R/W (Code) |
| `D_F_3_2` | Martedì |  | R/W (Code) |
| `D_F_3_3` | Mercoledì |  | R/W (Code) |
| `D_F_3_4` | Giovedì |  | R/W (Code) |
| `D_F_3_5` | Venerdì |  | R/W (Code) |
| `D_F_3_6` | Sabato |  | R/W (Code) |
| `D_F_3_7` | Domenica |  | R/W (Code) |
| `D_F_4` | Modello impianto | Int | R/W (Code) |
| `D_F_5` | Acqua dolce tasso impulsi | l/Imp | R (Code 290) |
| `D_F_6` | Rigenerazione tasso impulsi | l/Imp | R (Code 290) |
| `D_F_8` | Cerca posizione di riferimento valvola di trasferimento |  | R/W (Code) |
| `D_F_9` | Cerca posizione di riferimento valvola di rigenerazione |  | R/W (Code) |

## 🔧 Valori idraulici (Code 121)

| ID Parametro | Descrizione | Unità | Accesso |
|:---|:---|:---:|:---:|
| `D_I_1` | Durata fase di rigenerazione espulsione | Min. | R/W (Code 121) |
| `D_I_2` | Quantità fase di rigenerazione risciacquo | l | R/W (Code 121) |
| `D_I_3` | Quantità fase di rigenerazione primo filtrato | l | R/W (Code 121) |
| `D_I_4` | Quantità fase di rigenerazione risciacquo | l | R/W (Code 121) |
| `D_I_5` | Quantità min. riempimento serbatoio del sale capacità minima | l | R/W (Code 121) |
| `D_I_6` | Quantità max. riempimento serbatoio del sale capacità minima | l | R/W (Code 121) |
| `D_I_7` | Quantità min. riempimento serbatoio del sale capacità massima | l | R/W (Code 121) |
| `D_I_8` | Quantità max. riempimento serbatoio del sale capacità massima | l | R/W (Code 121) |
| `D_I_9` | Durata massima riempimento serbatoio della salamoia, primo filtrato | Min. | R/W (Code 121) |
| `D_I_10` | Frequenza finale valvola di rigenerazione | Hz | R/W (Code 121) |
| `D_I_11` | Frequenza finale valvola di trasferimento | Hz | R/W (Code 121) |
| `D_I_12` | Frequenza finale per ricerca punto di riferimento | Hz | R/W (Code 121) |
| `D_I_13` | Riserva di capacità Eco | % | R/W (Code 121) |
| `D_I_14` | Riserva di capacità Power | % | R/W (Code 121) |
| `D_I_15` | Portata nominale | m³/h | R/W (Code 121) |
| `D_I_16` | Contatore dell‘acqua dolce tasso di impulsi | l/Imp | R/W (Code 121) |
| `D_I_17` | Contatore dell‘acqua di rigenerazione tasso di impulsi | l/Imp | R/W (Code 121) |
| `D_I_18` | Valore nominale corrente di cloro | mA | R (Code 121) |
| `D_I_20` | Carica | mAmin | R/W (Code 121) |

## 📐 Incrementi (Code 302)

| ID Parametro | Descrizione | Unità | Accesso |
|:---|:---|:---:|:---:|
| `D_J_1` | Passi punto di riferimento - risciacquo | Steps | R/W (Code 302) |
| `D_J_3` | Passi risciacquo - servizio | Steps | R/W (Code 302) |
| `D_J_4` | Passi servizio – riempimento serbatoio del sale | Steps | R/W (Code 302) |
| `D_J_5` | Passi riempimento serbatoio del sale - aggiunta di sale | Steps | R/W (Code 302) |
| `D_J_6` | Passi aggiunta di sale - espulsione | Steps | R/W (Code 302) |
| `D_J_7` | Passi espulsione - risciacquo | Steps | R/W (Code 302) |
| `D_J_8` | Passi risciacquo – posizione di inversione | Steps | R/W (Code 302) |
| `D_J_9` | Passi ricerca del punto di riferimento | Steps | R/W (Code 302) |

## 🔒 Contatori & Dettagli portata (Code 245)

| ID Parametro | Descrizione | Unità | Accesso |
|:---|:---|:---:|:---:|
| `D_K_3` | Portata valore di picco | m³/h | R (Code 245) |
| `D_K_4` | Contatore temporale superamento portata nominale | h | R (Code 245) |
| `D_K_5` | Corrente di cloro | mA | R (Code 245) |
| `D_K_6` | Indicatore fase valvola di trasferimento | Steps | R (Code 245) |
| `D_K_7` | Indicatore fase valvola di rigenerazione | Steps | R (Code 245) |
| `D_K_8` | Coefficiente di capacità consumo | m³×°dH | R (Code 245) |
| `D_K_9` | Consumo medio negli ultimi 3 giorni | m³ | R (Code 245) |
| `D_K_11` | Parametro con ultima modifica delle impostazioni |  | R (Code 245) |
| `D_K_14` | Valore di picco AT1 | m³/h | R (Code 245) |
| `D_K_15` | Superamento portata nominale AT1 | Min. | R (Code 245) |
| `D_K_16` | Valore di picco AT2 | m³/h | R (Code 245) |
| `D_K_17` | Superamento portata nominale AT2 | Min. | R (Code 245) |

## 🔒 Volumi d'acqua (Code 005)

| ID Parametro | Descrizione | Unità | Accesso |
|:---|:---|:---:|:---:|
| `D_K_18` | Volume acqua dolce AT1 | m³ | R (Code 005) |
| `D_K_19` | Volume acqua dolce AT2 | m³ | R (Code 005) |
| `D_K_20` | Volume acqua grezza miscelazione | m³ | R (Code 005) |
| `D_K_21` | Volume di ricarica | l | R (Code 005) |

## ⚠️ Memoria guasti (Code 245)

| ID Parametro | Descrizione | Unità | Accesso |
|:---|:---|:---:|:---:|
| `D_K_10_1` | memoria guasti(1) |  | R (Code 245) |
| `D_K_10_2` | memoria guasti(2) |  | R (Code 245) |
| `D_K_10_3` | memoria guasti(3) |  | R (Code 245) |
| `D_K_10_4` | memoria guasti(4) |  | R (Code 245) |
| `D_K_10_5` | memoria guasti(5) |  | R (Code 245) |
| `D_K_10_6` | memoria guasti(6) |  | R (Code 245) |
| `D_K_10_7` | memoria guasti(7) |  | R (Code 245) |
| `D_K_10_8` | memoria guasti(8) |  | R (Code 245) |
| `D_K_10_9` | memoria guasti(9) |  | R (Code 245) |
| `D_K_10_10` | memoria guasti(10) |  | R (Code 245) |
| `D_K_10_11` | memoria guasti(11) |  | R (Code 245) |
| `D_K_10_12` | memoria guasti(12) |  | R (Code 245) |
| `D_K_10_13` | memoria guasti(13) |  | R (Code 245) |
| `D_K_10_14` | memoria guasti(14) |  | R (Code 245) |
| `D_K_10_15` | memoria guasti(15) |  | R (Code 245) |
| `D_K_10_16` | memoria guasti(16) |  | R (Code 245) |

## 📈 Storico consumo acqua (D_Y_2_x)

| ID Parametro | Descrizione | Unità | Accesso |
|:---|:---|:---:|:---:|
| `D_Y_2_1` | Consumo acqua 1 giorno/i fa | l | R |
| `D_Y_2_2` | Consumo acqua 2 giorno/i fa | l | R |
| `D_Y_2_3` | Consumo acqua 3 giorno/i fa | l | R |
| `D_Y_2_4` | Consumo acqua 4 giorno/i fa | l | R |
| `D_Y_2_5` | Consumo acqua 5 giorno/i fa | l | R |
| `D_Y_2_6` | Consumo acqua 6 giorno/i fa | l | R |
| `D_Y_2_7` | Consumo acqua 7 giorno/i fa | l | R |
| `D_Y_2_8` | Consumo acqua 8 giorno/i fa | l | R |
| `D_Y_2_9` | Consumo acqua 9 giorno/i fa | l | R |
| `D_Y_2_10` | Consumo acqua 10 giorno/i fa | l | R |
| `D_Y_2_11` | Consumo acqua 11 giorno/i fa | l | R |
| `D_Y_2_12` | Consumo acqua 12 giorno/i fa | l | R |
| `D_Y_2_13` | Consumo acqua 13 giorno/i fa | l | R |
| `D_Y_2_14` | Consumo acqua 14 giorno/i fa | l | R |
| `D_Y_2_15` | Consumo acqua 15 giorno/i fa | l | R |
| `D_Y_2_16` | Consumo acqua 16 giorno/i fa | l | R |
| `D_Y_2_17` | Consumo acqua 17 giorno/i fa | l | R |
| `D_Y_2_18` | Consumo acqua 18 giorno/i fa | l | R |
| `D_Y_2_19` | Consumo acqua 19 giorno/i fa | l | R |
| `D_Y_2_20` | Consumo acqua 20 giorno/i fa | l | R |
| `D_Y_2_21` | Consumo acqua 21 giorno/i fa | l | R |
| `D_Y_2_22` | Consumo acqua 22 giorno/i fa | l | R |
| `D_Y_2_23` | Consumo acqua 23 giorno/i fa | l | R |
| `D_Y_2_24` | Consumo acqua 24 giorno/i fa | l | R |
| `D_Y_2_25` | Consumo acqua 25 giorno/i fa | l | R |
| `D_Y_2_26` | Consumo acqua 26 giorno/i fa | l | R |
| `D_Y_2_27` | Consumo acqua 27 giorno/i fa | l | R |

## 📈 Storico consumo sale (D_Y_3_x)

| ID Parametro | Descrizione | Unità | Accesso |
|:---|:---|:---:|:---:|
| `D_Y_3_1` | Consumo sale 1 giorno/i fa | kg | R |
| `D_Y_3_2` | Consumo sale 2 giorno/i fa | kg | R |
| `D_Y_3_3` | Consumo sale 3 giorno/i fa | kg | R |
| `D_Y_3_4` | Consumo sale 4 giorno/i fa | kg | R |
| `D_Y_3_5` | Consumo sale 5 giorno/i fa | kg | R |
| `D_Y_3_6` | Consumo sale 6 giorno/i fa | kg | R |
| `D_Y_3_7` | Consumo sale 7 giorno/i fa | kg | R |
| `D_Y_3_8` | Consumo sale 8 giorno/i fa | kg | R |
| `D_Y_3_9` | Consumo sale 9 giorno/i fa | kg | R |
| `D_Y_3_10` | Consumo sale 10 giorno/i fa | kg | R |
| `D_Y_3_11` | Consumo sale 11 giorno/i fa | kg | R |
| `D_Y_3_12` | Consumo sale 12 giorno/i fa | kg | R |
| `D_Y_3_13` | Consumo sale 13 giorno/i fa | kg | R |
| `D_Y_3_14` | Consumo sale 14 giorno/i fa | kg | R |

## 📈 Storico tempi rigenerazione (D_Y_4_x)

| ID Parametro | Descrizione | Unità | Accesso |
|:---|:---|:---:|:---:|
| `D_Y_4_1` | Ultima rigenerazione 1 (più recente) |  | R |
| `D_Y_4_2` | Ultima rigenerazione 2 |  | R |
| `D_Y_4_3` | Ultima rigenerazione 3 |  | R |
| `D_Y_4_4` | Ultima rigenerazione 4 |  | R |
| `D_Y_4_5` | Ultima rigenerazione 5 |  | R |
| `D_Y_4_6` | Ultima rigenerazione 6 |  | R |
| `D_Y_4_7` | Ultima rigenerazione 7 |  | R |
| `D_Y_4_8` | Ultima rigenerazione 8 |  | R |
| `D_Y_4_9` | Ultima rigenerazione 9 |  | R |
| `D_Y_4_10` | Ultima rigenerazione 10 |  | R |
| `D_Y_4_11` | Ultima rigenerazione 11 |  | R |
| `D_Y_4_12` | Ultima rigenerazione 12 |  | R |
| `D_Y_4_13` | Ultima rigenerazione 13 |  | R |
| `D_Y_4_14` | Ultima rigenerazione 14 (più vecchia) |  | R |

## 📈 Capacità residua rigenerazione (D_A_3_2_x)

| ID Parametro | Descrizione | Unità | Accesso |
|:---|:---|:---:|:---:|
| `D_A_3_2_1` | Rigenerazione 1 – Capacità residua | % | R |
| `D_A_3_2_2` | Rigenerazione 2 – Capacità residua | % | R |
| `D_A_3_2_3` | Rigenerazione 3 – Capacità residua | % | R |
| `D_A_3_2_4` | Rigenerazione 4 – Capacità residua | % | R |
| `D_A_3_2_5` | Rigenerazione 5 – Capacità residua | % | R |
| `D_A_3_2_6` | Rigenerazione 6 – Capacità residua | % | R |
| `D_A_3_2_7` | Rigenerazione 7 – Capacità residua | % | R |
| `D_A_3_2_8` | Rigenerazione 8 – Capacità residua | % | R |
| `D_A_3_2_9` | Rigenerazione 9 – Capacità residua | % | R |
| `D_A_3_2_10` | Rigenerazione 10 – Capacità residua | % | R |
| `D_A_3_2_11` | Rigenerazione 11 – Capacità residua | % | R |
| `D_A_3_2_12` | Rigenerazione 12 – Capacità residua | % | R |
| `D_A_3_2_13` | Rigenerazione 13 – Capacità residua | % | R |
| `D_A_3_2_14` | Rigenerazione 14 – Capacità residua | % | R |
| `D_A_3_4` | Ultima rigenerazione AT2 | TT.MM.JJJJ HH:MM | R |
| `D_A_3_5` | Ultima rigenerazione AT2 rimanente | % | R |

## 🔒 Dettagli scambiatore 2 – solo MC32 (Code 005)

| ID Parametro | Descrizione | Unità | Accesso |
|:---|:---|:---:|:---:|
| `D_A_1_4` | Portata corrente AT2 | m³ | R (Code 005) |
| `D_A_1_5` | Capacità residua AT2 | m³×°dH | R (Code 005) |
| `D_A_1_8` | Coefficiente capacità AT2 | m³×°dH | R (Code 005) |
| `D_A_1_9` | Portata miscelazione corrente | m³ | R (Code 005) |
| `D_A_2_4` | Tempo/quantità residua fase rig. AT2 |  | R (Code 005) |

---

> **Nota:** Min. 15 secondi tra le richieste. Max 1000 byte per richiesta+risposta.
