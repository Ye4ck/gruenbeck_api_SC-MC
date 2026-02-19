# 🇫🇷 Grünbeck softliQ:SC – Liste complète des paramètres
*Français · Firmware v01.13*

> **Accès:** `R` = Lecture seule · `R/W` = Lecture & Écriture · `R/W (Code)` = Protégé par code

<details>
<summary> Référence API </summary>

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

| Code | Désignation |
|:---:|:---|
| `005` | Détails échangeur & E/S |
| `121` | Valeurs hydrauliques |
| `142` | Paramètres de contrôle |
| `189` | Reset mémoire de défauts |
| `245` | Mémoire défauts & compteurs |
| `290` | Taux d'impulsions & enregistrement |
| `302` | Intervalles des étapes |

</details>

---

## ⚙️ Paramètres (Lecture & Écriture)

| ID Paramètre | Désignation | Unité | Accès |
|:---|:---|:---:|:---:|
| `D_D_1` | Dureté de l‘eau brute | °dH | R/W |
| `D_D_2` | Valeur de consigne dureté eau douce | °dH | R/W |
| `D_A_4_1` | Nom installateur | String | R/W |
| `D_A_4_2` | Tél. installateur | String | R/W |
| `D_A_4_3` | E-mail installateur | String | R/W |
| `D_C_1_1` | Langue d‘utilisation | Int | R/W |
| `D_C_2_1` | Unité de dureté | Int | R/W |
| `D_C_4_1` | Choisir le moment de régénération: | Int | R/W |
| `D_C_4_2` | Heure | HH:MM | R/W |
| `D_C_4_3` | Moment de régénération quotidien | HH:MM | R/W |
| `D_C_4_4` | Heure démarrage régénération 2 (MC uniquement) | HH:MM | R/W |
| `D_C_4_5` | Heure démarrage régénération 3 (MC uniquement) | HH:MM | R/W |
| `D_C_5_1` | Mode Power | Int | R/W |
| `D_C_5_2` | Date | TT.MM.JJJJ | R/W |
| `D_C_5_3` | Heure été/hiver automatique | Int | R/W |
| `D_C_6_1` | écran actif en mode veille | Int | R/W |
| `D_C_6_3` | Mode de fonctionnement lun | Int | R/W |
| `D_C_6_4` | Mode de fonctionnement mar | Int | R/W |
| `D_C_6_5` | Mode de fonctionnement mer | Int | R/W |
| `D_C_6_6` | Mode de fonctionnement jeu | Int | R/W |
| `D_C_6_7` | Mode de fonctionnement ven | Int | R/W |
| `D_C_6_8` | Mode de fonctionnement sam | Int | R/W |
| `D_C_6_9` | Mode de fonctionnement dim | Int | R/W |
| `D_C_7_1` | Régler l‘intervalle de maintenance | d | R/W |
| `D_C_8_1` | Anneau lumineux LED fonction (uniquement pour softliQ:SC23) | Int | R/W |
| `D_C_8_2` | L‘anneau lumineux à LED clignote en cas de préalarme pour le niveau de sel (uniquement pour softliQ:sc23) | Int | R/W |

## 📧 Paramètres e-mail

| ID Paramètre | Désignation | Unité | Accès |
|:---|:---|:---:|:---:|
| `D_Y_8_1_1` | Adresse e-mail 1 pour transmission | String | R/W |
| `D_Y_8_1_2` | Adresse e-mail 2 pour transmission | String | R/W |
| `D_Y_8_1_3` | Adresse e-mail 3 pour transmission | String | R/W |
| `D_Y_8_2` | Serveur SMTP | String | R/W |
| `D_Y_8_3` | N° port | Int | R/W |
| `D_Y_8_4` | Nom d‘utilisateur | String | R/W |
| `D_Y_8_5` | Mot de passe | String | R/W |
| `D_Y_8_6` | Adresse e-mail | String | R/W |
| `D_Y_8_7` | N° de téléphone | String | R/W |
| `D_Y_8_8` | Nom | String | R/W |
| `D_Y_8_9` | Texte pour e-mail de transfert message d‘alerte | String | R/W |
| `D_Y_8_10` | Envoyer un e-mail test | Int | R/W |
| `D_Y_8_11` | État de l‘envoi de l‘e-mail | Int | R |
| `D_Y_8_12` | Heure de la dernière tentative d'envoi d'e-mail |  | R |

