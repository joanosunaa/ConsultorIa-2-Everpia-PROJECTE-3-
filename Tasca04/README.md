## 4. Integració de Client (Client Ubuntu Desktop)

ID
Descripció de la Tasca
Detalls de la Configuració
## T.CLI.01
Instal·lació del Client.
Instal·lar un client Ubuntu Desktop i configurar la interfície de xarxa per comunicar-se amb el servidor (Host-Only).
- hem de configurar els adaptadords primer de tot
![captura1](img/capt1.png)



![captura2](img/capt2.png)


## T.CLI.02
Resolució de Noms.
Configurar l'arxiu d'hosts del client per resoldre l'adreça IP del servidor a server.innovatechXX.test. S'ha de proporcionar una instantània (snapshot) de la màquina client un cop fet el canvi.

![captura3](img/capt3.png)


## T.CLI.03
Validació de la Connectivitat LDAP.
Comprovar la connectivitat amb el servidor fent una consulta ldapsearch des del client.

![captura4](img/capt4.png)


## T.CLI.04
Mòduls d'Autenticació.
Instal·lar els mòduls necessaris per permetre l'autenticació amb LDAP.
![captura5](img/capt5.png)


![captura6](img/capt6.png)


![captura7](img/capt7.png)


![captura8](img/capt8.png)


![captura9](img/capt9.png)


![captura10](img/capt10.png)


## T.CLI.05
Configuració del Client.
Modificar els arxius de configuració del client necessaris. S'han de mostrar clarament els canvis realitzats en el codi dels arxius.

![captura11](img/capt11.png)


![captura12](img/capt12.png)


![captura13](img/capt13.png)


![captura14](img/capt14.png)





## T.CLI.06
Comprovació del Sistema.
Reiniciar els serveis i verificar amb la comanda getent passwd que els usuaris del directori són visibles localment.


![captura15](img/capt15.png)



## T.CLI.07
Prova d'Accés Final.
Reiniciar el client i iniciar sessió amb l'usuari tech01. Es requereix una captura de pantalla que demostri l'accés correcte i la creació automàtica de la carpeta personal de l'usuari.

![captura16](img/capt16.png)


