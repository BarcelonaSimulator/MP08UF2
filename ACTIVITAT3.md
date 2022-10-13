# Activitat 3:

Per fer aquesta activitat comptem amb que **ja s'ha configurat el servei Owncloud a
una Màquina Virtual** (MV).

**3.1.-** Llista els Virtual Hosts d'Apache per tal de veure si **owncloud.XYZ.com** 
està habilitat amb la comanda:
```
apache2ctl -S
``` 
![Selecció_173](https://user-images.githubusercontent.com/114162334/195623305-535de764-0cda-4236-8ed5-042f1dcc3abd.png)

**RESPOSTA**

**3.2.-** A Owncloud podem veure que hi ha una serie de carpetes per defecte,
mostra la ruta real a les tres carpetes dins de la teva MV.
```
/var/www/html/owncloud/core/skeleton
```
![Selecció_175](https://user-images.githubusercontent.com/114162334/195626823-1d997d83-6155-42a4-8636-f8cbab8abfcb.png)

**RESPOSTA**

**3.3.-** Al directori **Learn more about owncloud** hi ha informació en forma de fitxers pdf. Consulta'ls i respon aquestes preguntes:

- Quin són els tres tipus de protecció de dades que ofereix Owncloud?

Xifratge en trànsit

Xifratge en repòs 

Xifratge d'extrem a extrem.

- Fes una petita descripció de cada un d'ells.

Xifratge en trànsit: L'Owncloud per defecte porta HTTPS i té més nous els protocols TLS

Xifratge en repòs : Els arxius es guarden al Owncloud envés de guardar-los al disc dur per a obtenir més seguretat.

Xifratge d'extrem a extrem: Per a ningú pugui entrar als arxius encriptats, l'Owncloud utilitza el "end-to-end" ja que és la seguretat maxima de dades

- Per quina raó ens recomana utilitzar Owncloud per als documents de Microsoft Office de la nostra empresa?  
Per a que els documents no es perdin de ninguna forma.

- Això passa a tots els països?

Europa té una regulació GDPR, que són uns acords de protecció de dades. no tots utilitzen els mateixos acords, però en són senblants.

- Quina és la llicència d'OWncloud Enterprise?

Es una de les caracteristiques de Owncloud que et pots adequerir a 12 € al mes

- I la d'Owncloud Standard?

Es similar a l'enterprise però es mes varat uns 5 € i sense llicencia comercial.

- Es poden veure videos en Streaming directament des de Owncloud?

Si, es pot veure

- Es poden connectar directoris de Google Drive a Owncloud?

Es poden conectar entre ells

- I Dropbox?

Tambe es poden conectar

- Compta Owncloud amb antivirus? En cas afirmatiu com es diu? 

Si, te una extensió que es: Owncloud Anti-Virus extension.

**RESPOSTA**

**3.4.-** Mostra els següents canvis de paràmetres d'usuari:

- Posa't una imatge d'usuari.

![Selecció_177](https://user-images.githubusercontent.com/114162334/195633042-8ff8afea-d039-44bd-ba43-96db9e626c43.png)

- Afegeix el teu mail de l'Institut.

![Selecció_178](https://user-images.githubusercontent.com/114162334/195633462-bcd2223a-b961-4685-a348-136d8039a5ae.png)

- Canvia l'idioma a català.

![Selecció_179](https://user-images.githubusercontent.com/114162334/195633704-b3b7e7e5-5868-4924-887d-ff908968eaf9.png)

- Mostra la versió d'Owncloud instal·lada.

![Selecció_180](https://user-images.githubusercontent.com/114162334/195634131-a0f7e253-c812-4100-932f-5ae8c729eee8.png)

