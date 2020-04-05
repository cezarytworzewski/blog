---
title: Instalacja i konfiguracja serwera SSH na Debian 9. Po co mi to?
date: 2020/04/05
---

Postanowiłem wznowić pisanie artykułów oraz dzielić się z Wami tym co się nauczyłem. Będę starał się pisać już regularnie  moje 
**daily raporty** z przebiegu swojej nauki.

# Instalacja Debiana

W swoim domowym zaciszu postanowiłem zainstalować Debian 9. Dlaczego akurat Debian 9? Odpowiedź prosta. Debian to system, na ktorym jest hosting w firmie, w której pracuje, a rownież są postawione serwery plików również z użciem tego systemu.
Wygrzebałem stary komputer... mała renowacja i gotowe.

System został zainstalowany. Podstawowe usługi jakie były domyślnie - również. Co prawda, była możiwość instalacji serwera SSH, ale pomyślałem, że byłoby za łatwo.

## Otwieram terminal

Na początku wydaję polecenia

```bash
'apt-get update' // polecenie to aktualizuję liste pakietów w repozytoriach
'apt-get upgrade' // polecenie aktualizuję pakiety
```

## Instalacja serwera ssh

Na to czekałem od samego początu...

```bash
'apt-get install openssh-server' // polecenie to pobiera i instaluje pakiet `openssh-server` 
```

W zasadzie to już wszystko powinno działać. Jakby tak było ze wszystkim, to byłoby super - ale **live is brutal**.

Po wydaniu polecenia `apt-get install openssh-server` pojawił się pierwszy niespodziewany błąd, o którym nikt nie pisał w źródłach z których korzystałem.
Problem to:

```
Czytanie listy pakietów...Gotowe
Budowanie drzewa zależności
.
.
.
Kontynuować? [T/n] T
Media change: please insert the disc labeled 
Debian GNU/Linux... - Official amd64 DVD Binary... in the drive '/media/cdrom/' and press [Enter]
```

No i właśnie to już **pierwszy problem**.

Po przeszukaniu Internetu. Znalazłem rozwiązanie.

Muszę wyedytować plik z `/etc/apt/sources.list` tzn zakomentować jedną z linijek:

Przed:

`deb cdrom"[Debian GNU/Linux 9.12.0 _sTRETCH_ - oFFICIAL AMD64 dvd bINARY-1 2$`

Po:

`# deb cdrom"[Debian GNU/Linux 9.12.0 _sTRETCH_ - oFFICIAL AMD64 dvd bINARY-1 2$`

Po wprowadzeniu tej zmiany, próbuję ponownie zainstalować serwer ssh, znowu ten sam problem co wcześniej. 

No dobra, to uruchamiamy ponownie system. W konsoli wydaję polecenie `reboot` - polecenie to uruchamia ponownie system. System się uruchamia, i próbujemy od nowa zainstalować. Tym razem się udało. Czas na świętowanie!!! :)

Do testowania sprawdzenia połączenia przez SSH'a użyje programu **Putty**. Program ten jest bezpłatnym klientem usług Telenet, SSH oraz działa pod systemami Windows oraz Linux.

### Uruchamiam **Putty**

 * ![](https://imgur.com/Yj2FVN4)
 * następnie podaję dane do logowania do systemu Debian. Połączenie wykonuje z systemu Windows.
 ![](https://imgur.com/00GXAT1)

 więc pojawił nam się **problem numer dwa**... **Access denied** - sądząc po komunikacje chodzi o jakieś uprawnienia, no dobra przeglądamy dalej Internet w poszukiwaniu rozwiązania :)

 Znalazłem rozwiązanie!!!

 Tym razem muszę wyedytować plik `sshd_config`, dokładna lokalziacja jest w katalogu `/etc/ssh`. Więc otweiramy sobie terminalowy edytor, wydając polecenie: `nano /etc/ssh/sshd_config`. W tym pliku odnajdujemy fragment kodu taki jak:

 ```bash
# Authentication:

#LoginGraceTime 2m
#PermitRootLogin prohibit-password
#StrictModes yes
#MaxAuthTries 6
#MaxSessions 10
 ```

linijkę `#PermitRootLogin prohibit-password` zamieniam na `#PermitRootLogin yes`, zapoisuję plik i próbujemy ponownie.

![](https://imgur.com/7IImWoN)

Musimy teraz zrestartować nasz serwer ssh

![](https://imgur.com/CEfgvcn)

### Testujemy ponownie połączenie

????