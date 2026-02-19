# 🇬🇧 Grünbeck softliQ:SC – Complete Parameter List
*English · Firmware v01.13*

> **Access:** `R` = Read only · `R/W` = Read & Write · `R/W (Code)` = Code-protected

<details>
<summary> API Reference </summary>

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
<summary> Codes </summary>

| Code | Description |
|:---:|:---|
| `005` | Exchanger details & I/O |
| `121` | Hydraulic values |
| `142` | Control parameters |
| `189` | Error memory reset |
| `245` | Error memory & meter readings |
| `290` | Pulse rates & system data record |
| `302` | Step distances |

</details>

---

## ⚙️ Settings (Read & Write Access)

| Parameter ID | Description | Unit | Access |
|:---|:---|:---:|:---:|
| `D_D_1` | Raw water hardness | °dH | R/W |
| `D_D_2` | Soft water hardness setpoint | °dH | R/W |
| `D_A_4_1` | Installer name | String | R/W |
| `D_A_4_2` | Installer phone | String | R/W |
| `D_A_4_3` | Installer email | String | R/W |
| `D_C_1_1` | Operating language | Int | R/W |
| `D_C_2_1` | Hardness unit | Int | R/W |
| `D_C_4_1` | Select regeneration time: | Int | R/W |
| `D_C_4_2` | Time | HH:MM | R/W |
| `D_C_4_3` | Daily regeneration time | HH:MM | R/W |
| `D_C_4_4` | Start time regeneration 2 (MC only) | HH:MM | R/W |
| `D_C_4_5` | Start time regeneration 3 (MC only) | HH:MM | R/W |
| `D_C_5_1` | Power mode | Int | R/W |
| `D_C_5_2` | Date | TT.MM.JJJJ | R/W |
| `D_C_5_3` | Auto daylight saving time | Int | R/W |
| `D_C_6_1` | Display in standby active | Int | R/W |
| `D_C_6_3` | Mon operating mode | Int | R/W |
| `D_C_6_4` | Tue operating mode | Int | R/W |
| `D_C_6_5` | Wed operating mode | Int | R/W |
| `D_C_6_6` | Thu operating mode | Int | R/W |
| `D_C_6_7` | Fri operating mode | Int | R/W |
| `D_C_6_8` | Sat operating mode | Int | R/W |
| `D_C_6_9` | Sun operating mode | Int | R/W |
| `D_C_7_1` | Set service interval | d | R/W |
| `D_C_8_1` | LED illuminated ring function (for softliQ:SC23 only) | Int | R/W |
| `D_C_8_2` | LED light ring flashes on salt advance warning (for softliQ:SC only) | Int | R/W |

## 📧 Email Settings

| Parameter ID | Description | Unit | Access |
|:---|:---|:---:|:---:|
| `D_Y_8_1_1` | Email address 1 for forwarding | String | R/W |
| `D_Y_8_1_2` | Email address 2 for forwarding | String | R/W |
| `D_Y_8_1_3` | Email address 3 for forwarding | String | R/W |
| `D_Y_8_2` | SMTP server | String | R/W |
| `D_Y_8_3` | Port no. | Int | R/W |
| `D_Y_8_4` | User name | String | R/W |
| `D_Y_8_5` | Password | String | R/W |
| `D_Y_8_6` | Email address | String | R/W |
| `D_Y_8_7` | Phone number | String | R/W |
| `D_Y_8_8` | Surname | String | R/W |
| `D_Y_8_9` | Text for Email forwarding of fault messages | String | R/W |
| `D_Y_8_10` | Send test Email | Int | R/W |
| `D_Y_8_11` | Status of email transmission | Int | R |
| `D_Y_8_12` | Time of last e-mail sending attempt |  | R |

## 🔧 Actions / Buttons

| Parameter ID | Description | Unit | Access |
|:---|:---|:---:|:---:|
| `D_B_1` | Start manual regeneration |  | R/W |
| `D_E_1` | Begin the start-up process |  | R/W |
| `D_M_3_3` | Delete error memory |  | R/W (Code 189) |
| `D_Y_12` | Reset network parameters |  | R/W |

## 📊 General Sensors (Read Only)

