# Level 0

```
$ ssh -p2220 bandit0@bandit.labs.overthweire.org #ssh konekcija po portu 2220 prema navedenom hostu

$ ls #provjera da li je fajl koji sadrzi password za sljedeci nivo prisutan

$ cat readme #ispis sadrzaja fajla koji sadrzi password za sljedeci nivo

$ exit #logout usera bandit0
```
![bandit0](https://i.ibb.co/R0VGxz1/bandit0.png)


# Level 1

`ssh -p2220 bandit1@bandit.labs.overthewire.org` # ssh konekcija po portu 2220 prema navedenom hostu

`ls` # provjera da li je fajl koji sadrzi password za sljedeci nivo prisutan

`cat < -` # ispis sadrzaja fajla koji sadrzi password za sljedeci nivo

`exit` # logout usera bandit1

![bandit1](https://i.ibb.co/B2CdRpp/bandit1.png)


# Level 2

`ssh -p2220 bandit2@bandit.labs.overthewire.org` # ssh konekcija po portu 2220 prema navedenom hostu

`ls` # provjera da li je fajl koji sadrzi password za sljedeci nivo prisutan

`cat spaces\ in\ this\ filename` # ispis sadrzaja fajla koji sadrzi password za sljedeci nivo

`exit` # logout usera bandit2

![bandit2](https://i.ibb.co/8MQwRyc/bandit2.png)


# Level 3

`ssh -p2220 bandit3@bandit.labs.overthewire.org` # ssh konekcija po portu 2220 prema navedenom hostu

`ls -la inhere/` # provjera da li je fajl koji sadrzi password za sljedeci nivo prisutan

`cat inhere/.hidden` # ispis sadrzaja fajla koji sadrzi password za sljedeci nivo

`exit` # logout usera bandit3

![bandit3](https://i.ibb.co/Y3tR1Tk/bandit3.png)


# Level 4
`ssh -p2220 bandit4@bandit.labs.overthewire.org` # ssh konekcija po portu 2220 prema navedenom hostu

`ls -la inhere` # provjera koji fajlovi su prisutni

`cd inhere` # prelazak u direktorijum gdje se nalaze fajlovi

`file * | grep ASCII` # provjera tipova fajla u direktorijumu inhere, te filtrira rezultate da prikaze samo ASCII text tipove

`cat inhere/-file07`

`exit` # logout usera bandit4

![bandit4](https://i.ibb.co/W3vNnj6/bandit4.png)


# Level 5
`ssh -p2220 bandit5@bandit.labs.overthewire.org` # ssh konekcija po portu 2220 prema navedenom hostu

`find . -type f -size 1033c ! -executable -exec file {} + | grep -w text` # trazi fajl ciji je size tacno 1033byte, koji je non-executable i filtrira rezultate gdje je tip fajla text

`cat ./inhere/maybehere07/.file2` # ovaj fajl je rezultat pretrage, te ispisujemo njegov sadrzaj u cilju obezbjedjivanja passworda za sljedeci nivo

`exit` # logout usera bandit5

![bandit5](https://i.ibb.co/x7H5tJC/bandit5.png)


# Level 6
`ssh -p2220 bandit6@bandit.labs.overthewire.org` # ssh konekcija po portu 2220 prema navedenom hostu

`find / -type f -size 33c -group bandit6 -user bandit7 2> /dev/null` # trazi fajl velicine 33 byte, u vlasnistvu grupe bandit6 i usera bandit7, stderr preusmjeren u /dev/null kako medju rezultatima koji zadovolje uslove pretrage ne bi bilo error messages poput "Permission denied" jer nemamo dozvole da pristupimo svim direktorijumima na serveru

`exit` # logout usera bandit6

![bandit6](https://i.ibb.co/9Yj1yty/bandit6.png)


# Level 7

`ssh -p2220 bandit7@bandit.labs.overthewire.org` # ssh konekcija po portu 2220 prema navedenom hostu

`grep millionth data.txt | cut -d"     " -f2` # grep pronalazi pojam millionth u fajlu data.txt, te rezultat prosljedjuje komandi 'cut' kojoj je definisan delimiter tab, te joj je receno da printa polje 2

`exit` # idemo dalje za iste pare

![bandit7](https://i.ibb.co/1GSkmdM/bandit7.png)


# Level 8

`ssh -p2220 bandit8@bandit.labs.overthewire.org` # ssh konekcija po portu 2220 prema navedenom hostu

`cat data.txt | sort | uniq -u` # ispis sadrzaja fajla data.txt, sortiranje rezultata u linije A-Z, ispis linije koja se samo jednom ponavlja

`exit` # logout usera bandit8

![bandit8](https://i.ibb.co/d6f4htX/bandit8.png)


# Level 9

`ssh -p2220 banditi9@bandit.labs.overthewire.org` # ssh konekcija po portu 2220 prema navedenom hostu

`strings data.txt | grep ==` # ispisuje 'citljive' stringove iz binarnog fajla data.txt, rezultat se prosljedjuje komandi grep

`exit` # logout usera bandit9

![bandit9](https://i.ibb.co/pQWqmw7/bandit9.png)


# Level 10

`ssh -p2220 bandit10@bandit.labs.overthewire.org` # ssh konekcija po portu 2220 prema navedenom hostu

`base64 data.txt` # dekodira fajl data.txt i ispisuje rezultat

`exit` # logout usera bandi10 

![bandit10](https://i.ibb.co/c1hZ5rj/bandit10.png)


# Level 11
