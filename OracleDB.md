
![](Aspose.Words.2fccffd3-2e7f-4e39-9870-7065a2a0ade0.001.png)

ORACLE

Base de dades

25 DE MARZO DE 2024

UNAI CONUS

Victor Redel

![](Aspose.Words.2fccffd3-2e7f-4e39-9870-7065a2a0ade0.002.png)


#
![](Aspose.Words.2fccffd3-2e7f-4e39-9870-7065a2a0ade0.003.png)



Contenido

[Base de dades	2](#_heading=h.gjdgxs)

[Historia de la base de dades	2](#_heading=h.30j0zll)

[Suport	4](#_heading=h.1fob9te)

[Usos recomanats	4](#_heading=h.3t9kunz224xf)

[Versions de solució	6](#_heading=h.3znysh7)

[Comparativa	8](#_heading=h.2et92p0)

[Documentació d'instal·lació i configuració	10](#_heading=h.tyjcwt)

[Preparació Maquina	10](#_heading=h.3dy6vkm)

[Descàrrega del programari	10](#_heading=h.1t3h5sf)

[Instal·lació del SGBD	10](#_heading=h.rmnm3m6qdfdz)

[Configuració del Firewall i altres elements de seguretat	11](#_heading=h.2s8eyo1)

[Securització de la instal·lació	11](#_heading=h.17dp8vu)

[Instruccions d'arrencada, verificació d’estat i apagada de servei	11](#_heading=h.3rdcrjn)

[Fitxer de configuració	12](#_heading=h.26in1rg)

[Fitxers de dades	12](#_heading=h.lnxbz9)

[Ports d'escolta del servei de la base de dades i passos per canviar-los	12](#_heading=h.35nkun2)

[Connexió a la BD	12](#_heading=h.1ksv4uv)

[Tipus de SGBD	12](#_heading=h.44sinio)

[Classificació del sistema de gestió de bases de dades	12](#_heading=h.2jxsxqh)

[Enfocament i model de dades	13](#_heading=h.z337ya)


# <a name="_heading=h.gjdgxs"></a>Base de dades

## <a name="_heading=h.30j0zll"></a>Historia de la base de dades

La història de Oracle comença a 1977, quan Larry Ellison, Bob Miner i Ed Oates van fundar la companyia amb el nom de “SDL” (*Software Development Laboratories)*,  i temps després obtenen un contracte amb la CIA per a dissenyar un sistema especial de bases de dades amb el nom de “Oracle”. On més tard en l’any 1979, la companyia va canviar el seu nom a “*Relational Software Inc”*, posteriorment cambiada  com “Oracle”  després de l'èxit del producte insígnia de base de dades Oracle. 

En 1982 i buscant la coherència amb els seus objectius empresarials, *Relational Software Inc*  canvia de nom a “Oracle Corporation”. La companyia busca tenir un producte que fos compatible amb el SQL d'IBM, i a més enfocar-se en un mercat de les minicomputadoras, abastant així un segment que en aquell temps no li interessava a IBM. Més tard i finalment la empresa va adoptar el nom "Oracle Corporation" en 1982.

El següent any comença a comercialitzar Oracle V3, agregant el maneig de transaccions a través de les instruccions COMMIT i ROLLBACK.

Al 1985, surt Oracle V4 que  suporta consistència de lectura i en 1986 Oracle V5 comença a suportar el model client/servidor per a unir-se a l'auge de l'aparició de les xarxes. A més,  suporta l'execució de queries distribuïts. El mateix any 1986 va ser quan Oracle va començar a cotitzar en l'índex NASDAQ de la borsa de Nova York ( Estats Units)

En 1989 llancen al mercat el ERP de Oracle, conegut com Oracle Financials, la versió 6 del motor, que agrega un llenguatge procedural (Pl/Sql), bloqueig a nivell de fila i les possibilitats de fer suports sense la necessitat d'acabar els processos involucrats.

En 1992, per a convertir-se en una base de dades completa, apareix Oracle V7h, que inclueix el suport de la integritat referencial, l'emmagatzematge i execució de programes escrits en \*Pl/\*Sql dins del motor i la definició de triggers de base de dades.

En 1997, sent Internet ja una realitat i amb els nous paradigmes de programació començant a aparèixer per a intentar desplaçar als paradigmes imperatius, Oracle V8 comença a suportar desenvolupaments orientats a objectes i l'emmagatzematge i execució de contingut multimèdia.

En 1999 surt Oracle 8i per a estar a to amb els requeriments de la Internet. A més, el motor incorpora una Màquina Virtual Java (Java Virtual Machine) interna per a suportar l'emmagatzematge i execució de codi Java dins del motor.

Una vegada que Informix i Sybase van ser derrotats, Oracle va gaudir d'anys de domini de la indústria fins al lloc de Microsoft SQL Server a la fi dels 90 i l'adquisició d'IBM Informix Programari en 2001 per a complementar la seva base de dades DB2. Avui dia la principal competencia de Oracle per a les llicències de nova base de dades en UNIX, Linux i sistemes operatius de Windows està amb DB2 d'IBM, i amb Microsoft SQL Server.

En 2001, Oracle 9i trae más de 400 nuevas características incluyendo la habilidad de manipular documentos XML, opciones de alta disponibilidad, bases de datos en clúster. Un avance importante se hace sobre la definición de bases de datos virtuales (VPD), autenticación vía LDAP y en la autoadministración de la base de datos.

En 2003 Oracle  llança Oracle 10g, incorporant el maneig i administració de bases de dades Grid Computing, un conjunt de bases de dades l'administració d'espai de les quals, recursos i serveis poden administrar-se com si fossin una sola.

En 2018 la companyia va anunciar el llançament de Oracle Autonomous Database, considera la primera base de dades autònoma.
## <a name="_heading=h.1fob9te"></a>Suport

Pel que fa a les polítiques de suport, Oracle ofereix diferents nivells de suport per als seus productes, incloent-hi Oracle Database. Aquests nivells de suport son:

- Premier support
- Extended Support
- Sustaining Support

Per trobar més informació sobre les característiques que ofereix cada nivell de suport es recomana revisar la següent documentació oficial de oracle, on es troba el període de temps que dura el suport segons les llicències:

<https://www.oracle.com/a/ocom/docs/oracle-software-technical-support-policies-mx-esp.pdf>

## <a name="_heading=h.2555f7qxmfzb"></a><a name="_heading=h.3t9kunz224xf"></a>Usos recomanats

<a name="_heading=h.vwr020vcti3p"></a>La base de dades Oracle és una opció sòlida per a una àmplia gamma de casos d'ús degut a les seves característiques d'escalabilitat, gestió de dades, velocitat, optimització, seguretat etc.

És per això que Oracle es ideal per aquestes característiques:

- **Aplicacions de Missió Crítica:** Garanteix la disponibilitat i seguretat de dades en sistemes empresarials, financers i d'atenció mèdica.
- **Grans Volums de Dades:** Escalable i eficient per a emmagatzemar i processar grans quantitats de dades en magatzems empresarials, anàlisis de big data i aplicacions IoT.
- **Altes Demandes de Rendiment:** Optimitzat per a transaccions financeres, comerç electrònic i anàlisi en temps real, assegurant un rendiment ràpid i eficient.
- **Requisits de Seguretat Rigorosos:** Compleix amb alts estàndards de seguretat per a protegir dades sensibles en sistemes governamentals, de defensa i gestió d'informació personal.
- **Integració Complexa:** Facilita la integració amb múltiples sistemes i tecnologies en entorns empresarials complexos.
- **Escenaris de Núvol i Virtualització:** Compatible amb una varietat d'entorns de núvol públic i privat, oferint flexibilitat i escalabilitat.

Alguns casos d'ús comuns on Oracle destaca son els següents:

1. **Aplicacions Empresarials:**

   Oracle és àmpliament utilitzat en entorns empresarials per a aplicacions de missió crítica com a sistemes de gestió empresarial (ERP), sistemes de gestió de relacions amb clients (CRM), sistemes de gestió de recursos humans (HRM), entre altres. La seva capacitat per a manejar grans volums de dades i transaccions ho fa ideal per a aquestes aplicacions.

1. **Sector de la Salut:**

   En el sector de la salut, Oracle s'utilitza per a gestionar registres mèdics electrònics, dades de pacients, programació de cites i facturació. La seva capacitat per a manejar grans quantitats de dades i complir amb els estàndards de seguretat i privacitat és crucial en aquest entorn altament regulat.

1. **Aplicacions Financeres:**

   En el sector financer, on la velocitat i la precisió són crítiques, Oracle s'utilitza en aplicacions com la gestió de riscos, la gestió de carteres i l'anàlisi financera. La seva capacitat per a processar transaccions ràpidament i manejar dades financeres sensibles ho converteix en una opció de confiança.

1. **Telecomunicacions:**

   En la indústria de les telecomunicacions, on es generen grans volums de dades d'usuaris i transaccions, Oracle s'utilitza per a la gestió de la xarxa, la facturació i la gestió de l'experiència del client. La seva capacitat per a escalar horitzontal i verticalment permet manejar la càrrega de treball de manera eficient.
1. **Educació:**

   En educació, Oracle es pot utilitzar per a administrar sistemes de gestió d'aprenentatge, dades estudiantils, biblioteques digitals i sistemes d'administració universitària entre altres coses. La seva capacitat per a manejar grans volums de dades i proporcionar un accés ràpid i segur a la informació és essencial per a aquestes aplicacions

## <a name="_heading=h.3znysh7"></a>Versions de solució
Actualmente oracle compta amb 7 versions/llicències que son las següents:

1. **Oracle Database Standard Edition One:** 

   Ofereix facilitat d'ús, potència i rendiment sense precedents per a aplicacions web, de nivell departamental i de grups de treball. Des d'entorns de servidor únic per a petites empreses fins a entorns de sucursals altament distribuït.

1. **Oracle Database Standard Edition:**

   Ofrece la facilidad de uso, la potencia y el rendimiento sin precedentes de Standard Edition One, con soporte para máquinas más grandes y agrupación de servicios con Oracle Real Application Clusters (Oracle RAC).

1. **Oracle Database Enterprise Edition:**

   Proporciona el rendiment, la disponibilitat, l'escalabilitat i la seguretat necessaris per a aplicacions de missió crítica, com a aplicacions de processament de transaccions en línia (OLTP) de gran volum, magatzems de dades amb ús intensiu de consultes i aplicacions d'Internet exigents.

1. **Oracle Database Express Edition:**

   És una edició bàsica de Oracle Database que es descarrega ràpidament, és fàcil d'instal·lar i administrar, i el seu desenvolupament, implementació i distribució són gratuïts. Oracle Database XE facilita l'actualització a altres edicions de Oracle sense migracions costoses i complexes.


1. **Oracle Database Personal Edition**

   Admet entorns de desenvolupament i implementació d'un solo usuari que requereixen compatibilitat total amb Oracle Database Standard Edition One, Oracle Database Standard Edition i Oracle Database Enterprise Edition.

1. **Oracle Database Standard Edition 2**

   Ofereix facilitat d'ús, potència i rendiment sense precedents per a aplicacions web, de nivell departamental i de grups de treball

1. **Oracle Cloud Infrastructure (OCI)**

   OCI ofereix un conjunt comú de més de 100 serveis en cada regió de núvol. Serveis des de contenidors i VMware fins a IA, per a migrar, modernitzar, construir i escalar infraestructura de TI.

El preu de les llicències, serveis etc es troba en les següents pàgines:

<https://www.oracle.com/a/ocom/docs/corporate/pricing/technology-price-list-070617.pdf>

<https://docs.oracle.com/cd/E21659_01/html/E10594/editions.htm>

<https://docs.oracle.com/cd/E55822_01/DBLIC/editions.htm#DBLIC116>
## <a name="_heading=h.2et92p0"></a>Comparativa

Oracle és una de les principals bases de dades en el mercat, però existeixen diverses altres opcions en el seu segment. Aquí tens una comparació general entre Oracle i algunes de les bases de dades més conegudes:

1. **MySQL**:
   1. **Tipus**: MySQL és una base de dades relacional de codi obert, mentre que Oracle és una base de dades relacional comercial.
   1. **Cost**: MySQL és gratuït per al seu ús en la majoria dels casos, mentre que Oracle té llicències que poden ser costoses.
   1. **Escalabilitat**: Oracle és conegut per la seva capacitat d'escalabilitat en aplicacions empresarials de gran grandària, mentre que MySQL pot ser més adequat per a aplicacions de grandària mitjana o petita, encara que pot escalar-se també.
   1. **Características**: Oracle ofereix una àmplia gamma de característiques empresarials avançades, com particionamient, replicació avançada, clustering, i suport per a bases de dades en memòria. MySQL ofereix moltes característiques similars, encara que algunes poden no ser tan avançades o poden requerir configuració addicional.
1. **Microsoft SQL Server**:
   1. **Tipus:** SQL Server és una base de dades relacional comercial desenvolupada per Microsoft.
   1. **Cost:** SQL Server té diverses edicions, incloent-hi una edició gratuïta (Express), així com edicions comercials amb diferents nivells de funcionalitat i cost. En general, pot ser menys costós que Oracle en algunes configuracions.
   1. **Integració:** SQL Server s'integra bé amb altres tecnologies de Microsoft, com .NET Framework i Azure, la qual cosa pot fer-ho una opció preferida per a entorns basats en Microsoft.
   1. **Plataforma:** Oracle és conegut per ser multiplataforma, mentre que SQL Server és més comunament utilitzat en entorns Windows.
1. **PostgreSQL**:
   1. **Tipus:** PostgreSQL és una base de dades relacional de codi obert.
   1. **Cost:** PostgreSQL és gratuït i de codi obert, la qual cosa pot ser atractiu per a moltes organitzacions.
   1. **Extensibilitat:** PostgreSQL és altament extensible i permet als usuaris crear noves funcions, tipus de dades, etc.
   1. **Rendiment**: Tots dos sistemes tenen un rendiment sòlid, però l'optimització pot variar depenent de la càrrega de treball i la configuració específica.

1. **MongoDB**:
   1. **Tipus**: MongoDB és una base de dades NoSQL, cosa que significa que difereix significativament de Oracle en la seva arquitectura i model de dades.
   1. **Model de dades:** Oracle és una base de dades relacional que utilitza taules amb files i columnes, mentre que MongoDB és una base de dades de documents que emmagatzema dades en documents JSON.
   1. **Escalabilitat:** MongoDB es destaca en escalabilitat horitzontal i pot ser una millor opció per a aplicacions que requereixen una gran quantitat de lectures i escriptures ràpides en conjunts de dades massives.




# <a name="_heading=h.tyjcwt"></a>Documentació d'instal·lació i configuració
## <a name="_heading=h.3dy6vkm"></a>Preparació Maquina
Necessitem una màquina Oracle Linux 

No té requisits mínims pro per una empresa petita un bon punt de partida seria:

|Requisits||
| :- | :- |
|CPU|CPU x86 4-6 Nuclis|
|RAM|4096Mb +|
|Disco OS|dos discos SSD 128/256GB en Raid 1|
|Disco BD|Depèn de l’ús un bon punt de partida sería 8 TB en Raid 5|
## <a name="_heading=h.rmnm3m6qdfdz"></a>Instal·lació del SGBD
Primer descarreguem els paquets amb la comanda:

|curl -OL https://download.oracle.com/otn-pub/otn\_software/db-express/oracle-database-xe-18c-1.0-1.x86\_64.rpm|
| :- |

Exemple de captura:

|![](Aspose.Words.2fccffd3-2e7f-4e39-9870-7065a2a0ade0.004.png)|
| :- |

Després instal·lem el paquets:

|dnf install -y /bin/bash /bin/sh /etc/redhat-release bc bind-utils binutils ethtool glibc glibc-devel initscripts ksh libaio libaio-devel libgcc libstdc++ libstdc++-devel make module-init-tools net-tools nfs-utils openssh-clients pam procps psmisc smartmontools sysstat unzip util-linux-ng xorg-x11-utils xorg-x11-xauth libnsl|
| :- |

Exemple de captura:

|![](Aspose.Words.2fccffd3-2e7f-4e39-9870-7065a2a0ade0.005.png)|
| :- |

|rpm -i --nodeps oracle-database-xe-18c-1.0-1.x86\_64.rpm|
| :- |

Exemple de captura:

|![](Aspose.Words.2fccffd3-2e7f-4e39-9870-7065a2a0ade0.006.png)|
| :- |

Per configurar:

|/etc/init.d/oracle-xe-18c configure|
| :- |

|![](Aspose.Words.2fccffd3-2e7f-4e39-9870-7065a2a0ade0.007.png)|
| :- |
## <a name="_heading=h.2s8eyo1"></a>Configuració del Firewall i altres elements de seguretat
Per connectar-nos amb la xarxa local hem d'obrir el port 5500 i el de connexió 1521

|sudo firewall-cmd --permanent --zone=public --add-port=5500/tcp|
| :- |

|sudo systemctl reload firewalld|
| :- |

|sudo firewall-cmd --list-all|
| :- |

## <a name="_heading=h.dkrfazxwaxvg"></a><a name="_heading=h.oviaxgi6racv"></a><a name="_heading=h.rtbzg8inhnuq"></a><a name="_heading=h.qgdws04cjoru"></a><a name="_heading=h.fpvyhm1of20h"></a><a name="_heading=h.17dp8vu"></a>Securització de la instal·lació

En Oracle es poden implementar bastant mesures de seguretat, alguns exemples de seguretat son els seguentsr:

1. **Autenticació robusta**:
   1. Utilitzar autenticació forta per als usuaris, com a contrasenyes complexes i polítiques de canvi de contrasenya periòdiques.
   1. Considerar autenticació multifactor per a agregar una capa addicional de seguretat.
1. **Autorització adecuada**:
   1. Assignar rols i privilegis de manera apropiada. No concedir més privilegis dels necessaris per a fer les tasques específiques.
   1. Utilitzar el principi de privilegis mínims necessaris (least privilege) per a limitar l'accés dels usuaris sol als recursos que necessiten per al seu treball.
1. **Auditoria i monitoratge**:
   1. Configurar l'auditoria per a registrar activitats importants, com a intents d'accés fallits, canvis en l'estructura de la base de dades i consultes sensibles.
   1. Implementar eines de monitoratge per a supervisar el rendiment i l'activitat de la base de dades en temps real.
1. **Encriptació de dades:**
   1. Utilitzar l'encriptació per a protegir les dades sensibles tant en repòs com en trànsit.
   1. Considerar l'encriptació de columna per a protegir dades específiques dins de les taules.
1. **Parches i actualitzacions regulars:**
   1. Mantenir la base de dades actualitzada amb els últims pegats de seguretat i actualitzacions de Oracle per a mitigar vulnerabilitats conegudes.
1. **Firewalls y segmentació de xarxa**:
   1. Implementar firewalls i segmentació de xarxa per a restringir l'accés a la base de dades des d'ubicacions no autoritzades.
1. **Control de acces basat en IP**:
   1. Configurar llistes blanques d'adreces IP per a restringir l'accés a la base de dades des d'ubicacions específiques.
1. **Políticas de seguretat i capacitació del usuari**:
   1. Estableix polítiques clares de seguretat de dades i assegura't que tots els usuaris estiguin capacitats per a comprendre i seguir aquestes polítiques.
1. **Suports i recuperació de dades**:
   1. Implementar un pla de suport i recuperació sòlid per a protegir les dades contra pèrdues accidentals o atacs malintencionats.
1. **Avaluació de vulnerabilitats i proves de penetració**:
   1. Realitzar avaluacions regulars de vulnerabilitats i proves de penetració per a identificar i corregir possibles bretxes de seguretat.

A més hem fet un petit exemple de cambiar la contrasenya dels 3 usuaris principals   de la SGBD que tenen la mateixa contrasenya a 1 contrasenya distinta per cada usuari.

Per defecte tenim tres usuaris princiapls, SYS, SYSTEM i PBDADMIN, tots tres tenen la mateixa contrasenya així que canviarem això, jo usaré el programa Oracle SQL Developer, ens n'anem a l’usuari (dins de ‘otros usuarios’), per exemple SYS:

![](Aspose.Words.2fccffd3-2e7f-4e39-9870-7065a2a0ade0.008.png)

i aquí podem posar una contrasenya nova:

![](Aspose.Words.2fccffd3-2e7f-4e39-9870-7065a2a0ade0.009.png)

recomano posar-li contrasenyes diferents de tots els usuaris per defecte i si pot ser inclòs fer usuaris nous i desactivar els usaris per defecte.
## <a name="_heading=h.3rdcrjn"></a>Instruccions d'arrencada, verificació d’estat i apagada de servei
Per arrancar el servei:

|/etc/init.d/oracle-xe-18c start|
| :- |

Per apagar:

|/etc/init.d/oracle-xe-18c stop|
| :- |
## <a name="_heading=h.26in1rg"></a>Fitxer de configuració
Per anar al fitxer de configuració:

|nano /etc/sysconfig/oracle-xe-18c.conf|
| :- |

|![ref1]|
| :- |
## <a name="_heading=h.lnxbz9"></a>Fitxers de dades
Els fitxers de dades estan en:

|/opt/oracle/oradata/|
| :- |
## <a name="_heading=h.35nkun2"></a>Ports d'escolta del servei de la base de dades i passos per canviar-los
Port per defecte per connectar-se a la base de dades: 1512

Per canviar ens n'anem a:

|nano /etc/sysconfig/oracle-xe-18c.conf|
| :- |

i canviem el ‘LISTENER\_PORT’:

|![ref2]|
| :- |
## <a name="_heading=h.pl6pcsuhizme"></a><a name="_heading=h.1ksv4uv"></a>Connexió a la BD
Per connectar-nos tenim moltes maneres per exemple amb sqlplus:

Primer posem de SID ‘XE’ amb ‘. oraenv’

![](Aspose.Words.2fccffd3-2e7f-4e39-9870-7065a2a0ade0.012.png)

y per connectar-nos usem:

|sqlplus sys/GetStarted18c@//localhost:1521/XE as sysdba|
| :- |

![](Aspose.Words.2fccffd3-2e7f-4e39-9870-7065a2a0ade0.013.png)

per Visual Studio (amb l'extensió SQl Server Client (mssql)) en Host posem la IP de la BD, el usuari i contrasenya

![](Aspose.Words.2fccffd3-2e7f-4e39-9870-7065a2a0ade0.014.png)



# <a name="_heading=h.44sinio"></a>Tipus de SGBD

## <a name="_heading=h.z337ya"></a>Enfocament i model de dades

Oracle ofereix diversos sistemes de gestió de bases de dades (SGBD), incloent SGBD relacionals com Oracle Database i SGBD no relacionals com Oracle NoSQL Database. Aquestes opcions cobreixen una àmplia gamma de necessitats d'emmagatzematge de dades, des de les estructures tradicionals fins a les dades no estructurades o semiestructurades.





[ref1]: Aspose.Words.2fccffd3-2e7f-4e39-9870-7065a2a0ade0.010.png
[ref2]: Aspose.Words.2fccffd3-2e7f-4e39-9870-7065a2a0ade0.011.png
