# Instal·lacio Owncloud

## Guia de instal·lacio

**Linux: Ubuntu 22.04LTS**

**Servidor web: Apache**

**Base de dades: MariaDB**

**PHP (versio 7.3 o 7.4)**


1 He fet que el meu nom de domini cambïi a OFL per a distengir el meu treball dels altres companys
```
sudo nano /etc/hostname
```
![Selecció_041](https://user-images.githubusercontent.com/114162334/193090537-64c39fc6-3eb3-4708-b794-413165184564.png)

2 Instal·lem el servidor Apache amb aquesta comanda

![Selecció_042](https://user-images.githubusercontent.com/114162334/193090544-3c6b7136-2b2a-48f7-986e-922ed360b81b.png)

3 Desactivem el llistat de directoris del servidor

![Selecció_043](https://user-images.githubusercontent.com/114162334/193090562-ecbb7adc-f329-4ea0-a24b-c55e561842ae.png)

4 Instal·lem MariaDB

![Selecció_044](https://user-images.githubusercontent.com/114162334/193090572-6fee5ba8-adb9-4be6-b7ae-956231664b59.png)
![68747470733a2f2f64756e67656f6e6f66626974732e636f6d2f696d616765732f6f776e636c6f7564312e6a7067](https://user-images.githubusercontent.com/114162334/195784774-e6b4ebe0-6633-4167-8eae-f18178768fb0.jpg)

5 Configurem la instal·lació

![Selecció_045](https://user-images.githubusercontent.com/114162334/193090581-3cc203b5-369b-4e9e-9988-4a1c80798751.png)

6 **Aqui tenim que ficar si o no depen el que pregunti**

- Deshabilitar usuaris anònims.

- Desactivar accés remot com a root.

- Eliminar les bases de dades de testeig i accedir-hi.

- Actualitzar les taules de privilegis.

![Selecció_046](https://user-images.githubusercontent.com/114162334/193090591-563a239c-81fc-442d-8062-2847ebdcb72e.png)

Finalment reiniciem el servidor MariaDB

![Selecció_047](https://user-images.githubusercontent.com/114162334/193090604-d948594e-aa35-4198-bf26-f34a1af9a950.png)

7 ## Crear la base de dades d'owncloud

**Aqui mhe deixat de fer una captura de una comanda que es per entrar a MariaDB**
```
- sudo mysql -u root -p
```
**Creem la base de dades**
```
- CREATE DATABASE owncloud;
```
**Creem un usuari que es digui ownclouduser amb una contrasenya, per exemple Admin1234** 
```
- CREATE USER 'ownclouduser'@'localhost' IDENTIFIED BY 'Admin1234';
```
**Us donem accés a l'usuari a la base de dades creada**
```
- GRANT ALL ON owncloud.* TO 'ownclouduser'@'localhost' IDENTIFIED BY 'Admin1234' WITH GRANT OPTION;
```
**Apliquem els canvis i sortim**
```
- FLUSH PRIVILEGES;

- EXIT;
```
## 8 Instal·lar PHP i els seus mòduls necessaris:
```
sudo apt-get install software-properties-common -y
```
![Selecció_048](https://user-images.githubusercontent.com/114162334/193090616-6a665579-17ea-42f5-be01-2d7a5ec0f443.png)

9 Actualitzem els paquets amb el repositori afegit
![Selecció_051](https://user-images.githubusercontent.com/114162334/193092740-0e4a7903-a743-486d-b962-3f543c761105.png)

Instal·lem PHP i els mòduls necessaris
Hem de tenir en compte els requisits d'Owncloud abans d'instal·lar els mòduls.
![Selecció_050](https://user-images.githubusercontent.com/114162334/193090629-09e16a84-23b2-477b-8cbd-71e6329bb53d.png)

10 Després de la instal·lació editem el fitxer php.ini i canviarem alguns valors

Jo he ficat gedit per el simple fet de que es molt mes facil trobar la informacio 
![Selecció_035](https://user-images.githubusercontent.com/114162334/193079572-33825bf8-e9af-4dbb-9078-47b71edf94f7.png)

11 **Tenim que cambiar aquestes coses a file_uploads**
```
On allow_url_fopen = On memory_limit = 256M upload_max_filesize = 100M display_errors = Off date.timezone = Europe/Madrid
``` 
![Selecció_034](https://user-images.githubusercontent.com/114162334/193079556-ef646df0-1820-4c2c-8ed7-da400c69fc26.png)

 ## 12 Instal·lem Owncloud:

Descarreguem la ultima versió del programa i descomprimim els fitxers, a més movem els fitxers d'Owncloud a "/var/www/html/owncloud".

![Selecció_036](https://user-images.githubusercontent.com/114162334/193079645-ce336612-f3b3-41df-9a70-3171aa3cbbb4.png)

13 Canviem propietari i permisos dels directoris d'owncloud. www-data per fer servir Apache, 755 perquè es pugui executar i llegir qualsevol usuari de Linux

![Selecció_037](https://user-images.githubusercontent.com/114162334/193079664-24edfba0-140c-44a9-a435-d744d01c0088.png)

![Selecció_038](https://user-images.githubusercontent.com/114162334/193079673-c1a4b5b8-6945-4aba-8d11-6ef33780b6b4.png)

![Selecció_039](https://user-images.githubusercontent.com/114162334/193079681-a12b7409-7d76-4516-abb1-5d7c43d077d3.png)

14 Ara fiquem al buscador localhost/owncloud

I ens surtira el owncloud per iniciar sesió

![Selecció_040](https://user-images.githubusercontent.com/114162334/193079692-c3383e3d-639c-467d-81e9-b0be88086af4.png)

Ara li fiquem la nostra ip i la adewça wheb dins de la carpeta config de owncloud amb aquesta comanda
```
sudo nano/var/www/html/owncloud/config/gonfig.php
```

![Selecció_171](https://user-images.githubusercontent.com/114162334/195617056-7a7f50b7-3cfe-47d0-98ea-d395116ff649.png)

I ara ens foncionara el oncloud personal

![Selecció_172](https://user-images.githubusercontent.com/114162334/195617080-f780894c-8b54-43d0-a2f2-34d390fc78af.png)


Expliqueu:

Què signifiquen a Apache les línies de configuració del fitxer owncloud.conf.

![68747470733a2f2f64756e67656f6e6f66626974732e636f6d2f696d616765732f6f776e636c6f7564312e6a7067](https://user-images.githubusercontent.com/114162334/195784901-1d83f3c1-ee2d-46f1-b432-a27156d55f50.jpg)

ServerAdmin admin@exemple.com: Identificador de l'admin.

DocumentRoot /var/www/html/owncloud: On l'owncloud està instal·lat

ServerName Dungeonofbits.com: Nom del servidor

ServerAlias www.dungeonofbits.com: Alias del servidor 

Alias /oncloud "/var/www/html/owncloud": Per a sapiger que /owncloud esta dins daquetes carpetes /var/www/html/owncloud.

<Directory /var/www/html/owncloud/>: El directori de Owncloud.

Options +Followsymlinks: controla la capacitat del servidor de seguir enllaços simbòlics

AllowOverride all: Facilita els canvis en la configuració, htaccess funcionin.

Require all granted: Significa que todos pueden acceder al directorio /var/www/html/owncloud

Dav off: Desactiva el dav.

SetEnv HOME /var/www/html/owncloud: Fa que el HOME sigui /var/www/html/owncloud

ErrorLog ${APACHE_LOG_DIR}/erroro.log: conté missatges informatius, advertències i informació sobre esdeveniments crítics.

CustomLog ${APACHE_LOG_DIR}/access.log combined: és una llista de totes les sol·licituds de fitxers individuals

### Què fa la comanda a2ensite?

-Activa una pagina web

### I la comando a2dissite?

-Desactiva la pagina web

### Què significa la línia de /etc/hosts

127.0.0.1 owncloud.XYZ.com

Es per a fer una conecsio entre la ip una direcció

