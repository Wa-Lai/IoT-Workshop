
# IoT Prototyping: Sensorer og Mikrokontrollere
Denne workshoppen går ut på å lære om IoT Prototyping. Det er i hovedsak en informativ workshop med noe lett coding og testing. 

## 1. Installering av software

1. Installer [VS Code](https://code.visualstudio.com/download)

2. Installer [nRF Connect for Desktop](https://www.nordicsemi.com/Products/Development-tools/nrf-connect-for-desktop/download)
  
 3. I nRF Connect for Desktop, Innstaller:
 - LTE Link Monitor
 - Toolchain Manager 
 
 4. Åpne Toolchain Manager og installer `nRF Connect SDK v2.4.2`
 
 5. Trykk på `Open in VS Code` og installer `missing packages`.

 6. I extensions taben i VS code søk opp og installer `Serial Monitor`.
 
 7. Installer [Command Line Tools](https://www.nordicsemi.com/Products/Development-tools/nRF-Command-Line-Tools/Download#infotabs)
 
 
 ## 2. En enkel applikasjon
 
 1. Lage en ny mappe i `C:\` driven din med et navn du husker. F.eks. `Nordic`.
 
 2. I VS Code, gå til nRF Connect som er vist i activity bar på venstre side, og under `WELCOME` trykke på `Create a new application` og velg `Copy a Sample`.
 
 3.  I feltet som kommer opp, søk etter og velg `Blinky Sample`.
 
 4.  I det neste feltet, trykk på mappe iconet over feltet til høyre. Velg mappen du lagde tidliger, eller skriv inn mappe adressen manuelt, f.eks. `C:\Nordic`.
 
 5.  Lag et navn på applikasjon, f.eks. `Blinky_test`, trykk så på `Open` i dialogen som popper opp.
 
 7. Under `Application` vil prosjektet dukke opp og det vil stå `No build configurations`. Trykke på den og velg `Board` velger du `nrf52840dk_nrf52840` og trykker på `Build Configuration`. 
 
 8. Når build er ferdig, må du velge `Link Build Configuration And Device`, deretter `Flash` under `ACTIONS`. 
 
 9. Nå skal lyset blinke.

## 3. Sende meldinger over bluetooth

1. Lastned Appen `nRF Connect for Mobile`.

2. Lag en ny applikasjon, velg `Copy a sample`.

3. I feltet som kommer opp, søk etter og velg `BLE UART service`.

4. Velg mappen fra tidligere og trykk på `Enter` for resten av promtene.

5. Lag en `Build Configuration` for applikasjonen.

6. Gå inn i main filen til programmet og finn line `42` hvor det står `#define DEVICE_NAME CONFIG_BT_DEVICE_NAME`.

7. Hold inne ctrl og trykk på `CONFIG_BT_DEVICE_NAME`.

8. Endre på stringen hvor det står `Nordic_UART_Service` til noe du kjenner igjen, f.eks kan du legge til navnet ditt på slutten.

9. Trykk `ctrl + s` for å lagre endringene.

10. `Link` build og `Flash` coden til brettet slik som med forje eksempel, du burde nå se `LED1` blinke hvert sekund.

11. I terminalen i VS code åpne fanen `Serial Monitor` og trykk på `Start Monitoring`.

12. Gå inn på mobil appliksajonen du lastet ned og finn navnet du endretet til under `Scanner`.

13. Trykk på `Connect` og se at `LED2` nå lyser konstant.

14. Under `Client` trykk på `Nordic UART Service`.

15. Trykk på Opplastningspilen på til høyre for `RX Characteristic`.

16. I feltet hvor det står `New Value` skriv inn det du har lyst til å sende over bluetooth til PC'en trykk `Send` så vil det dukke opp i Tera Term.

## 4. Asset tracker

1. Opprett ny en ny applicasjon på sammen måte som forje eksempel, men denne gangen søk etter og velg `asset_tracker_v2` istendenfor `Blinky Sample`.

2.  Gå til [nRF Cloud](https://nrfcloud.com) og lag en bruker.

3.  Trykk på plusset, registrer LTE Device. Nederst til høyre kan du velge å hoppe over å registrere sim-kort.

4.  Build, link og flash Application slik som i forrige eksempel. Etter det skal det begyne å komme data inn på nRF Cloud.
