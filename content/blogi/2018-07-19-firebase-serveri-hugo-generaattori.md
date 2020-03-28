---
title: "Nopea serveri on ympäristöteko"
date: 2018-07-19T09:38:34+03:00
author: saku
type: post
aihealueet:
  - Ekologia ja ympäristön tila
  - Yleinen
---
Mieti tätä:

<h2>Blogin pitäjälle sivuston latausnopeus on tärkeätä</h2>

Olen vuosien mittaan pitänyt tätä blogiani eri paikoissa. Nyt jo muutaman vuoden ajan olen seurannut keskustelua staattisten sivustojen tiimoilta. Ne tarjoavat suuren latausnopeuden koska http-serveri on itsessään nopea, mutta yleisesti käytettävät sivustogeneraattorit (kuten Wordpress) vaativat taustajärjestelmän, jotka ovat hitaita.

Blogin ylläpitäjä haluaa, että sivusto latautuu nopeasti monestakin eri syystä, mutta nopeus vaatii usein rahaa. Rahaa minulla taas ei ole, joten on keksittävä vaihtoehto.

Tähän maaperään on syntynyt [Hugo](http://gohugo.io/), joka on omalla tietokoneellasi toimiva sivustogeneraattori, joka luo staattisia sivustoja. Sellaisia kuin tämä minun blogini on. [Firebase](https://firebase.google.com/) puolestaan on Googlen omistama aivan mahtava tiedontallennusväline. Firebase sallii myös https-sivustojen hostaamisen ilmaiseksi silloin kun sivuston liikennemäärä on riittävän pieni.

### Serverit ja luonto
Rahan lisäksi seikka, jota ihmiset eivät useinkaan ajattele, on serverien vaatima tolkuton energiamäärä. Siinä missä tehottomasti toimitettava Wordpress-sivusto rasittaa serveriä jokaisella sivulatauksella noin kaksi sekuntia, tehokkaasti toimitettava staattinen sivusto latautuu noin 400 ms kuluessa. Siis 1/5 energian käytöllä.

Eräs asioista tietävä kertoi minulle suurkonesalifoorumilla aiheesta puhuessamme, että jokainen serveri on kuin saunan kiuas. Se vie kiukaan energiamäärän ja se kuumenee kuin kius. Prosessorit taas eivät saa ylikuumeta ja siksi konesalit pitää jäähdyttää, joka sekin vie energiaa.

Tehokas sivusto on siis ympäristöteko ja säästää ehkä jopa rahaa.

## Hugo ja Firebase -yhdistelmä toimii nopeasti
![Tämän sivuston latausnopeusraportti 19.7.2018](https://lh3.googleusercontent.com/wjMyMYyHME-eTCSXgzC5ciP1H1l8WEBBDFshvWOod6bAuzGcklNFkkkH_m-SphHPW7ZXHyQo5-7UKPKY4JQTX_FRhMvjvXUi3DW97SVbXWov8e_kf8KZWwFA4Tg1-Boa_vZPIHqXssanNT0DgBK-QIDekqAleCwVBqz6Mn4MPdp6mgj-3fI1UCErFhfhy6QlTsw6B3s7ToYT7e1FVCHaExjVV-nHMimWfBUkNL0svp9D2YeL62TWmQCQYyxJWpJmFJ0GhsZCRREO8TD8rRwttyuAROSSb9cwdB0truwc1SxmQEL8RchAD4mqaNlbF0g5yYGSRmVrJj1Ts1sMNa3cXBZQl4Bck-WgSethoFa6oFHlHbK2UZf1SHVYqIeCAPum1RtmEczwFUZAfmGc0OYBoX1sQShb4A5nL42EuY9TeVBPwtTlak5Zdjbw7rM4mOIi6x5AAH9ic9MwWNRcFNrBH9fg8TVRrYE5T3fWXnCqZps5Lq4wvSrmTq8fiXYQDcHADIO8heyFEzvdnS0kLc0vtm6QRJ10PPnY8JUIq7n38fc61w2us9dVe8q2GxVdRnx7xT64kR_G0yriX3bmxVi3I4YbfTwYi_Acelu4KZE=w301-h930-no)

Tämän oman sivustoni siirsin Hugo+Firebaselle eilen. Nopeus kasvoi dramaattisesti. Nyt sivuston hosting on ilmaista ja energiaa säästyy, ja sinä lukijani näet vastaisuudessa blogini tekstin nopeammin. Aika hyvä juttu.

###2020 muutos
Olen hiljattain siirtänyt sivuston Netlifyn koneelle. Syy oli continuous deployment joka onnistuu nyt siten, että Netlify hakee automaattisesti Githubin muutokset julkaistavaksi, joten nyt päivitys menee yhdellä helpolla komennolla läppäriltäni, esim "now=$(date +"%Y-%m-%d") && git add -A && git commit -m "$now .btn--default:hover inherit" && git push -u  origin master" ja minuutin päästä sivusto on julkistettu päivitettynä.
[Lue lisää Jamstackistä](https://medium.com/better-programming/12-tips-for-working-with-the-jamstack-1625fc8e40f)

Netlifyn täyden tehon saamiseksi täytyy sivuston DNS myös siirtää Netlifyn servereille. Olen tähän asti käyttänyt Cloudflarea DNS:ään ja se on ollut kaikin puolin hyvä, mielenkiintoista nähdä mitä muutoksia tulen näkemään.