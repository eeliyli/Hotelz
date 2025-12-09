Aloitin hotellin varausohjelman tekemisen miettimällä, mitä tietoja ohjelma tarvitsee ja miten ne olisi järkevintä tallentaa.Loin kaksi rakennetta: room huoneiden tiedoille ja reservation varausten tiedoille. Käytin vector-kontteja tavallisten taulukoiden sijaan, koska ne kasvavat ja pienenevät automaattisesti koska varauksia lisätään ja poistetaan jatkuvasti.

Pääsilmukan toteutin do–while-rakenteella, jotta valikko toistuu, kunnes käyttäjä poistuu. switch-rakennetta käytin selkeyden vuoksi: jokainen toiminto (varaus, haku, peruutus, tilastot) on omana lohkonaan. Pieni viive this_thread::sleep_for-komennolla teki ohjelmasta rauhallisemman ja aidomman tuntuisen.

 käytin random_device ja mt19937 -generaattoreita arpomaan huonemäärät ja alennukset. Tallennusta varten tein tallenna_varaukset- ja lataa_varaukset-funktiot, jotka käyttävät fstream-kirjastoa. Näin ohjelma muistaa varaukset myös seuraavalla käynnistyskerralla. syncvaraukset pitää tiedoston ja huonelistan ajan tasalla, jotta varatut huoneet eivät mene sekaisin.

Lopuksi lisäsin tilastointiominaisuuden, joka laskee esimerkiksi kokonaistulot ja keskimääräisen varauksen hinnan. Kommentointi jäi kesken.

Työ oli kiva, koska siinä pääsi yhdistämään monia C++-asioita yhdeksi toimivaksi ja oikean oloiseksi ohjelmaksi.