| Parameter ID | Description | Unit | Access |
|:---|:---|:---:|:---:|
| `D_A_1_1` | Current flow | m³/h | R |
| `D_A_1_2` | Residual capacity | m³ | R |
| `D_A_1_3` | Current system capacity | m³×°dH | R |
| `D_A_1_6` | Actual/setpoint soft water hardness | °dH | R |
| `D_A_1_7` | Total system flow | m³/h | R |
| `D_A_2_1` | Remaining time or residual volume of current regeneration step |  | R |
| `D_A_2_2` | Remaining duration of maintenance interval | d | R |
| `D_A_2_3` | Salt range (for softliQ:SC23 only) | d | R |
| `D_A_3_1` | Time since last regeneration | h | R |
| `D_A_3_2` | Percentage of current regeneration | % | R |
| `D_Y_1` | Water consumption per day | l | R |
| `D_Y_3` | Salt consumption per year | kg | R |
| `D_Y_5` | Current regeneration step: | Int | R |
| `D_Y_6` | Software version | String | R |
| `D_Y_7` | Commissioning date | TT.MM.JJJJ | R |
| `D_Y_9` | Current index commissioning program |  | R |
| `D_Y_9_8` | Countdown time for venting program |  | R |
| `D_Y_9_24` | Remaining duration of test regeneration |  | R |
| `D_Y_10_1` | Current residual capacity AT1 | % | R |
| `D_Y_10_2` | Current residual capacity AT2 | % | R |
| `D_Y_13` | Exchanger in operation | Int | R |
| `D_Y_14` | Expected next regeneration | TT.MM.JJJJ HH:MM | R |
| `D_K_1` | Regeneration meter | Int | R |
| `D_K_2` | Soft water volume meter | m³ | R |

## 🌐 Network

| Parameter ID | Description | Unit | Access |
|:---|:---|:---:|:---:|
| `D_C_3_1` | Deactivate WLAN |  | R/W |
| `D_C_3_2` | Search WLAN |  | R/W |
| `D_C_3_6_1` | WLAN IP address | String | R |
| `D_C_3_6_2` | Default Gateway | String | R |
| `D_C_3_6_3` | Primary DNS | String | R |
| `D_C_3_6_4` | Secondary DNS | String | R |
| `D_C_3_6_5` | WLAN Status | Int | R |
| `D_C_3_7_1` | IP address | String | R |
| `D_C_3_7_2` | SSID | String | R |
| `D_C_3_7_3` | Status: | Int | R |

## 🔌 Programmable Input/Output (Code 005)

| Parameter ID | Description | Unit | Access |
|:---|:---|:---:|:---:|
| `D_G_1` | Voltage-free contact function | Int | R/W (Code 005) |
| `D_G_2` | Residual hardness monitoring delay | Min. | R/W (Code 005) |
| `D_G_3` | Function programmable input | Int | R/W (Code 005) |

## 🛡️ Control Parameters (Code 142)

| Parameter ID | Description | Unit | Access |
|:---|:---|:---:|:---:|
| `D_H_2` | Reaction to power failure | Int | R/W (Code 142) |
| `D_H_3` | System overloaded | Int | R/W (Code 142) |
| `D_H_4` | Disinfection monitoring |  | R/W (Code 142) |
| `D_H_5` | Chlorine cell |  | R/W (Code 142) |
| `D_H_6` | Regeneration water meter monitoring time | Min. | R/W (Code 142) |
| `D_H_7` | Salting monitoring time | Min. | R/W (Code 142) |
| `D_H_8` | Daily interval for compulsory regeneration | d | R/W (Code 142) |
| `D_H_9` | Nominal flow monitoring |  | R/W (Code 142) |
| `D_H_10` | Regeneration time and system capacity | d | R/W (Code 142) |
| `D_H_11` | Residual capacity limit value | % | R/W (Code 142) |

## 📋 System Data Record (Code 005 & 290)

| Parameter ID | Description | Unit | Access |
|:---|:---|:---:|:---:|
| `D_F_1` | Select regeneration time | Int | R/W (Code) |
| `D_F_2` | Weekday | Int | R/W (Code) |
| `D_F_3_1` | Monday |  | R/W (Code) |
| `D_F_3_2` | Tuesday |  | R/W (Code) |
| `D_F_3_3` | Wednesday |  | R/W (Code) |
| `D_F_3_4` | Thursday |  | R/W (Code) |
| `D_F_3_5` | Friday |  | R/W (Code) |
| `D_F_3_6` | Saturday |  | R/W (Code) |
| `D_F_3_7` | Sunday |  | R/W (Code) |
| `D_F_4` | System type | Int | R/W (Code) |
| `D_F_5` | Soft water pulse rate | l/Imp | R (Code 290) |
| `D_F_6` | Regeneration pulse rate | l/Imp | R (Code 290) |
| `D_F_8` | Search reference position transfer valve |  | R/W (Code) |
| `D_F_9` | Search reference position regeneration valve |  | R/W (Code) |

