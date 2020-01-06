# sakumatto.fi

Tallennettu 6.1.2020
Muutetaan netlify jatkuvaan julkaisemiseen, jossa netlify hakee (oletusarvoisesti) master branchiin tulevat muutokset automaattisesti ja julkaisee ne. Netlify tunnistaa suoraan Hugon ja osaa ajaa sen käskyt oletuksena oikein ->
joten yhdellä komennolla 
now=$(date +"%Y-%m-%d") && git add -A && git commit -m "Muut uudet $now" && git push -u  origin master
saa puskettua muutokset ja commitin suoraan maailmalle automaattisesti. Tämä korvaa firebasen 2020 alkaen sivustollani.


Tallennettu 3.8.2018

Perusajatus Hugolle on se, että se luo public-hakemistoon kaiken sivustolle menevän ja kaikki muut alihakemistot ovat sitä varten, että niillä luodaan säännöt miten public koostetaan.

lopuksi hugo && firebase deploy ajetaan sivu firebasen serverille.
