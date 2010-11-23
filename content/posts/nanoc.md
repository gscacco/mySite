---
title: 'nanoc'
disqus_id: blogpost_<1>
post_url: '/posts/mio/'
disqus_title: 'nanoc'
---

# nanoc

Nanoc ([sito web](http://nanoc.stoneship.org/)) è un'applicazione *Ruby* che compila documenti scritti in html, markdown, textile ed altro, e genera siti web statici.

Un sito web così generato potrà essere copiato su un qualunque webserver, senza la necessità di particolari server istallati (per esempio php, java, ruby o altro).

Il sito sarà interamente scritto e provato in locale prima di essere trasferito sul server. Il deploy potrà, a questo punto, essere effettuato semplicemente compiando i files in remoto (ftp, rsync, etc.): addirittura quest'ultima operazione può essere automatizzata utilizzando il seguente comando:

`% rake deploy:rsync`

Quali sono i vantaggi nell'uso di questa tecnica:

* **Velocità** il sito prodotto è molto veloce perchè le pagine non devono essere generate dinamicamente
* **Sicuro** non ci sono database o server che possano essere craccati
* **Affidabile** nessun server da manutenere, debug-abile localmente
* **Manutenibile** le pagine web non sono altro che files di testo che possono essere mantenute in controllo configurazione (svn, git, etc.)

*Questo sito usa nanoc per la generazione delle pagine statiche.*

## Istallazione
Per istallare nanoc a riga di comando eseguire:

`% sudo gem install nanoc`

Se utilizzate [markdown](http://daringfireball.net/projects/markdown/) per le pagine sarà necessario istallare kramdown:

`% sudo gem install kramdown`

Meglio istallare anche [adsf](http://stoneship.org/software/adsf/) per visualizzare localmente il sito web generato:

`% sudo gem install adsf`

## Come si usa
Una volta istallato bisogna modificare la variabile ambiente $PATH nel seguente modo:

`% export PATH=$PATH:/var/lib/gems/1.8/bin`

Se tutto è andato per il verso giusto possiamo invocare l'help in linea:

<pre>
<code>
% nanoc help 
nanoc, a static site compiler written in Ruby.

Available commands:

    autocompile          start the autocompiler
    compile              compile items of this site
    create_item          create a item
    create_layout        create a layout
    create_site          create a site
    debug                show debug information for this site
    help                 show help for a command
    info                 show info about available plugins
    update               update the data stored by the data source to a newer version
    view                 start the web server that serves static files

Global options:

    -d --debug           enable debugging (set $DEBUG to true)
    -h --help            show this help message and quit
    -C --no-color        disable color
    -V --verbose         make nanoc output more detailed
    -v --version         show version information and quit
    -w --warn            enable warnings
</code>
</pre>

Potete trovare la documentazione completa e molto ben fatta sul sito di [nanoc](http://nanoc.stoneship.org/)
