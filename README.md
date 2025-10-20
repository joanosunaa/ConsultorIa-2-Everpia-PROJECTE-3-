# 🧠 Informe Tècnic: Avaluació de Gestors de Contrasenyes per al Personal Tècnic

## 🔐 Introducció i Justificació

Recentment, **EverPia** ha patit una greu *fuita d’informació (data breach)* com a conseqüència de l’ús d’una **contrasenya feble o reutilitzada**. Aquest incident ha posat en risc informació confidencial i ha exposat la companyia a **xantatges i pèrdues econòmiques**.

### Riscos de contrasenyes febles o reutilitzades
L’ús de contrasenyes poc segures o repetides entre serveis suposa un risc crític per diversos motius:

- **Atacs de diccionari**: Els ciberdelinqüents proven milions de combinacions comunes (com “123456” o “password”) per accedir a comptes.
- **Credential stuffing**: Si una contrasenya és reutilitzada en diversos serveis, una filtració en un d’ells pot permetre l’accés a tots els altres.
- **Phishing i enginyeria social**: Les contrasenyes senzilles són fàcils de recordar, però també de descobrir.

Aquest tipus d’atacs poden comprometre **la seguretat global de l’empresa**, provocant pèrdua de dades, dany reputacional i sancions legals.

### Funció d’un gestor de contrasenyes
Un **gestor de contrasenyes** permet generar, emmagatzemar i gestionar de manera segura contrasenyes úniques i complexes per a cada compte.  
Les seves principals funcions són:

- 🔸 **Xifratge end-to-end**: Les dades s’emmagatzemen de manera xifrada, només accessibles amb la contrasenya mestra.  
- 🔸 **Generació automàtica** de contrasenyes robustes.  
- 🔸 **Sincronització segura** entre dispositius.  
- 🔸 **Eliminació de la reutilització** de contrasenyes.

---

## ⚙️ Comparativa Tècnica

| Característica | **Bitwarden (Online / Núvol)** | **KeePassXC (Offline / Escriptori)** |
|----------------|--------------------------------|--------------------------------------|
| **Model de seguretat** | Xifratge *end-to-end* (AES-256) | Xifratge local d’arxiu KDBX (AES-256) |
| **Emmagatzematge** | Núvol (servidors propis o autogestionats) | Local (fitxer KDBX al dispositiu) |
| **Accés multi-dispositiu** | Sí (web, app, extensió, mòbil) | Sí, però mitjançant còpia manual de l’arxiu |
| **Model Freemium / Cost** | Gratuït amb opcions premium (~10€/any) | Totalment gratuït i open source |
| **Codi obert** | Sí (Open Source, auditat) | Sí (Open Source, comunitari) |
| **Sincronització automàtica** | Sí, via núvol | No nativa (requereix serveis externs com Nextcloud o Dropbox) |
| **Facilitat d’ús** | Interfície moderna i intuïtiva | Més tècnica, enfocada a usuaris avançats |
| **Autenticació en dos passos (2FA)** | Sí | Limitada (depèn de l’usuari) |
| **Portabilitat** | Alta (web i app mòbil) | Mitjana (requereix transferir el fitxer manualment) |

---

## ⚖️ Avantatges i Inconvenients

### 🔹 Bitwarden (Online / Núvol)
**Avantatges:**
- Sincronització automàtica entre tots els dispositius.  
- Interfície amigable i fàcil d’aprendre.  
- Compatible amb 2FA i navegadors.  
- Disponible en versió *self-hosted* per a més control intern.

**Inconvenients:**
- Dependència d’internet o del servidor.  
- Possible risc si el servidor és compromès (encara que les dades estan xifrades).  
- Cost per a funcions avançades.

---

### 🔹 KeePassXC (Offline / Escriptori)
**Avantatges:**
- No depèn del núvol: màxim control local de les dades.  
- Totalment gratuït i open source.  
- Arxiu KDBX fàcil de transportar (USB, disc extern, etc.).  
- Ideal per a entorns sense connexió o amb requisits de seguretat estrictes.

**Inconvenients:**
- Sense sincronització automàtica nativa.  
- Interfície menys intuïtiva per a usuaris no tècnics.  
- Risc de pèrdua de l’arxiu si no es fan còpies de seguretat.

---

## 💡 Recomanació Final

Després d’analitzar les dues opcions, **es recomana implementar _Bitwarden_ com a gestor de contrasenyes per al personal tècnic d’EverPia**.

### Justificació:
- ✅ Facilita l’adopció gràcies a la seva **interfície intuïtiva** i la sincronització automàtica entre dispositius.  
- ✅ Ofereix **xifratge end-to-end** i autenticació en dos passos, garantint un alt nivell de seguretat.  
- ✅ Permet **autogestionar el servidor internament**, combinant els avantatges del núvol amb el control total sobre les dades.  
- ✅ És **compatible amb equips col·laboratius**, permetent compartir credencials de forma segura.

En conclusió, **Bitwarden és l’opció òptima per a una empresa com EverPia**, que necessita un equilibri entre **seguretat, usabilitat i gestió centralitzada** de credencials.

---

📅 **Data:** 20 d’octubre de 2025  
👨‍💻 **Autor:** Equip de Ciberseguretat - Consultora EverPia  

