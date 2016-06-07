# WMUBot
Bot per telegram che mostra le foto delle webcam delle mense UNITN
https://telegram.me/wmubot

# N.B.: versione vecchia con bug, non usare!
Se un'immagine richiesta non è disponibile (es. 404 http error in http://ftp.tn.ymir.eu/mesiano01.jpg, alla riga https://github.com/micheledallatorre/WMUBot/blob/master/main.py#L156) allora il bot va in loop. Ogni minuto ovvero tenta di nuovo di fare la richiesta (in questo caso /test) e restituisce le prime 3 immagini (che sono raggiungibili, ovvero non danno 404 http error).

## Esempio
![alt tag](http://i.imgur.com/WxneQei.png?1)

## Webcam disponibili
- /povo Webcam del Polo Ferrari (Mensa veloce e normale)
- /mesiano Webcam ????
- /lettere Webcam di via Tommaso Gar

Il bot è pronto per essere deployato su Google App Engine. 

### Istruzioni
Una volta ottenuto il token da [Bot Father](https://telegram.me/botfather) è sufficiente inserirlo alla riga 20 di main.py.

Il Project ID scelto dalla [developer console](https://console.developers.google.com/project) va inserito nella prima riga nel file app.yaml

Se non hai mai usato Bot Father e/o Google App Engine potrebbe esserti utile questa guida: https://github.com/yukuku/telebot#instructions
