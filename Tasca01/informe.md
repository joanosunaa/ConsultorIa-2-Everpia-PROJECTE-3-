# Informe Tècnic: Avaluació de Gestors de Contrasenyes per al Personal Tècnic

##  Introducció i Justificació

Recentment, EverPia ha patit una **fuita de dades** causada per l’ús d’una **contrasenya feble i reutilitzada**.  
Aquesta situació ha exposat informació crítica i ha posat en risc la continuïtat del negoci.

### Riscos de contrasenyes febles o reutilitzades

1. **Atacs de diccionari:** Els ciberdelinqüents proven milions de combinacions comunes com “123456” o “password”.
2. **Credential stuffing:** Si una contrasenya s’utilitza en diversos serveis, una filtració en un pot permetre l’accés a tots els altres.
3. **Phishing i enginyeria social:** Les contrasenyes senzilles són fàcils d’endevinar o d’obtenir mitjançant correus fraudulents.
4. **Pèrdua de dades i sancions:** Un compte compromès pot donar accés a dades sensibles, provocant multes i danys reputacionals.

### Funció d’un gestor de contrasenyes

Un gestor de contrasenyes permet:
- Generar contrasenyes úniques i complexes.
- Emmagatzemar-les de manera **xifrada**.
- Sincronitzar-les entre dispositius de forma segura.
- Evitar la reutilització i l’oblit de contrasenyes.


##  Comparativa Tècnica

| **Característica** | **Bitwarden (Online / Núvol)** | **KeePassXC (Offline / Escriptori)** |
|---------------------|--------------------------------|-------------------------------------|
| **Model de seguretat** | Xifratge d'extrem a extrem  | Xifratge local d’arxiu KDBX  |
| **Emmagatzematge** | Núvol servidors propis  | Local  |
| **Accés multidispositiu** | Sí  | Sí |
| **Cost / Model freemium** | Gratuït + premium (~10 €/any) | Gratuït i codi obert |
| **Codi obert** | Sí, auditat | Sí, comunitari |
| **Sincronització automàtica** | Sí, via núvol | No nativa |
| **Facilitat d’ús** | Interfície moderna i intuïtiva | Més tècnica, per usuaris avançats |
| **Autenticació en dos passos** | Sí | Limitada |
| **Portabilitat** | Alta  | Mitjana  |


##  Avantatges i Inconvenients

### 🔹 Bitwarden (Online / Núvol)
**Avantatges**
- Sincronització automàtica entre dispositius.
- Interfície moderna i fàcil d’utilitzar.
- Compatible amb 2FA i navegadors.
- Permet opció *self-hosted* (autogestionada).

**Inconvenients**
- Depèn d’internet o del servidor.
- Pot existir risc si el servidor és atacat (tot i el xifratge).
- Algunes funcions són de pagament.


### 🔹 KeePassXC (Offline / Escriptori)
**Avantatges**
- Control total de les dades (no depèn del núvol).
- 100% gratuït i de codi obert.
- Ideal per entorns sense connexió o molt segurs.

**Inconvenients**
- No té sincronització automàtica.
- Interfície menys intuïtiva.
- Risc de pèrdua de dades si no es fan còpies de seguretat.


##  Recomanació Final

Després de l’anàlisi, es recomana implementar **Bitwarden** com a gestor de contrasenyes per al personal tècnic d’EverPia.

### Justificació:
 Interfície intuïtiva i fàcil d’adoptar.  
 Sincronització automàtica entre dispositius.  
 Alt nivell de seguretat amb xifratge end-to-end i 2FA.  
 Possibilitat d’instal·lar un servidor intern (*self-hosted*) per mantenir el control de les dades.  
 Facilita la col·laboració i el treball en equip amb credencials compartides de manera segura.


**Data:** 20 d’octubre de 2025  




