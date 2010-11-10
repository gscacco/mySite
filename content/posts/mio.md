---
title: 'nanoc'
disqus_id: 1
disqus_title: nanoc
---

# nanoc

Nanoc ([sito web](http://nanoc.stoneship.org/)) è un'applicazione scritta in *Ruby* che compila documenti scritti in html, markdown, textile ed altro, e genera siti web statici.

Un sito web così generato potrà essere copiato su un qualunque server statico, senza la necessità di particolari server istallati (per esempio php, java, ruby o altro).

Il sito sarà interamente scritto e provato in locale prima di essere trasferito sul server. Il deploy potrà, a questo punto, essere effettuato semplicemente compiando i files in remoto (ftp, rsync, etc.): addirittura quest'ultima operazione può essere automatizzata utilizzando il seguente comando:

`% rake deploy:rsync`

## Istallazione
Per istallare nanoc a riga di comando eseguire:

`% sudo gem install nanoc`

Se utilizzate un proxy:

`% sudo gem install --http-proxy http://server:port nanoc`