## 🔧 Hydraulic Values (Code 121)

| Parameter ID | Description | Unit | Access |
|:---|:---|:---:|:---:|
| `D_I_1` | Duration of slow rinsing regeneration step | Min. | R/W (Code 121) |
| `D_I_2` | Volume of backwashing regeneration step | l | R/W (Code 121) |
| `D_I_3` | Volume of first filtrate regeneration step | l | R/W (Code 121) |
| `D_I_4` | Volume of washing out regeneration step | l | R/W (Code 121) |
| `D_I_5` | Min. backfeed water fill brine tank minimum capacity | l | R/W (Code 121) |
| `D_I_6` | Max. backfeed water fill brine tank minimum capacity | l | R/W (Code 121) |
| `D_I_7` | Min. backfeed water fill brine tank maximum capacity | l | R/W (Code 121) |
| `D_I_8` | Max. backfeed water fill brine tank maximum capacity | l | R/W (Code 121) |
| `D_I_9` | Maximum duration fill brine tank, washing out | Min. | R/W (Code 121) |
| `D_I_10` | Regeneration valve end frequency | Hz | R/W (Code 121) |
| `D_I_11` | Transfer valve end frequency | Hz | R/W (Code 121) |
| `D_I_12` | End frequency with reference point search | Hz | R/W (Code 121) |
| `D_I_13` | Spare capacity in Eco mode | % | R/W (Code 121) |
| `D_I_14` | Spare capacity in Power mode | % | R/W (Code 121) |
| `D_I_15` | Nominal flow | m³/h | R/W (Code 121) |
| `D_I_16` | Soft water meter pulse rate | l/Imp | R/W (Code 121) |
| `D_I_17` | Regeneration water meter pulse rate | l/Imp | R/W (Code 121) |
| `D_I_18` | Chlorine current reference value | mA | R (Code 121) |
| `D_I_20` | Charge | mAmin | R/W (Code 121) |

## 📐 Step Distances (Code 302)

| Parameter ID | Description | Unit | Access |
|:---|:---|:---:|:---:|
| `D_J_1` | Steps reference point - washing out | Steps | R/W (Code 302) |
| `D_J_3` | Steps washing out - operation | Steps | R/W (Code 302) |
| `D_J_4` | Steps operation - fill brine tank | Steps | R/W (Code 302) |
| `D_J_5` | Steps fill brine tank - salting | Steps | R/W (Code 302) |
| `D_J_6` | Steps salting - purging | Steps | R/W (Code 302) |
| `D_J_7` | Steps purging - backwashing | Steps | R/W (Code 302) |
| `D_J_8` | Steps backwashing - reverse position | Steps | R/W (Code 302) |
| `D_J_9` | Steps reference point search | Steps | R/W (Code 302) |

## 🔒 Meter Readings & Flow Details (Code 245)

| Parameter ID | Description | Unit | Access |
|:---|:---|:---:|:---:|
| `D_K_3` | Flow peak value | m³/h | R (Code 245) |
| `D_K_4` | Nominal flow timer exceeded | h | R (Code 245) |
| `D_K_5` | Chlorine current | mA | R (Code 245) |
| `D_K_6` | Transfer valve step indicator | Steps | R (Code 245) |
| `D_K_7` | Regeneration valve step indicator | Steps | R (Code 245) |
| `D_K_8` | Consumption capacity rate | m³×°dH | R (Code 245) |
| `D_K_9` | Average consumption over the last 3 days | m³ | R (Code 245) |
| `D_K_11` | Parameter with the last setting change |  | R (Code 245) |
| `D_K_14` | Peak value AT1 | m³/h | R (Code 245) |
| `D_K_15` | Nominal flow exceeded AT1 | Min. | R (Code 245) |
| `D_K_16` | Peak value AT2 | m³/h | R (Code 245) |
| `D_K_17` | Nominal flow exceeded AT2 | Min. | R (Code 245) |

## 🔒 Water Volumes (Code 005)

