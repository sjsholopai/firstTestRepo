---
title: "Something fascinating"
author: "Jenny Bryan"
date: "2019-05-16"
output:
  html_document:
    keep_md: true
---

# Harjoitus, datavaraston laadinta
githubissa: > new repository
“firstTestRepo”, “Testing my setup”
public
initialise with readme (“This will let you immediately clone the repository to your computer”)
kopioi URL
Tee työhakemisto tmp-kansioon
cd /Users/jyrkiholopainen/Desktop/testi/githubWD
$ pwd
/Users/jyrkiholopainen/Desktop/testi/githubWD
Jyrki-Holopainens-MacBook-Pro:githubWD jyrkiholopainen$
clone or download -> leiketauluun url
https://github.com/sjsholopai/firstTestRepo.git
$ git clone https://github.com/sjsholopai/firstTestRepo.git
$ cd firstTestRepo
$ git remote show origin
* remote origin
  Fetch URL: https://github.com/sjsholopai/firstTestRepo.git
  Push  URL: https://github.com/sjsholopai/firstTestRepo.git
  HEAD branch: master
  Remote branch:
    master tracked
  Local branch configured for 'git pull':
    master merges with remote master
  Local ref configured for 'git push':
    master pushes to master (up to date)

# DATAN MUOKKAUS JA DATAVARASTON PÄIVITYS
$ echo "Lisätään rivi README.md tekstitiedostoon" >> README.md
$ git status
Komento kertoo, että README.md tiedostoa on modifioitu: “Changes not staged for commit”
$ git add -A
Nyt “Changes to be committed” ja lopuksi
$ git commit -m "työhakemistossa tehty commit"

# DATAVARASTON POISTAMINEN  
$ cd..
$ rm -rf firstTestRepo/

# TUNNUSSANOISTA
SSH-avaimen käyttö on vaihtoehto HTTPS-protokollalle  ja sitä suositellaan. Se mahdollistaa datavaraston käytön ilman jatkuvaa tunnusten ja salasanan syöttöä projektikohtaisesti. SSH-avaimen käyttöönotto tapahtuu automaattisesti, kun github-projekti laaditaan mac:illä, windowsissa saattaa joutua säätämään.

# R-STUDION ja GITHUB:n kytkentä
Korvataan em. työhakemisto firstTestRepo R-studio-työhakemistolla, vanha deletoidaan ja uusi tuodaan R-studion kautta.
R-studiossa aloita uusi projekti:
File > New Project > Version Control > Git
leikkaa-liitä github datavaraston url osoite. Käytä projektin nimenä samaa nimeä, mikä on datavarastollakin (oletus).

# VANHAN R-PROJEKTIN SIIRTO GITHUBIIN
1. laaditaan githubiin uusi tyhjä datavarasto
2. muodostetaan siitä R:ään työtiedosto
3. leikkaa-liitä tiedostot R-työtiedostoon ja päivitä datavarasto.

# SIIRRETTÄVÄ PROJEKTI ON ENNESTÄÄN DATAVARASTO
Paikallisen koneen siirrettävän git-hakemiston r-projektissa:
1. "New branch" -työkalusta löytyy "add remote"-painike, johon voi leiketaulusta liittää remote datavaraston (github) osoitteen. "*remote name*" on "*origin*". painikkeella ""*Add*" prosessi siirtyy "*new branch*" -kohtaan. Tarkoitus on kopioida työprojektin "*master*"-haara github-projektin "*master*"-haaraksi. Siirrettävän haaran nimi on siis "*master*" ja varmista että "*Sync branch with remote*" on käytössä. Päällekirjoitetaan olemassa oleva haara.

konsolissa homma on helpoin:
```
git remote add origin https://github.com/sjsholopai/firstTestRepo.git
git push --set-upstream origin master
```
