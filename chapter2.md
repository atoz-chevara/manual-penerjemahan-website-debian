# PETUNJUK SINGKAT

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

## Contoh Menerjemahkan berkas po.

```bash
cd webwml/indonesian/po
vi templates.id.po
```

Sunting berkas *templates.id.po* sehingga sesuai dengan berikut ini:

```
"Last-Translator: Nama Anda <nama-user@debian-id.org>\n"
"Language-Team: Indonesian <debian-l10n-indonesian@lists.debian.org>\n"
```

Anda dapat menggunakan text editor atau applikasi seperti [poedit](https://poedit.net/download "unduh poedit") & 
[virtaal](http://virtaal.translatehouse.org/download.html "unduh virtaal"). Periksa kembali hasil terjemahan Anda:

```bash
$ msgfmt --statistics -c -v -o /dev/null templates.id.po
```

Upload berkas *templates.id.po* yang telah diterjemahkan ke alamat email debian-l10n-indonesian@lists.debian.org dengan 
menyertakan deskripsi tentang apa yang telah Anda kerjakan.

Contoh: ftp://debian-id.alioth.debian.org/pub/debian-id/send-email-po.png

```
Subjek: Changes by atoz-chevara-guest: webwml/indonesian/po templates.id.po

Changes by:
       atoz-chevara-guest

Modified files:
       indonesian/po: templates.id.po

Log message:
       update po and translate
```

## Contoh Menerjemahkan sebuah halaman.

```bash
cd webwml/indonesian
cp ../english/social_contract.wml .
```

Sunting berkas *social_contract.wml* dan lakukan terjemahan.

> Jangan melakukan perubahan pada alamat URL & tags.

Perhatikan pada bagian header dari setiap berkas wml yang ingin Anda terjemahkan, contoh berikut masih dengan berkas *social_contract.wml*:

```
#use wml::debian::template title="Debian Social Contract" BARETITLE=true

#  Original document: contract.html
#  Author           : Manoj Srivastava ( srivasta@tiamat.datasync.com )
#  Created On       : Wed Jul  2 12:47:56 1997
```

Selalu menyertakan *translation-check* pada bagian header di semua berkas wml yang diterjemahkan:

```
#use wml::debian::template title="Kontrak Sosial Debian" BARETITLE=true
#use wml::debian::translation-check translation="1.24" maintainer="Izharul Haq"
#  Original document: contract.html
#  Author           : Manoj Srivastava ( srivasta@tiamat.datasync.com )
#  Created On       : Wed Jul  2 12:47:56 1997
```

Kenapa harus menggunakan versi *1.24* ? versi ini digunakan jika Anda telah menerjemahkan versi bahasa Inggris saat ini. 
Silahkan menggunakan perintah berikut:

```bash
$ cvs status english/social_contract.wml
===================================================================
File: social_contract.wml       Status: Up-to-date

   Working revision:    1.24
   Repository revision: 1.24    /cvsroot/webwml/webwml/english/social_contract.wml,v
   Commit Identifier:   D9MpCvx8enbuSCHu
   Sticky Tag:          (none)
   Sticky Date:         (none)
   Sticky Options:      (none)
```

Upload berkas *social_contract.wml* yang telah diterjemahkan ke alamat email debian-l10n-indonesian@lists.debian.org dengan 
menyertakan deskripsi tentang apa yang telah Anda kerjakan.

Contoh: ftp://debian-id.alioth.debian.org/pub/debian-id/send-email-page.png