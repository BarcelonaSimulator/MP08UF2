# Activitat 4:

## Gestió d'usuaris:

Hi ha dos tipus d'usuaris, els admins amb permissos per gestionar Owncloud i els usuaris normals.

On fica resposta afegeix una captura de pantalla on es vegi que has fet l'acció que es demana.

**Aquesta part de la pràctica la feu amb un company/a, li creeu un usuari i li doneu el vostre nom de domini d'Owncloud.**

Per a que pugui accedir necessitarà:

- La MV amb owncloud ha d'estar en mode "adaptador pont".
- El fitxer /etc/hosts del company ha de tenir la IP de la MV i el nom de domini de la MV del company/a.


**4.1.-** Crea un usuari admin que es digui adminXYZ, on XYZ són les inicials del teu nom:

**RESPOSTA**

![Selecció_238](https://user-images.githubusercontent.com/114162334/196974464-9ad518a6-f506-49f5-be60-fe4590c386ac.png)

**4.2.-** Inicia sessió com a l'usuari adminXYZ.

**RESPOSTA**

![Selecció_239](https://user-images.githubusercontent.com/114162334/196974547-3ed64b28-36d9-469d-8e18-b10ad7f930ee.png)

**4.3.-** Crea un usuari XYZ on XYZ son les inicials del company/a i afegeix-lo al grup usuaris, aquest usuari tindrà una quota de 512 MB.

**RESPOSTA**

![Selecció_239](https://user-images.githubusercontent.com/114162334/196975855-06b0e8cb-0d93-4550-b09a-c01a5989f31d.png)

![Selecció_240](https://user-images.githubusercontent.com/114162334/196975876-068c423b-2462-42d8-a81f-2199dffdfb1c.png)

**4.4.-** Podem crear fitxers d'una mida determinada a Linux amb la comanda:

```
truncate -s 10M file.txt
```
A l'exemple es crea un fitxer de 10MB.

![Selecció_241](https://user-images.githubusercontent.com/114162334/196982076-a8e72708-fcd7-4e40-86cd-481cda83ceca.png)

Crea 6 fitxers de 100MB i pujal's a Owncloud un per un.

**RESPOSTA**

![Selecció_242](https://user-images.githubusercontent.com/114162334/196982260-a1038992-f064-46bb-93fd-426a2a11fdde.png)

**4.5.-** Mostra el missatge d'error per haver superat la quota d'usuari.

**RESPOSTA**

![Selecció_243](https://user-images.githubusercontent.com/114162334/196982842-2ea46961-fc34-45b1-b8d2-280b5ef59edb.png)

![Selecció_244](https://user-images.githubusercontent.com/114162334/196987003-6fd6b296-4f4e-45c0-8190-a4c4f39ae563.png)

**4.6.-** Busca al teu perfil quin percentatge de quota estas utilitzant.

**RESPOSTA**

![Selecció_245](https://user-images.githubusercontent.com/114162334/196987205-1801db9e-f9f1-4461-9426-37f6fa7ea1e6.png)

**4.7.-** Canvia la quota de l'usuari a 1GB i mostra tots els fitxers pujats.

**RESPOSTA**

![Selecció_246](https://user-images.githubusercontent.com/114162334/196987598-4bae38d3-6f1d-4dbd-b572-39abd385596c.png)

**4.8.-** Crea un usuari anomenat usuari2XYZ i fical al grup usuaris.

**RESPOSTA**

![Selecció_247](https://user-images.githubusercontent.com/114162334/196991981-1a77f167-3fe7-410a-ae88-f845d97bd1f1.png)

**4.9.-** Comparteix un fitxer de usuariXYZ a usuari2XYZ i mostra com l'usuari2XYZ pot veure i descarregar el fitxer.

**RESPOSTA**

**4.10.-** Esborra la carpeta Learn more about owncloud.

**RESPOSTA**

**4.11.-** Recupera la carpeta Learn more about owncloud.

**RESPOSTA**

**4.12.-** Com a usuariXYZ crea una carpeta nova anomenada shared i comparteix-la amb l'usuari usuari2XYZ.

**RESPOSTA**

**4.13.-** Entra a Market instal·la dues aplicacions que no estiguin ja instal·lades i explica què fan i com funcionen.

![image](https://user-images.githubusercontent.com/110727546/196159706-705ff624-c409-4632-acb4-f43ffcc486d4.png)

**RESPOSTA PRIMERA APP**

**RESPOSTA SEGONA APP**

**4.14.-** Crearem una carpeta nova per emmagatzematge a Owncloud, la carpeta serà /media/publicXYZ on XYZ són les teves inicials i apareixerà amb el nom de public als usuaris.

Aquesta carpeta haurà de pertànyer a l'usuari www-data.

**RESPOSTA**

**4.15.-** Connectarem la carpeta publicXYZ com emmagatzematge local, tal i com s'indica [aquí](https://doc.owncloud.com/server/next/admin_manual/configuration/files/external_storage/local.html). Tots els usuaris tindran accés a la carpeta.

**RESPOSTA**

**4.16.-** Un usuari normal pujarà un fitxer a la carpeta public.

**RESPOSTA**

**OPCIONAL.-** Aquesta tasca és opcional.

Intenta connectar com a emmagatzematge extern el teu compte de Google Drive de l'Institut. Tens com fer-ho [aquí](https://doc.owncloud.com/server/next/admin_manual/configuration/files/external_storage/google.html).

**RESPOSTA**
