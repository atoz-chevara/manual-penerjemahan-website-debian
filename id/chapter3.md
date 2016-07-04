# MENERJEMAHKAN BERKAS po.

    $ cd webwml/indonesian/po
    $ vi templates.id.po

Sunting berkas *templates.id.po* sehingga sesuai dengan berikut ini:

```
"Last-Translator: Nama Anda <nama-user@debian-id.org>\n"
"Language-Team: Indonesian <debian-l10n-indonesian@lists.debian.org>\n"
```

Anda dapat menggunakan text editor atau applikasi seperti [poedit](https://poedit.net/download "unduh poedit") & 
[virtaal](http://virtaal.translatehouse.org/download.html "unduh virtaal"). Periksa kembali hasil terjemahan Anda:

    $ msgfmt --statistics -c -v -o /dev/null templates.id.po

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