| Parameter ID | Description | Unit | Access |
|:---|:---|:---:|:---:|
| `D_K_18` | Soft water volume AT1 | m³ | R (Code 005) |
| `D_K_19` | Soft water volume AT2 | m³ | R (Code 005) |
| `D_K_20` | Raw water blending volume | m³ | R (Code 005) |
| `D_K_21` | Backfeed volume | l | R (Code 005) |

## ⚠️ Error Memory (Code 245)

| Parameter ID | Description | Unit | Access |
|:---|:---|:---:|:---:|
| `D_K_10_1` | Error memory(1) |  | R (Code 245) |
| `D_K_10_2` | Error memory(2) |  | R (Code 245) |
| `D_K_10_3` | Error memory(3) |  | R (Code 245) |
| `D_K_10_4` | Error memory(4) |  | R (Code 245) |
| `D_K_10_5` | Error memory(5) |  | R (Code 245) |
| `D_K_10_6` | Error memory(6) |  | R (Code 245) |
| `D_K_10_7` | Error memory(7) |  | R (Code 245) |
| `D_K_10_8` | Error memory(8) |  | R (Code 245) |
| `D_K_10_9` | Error memory(9) |  | R (Code 245) |
| `D_K_10_10` | Error memory(10) |  | R (Code 245) |
| `D_K_10_11` | Error memory(11) |  | R (Code 245) |
| `D_K_10_12` | Error memory(12) |  | R (Code 245) |
| `D_K_10_13` | Error memory(13) |  | R (Code 245) |
| `D_K_10_14` | Error memory(14) |  | R (Code 245) |
| `D_K_10_15` | Error memory(15) |  | R (Code 245) |
| `D_K_10_16` | Error memory(16) |  | R (Code 245) |

## 📈 Water Consumption History (D_Y_2_x)

| Parameter ID | Description | Unit | Access |
|:---|:---|:---:|:---:|
| `D_Y_2_1` | Water consumption 1 day(s) ago | l | R |
| `D_Y_2_2` | Water consumption 2 day(s) ago | l | R |
| `D_Y_2_3` | Water consumption 3 day(s) ago | l | R |
| `D_Y_2_4` | Water consumption 4 day(s) ago | l | R |
| `D_Y_2_5` | Water consumption 5 day(s) ago | l | R |
| `D_Y_2_6` | Water consumption 6 day(s) ago | l | R |
| `D_Y_2_7` | Water consumption 7 day(s) ago | l | R |
| `D_Y_2_8` | Water consumption 8 day(s) ago | l | R |
| `D_Y_2_9` | Water consumption 9 day(s) ago | l | R |
| `D_Y_2_10` | Water consumption 10 day(s) ago | l | R |
| `D_Y_2_11` | Water consumption 11 day(s) ago | l | R |
| `D_Y_2_12` | Water consumption 12 day(s) ago | l | R |
| `D_Y_2_13` | Water consumption 13 day(s) ago | l | R |
| `D_Y_2_14` | Water consumption 14 day(s) ago | l | R |
| `D_Y_2_15` | Water consumption 15 day(s) ago | l | R |
| `D_Y_2_16` | Water consumption 16 day(s) ago | l | R |
| `D_Y_2_17` | Water consumption 17 day(s) ago | l | R |
| `D_Y_2_18` | Water consumption 18 day(s) ago | l | R |
| `D_Y_2_19` | Water consumption 19 day(s) ago | l | R |
| `D_Y_2_20` | Water consumption 20 day(s) ago | l | R |
| `D_Y_2_21` | Water consumption 21 day(s) ago | l | R |
| `D_Y_2_22` | Water consumption 22 day(s) ago | l | R |
| `D_Y_2_23` | Water consumption 23 day(s) ago | l | R |
| `D_Y_2_24` | Water consumption 24 day(s) ago | l | R |
| `D_Y_2_25` | Water consumption 25 day(s) ago | l | R |
| `D_Y_2_26` | Water consumption 26 day(s) ago | l | R |
| `D_Y_2_27` | Water consumption 27 day(s) ago | l | R |

## 📈 Salt Consumption History (D_Y_3_x)

