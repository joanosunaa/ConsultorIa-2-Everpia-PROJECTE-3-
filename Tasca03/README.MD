

## 🌐 T03 — Gestió flexible de discos (LVM i Storage Spaces)

📝 Descripció General

El bufet Garriga i Associats, un dels més prestigiosos de la ciutat, necessita modernitzar els seus sistemes d’emmagatzematge per garantir que la seva informació legal sensible tingui:

- 🔒 Integritat

- ♻️ Alta disponibilitat i redundància

- 📈 Escalabilitat i gestió flexible

Com a tècnics d’Everpia, se’ns encarrega dissenyar, implementar i documentar dues solucions d’emmagatzematge:

- 💻 Linux → Gestió amb LVM

- 🪟 Windows → Gestió amb Espais d’emmagatzematge (Storage Spaces)

Tot es realitzarà amb màquines virtuals per crear una prova de concepte funcional.

- 🧩 Estructura del Projecte

La carpeta tasca03/ contindrà:

** Part 1 — Linux: LVM amb Zorin OS (o equivalent)**

🎯 Objectius

Implementar una solució basada en LVM, demostrant la seva alta disponibilitat, flexibilitat i capacitat d’expansió.

📌 Requisits i procediments a documentar
1️⃣ Configuració inicial

Crear dos discos de 10 GB i afegir-los com a PVs.

Crear un VG.

Crear un LV.

Formatejar-lo i afegir-lo a /etc/fstab per muntatge automàtic.

2️⃣ Alta disponibilitat

Implementar un mirror LVM (lvm_mirror) per protegir dades davant fallada de disc.

3️⃣ Instantànies (Snapshots)

Afegir dos discos addicionals de 10 GB al VG.

Crear LV lvm_dades.

Omplir-lo amb fitxers (p. ex. imatges).

Crear un snapshot lv_snapshot.

Documentar procés de restauració des del snapshot.

4️⃣ Escalabilitat

Ampliar el LV lvm_dades utilitzant espai lliure del VG.

🪟 Part 2 — Windows: Espais d’Emmagatzematge
🎯 Objectius

Mostrar com Windows 11 utilitza Storage Spaces per proporcionar redundància flexible i escalabilitat.

📌 Requisits i procediments a documentar
1️⃣ Configuració inicial

Crear un Storage Pool amb tres discos de 10 GB.

2️⃣ Estudi de configuracions de resiliència
⭐ Mirroring (2 discos)

Crear un Storage Space amb mirall simple.

Verificar alta disponibilitat.

⭐ Parity (3 discos)

Crear un Storage Space amb paritat.

Explicar l’eficiència comparada amb el mirall.

⭐ Triple Mirror

Afegir els discos necessaris.

Crear l'espai tolerant fins a dues fallades simultànies.

3️⃣ Gestió i monitoratge

  Mostrar la informació del pool, discos i espais des de la consola de Windows.

- 🧠 Metodologia de Treball
- 👥 Organització del grup

Dividir-se en equip Linux i equip Windows.

Cada membre prepara una guia prèvia personal (comandes, notes, documentació).

Cada parella realitza la implementació pràctica.

El grup complet revisa i valida tota la documentació.

Cada membre puja la tasca al seu repositori personal.

## Tasques:

-  [LINUX](Tasca03/linux.md)

-  [WINDOWS](Tasca03/windows.md)

