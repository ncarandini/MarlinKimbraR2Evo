# MarlinKimbraR2Evo

## Istruzioni per la modifica del Firmware R2 EVO

1. Installare l'IDE di Arduino, scaricabile dal sito di Arduino (https://www.arduino.cc/en/Main/Software).
2. Scaricare la libreria "U8glib per display full Matrix", farne l'unzip e aggiungere la cartella "U8glib" alle librerie di Arduino (tipicamente "C:\Program Files (x86)\Arduino\libraries").
3. Aprire la cartella in cui si è salvato il sorgente del firmware e aprire il file "MarlinKimbraEvo.ino".
4. Usare il comando "Modifica|Trova…" per rinominare tutte le occorrenze di "fpos_t"  in "filepos_t" nei file "SdBaseFile.h" e "SdBaseFile.cpp" (vedi http://forums.reprap.org/read.php?146,691608).
5. Decommentare la riga "#define FILAMENT_RUNOUT_SENSOR" nel file "Configuration.h".
6. Impostare FILRUNOUT_PIN_INVERTING = true.
7. Da "Strumenti|Scheda" selezionare la scheda "Arduino/Genuino Mega or Mega2560".
8. Da "Strumenti|Porta" selezionare la porta COM a cui è connessa la scheda della stampante
9. Verificare la compilazione.
10. Caricare il firmware così modificato nella scheda della stampante.

### Modifica Firmware del 21/05/2022

1. Decommentato #define EEPROM_SETTINGS per abilitare la EEPROM nel file config.h
2. Cambiato #include <utility/u8g.h> in #include <clib/u8g.h>

### Modifica Firmware del 22/05/2022

1. Impostato #define TEMP_SENSOR_BED 0 nel file config.h per disabilitare il sensore di temperatura del bed visto che nella mia stampante ancora non l'ho montato
