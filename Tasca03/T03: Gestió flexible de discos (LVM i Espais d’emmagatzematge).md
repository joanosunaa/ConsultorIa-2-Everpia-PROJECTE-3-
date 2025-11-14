# 🪟 Solució d’Emmagatzematge a Windows amb **Storage Spaces**


# 1. Creació del Storage Pool

## ➤ 1.1 Afegir tres discos virtuals de 10 GB
Afegim tres discos des de la configuració de la màquina virtual.

[capt1](img/capt1.png)


## ➤ 1.2 Crear el Storage Pool
1. Obrim **Configuració** → *Espais d’emmagatzematge*.  
2. Seleccionem els tres discos nous.  
3. Creem el **Storage Pool inicial**.


[capt2](img/capt2.png)



#  2. Creació d’un espai amb **Mirall Doble**

## ➤ 2.1 Configuració del mirall doble
- Seleccionem **dos discos** del Storage Pool.
- Creem un nou espai amb:
  - 🔒 *Resiliència*: **Mirall**
  - 📏 *Mida*: **20 GB**


[capt3](img/capt3.png)



## ➤ 2.2 Verificació d’alta disponibilitat
1. Creem un arxiu dins del disc virtual.  
2. Apaguem la VM i eliminem físicament **un disc** del mirall.  
3. Reiniciem.

   
El sistema mostra una advertència però **l’arxiu continua disponible**.

 
[capt4](img/capt4.png)



#  3. Substitució del disc fallat

1. Afegim un nou disc a la VM.  
2. L’assignem al mateix Storage Pool.  
3. Windows el detecta i reconstrueix automàticament el mirall.

 *Així garantim que no hi ha pèrdua de dades.*


[capt5](img/capt5.png)



#  4. Creació d’un **Mirall Triple**

## ➤ 4.1 Esborrar l’espai anterior
Esborrem l’espai amb mirall doble per crear el nou espai.


[capt6](img/capt6.png)



## ➤ 4.2 Crear un nou espai amb **3 discos**
Configuració:
- 🔐 **Tipus:** Mirall triple  
- 🧩 **Discos:** 3  


[capt7](img/capt7.png)



##  Avantatges del Mirall Triple

| Configuració | Tolerància a fallades | Eficiència d'espai | Fiabilitat |
|--------------|------------------------|----------------------|------------|
| Mirall doble | 1 disc                 | 50%                 | Alta       |
| **Mirall triple** | **2 discos** | 33% | **Molt alta** |

🎯 Ideal per dades altament sensibles com les d’un bufet d’advocats.



#  5. Prova de resiliència del Mirall Triple

## ➤ 5.1 Eliminació de dos discos
Amb la VM apagada, eliminem **dos discos** del mirall triple.


[capt8](img/capt8.png)



## ➤ 5.2 Resultat de la prova
En reiniciar:
- No hi ha errors greus.  
- Les dades continuen disponibles.  
- L’estat del Storage Space mostra alertes, però es manté funcional.


[capt9](img/capt9.png)


#  6. Reconnectar els discos eliminats

Quan tornem a afegir els discos:
- Windows els detecta
- Comença la **reconstrucció automàtica**
- Tot el contingut reapareix correctament


[capt10](img/capt10.png)


#  7. Creació d’un espai amb **Paritat**

## ➤ 7.1 Configuració
Esborrem l’espai anterior i configurem un nou espai amb:
- 🔁 **Resiliència de paritat**
- Requereix **mínim 3 discos**
- Ideal per estalviar espai

 
[capt11](img/capt11.png)


## 💡 Avantatges de la *Paritat*

- 🧮 Molt més eficient en espai que el mirall
- 🔧 Tolerància a fallades moderada
- 📚 Perfecte per grans volums o backups

| Resiliència | Protecció | Eficiència | Ús recomanat |
|-------------|-----------|------------|--------------|
| Mirall doble | Alta | Baixa | Sistemes essencials |
| Mirall triple | Molt alta | Mitjana | Dades crítiques |
| **Paritat** | Mitjana | **Alta** | Emmagatzematge massiu |


#  8. Gestió del Storage Pool

Des de la consola podem veure:
- Estat dels discos (OK / Fallats)  
- Capacitat disponible  
- Avisos i alertes  
- Estat del pool  
- Necessitat de reconstrucció

  
[capt12](img/capt12.png)


#  Conclusions

La solució de **Windows Storage Spaces** ofereix:

✔️ Alta disponibilitat  
✔️ Protecció davant fallades de disc  
✔️ Escalabilitat senzilla  
✔️ Gestió centralitzada i intuïtiva  
✔️ Adaptació flexible (mirall, triple mirall, paritat)