## 🔧 Actions / Boutons

| ID Paramètre | Désignation | Unité | Accès |
|:---|:---|:---:|:---:|
| `D_B_1` | Démarrer la régénération manuelle |  | R/W |
| `D_E_1` | Démarrer la mise en service |  | R/W |
| `D_M_3_3` | Effacer la mémoire de défauts |  | R/W (Code 189) |
| `D_Y_12` | Réinitialiser les paramètres réseau |  | R/W |

## 📊 Capteurs généraux (Lecture seule)

| ID Paramètre | Désignation | Unité | Accès |
|:---|:---|:---:|:---:|
| `D_A_1_1` | Débit actuel | m³/h | R |
| `D_A_1_2` | Capacité résiduelle | m³ | R |
| `D_A_1_3` | Capacité actuelle de l‘installation | m³×°dH | R |
| `D_A_1_6` | Valeur réelle/consigne dureté eau douce | °dH | R |
| `D_A_1_7` | Débit total installation | m³/h | R |
| `D_A_2_1` | Durée ou quantité de l'étape de régénération actuelle |  | R |
| `D_A_2_2` | Durée résiduelle intervalle d‘entretien | d | R |
| `D_A_2_3` | Capacité du sel (uniquement pou softliQ:SC23) | d | R |
| `D_A_3_1` | Temps écoulé depuis la dernière | h | R |
| `D_A_3_2` | Pourcentage de régénération en cours | % | R |
| `D_Y_1` | Consommation d‘eau par jour | l | R |
| `D_Y_3` | Consommation de sel par an | kg | R |
| `D_Y_5` | étape de régénération actuelle: | Int | R |
| `D_Y_6` | Version du logiciel | String | R |
| `D_Y_7` | Date de mise en service | TT.MM.JJJJ | R |
| `D_Y_9` | Indice actuel programme de mise en service |  | R |
| `D_Y_9_8` | Compte à rebours durée programme de purge |  | R |
| `D_Y_9_24` | Durée résiduelle régénération test |  | R |
| `D_Y_10_1` | Capacité résiduelle actuelle AT1 | % | R |
| `D_Y_10_2` | Capacité résiduelle actuelle AT2 | % | R |
| `D_Y_13` | Échangeur en service | Int | R |
| `D_Y_14` | Prochaine régénération prévue | TT.MM.JJJJ HH:MM | R |
| `D_K_1` | Compteur de régénération | Int | R |
| `D_K_2` | Compteur du volume d‘eau douce | m³ | R |

## 🌐 Réseau

| ID Paramètre | Désignation | Unité | Accès |
|:---|:---|:---:|:---:|
| `D_C_3_1` | Désactiver WiFi |  | R/W |
| `D_C_3_2` | Chercher WiFi |  | R/W |
| `D_C_3_6_1` | Adresse IP WiFi | String | R |
| `D_C_3_6_2` | Passerelle par défaut | String | R |
| `D_C_3_6_3` | DNS primaire | String | R |
| `D_C_3_6_4` | DNS secondaire | String | R |
| `D_C_3_6_5` | Statut WiFi | Int | R |
| `D_C_3_7_1` | Adresse IP | String | R |
| `D_C_3_7_2` | SSID | String | R |
| `D_C_3_7_3` | Statut: | Int | R |

## 🔌 Entrée/Sortie programmable (Code 005)

| ID Paramètre | Désignation | Unité | Accès |
|:---|:---|:---:|:---:|
| `D_G_1` | Fonction contact sans potentiel | Int | R/W (Code 005) |
| `D_G_2` | Temporisation contrôle dureté résiduelle | Min. | R/W (Code 005) |
| `D_G_3` | Fonction entrée program. | Int | R/W (Code 005) |

