# Staattisten näkymien mallintaminen kolmiulotteisella Gaussin kerrostamisella
Kandidaatintyö kolmiulotteisesta Gaussin kerrostamisesta (engl. 3D Gaussian Splatting).

Koko opinnäytetyö on luettavissa [Aaltodoc-julkaisuarkistossa](https://aaltodoc.aalto.fi/items/726d5ddd-393f-4e0a-9697-333e027197fb).

### Tiivistelmä
Tuntemattomien näkymien synteesi on tutkimusongelma, jossa pyritään luomaan jatkuva visuaalis-geometrinen esitys tilasta äärellisellä joukolla kuvia. Koneoppimiseen perustuvat ratkaisut käyttävät tätä kuvajoukkoa opetusdatanaan muodostaakseen esityksen. Tämä kandidaatintyö perehtyy kolmiulotteiseen Gaussin kerrostamiseen (three-dimensional Gaussian Splatting, lyhyemmin 3DGS). 3DGS on staattisten tuntemattomien näkymien synteesiin suunniteltu dataputki.

3DGS käyttää suurta määrää kolmiulotteisia normaalijakaumia säädettävin parametrein esittääkseen tilan. Esitys alustetaan asettamalla normaalijakaumia pisteisiin, jotka on tuotettu Structure-from-Motion-menetelmällä. Sekä normaalijakaumien projisointi maailma-avaruudesta kuva-avaruuteen että lopullisen kuvan rasterointi ovat kummatkin derivoituvia operaatioita. Tästä seuraa, että 3DGS:n dataputki on täysin derivoituva, ja normaalijakaumien parametrit voidaan iteratiivisesti optimoida käyttäen aiemmin kerättyä opetusdataa. Normaalijakaumien määrää kasvatetaan jaksoittain. Käyttämällä sopivia opetuskuvia optimointi johtaa todenmukaiseen esitykseen kuviin vangitusta kolmiulotteisesta tilasta.

Kokeissamme alkuperäistä 3DGS:n toteutusta vertaillaan gsplat-nimiseen avoimen lähdekoodin toteutukseen. Dataputkien suorityskyky mitataan sekä kvantitatiivisesti että kvalitatiivisesti. Lukijan huomio kiinnitetään tämänhetkisen tekniikan tason rajoihin, kuten hyvin yksityiskohtaiseen geometriaan sekä okkluusioihin. Myös teknologian sovelluskohteita käsitellään.

Opinnäytetyön tärkein kontribuutio on täydentää alan kirjallisuutta tarjoamalla aiempien teoksien huomiotta jättämiä matemaattisia päätelmiä ja todistuksia. Tämä täsmällinen lähestymistapa tarjoaa lukijalle syvemmän ymmärryksen dataputken toiminnasta. Lisäksi kandidaatintyö esittää aiemmassa kirjallisuudessa huomiotta jätetyn todistuksen kolmiulotteisen kovarianssimatriisin validiteetista. Kyseinen todistus osoittaa, että 3DGS:n optimointimenetelmä toimii poikkeuksetta.

### Avainsanat
tietokonenäkö, Gaussin kerrostaminen, dynaaminen Gaussin kerrostaminen, kolmiulotteinen rekonstruktio, volumetrinen renderöinti, uusien näkymien synteesi
