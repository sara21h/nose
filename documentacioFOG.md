#### SERVIDOR D'IMATGES 

- [x] FOG

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

> Primer de tot mirem què és FOG i per a què serveix.

###### Què és fog?

FOG és una solució de codi obert que permet gestionar imatges de disc en sistemes d'ordinadors. El seu objectiu és facilitar la implementació, la clonació i l'administració centralitzada d'imatges en múltiples ordinadors d'una xarxa. Això ofereix una manera eficient de crear, distribuir i restaurar imatges de sistemes operatius i programari en un gran nombre dordinadors.


| característiques |        
| ---------------- | 
| creació d'imatges (de discs de sistemes operatius i aplicacions instal·lades) | 
| distribució (facilita la distribució ràpida d'imatges de disc) | 
| restauració d'matges (permet restaurar imatges de disc, retornant-les a un estat previ a la configuració) | 
| administració centralitzada (ens proporciona una interficie web per administrar i controlar-ho tot) | 
| Programació de tasques (ens permet programar tasques d'implementació i clonació que es faiguin en x moment) | 


https://docs.fogproject.org/en/stable/installation/install_fog_server.html

(documentació, veiem que tenim varies guies)

![image](https://github.com/sara21h/nose/assets/113586105/01b7d7ac-7256-4a6a-92db-ed7cd0eb39c1)

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

> Ara passarem a l'instal·lació.

On el què he fet ha sigut seguir aquestes pàgines.

https://www.bujarra.com/instalando-fog/

https://docs.fogproject.org/en/stable/installation/install_fog_server.html

![image](https://github.com/sara21h/nose/assets/113586105/0124fc7f-1ac0-457f-af91-98d60da43442)

- Creem un servidor d'Ubuntu.
-  ![image](https://github.com/sara21h/nose/assets/113586105/278b8d6e-c2be-4209-a11b-222d6829a54e)

- Clonem el repositori del git:

![image](https://github.com/sara21h/nose/assets/113586105/7e261463-8ac4-402c-9863-ddf57b5c2f23)

![image](https://github.com/sara21h/nose/assets/113586105/eb7c74a3-0e2c-45fb-ac42-0524ebb1d04c)

- Anem a la carpeta del repositori clonat i executem el .sh.  

![image](https://github.com/sara21h/nose/assets/113586105/8f0e88f7-aeb5-41b4-8e2b-899a25706fb5)

![image](https://github.com/sara21h/nose/assets/113586105/8430df9b-3f94-41a3-ad3b-429264aaca47)

![image](https://github.com/sara21h/nose/assets/113586105/1661cced-46c1-4c24-ab86-f5884bdd2f00)

- Ara ens pregunta sobre la configuració a l'hora d'instal·lar

Primer seleccionem l'opció 2, ja que utilitzem Ubuntu.

![image](https://github.com/sara21h/nose/assets/113586105/8e854959-2a26-4115-9301-e2d03bd1cce3)

Ara seleccionarem N per a una instal·lació de servidor normal i també ens pregunta sobre altres paràmetres, com la IP, l'interficie..

![image](https://github.com/sara21h/nose/assets/113586105/2b561aa9-2a06-4107-b219-9a538a060db0)

![image](https://github.com/sara21h/nose/assets/113586105/6827427f-dbfa-4afa-a96b-45561739a69a)

Confirmem la configuració i començarem amb l'instal·lació.

![image](https://github.com/sara21h/nose/assets/113586105/3120d972-e740-4b1f-9ad1-0d99ad7f5064)

![image](https://github.com/sara21h/nose/assets/113586105/81ce32b4-b1c3-439c-aeb4-ce8d9dad7534)

![image](https://github.com/sara21h/nose/assets/113586105/b64424e2-ccd7-4311-9896-900f245edd19)

![image](https://github.com/sara21h/nose/assets/113586105/b2b8cab8-ad17-43e9-9682-832168b51d3a)

He tornat a fer l’instal·lació amb  una altra màquina on tinc posada xarxa nat i xarxa interna, seguint els mateixos passos que abans, ja que no em funcionava algo.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

> Una vegada hem fet l'instal·lació, entrarem a la web

Seria http://l'ip/fog/management

On l'usuari és fog i la contrasenya és password.

![image](https://github.com/sara21h/nose/assets/113586105/60195aeb-71a7-4d05-ac07-b0a037916ff8)

![image](https://github.com/sara21h/nose/assets/113586105/d1b1e045-01c7-46ff-8724-3a6a550a6aa1)

![image](https://github.com/sara21h/nose/assets/113586105/462ccfcd-ac66-40c6-987b-f04c38179957)

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

> Una vegada dins, el que volem fer és capturar l'imatge i instalar-la.

Aquestes 2 pàgines ens poden ajudar:

https://www.bujarra.com/fog-configuracion-base-generacion-de-imagen-despliegue/

https://docs.fogproject.org/en/stable/getting_started/capture_an_image.html

Ens surt un menú en opcions i anirem a images, on crearem una de nova, per a Ubuntu i per a Windows.

![image](https://github.com/sara21h/nose/assets/113586105/5df191c4-5c0e-4f2a-9eb9-9a9d88f32e3b)

![image](https://github.com/sara21h/nose/assets/113586105/b1b97287-05a9-4c89-b05f-6d2f1413b028)

(aquí a sistema operatiu és ubuntu*)

Les configurem com preferim, seleccionant el nom, el sistema operatiu, descripció, entre altes opcions.

![image](https://github.com/sara21h/nose/assets/113586105/3bea35da-0ddb-44c1-802e-191613b97ebc)

Després a list all images veiem les que tenim:

![image](https://github.com/sara21h/nose/assets/113586105/70862dbd-3e0e-4403-85ab-895b3a4b0522)

Per a que ens funcioni, hem de configurar la BIOS per a que arranqui per xarxa, configurem l'ordre d'arrancada:

![image](https://github.com/sara21h/nose/assets/113586105/5fb0b94a-2d23-40db-8c21-6c760781a23d)

I jo he seleccionat com a primera xarxa la xarxa NAT i la segona la xarxa interna.

![image](https://github.com/sara21h/nose/assets/113586105/30d07933-956b-4a0b-bd9e-8dd0f7ea004a)

Ens diu que el host no està registrat així que el registrem a perform full host registration and inventory:

![image](https://github.com/sara21h/nose/assets/113586105/3a974039-c6d4-4fcc-9da8-9f42ca3cd087)

Ens preguntarà coses i surt que ja està registrat.

![image](https://github.com/sara21h/nose/assets/113586105/57bd1716-91d5-4578-b471-ed8aeb912460)

I ara:

![image](https://github.com/sara21h/nose/assets/113586105/00790497-fd7f-4a0a-8a5c-9237c445c403)

Per instalar l'imatge:

![image](https://github.com/sara21h/nose/assets/113586105/57bd1716-91d5-4578-b471-ed8aeb912460)

Seleccionem l'imatge

![image](https://github.com/sara21h/nose/assets/113586105/85b997b4-e426-4312-aff0-5a1917b35912)

A la màquina Windows hem seleccionat la de Windows i a la d'Ubuntu la d'Ubuntu.

![image](https://github.com/sara21h/nose/assets/113586105/71aef174-d462-4198-bc3c-080da30d4a0d)

A configuració avançada, creem una tasca de captura del host:

![image](https://github.com/sara21h/nose/assets/113586105/34ba14dd-d3b3-4569-b81a-dd2eb1992563)

Ara quan es reinicie:

![image](https://github.com/sara21h/nose/assets/113586105/71aef174-d462-4198-bc3c-080da30d4a0d)








