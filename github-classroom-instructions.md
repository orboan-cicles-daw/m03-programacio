# Instruccions Github Classroom

Instruccions per a realitzar una activitat avaluable a través de github classroom:

**Nota: hauràs de tenir a mà el teu token de github**. Si no el tens, l'hauràs de crear i guardar-lo en un lloc fàcilment accessible per a tu.

[Cómo generar token personal en github](https://desarrolloweb.com/articulos/autenticar-github-personal-access-token)

**Instruccions pas a pas**:

1. Obre un navegador web i fes login a github. 
2. Entra a l'aula de Moodle i busca l'activitat avaluable a fer.
3. Hi trobaràs un enllaç: clica-hi.
4. Se t'obrirà un una nova pestanya una web de github preguntant-te si acceptes la tasca.
5. Si és la primera vegada que acceptes una tasca en aquest curs, hauràs de seleccionar-te a tu mateix d'una llista d'alumnes. Si no apareixes a la llista, la pots acceptar igualment.
6. Un cop acceptada la tasca, s'iniciarà un procés de clonatge del repositori original de la tasca, a una còpia que se't farà exclusivament per a tu (només tu i els professors hi tenen accés).
7. En finalitzar la clonació, tindràs al teu navegador una còpia del repositori amb l'enunciat de la tasca. **Important: NO has de fer CAP modificació en aquest repositori directament des de github**.
8. Obre el teu entorn de treball Entorn, obre-hi un terminal i crea el següent directori si encara no el tens:
```
$ mkdir -p /home/elteunomdusuari/m031/uf1
```
on ``elteunomdusuari`` és el teu nom d'usuari de l'Entorn (o de github), ``uf1`` indica la UF1 (canvia el número si la tasca correspon a una altra UF).

9. Entra dins del directori creat ``cd ~/m031/uf1``
10. Ves **al teu** repositori de github de la tasca (la teva còpia) i copia la URL (https).
11. **Estant dins de ``~/m031/uf1``** clona en local la teva còpia del repositori:
```
$ git clone https://github.com/xxxxx/nomdelrepo
```
12. En fer el clonatge en local se't crearà un directori anomenat ``nomdelrepo`` (essent el nom del repositori que correspongui a la tasca). Ara hauràs de tenir el repositori clonat en local en aquesta ruta:
```
/home/elteunomdusuari/m031/uf1/nomdelrepo
```
14. Des del navegador de fitxers de l'Entorn, obre el notebook corresponent a l'activitat.
15. Resol l'activitat.
16. Quan hagis finalitzat, guarda el notebook i executa en el terminal, **estant dins de ``~/m031/uf1/nomdelrepo``** les següents comandes:
```
$ git add .
$ git commit -m "tasca finalitzada"
$ git push origin main
```
**Nota**: en fer el ``git commit`` és possible que et demani que hagis de configurar el git amb les teves dades (les que tens a github) de la següent manera. Ho fas i després ja et deixarà fer el commit sense problema:

```
  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"
``` 

Quan facis el ``git push`` et demanarà auntenticar-te amb les teves credencials de github. Has de posar el teu nom d'usuari de github, i com a contrasenya **has de posar el teu token** (no la teva contrasenya de github).

**Ja està, no cal fer res més. Els professors ja poden accedir al teu repositori i corregir la teva activitat**.

**Nota**: si treballes amb Google collab enlloc de l'Entorn de l'Institut, has de tenir en compte el següent:

1. El clonatge en local (passes de 8 a la 12) l'has de fer en l'Ubuntu per a Windows que hi ha als PCs de l'aula.
2. Un cop fet el clonatge, has de pujar el fitxer notebook amb l'enunciat de l'activitat al Google Collab.
3. Resols l'activitat a Google Collab.
4. Un cop finalitzada, descarregues el fitxer i sobreescrius el que prèviament tenies en el repositori local.
5. Continues les instruccions a partir del punt 15.
