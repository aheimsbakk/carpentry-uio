# Notater fra carpentry@uio

https://etherpad.wikimedia.org/p/230321_ttshell

2023-03-21

* To hjelpere, som hjelper mens man fortsetter.
  * Repeterer mens hjelp foregår, eller går videre med ekstra-materiell.
* Rød og grønne postit.
* Hjelpere jobber med andre ting, når det ikke er problemer.
  * Foreleser sier at nå er det er rød lappe oppe.

## Innhold

* Pakk ut en tarfil.
* Aliaser i `.bash_login` / `.bashrc`.
  * For `ls`, `la`, `ll`, untar, tarlist, maketar.
* Variabler
  * Eksempel på variabel som inneholder katalog
    ```bash
    g=${HOME}/git
    cd $g
    ```
* `mkdir -p`  
  For å lage katalgoer med underkataloger.
* `rmdir` / `rm -r`
* Funksjon i `.bash_login` / `.bashrc`. Eksemplet viser hvodan lage en spesifikk temp-katalog.
* Prompt, og hva den kan vise. Rensket opp `PS1` før kurset begynte.
  ```bash
  PS1="$ "
  ```
* For å lage din egen promt https://bashrcgenerator.com/.
  * Unngå å bruke `export` for `PS1` for da blir de tilgjengelige for shell-script og andre ting du kjører.
* `CTRL+D` samme som `exit`.
* Pause, liten oppsumering og svare på spørsmål så langt i plenum.

### Pause 1

#### `history`

* `history`
* `history | less`
  * `g` og `G`
  * `/` for søk.
  * `q` for å avslutte.
* Skjør en kommando en gang til `!kommandonummer`.
* `CTRL-R` og `CTRL-R` igjen for å søke tilbake, og endre den.
* Pil opp og ned.
* `ls data/velvet/temp`
* `cd !$`, få ut siste argumentet av siste komando.
* Repeter hovedpunktene fra `history`.

####

* Autocomplete, med `TAB`.
* `cat -t gapminderDataFiveYear.txt | head`, visal tab.
* `cat -n gapminderDataFiveYear.txt | head`, linjenummer.
* `cat -e gapminderDataFiveYear.txt | head`, end av linjer blir synlige for å se om det er spaces osv på slutten av linjen.

---

* `CTRL+e`, `CTRL+a`, `CTRL+k`, `CTRL+w` på kommandolinjen.

---

* `less -S stats.txt`, ingen linjeshift.
* `column -t gapminderDataFiveYear.txt` align tabserarete kolonner i fil.

#### Fra nettskjema, løse brukeroppgaver

* `man` sider for å finne fram for å løse det som det ble spurt om. Skrevet for ekseperter.
* `ls -lS`
* `ls -l | sort -n -k 5`
* `ls -F`, for å vise bare mapper.
* `ls *`, wildcards.
* `find .`
* `find . -name *.sam`
* `touch` oppdaterer timestamp på en fil. Lager en ny fil hvis den ikke eksisterer.
* `touch emptyfile.txt`
* `find . -name *.txt`, må brukes med quotes - hvis ikke så risikerer man shell expansion.
* `find . -name '*.txt'`
* `find . | grep txt`
* `find . -maxdepth 2` for å unngå å søke i alt. Eller `-mindepth 2`.
* `find . -name '*.txt' | xargs wc -l` for å se lengden på alle filene.
* `du -hs *`, for å se mappestørrelse.
* `for f in $(find -name '*.txt'); do wc -l $f; done`, i stedet for xargs.
* 

### Pause 2
