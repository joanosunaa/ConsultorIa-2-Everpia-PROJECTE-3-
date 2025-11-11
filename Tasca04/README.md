# T04: Serveis de directori — LDAP

## Breu descripció

**Innovatech**, una start-up tecnològica emergent, està experimentant un ràpid creixement i pateix un caos en la gestió dels seus usuaris i accessos.

Actualment, cada servei intern (servidor de fitxers, wiki de documentació, etc.) utilitza la seva pròpia base de dades d'usuaris i contrasenyes i, a més, als ordinadors clients s’usa autentificació local. Això genera diversos problemes crítics:

- **Ineficiència Operativa:** Cal crear o eliminar comptes manualment a diversos sistemes.
- **Risc de Seguretat:** Reutilització de contrasenyes entre serveis.
- **Manca d'Escalabilitat:** Dificultat per gestionar nous serveis.

El CEO d’Innovatech ha contactat amb **EverPia** per implementar una solució d’autenticació centralitzada utilitzant **OpenLDAP (Lightweight Directory Access Protocol)**, una solució robusta i de codi obert compatible amb GNU/Linux.

La missió és implementar el servei OpenLDAP en un servidor Linux: instal·lar el servei, configurar el domini base, crear la jerarquia d’unitats organitzatives, integrar usuaris i grups, i configurar un client perquè utilitzi el directori per autenticar-se.



## Configuració Principal

| ID | Descripció del Requeriment | Configuració Requerida |
|----|-----------------------------|--------------------------|
| R.INF.01 | Configuració de la màquina Server (Server Hostname). | `server.innovatechXX.test` |
![captura1](img/capt1.png)                                
| R.INF.02 | Interfície de Xarxa Pública. | NAT (Per accés a Internet i descàrrega de paquets). |
![captura2](img/capt2.png) 
| R.INF.03 | Interfície de Xarxa Privada. | Host-Only (Per comunicació privada amb el client virtual i la màquina física). |
 ![captura3](img/capt3.png)


## 3. Tasques d'Implementació i Configuració del Servidor LDAP

### 3.1 Instal·lació i Configuració Base d'OpenLDAP

| ID | Descripció de la Tasca | Detalls de la Configuració |
|----|-------------------------|-----------------------------|
| T.LDAP.01 | Instal·lació del servei OpenLDAP. | Mostrar el resultat de la comanda `slapcat` per validar la instal·lació base. |
![captura4](img/capt4.png)
| T.LDAP.02 | Configuració de la base de dades. | Nom del Domini: `innovatechXX.test`<br>Contrasenya: `p@ssw0rd` |
![captura5](img/capt5.png)
| T.LDAP.03 | Configuració de la contrasenya d’administrador. | Contrasenya: `p@ssw0rd`.<br>Acceptar l’eliminació de la base de dades existent i fer un backup automàtic. |
![captura6](img/capt6.png)
![captura7](img/capt7.png)
![captura8](img/capt8.png)
| T.LDAP.4 | Creació d’Unitats Organitzatives (OU) inicials. | Crear dues OUs: `users` i `groups` mitjançant un fitxer `.ldif`. |
![captura9](img/capt9.png)
![captura10](img/capt10.png)
| T.LDAP.05 | Validació de les Unitats Organitzatives. | Executar `ldapsearch -xLLL -b "dc=innovatechXX,dc=test"` per comprovar les OUs creades. |
![captura11](img/capt11.png)
![captura12](img/capt12.png)
![captura13](img/capt13.png)

### 3.2 Gestió i Administració (LAM)

| ID | Descripció de la Tasca | Detalls de la Configuració |
|----|-------------------------|-----------------------------|
| T.LAM.01 | Instal·lació del Gestor d'Usuaris LDAP (LAM). | Executar `sudo apt install ldap-account-manager -y`.<br>Accedir via navegador a `https://192.168.56.101/lam`. |
![captura14](img/capt14.png)
![captura15](img/capt15.png)
![captura16](img/capt16.png)
| T.LAM.02 | Accés Remot i Configuració. | Accedir des de la màquina física mitjançant la IP Host-Only.<br>Configuració inicial amb contrasenya `lam`. |
![captura17](img/capt17.png)
![captura18](img/capt18.png)
![captura19](img/capt19.png)
| T.LAM.03 | Configuració per defecte. | Definir OUs per defecte: `users` i `groups`.<br>Modificar els camps `LDAP suffix` a les seccions corresponents i desar els canvis. |
![captura20](img/capt20.png)
![captura21](img/capt21.png)
| T.LAM.04 | Creació de Grups. | Crear dos grups de seguretat: `tech` i `manager`. |
![captura22](img/capt22.png)
![captura23](img/capt23.png)
![captura24](img/capt24.png)
| T.LAM.05 | Creació d'Usuaris de Prova. | Crear usuaris `tech01` (membre de `tech`) i `manager01` (membre de `manager`). |
![captura25](img/capt25.png)



## 4. Integració de Client (Ubuntu Desktop)

| ID | Descripció de la Tasca | Detalls de la Configuració |
|----|-------------------------|-----------------------------|
| T.CLI.01 | Instal·lació del Client. | Instal·lar Ubuntu Desktop i configurar interfície Host-Only. |  
![captura26](img/capt26.png)                             ![captura27](img/capt27.png)
| T.CLI.02 | Resolució de Noms. | Afegir al fitxer `/etc/hosts` la IP del servidor associada a `server.innovatechXX.test`. |
![captura28](img/capt28.png)
| T.CLI.03 | Validació de la Connectivitat LDAP. | Provar connexió amb `ldapsearch` des del client. |
![captura29](img/capt29.png)
| T.CLI.04 | Mòduls d'Autenticació. | Instal·lar els mòduls necessaris per a l’autenticació LDAP. |
![captura30](img/capt30.png)
![captura31](img/capt32.png)
![captura33](img/capt33.png)
![captura34](img/capt34.png)
![captura50](img/capt50.png)
| T.CLI.05 | Configuració del Client. | Modificar els arxius de configuració i documentar els canvis realitzats. |
![captura36](img/capt36.png)
![captura39](img/capt39.png)
![captura40](img/capt40png)

| T.CLI.06 | Comprovació del Sistema. | Executar `getent passwd` per verificar usuaris LDAP visibles localment. |
![captura41](img/capt41.png)
| T.CLI.07 | Prova d'Accés Final. | Reiniciar i iniciar sessió amb `tech01`. Verificar creació automàtica de la carpeta personal. |
![captura42](img/capt42.png)


