
# IoT Prototyping: Sensorer og Mikrokontrollere
Denne workshoppen går ut på å lære om IoT Prototyping. Det er i hovedsak en informativ workshop med noe lett coding og testing. 

## 1. Installering av software

1. Installer [VS Code](https://code.visualstudio.com/download)

2. Installer [nRF Connect for Desktop](https://www.nordicsemi.com/Products/Development-tools/nrf-connect-for-desktop/download)
  
 3. I nRF Connect for Desktop, Innstaller:
 - LTE Link Monitor
 - Toolchain Manager 
 
 4. Åpne Toolchain Manager og installer nRF Connect SDK v2.3.0
 
 5. Trykk på `Open in VS Code` og installer `missing packages`. 
 
 6. Installer [Command Line Tools](https://www.nordicsemi.com/Products/Development-tools/nRF-Command-Line-Tools/Download#infotabs)
 
 
 ## 2. En enkel applikasjon
 
 1. Lage en ny mappe i `C:\` driven din med et navn du husker. F.eks. `Nordic`.
 
 2. I VS Code, gå til nRF Connect som er vist i activity bar på venstre side, og under `WELCOME` trykke på `Create a new application` og velg `Copy a Sample`.
 
 3.  I feltet som kommer opp, søk etter og velg `Blinky Sample`.
 
 4.  I det neste feltet, trykk på mappe iconet over feltet til høyre. Velg mappen du lagde tidliger, eller skriv inn mappe adressen manuelt, f.eks. `C:\Nordic`.
 
 5.  Lag et navn på aplicasjoen, f.eks. `Blinky_test`, trykk så på `Open` i dialogen som popper opp.
 
 7. Under `Application` vil prosjektet dukke opp og det vil stå `No build configurations`. Trykke på den og velg `Board` velger du `thingy91_nrf9160_ns` eller `nrf9160dk_nrf9160_nsog trykker på `Build Configuration`. 
 
 8. Når build er ferdig, må du velge `Link Build Configuration And Device`, deretter `Flash` under `ACTIONS`. 
 
 9. Nå skal lyset blinke.

## 3. Asset tracker

1. Opprett ny en ny applicasjon på sammen måte som forje eksempel, men denne gangen søk etter og velg `asset_tracker_v2` istendenfor `Blinky Sample`.

2.  Gå til [nRF Cloud](https://nrfcloud.com) og lag en bruker.

3.  Trykk på plusset, registrer LTE Device. Nederst til høyre kan du velge å hoppe over å registrere sim-kort.

4.  Build, link og flash Application slik som i forje eksempel. Etter det skal det begyne å komme data inn på nRF Cloud.