## 🛡️ Paramètres de contrôle (Code 142)

| ID Paramètre | Désignation | Unité | Accès |
|:---|:---|:---:|:---:|
| `D_H_2` | Réaction en cas de coupure de courant | Int | R/W (Code 142) |
| `D_H_3` | Installation surchargée | Int | R/W (Code 142) |
| `D_H_4` | Monitorage désinfection |  | R/W (Code 142) |
| `D_H_5` | Cellule de chlore |  | R/W (Code 142) |
| `D_H_6` | Temps de monitorage compteur d‘eau régénération | Min. | R/W (Code 142) |
| `D_H_7` | Temps de monitorage saumurage | Min. | R/W (Code 142) |
| `D_H_8` | Intervalles en jours pour la régénération forcée | d | R/W (Code 142) |
| `D_H_9` | Monitorage débit nominal |  | R/W (Code 142) |
| `D_H_10` | Moment de régénération et capacité de l‘installation sur | d | R/W (Code 142) |
| `D_H_11` | Valeur limite capacité résiduelle | % | R/W (Code 142) |

## 📋 Enregistrement installation (Code 005 & 290)

| ID Paramètre | Désignation | Unité | Accès |
|:---|:---|:---:|:---:|
| `D_F_1` | Choisir le moment de régénération | Int | R/W (Code) |
| `D_F_2` | Jour de la semaine | Int | R/W (Code) |
| `D_F_3_1` | Lundi |  | R/W (Code) |
| `D_F_3_2` | Mardi |  | R/W (Code) |
| `D_F_3_3` | Mercredi |  | R/W (Code) |
| `D_F_3_4` | Jeudi |  | R/W (Code) |
| `D_F_3_5` | Vendredi |  | R/W (Code) |
| `D_F_3_6` | Samedi |  | R/W (Code) |
| `D_F_3_7` | Dimanche |  | R/W (Code) |
| `D_F_4` | Type d'installation | Int | R/W (Code) |
| `D_F_5` | Taux d'impulsions eau douce | l/Imp | R (Code 290) |
| `D_F_6` | Taux d'impulsions régénération | l/Imp | R (Code 290) |
| `D_F_8` | Chercher la position de référence vanne de transfert |  | R/W (Code) |
| `D_F_9` | Chercher la position de référence vanne de régénération |  | R/W (Code) |

## 🔧 Valeurs hydrauliques (Code 121)

| ID Paramètre | Désignation | Unité | Accès |
|:---|:---|:---:|:---:|
| `D_I_1` | Durée étape de régénération Refoulement | Min. | R/W (Code 121) |
| `D_I_2` | Volume étape de régénération Rétrolavage | l | R/W (Code 121) |
| `D_I_3` | Volume étape de régénération Premier filtrat | l | R/W (Code 121) |
| `D_I_4` | Volume étape de régénération Lavage | l | R/W (Code 121) |
| `D_I_5` | Volume d‘appoint min. cuve de sel capacité min. | l | R/W (Code 121) |
| `D_I_6` | Volume d‘appoint max. cuve de sel capacité min. | l | R/W (Code 121) |
| `D_I_7` | Volume d‘appoint min. cuve de sel capacité max. | l | R/W (Code 121) |
| `D_I_8` | Volume d‘appoint max. cuve de sel capacité max. | l | R/W (Code 121) |
| `D_I_9` | Durée max. appoint cuve de sel, premier filtrat | Min. | R/W (Code 121) |
| `D_I_10` | Fréquence finale vanne de régénération | Hz | R/W (Code 121) |
| `D_I_11` | Fréquence finale vanne de transfert | Hz | R/W (Code 121) |
| `D_I_12` | Fréquence finale pendant recherche point de référence | Hz | R/W (Code 121) |
| `D_I_13` | Capacité de réserve Eco | % | R/W (Code 121) |
| `D_I_14` | Capacité de réserve Power | % | R/W (Code 121) |
| `D_I_15` | Débit nominal | m³/h | R/W (Code 121) |
| `D_I_16` | Taux d‘impulsions compteur eau douce | l/Imp | R/W (Code 121) |
| `D_I_17` | Taux d‘impulsions compteur régénération | l/Imp | R/W (Code 121) |
| `D_I_18` | Valeur de consigne courant de chlore | mA | R (Code 121) |
| `D_I_20` | Charge | mAmin | R/W (Code 121) |

