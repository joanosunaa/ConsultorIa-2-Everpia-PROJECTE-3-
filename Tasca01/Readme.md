# 🧠 Tasca 01: Gestor de Contrasenyes

## 🧩 Fase 1: Anàlisi i Justificació 

###  Introducció i Justificació
Riscos de contrasenyes febles o reutilitzades

1. **Atacs de diccionari:** Els ciberdelinqüents proven milions de combinacions comunes com “123456” o “password”.
2. **Credential stuffing:** Si una contrasenya s’utilitza en diversos serveis, una filtració en un pot permetre l’accés a tots els altres.
3. **Phishing i enginyeria social:** Les contrasenyes senzilles són fàcils d’endevinar o d’obtenir mitjançant correus fraudulents.
4. **Pèrdua de dades i sancions:** Un compte compromès pot donar accés a dades sensibles, provocant multes i danys reputacionals.

### Funció d’un gestor de contrasenyes

Un gestor de contrasenyes permet:
- Generar contrasenyes úniques i complexes.
- Emmagatzemar-les de manera **xifrada**.
- Sincronitzar-les entre dispositius de forma segura.
- Evitar la reutilització i l’oblit de contrasenyes

### Comparativa Tècnica
Realitzeu una **taula comparativa detallada** entre:

**Bitwarden (Alternativa Online / Núvol):**
- Sincronització entre dispositius.
- Model de seguretat (*xifratge end-to-end*).
- Facilitat d'accés multi-dispositiu.
- Cost / model freemium.

**KeePassX / KeePassXC (Alternativa Offline / Escriptori):**
- Emmagatzematge local de l'arxiu (KDBX).
- Independència del núvol.
- Model *open source*.
- Portabilitat de l'arxiu.

### 🔹 Avantatges i Inconvenients
Resumiu els principals **pros i contres de cada model (online vs offline)** des del punt de vista de:
- Seguretat
- Usabilitat
- Continuïtat del negoci

### 🔹 Recomanació
Concloeu l’informe escollint **l’eina més adequada** per al personal tècnic de l’empresa i **justifiqueu la vostra elecció.**

---

## 🧭 Fase 2: Guia d'Ús Tècnica (Manual Operatiu)

Utilitzant l’eina seleccionada a la Fase 1 (**Bitwarden**, **KeePassX**, o similar), heu de crear una **Guia d’Ús per a l’Equip Tècnic**, amb captures de pantalla i passos detallats.

### Contingut obligatori:

1. **Instal·lació i Configuració Inicial**
   - Descàrrega, instal·lació i creació del compte mestre o BBDD principal.

2. **Generació de Contrasenyes Segures**
   - Com utilitzar el generador de contrasenyes (longitud, caràcters especials, etc.).

3. **Exemples d'Ús i Emplenament Automàtic**
   - Com desar una credencial d’un compte de correu electrònic.
   - Com desar una credencial d’una aplicació o servei web.
   - Com utilitzar l’extensió del navegador per emplenar automàticament.

4. **Gestió de Còpies de Seguretat (Backup)**
   - Com fer una còpia de seguretat de l’arxiu (KDBX en KeePass o exportació en Bitwarden).
   - Recomanació per emmagatzemar la còpia de forma segura (clau USB xifrada o núvol xifrat).

---

## 📂 Estructura del lliurament

Dins del repositori del **projecte-3**, heu de crear una carpeta anomenada **`tasca01`**, que contingui:


