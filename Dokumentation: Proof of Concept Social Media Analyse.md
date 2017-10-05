# PoC Social Media Analyse

# Architektur
Die vier physikalischen Maschinen wurden vom enterpriselab aufgesetzt und in Betrieb genommen. Alle Grundlagen für die Inbetriebnahme des ElasticStack sind gegeben.
Weitere Infos sind im [Wiki](https://wiki.enterpriselab.ch/el/lab:elasticstack) des enterpriselab zu finden. Bei Fragen steht Patrick Zwicker zur Verfügung.

Die Maschinen werden in folgender Pipeline genutzt:

weibo-reader &rarr; weibo-queue &rarr; weibo-worker &rarr; weibo-dbXX &rarr; weibo-visual

![enter image description here](https://lh3.googleusercontent.com/FfNOvfgRsD79wvt0-yBpG7hgYcLtu44iWH62yCcnmctQkCCa9ug4ef_7EjbPw0j35NVNQsepQ_Fk)

## weibo-reader
Der weibo-reader ist zuständig für die Verarbeitung von Eingaben. Für diesen Zweck wird LogStash genutzt. Hier stehen diverse Plugins zur Verfügung. Sie können auch eigenhändig entwickelt oder ausgebaut werden.



Logstash service ist nicht existent
Startskript
/usr/share/logstash/bin/logstash/

Konfiguration: 
/etc/logstash/logstash.yml

Starten über
./logstash –path.settings /etc/logstash/logstash.yml

Service nicht vorhanden?
sudo systemctl start logstash.service  aus Doku funktioniert aber nicht

Startup?
/usr/share/logstash/bin/logstash --path.settings /etc/logstash/ -f /etc/logstash/conf.d/

 Test
/usr/share/logstash/bin/logstash --path.settings /etc/logstash/ -t -f /etc/logstash/conf.d/



systemctl stop logstash
/usr/share/logstash/bin/logstash --path.settings /etc/logstash/ -f /etc/logstash/conf.d/


## weibo-queue

## weibo-worker

## weibo-dbXX

## weibo-visual


> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTExNTg4MzY4MzRdfQ==
-->