## 📐 Intervalles des étapes (Code 302)

| ID Paramètre | Désignation | Unité | Accès |
|:---|:---|:---:|:---:|
| `D_J_1` | étapes point de référence - lavage | Steps | R/W (Code 302) |
| `D_J_3` | étapes lavage - fonctionnement | Steps | R/W (Code 302) |
| `D_J_4` | étapes fonctionnement - appoint cuve de sel | Steps | R/W (Code 302) |
| `D_J_5` | étapes appoint cuve de sel - saumurage | Steps | R/W (Code 302) |
| `D_J_6` | étapes saumurage - refoulement | Steps | R/W (Code 302) |
| `D_J_7` | étapes refoulement - rétrolavage | Steps | R/W (Code 302) |
| `D_J_8` | étapes rétrolavage - position de retour | Steps | R/W (Code 302) |
| `D_J_9` | étapes recherche point de référence | Steps | R/W (Code 302) |

## 🔒 Compteurs & Débit détaillé (Code 245)

| ID Paramètre | Désignation | Unité | Accès |
|:---|:---|:---:|:---:|
| `D_K_3` | Débit valeur de pointe | m³/h | R (Code 245) |
| `D_K_4` | Compteur horaire dépassement débit nominal | h | R (Code 245) |
| `D_K_5` | Courant de chlore | mA | R (Code 245) |
| `D_K_6` | Affichage des étapes vanne de transfert | Steps | R (Code 245) |
| `D_K_7` | Affichage des étapes vanne de régénération | Steps | R (Code 245) |
| `D_K_8` | Chiffre de capacité de consommation | m³×°dH | R (Code 245) |
| `D_K_9` | Consommation moyenne des 3 derniers jours | m³ | R (Code 245) |
| `D_K_11` | Paramètres avec la dernière modification des réglages |  | R (Code 245) |
| `D_K_14` | Valeur de pointe AT1 | m³/h | R (Code 245) |
| `D_K_15` | Dépassement débit nominal AT1 | Min. | R (Code 245) |
| `D_K_16` | Valeur de pointe AT2 | m³/h | R (Code 245) |
| `D_K_17` | Dépassement débit nominal AT2 | Min. | R (Code 245) |

## 🔒 Volumes d'eau (Code 005)

| ID Paramètre | Désignation | Unité | Accès |
|:---|:---|:---:|:---:|
| `D_K_18` | Volume eau douce AT1 | m³ | R (Code 005) |
| `D_K_19` | Volume eau douce AT2 | m³ | R (Code 005) |
| `D_K_20` | Volume eau brute mélange | m³ | R (Code 005) |
| `D_K_21` | Volume d'appoint | l | R (Code 005) |

## ⚠️ Mémoire de défauts (Code 245)

| ID Paramètre | Désignation | Unité | Accès |
|:---|:---|:---:|:---:|
| `D_K_10_1` | mémoire de défauts(1) |  | R (Code 245) |
| `D_K_10_2` | mémoire de défauts(2) |  | R (Code 245) |
| `D_K_10_3` | mémoire de défauts(3) |  | R (Code 245) |
| `D_K_10_4` | mémoire de défauts(4) |  | R (Code 245) |
| `D_K_10_5` | mémoire de défauts(5) |  | R (Code 245) |
| `D_K_10_6` | mémoire de défauts(6) |  | R (Code 245) |
| `D_K_10_7` | mémoire de défauts(7) |  | R (Code 245) |
| `D_K_10_8` | mémoire de défauts(8) |  | R (Code 245) |
| `D_K_10_9` | mémoire de défauts(9) |  | R (Code 245) |
| `D_K_10_10` | mémoire de défauts(10) |  | R (Code 245) |
| `D_K_10_11` | mémoire de défauts(11) |  | R (Code 245) |
| `D_K_10_12` | mémoire de défauts(12) |  | R (Code 245) |
| `D_K_10_13` | mémoire de défauts(13) |  | R (Code 245) |
| `D_K_10_14` | mémoire de défauts(14) |  | R (Code 245) |
| `D_K_10_15` | mémoire de défauts(15) |  | R (Code 245) |
| `D_K_10_16` | mémoire de défauts(16) |  | R (Code 245) |

