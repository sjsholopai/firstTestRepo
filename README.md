Harjoitus, datavaraston laadinta
================================
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

$ echo "Lisätään rivi README.md tekstitiedostoon" >> README.md
$ git status
Komento kertoo, että README.md tiedostoa on modifioitu: “Changes not staged for commit”
$ git add -A
Nyt “Changes to be committed” ja lopuksi
$ git commit -m "työhakemistossa tehty commit"

DATAVARASTON POISTAMINEN
cd ..
rm -rf firstTestRepo/

SSH-avaimen käyttö on vaihtoehto HTTPS-protokollalle  ja sitä suositellaan. Se mahdollistaa datavaraston käytön ilman jatkuvaa tunnusten ja salasanan syöttöä projektikohtaisesti.

R-STUDION ja GITHUB:n kytkentä
Korvataan em. työhakemisto firstTestRepo R-studio-työhakemistolla, vanha deletoidaan ja uusi tuodaan R-studion kautta.

R-studiossa aloita uusi projekti:
File > New Project > Version Control > Git
leikkaa-liitä github datavaraston url osoite. Käytä projektin nimenä samaa nimeä, mikä on datavarastollakin (oletus).
