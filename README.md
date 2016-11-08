## h5

Tehtävänanto: h5. Tee moduli git-varastoon ja kirjoita raportti sinne MarkDownilla.
Update: Bonustehtävänä voit kokeilla kloonata uusi modulisi vasta bootatulle live-USB:lle.

http://terokarvinen.com/2016/aikataulu-palvelinten-hallinta-ict4tn022-1-5-op-uusi-ops-loppusyksy-2016

Aluksi kirjauduin Githubiin ja tein itselleni uuden repositoryn nimeltä ''Asennus''. Sen jälkeen latasin Git:n ja Puppetin.
Seuraavaksi ajoin komennot
$ git config --global user.email "spostiosoite"
$ git config --global user.name "oma nimi"
$ git config --global credential.helper "cache --timeout=3600
nyt minulla on annettu omat tiedot sekä salasanan timeout tunniksi, jotta joka kerta kun uppaan githubiin jotain, ei tarvitse kirjoittaa
käyttäjätunnusta sekä salasanaa.
Siirryin /etc/puppet/modules kansioon johon cloonasin oman repositoryni komennolla sudo git clone https://github.com/jooelnurmi/asennus.git
Nyt kun minulla oli moduulilleni sopiva kansio nimeltä asennus ja kyseisen kansion sisällä LICENSE ja README.md tein sen sisälle vielä manifests
kansion jonka sisälle init.pp moduulin johon laitoin apachen lataus komennon.

## pull & push & testaus

Nyt kun minulla oli haluamani tiedostot ja kansiot jotka halusin siirtää githubiin, siirryin polussa Asennus kansioon asti, jotta kaikki sen sisällä olevat
tiedostot siirtyisivät githubiin. Annoin komennon sudo git add . && git commit && git pull && git push. Tämän jälkeen minulta kysyttiin kerran käyttäjä
tunnukseni sekä salasana, annoin ne oikein ja huomasin, että onnistuneesti sain siirrettyä tekemäni tiedostot githubiin. Sinne ilmestyi manifests kansioni
jossa oli sisällä init.pp moduulini, jossa oli tekemäni apache2 package. Huomattuani, että onnistuin, tulin vielä kirjoittamaan tähän README.md tiedostoon
loppuraporttini tehtävästä. Joudun siis kerran vielä ajamaan tuon sudo git add . && git commit && git pull && git push komennon.

## yhteenveto & linkit

Tehtävä oli ihan mielenkiintoinen ja onnistuin ensimmäisellä yrityksellä tekemään kaiken oikein. Tästä on varmasti hyötyä jatkossa kun haluaa tehdä moni
mutkaisempia moduuleita ja ne voi vaan upata githubiin niin ei tarvitse aina aloittaa alusta.

http://terokarvinen.com/2016/publish-your-project-with-github
http://terokarvinen.com/2016/aikataulu-palvelinten-hallinta-ict4tn022-1-5-op-uusi-ops-loppusyksy-2016  
