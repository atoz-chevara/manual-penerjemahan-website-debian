# BRIEF INSTRUCTIONS

Membuat direktori untuk menyimpan proyek:

    $ mkdir ~/debian-www/

Mengakses direktori yang telah dibuat:

    $ cd ~/debian-www/

Mengakses repository webwml:

    $ cvs -d :pserver:anonymous@cvs.alioth.debian.org:/cvsroot/webwml login
    (Apabila di minta password, tekan Enter)

Mengunduh direktori english dan indonesian:

    $ cvs -d :pserver:anonymous@anonscm.debian.org:/cvs/webwml checkout -l webwml webwml/english
    $ cvs -d :pserver:anonymous@anonscm.debian.org:/cvs/webwml checkout -l webwml webwml/indonesian

