# BRIEF INSTRUCTIONS

Membuat direktori untuk menyimpan proyek:

```bash
mkdir ~/debian-www/
```

Mengakses direktori yang telah dibuat:

```bash
cd ~/debian-www/
```

Mengakses repository webwml:

```bash
cvs -d :pserver:anonymous@cvs.alioth.debian.org:/cvsroot/webwml login
(Apabila di minta password, tekan Enter)
```

Mengunduh direktori english dan indonesian:

```bash
cvs -d :pserver:anonymous@cvs.alioth.debian.org:/cvsroot/webwml 
checkout webwml/english
cvs -d :pserver:anonymous@cvs.alioth.debian.org:/cvsroot/webwml 
checkout webwml/indonesian
```