## 📈 Historique consommation eau (D_Y_2_x)

| ID Paramètre | Désignation | Unité | Accès |
|:---|:---|:---:|:---:|
| `D_Y_2_1` | Consommation eau il y a 1 jour(s) | l | R |
| `D_Y_2_2` | Consommation eau il y a 2 jour(s) | l | R |
| `D_Y_2_3` | Consommation eau il y a 3 jour(s) | l | R |
| `D_Y_2_4` | Consommation eau il y a 4 jour(s) | l | R |
| `D_Y_2_5` | Consommation eau il y a 5 jour(s) | l | R |
| `D_Y_2_6` | Consommation eau il y a 6 jour(s) | l | R |
| `D_Y_2_7` | Consommation eau il y a 7 jour(s) | l | R |
| `D_Y_2_8` | Consommation eau il y a 8 jour(s) | l | R |
| `D_Y_2_9` | Consommation eau il y a 9 jour(s) | l | R |
| `D_Y_2_10` | Consommation eau il y a 10 jour(s) | l | R |
| `D_Y_2_11` | Consommation eau il y a 11 jour(s) | l | R |
| `D_Y_2_12` | Consommation eau il y a 12 jour(s) | l | R |
| `D_Y_2_13` | Consommation eau il y a 13 jour(s) | l | R |
| `D_Y_2_14` | Consommation eau il y a 14 jour(s) | l | R |
| `D_Y_2_15` | Consommation eau il y a 15 jour(s) | l | R |
| `D_Y_2_16` | Consommation eau il y a 16 jour(s) | l | R |
| `D_Y_2_17` | Consommation eau il y a 17 jour(s) | l | R |
| `D_Y_2_18` | Consommation eau il y a 18 jour(s) | l | R |
| `D_Y_2_19` | Consommation eau il y a 19 jour(s) | l | R |
| `D_Y_2_20` | Consommation eau il y a 20 jour(s) | l | R |
| `D_Y_2_21` | Consommation eau il y a 21 jour(s) | l | R |
| `D_Y_2_22` | Consommation eau il y a 22 jour(s) | l | R |
| `D_Y_2_23` | Consommation eau il y a 23 jour(s) | l | R |
| `D_Y_2_24` | Consommation eau il y a 24 jour(s) | l | R |
| `D_Y_2_25` | Consommation eau il y a 25 jour(s) | l | R |
| `D_Y_2_26` | Consommation eau il y a 26 jour(s) | l | R |
| `D_Y_2_27` | Consommation eau il y a 27 jour(s) | l | R |

## 📈 Historique consommation sel (D_Y_3_x)

| ID Paramètre | Désignation | Unité | Accès |
|:---|:---|:---:|:---:|
| `D_Y_3_1` | Consommation sel il y a 1 jour(s) | kg | R |
| `D_Y_3_2` | Consommation sel il y a 2 jour(s) | kg | R |
| `D_Y_3_3` | Consommation sel il y a 3 jour(s) | kg | R |
| `D_Y_3_4` | Consommation sel il y a 4 jour(s) | kg | R |
| `D_Y_3_5` | Consommation sel il y a 5 jour(s) | kg | R |
| `D_Y_3_6` | Consommation sel il y a 6 jour(s) | kg | R |
| `D_Y_3_7` | Consommation sel il y a 7 jour(s) | kg | R |
| `D_Y_3_8` | Consommation sel il y a 8 jour(s) | kg | R |
| `D_Y_3_9` | Consommation sel il y a 9 jour(s) | kg | R |
| `D_Y_3_10` | Consommation sel il y a 10 jour(s) | kg | R |
| `D_Y_3_11` | Consommation sel il y a 11 jour(s) | kg | R |
| `D_Y_3_12` | Consommation sel il y a 12 jour(s) | kg | R |
| `D_Y_3_13` | Consommation sel il y a 13 jour(s) | kg | R |
| `D_Y_3_14` | Consommation sel il y a 14 jour(s) | kg | R |