| Parameter ID | Description | Unit | Access |
|:---|:---|:---:|:---:|
| `D_Y_3_1` | Salt consumption 1 day(s) ago | kg | R |
| `D_Y_3_2` | Salt consumption 2 day(s) ago | kg | R |
| `D_Y_3_3` | Salt consumption 3 day(s) ago | kg | R |
| `D_Y_3_4` | Salt consumption 4 day(s) ago | kg | R |
| `D_Y_3_5` | Salt consumption 5 day(s) ago | kg | R |
| `D_Y_3_6` | Salt consumption 6 day(s) ago | kg | R |
| `D_Y_3_7` | Salt consumption 7 day(s) ago | kg | R |
| `D_Y_3_8` | Salt consumption 8 day(s) ago | kg | R |
| `D_Y_3_9` | Salt consumption 9 day(s) ago | kg | R |
| `D_Y_3_10` | Salt consumption 10 day(s) ago | kg | R |
| `D_Y_3_11` | Salt consumption 11 day(s) ago | kg | R |
| `D_Y_3_12` | Salt consumption 12 day(s) ago | kg | R |
| `D_Y_3_13` | Salt consumption 13 day(s) ago | kg | R |
| `D_Y_3_14` | Salt consumption 14 day(s) ago | kg | R |

## 📈 Regeneration Time History (D_Y_4_x)

| Parameter ID | Description | Unit | Access |
|:---|:---|:---:|:---:|
| `D_Y_4_1` | Last regeneration 1 (latest) |  | R |
| `D_Y_4_2` | Last regeneration 2 |  | R |
| `D_Y_4_3` | Last regeneration 3 |  | R |
| `D_Y_4_4` | Last regeneration 4 |  | R |
| `D_Y_4_5` | Last regeneration 5 |  | R |
| `D_Y_4_6` | Last regeneration 6 |  | R |
| `D_Y_4_7` | Last regeneration 7 |  | R |
| `D_Y_4_8` | Last regeneration 8 |  | R |
| `D_Y_4_9` | Last regeneration 9 |  | R |
| `D_Y_4_10` | Last regeneration 10 |  | R |
| `D_Y_4_11` | Last regeneration 11 |  | R |
| `D_Y_4_12` | Last regeneration 12 |  | R |
| `D_Y_4_13` | Last regeneration 13 |  | R |
| `D_Y_4_14` | Last regeneration 14 (oldest) |  | R |

## 📈 Regeneration Residual Capacities (D_A_3_2_x)

| Parameter ID | Description | Unit | Access |
|:---|:---|:---:|:---:|
| `D_A_3_2_1` | Regeneration 1 – Residual capacity | % | R |
| `D_A_3_2_2` | Regeneration 2 – Residual capacity | % | R |
| `D_A_3_2_3` | Regeneration 3 – Residual capacity | % | R |
| `D_A_3_2_4` | Regeneration 4 – Residual capacity | % | R |
| `D_A_3_2_5` | Regeneration 5 – Residual capacity | % | R |
| `D_A_3_2_6` | Regeneration 6 – Residual capacity | % | R |
| `D_A_3_2_7` | Regeneration 7 – Residual capacity | % | R |
| `D_A_3_2_8` | Regeneration 8 – Residual capacity | % | R |
| `D_A_3_2_9` | Regeneration 9 – Residual capacity | % | R |
| `D_A_3_2_10` | Regeneration 10 – Residual capacity | % | R |
| `D_A_3_2_11` | Regeneration 11 – Residual capacity | % | R |
| `D_A_3_2_12` | Regeneration 12 – Residual capacity | % | R |
| `D_A_3_2_13` | Regeneration 13 – Residual capacity | % | R |
| `D_A_3_2_14` | Regeneration 14 – Residual capacity | % | R |
| `D_A_3_4` | Last regeneration AT2 | TT.MM.JJJJ HH:MM | R |
| `D_A_3_5` | Last regeneration AT2 remaining | % | R |

## 🔒 Exchanger 2 Details – MC32 only (Code 005)

| Parameter ID | Description | Unit | Access |
|:---|:---|:---:|:---:|
| `D_A_1_4` | Current flow AT2 | m³ | R (Code 005) |
| `D_A_1_5` | Residual capacity AT2 | m³×°dH | R (Code 005) |
| `D_A_1_8` | Capacity rate AT2 | m³×°dH | R (Code 005) |
| `D_A_1_9` | Current blending flow | m³ | R (Code 005) |
| `D_A_2_4` | Remaining time/volume regen. step AT2 |  | R (Code 005) |

---

> **Note:** Min. 15 seconds between requests. Max 1000 bytes per request+response.
