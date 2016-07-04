# PETUNJUK SINGKAT

Membuat direktori untuk menyimpan proyek:

```bash
$ mkdir ~/debian-www/
```

Mengakses direktori yang telah dibuat:

```bash
$ cd ~/debian-www/
```

Mengakses repository webwml:

```bash
$ cvs -d :pserver:anonymous@anonscm.debian.org:/cvs/webwml login
(Apabila di minta password, tekan Enter)
```

Mengunduh direktori english dan indonesian:

```bash
$ cvs -d :pserver:anonymous@anonscm.debian.org:/cvs/webwml checkout -l \ 
    webwml webwml/english
$ cvs -d :pserver:anonymous@anonscm.debian.org:/cvs/webwml checkout -l \ 
    webwml webwml/indonesian
```
