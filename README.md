# CISCO20220125
Tisztelt Kollégák a Packet Tracer pontozása csak tájékoztatás jellegű, nem súlyoztam, minden műveletre 1 pontot ad és egyszer sem ellenőriztem le a beállításokat. Ezért kérem, ne kapjanak szívizom görcsöt ha nem kapnak pontot valamire, majd én felülbírálom a pontozást!



Jó munkát!

 

Nevezze el az eszközöket!

A Jozsi_Home hálózatrészben, konfigurálja a SOHO routert, a privát hálózat a 192.168.20.0/26, az első 10 IP címet zárja ki a terjesztésből, korlátozza a maximálisan kiosztható IP címek számát 50-re.

A nyomtatónak készítsen fenntartást Printer néven és a hálózat 60. IP címét kapja meg.

A Home_PC-t csatlakoztassa a 1-es portba, a nyomtatót a 2-esbe.

Konfigurálja a Wifi beállításokat a 2,4GHz és az 5GHz hálózat SSID-je legyen Home, authentikáció WPA2 Personal, AES, jelszó: Almafa12.

A Home Tablet és a Home Laptop Wifivel csatlakozzon a hálózatra.

A SOHO router jelszava legyen „CsakAPihi”.

 

Csatlakozzon az ISP_Admin PC-ről SSH-val az ISP szerverre (70.0.0.1, Jozsi, CsakALinux) és készítse el az ISP előfizetőinek DHCP készletét.

A készlet neve legyen Users, a hálózat 194.41.10.0/24, alapértelmezett átjáró: 194.41.10.1, DNS:70.0.0.10, domain: isp.hu. Zárja ki az osztásból az első 100 Ip címet.

 

Konfigurálja a Home_PC-n az email klienst (mail cím:jozsi@isp.hu, username: Jozsi, password: CsakALinux, POP3, SMTP: 70.0.0.20) és küldjön egy levelet saját nevével az admin@isp.hu címre.

 

Ceg forgalomirányító Gig0/1-es interfészére állítsa be a 193.41.10.2/30-as IP címet.

Konfiguráljon alapértelmezett utat a felhő felé a 193.41.10.1-es IP címet megadva cél címként.

Ceg forgalomirányító Gig0/0-s interfészét csatlakoztassa a CegSw1 kapcsoló Gig0/1-es interfészhez, és hozzon létre három alinterfészt 802.1Q beágyazással Gig0/0.10-es 192.168.10.1/24, Gig0/0.20-as 192.168.20.1/24 és a Gig0/0.30-as 192.168.30.1/24 IP cím beállítással.

Készítsen három DHCP készletet a belső hálózat számára, Iroda – 192.168.10.0/24, Informatika – 192.168.20.0/24 és Wifi – 192.168.30.0/24. DNS szerver 70.0.0.10, domain név ceg.hu.

A .10 és a .20 hálózatból zárja ki az első 50 Ip címet, a .30-as hálózatból csak a hálózat alapértelmezett átjáróját.

 

Készítsen listás NAT szolgáltatást a belső hálózatnak, publikus IP címként használja a Gig0/1-es interfészre beállított IP címet.

 

Vegyen fel két helyi felhasználót 15-ös jogosultsági szinttel a forgalomirányítóra, (Jozsi, CsakALinux), és saját magát tetszőleges jelszóval.

Készítsen 1024 bit-es RSA kulcsot (domain név:ceg.hu) és csak SSH-val engedélyezze a belépést az első öt virtuális terminál vonalon.

 

Csatlakoztassa a Cég hálózatában a két kapcsolót egymáshoz a Gig0/2-es porton.

CegSw1 lesz a hálózat VTP szervere (ceg.hu, VTPtitok), hozzon létre négy Vlan-t (Vlan 10- Iroda, Vlan20 – Informatika, Vlan 30 – Wifi és Vlan 40 – NemHasznált)

A kapcsoló kapja meg az Informatika Vlan második IP címét.

Konfigurálja a privilegizált mód jelszavát „PingvinKiralysag”, és biztosítson Telnet hozzáférést az eszközhöz jelszó „LinuxAzIsten”.

Konfigurálja a kapcsoló portjait:

·        Gig0/1-2 – Trunk

·        Fa0/1-10 – Vlan10 (Iroda)

·        Fa0/11-20 – Vlan20 (Informatika)

·        Fa0/24 – Vlan30 (Wifi)

·        Nem használt portok – Vlan40 (NemHasznalt).

 

CegSw2 VTP kliens(ceg.hu, VTPtitok), az Informatika Vlan 3. IP címét birtokolja, a privilegizált mód jelszava legyen „PingvinKiralysag”, és biztosítson Telnet hozzáférést az eszközhöz jelszó „LinuxAzIsten”.

Konfigurálja a kapcsoló portjait:

·        Gig0/2 – Trunk

·        Fa0/1-10 – Vlan10 (Iroda)

·        Fa0/11-20 – Vlan20 (Informatika)

·        Fa0/24 – Vlan30 (Wifi)

·        Nem használt portok – Vlan40 (NemHasznalt).

 

A Cég hálózatában az Access Point01 SSID-je „Ceg”, jelszava „CegWifi01”, az Access Point02 SSID-je „CegQuest”, jelszava „CegQuest01”. Csatlakoztassa az Access Point-okat a Wifi Vlan-hoz rendelt portba.

 

 