## 📈 Historique temps régénération (D_Y_4_x)

| ID Paramètre | Désignation | Unité | Accès |
|:---|:---|:---:|:---:|
| `D_Y_4_1` | Dernière régénération 1 (la plus récente) |  | R |
| `D_Y_4_2` | Dernière régénération 2 |  | R |
| `D_Y_4_3` | Dernière régénération 3 |  | R |
| `D_Y_4_4` | Dernière régénération 4 |  | R |
| `D_Y_4_5` | Dernière régénération 5 |  | R |
| `D_Y_4_6` | Dernière régénération 6 |  | R |
| `D_Y_4_7` | Dernière régénération 7 |  | R |
| `D_Y_4_8` | Dernière régénération 8 |  | R |
| `D_Y_4_9` | Dernière régénération 9 |  | R |
| `D_Y_4_10` | Dernière régénération 10 |  | R |
| `D_Y_4_11` | Dernière régénération 11 |  | R |
| `D_Y_4_12` | Dernière régénération 12 |  | R |
| `D_Y_4_13` | Dernière régénération 13 |  | R |
| `D_Y_4_14` | Dernière régénération 14 (la plus ancienne) |  | R |

## 📈 Capacités résiduelles régénération (D_A_3_2_x)

| ID Paramètre | Désignation | Unité | Accès |
|:---|:---|:---:|:---:|
| `D_A_3_2_1` | Régénération 1 – Capacité résiduelle | % | R |
| `D_A_3_2_2` | Régénération 2 – Capacité résiduelle | % | R |
| `D_A_3_2_3` | Régénération 3 – Capacité résiduelle | % | R |
| `D_A_3_2_4` | Régénération 4 – Capacité résiduelle | % | R |
| `D_A_3_2_5` | Régénération 5 – Capacité résiduelle | % | R |
| `D_A_3_2_6` | Régénération 6 – Capacité résiduelle | % | R |
| `D_A_3_2_7` | Régénération 7 – Capacité résiduelle | % | R |
| `D_A_3_2_8` | Régénération 8 – Capacité résiduelle | % | R |
| `D_A_3_2_9` | Régénération 9 – Capacité résiduelle | % | R |
| `D_A_3_2_10` | Régénération 10 – Capacité résiduelle | % | R |
| `D_A_3_2_11` | Régénération 11 – Capacité résiduelle | % | R |
| `D_A_3_2_12` | Régénération 12 – Capacité résiduelle | % | R |
| `D_A_3_2_13` | Régénération 13 – Capacité résiduelle | % | R |
| `D_A_3_2_14` | Régénération 14 – Capacité résiduelle | % | R |
| `D_A_3_4` | Dernière régénération AT2 | TT.MM.JJJJ HH:MM | R |
| `D_A_3_5` | Dernière régénération AT2 restante | % | R |

## 🔒 Détails échangeur 2 – MC32 seulement (Code 005)

| ID Paramètre | Désignation | Unité | Accès |
|:---|:---|:---:|:---:|
| `D_A_1_4` | Débit actuel AT2 | m³ | R (Code 005) |
| `D_A_1_5` | Capacité résiduelle AT2 | m³×°dH | R (Code 005) |
| `D_A_1_8` | Coefficient capacité AT2 | m³×°dH | R (Code 005) |
| `D_A_1_9` | Débit de mélange actuel | m³ | R (Code 005) |
| `D_A_2_4` | Durée/volume restant étape régén. AT2 |  | R (Code 005) |

---

> **Remarque :** Min. 15 secondes entre les requêtes. Max 1000 octets par requête+réponse.
