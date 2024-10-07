# An epic filesystem quest

Stay patient and keep on using the ls ls -a cat cd commands

```bash
Connected!                                                                        
cd /hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls -a
.   .dockerenv  bin   challenge  etc   home  lib32  libx32  mnt  opt   root  sbin  sys  usr
..  MESSAGE     boot  dev        flag  lib   lib64  media   nix  proc  run   srv   tmp  var
hacker@commands~an-epic-filesystem-quest:/$ cat MESSAGE
Yahaha, you found me!
The next clue is in: /usr/share/javascript/mathjax/unpacked/jax/output/HTML-CSS/fonts/TeX/Math/BoldItalic
hacker@commands~an-epic-filesystem-quest:/$ cd /usr/share/javascript/mathjax/unpacked/jax/output/HTML-CSS/fonts/TeX/Math/BoldItalic
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/unpacked/jax/output/HTML-CSS/fonts/TeX/Math/BoldItalic$ ls -a
.  ..  CUE  Main.js
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/unpacked/jax/output/HTML-CSS/fonts/TeX/Math/BoldItalic$ cat CUE
Great sleuthing!
The next clue is in: /usr/lib/x86_64-linux-gnu/gconv

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/unpacked/jax/output/HTML-CSS/fonts/TeX/Math/BoldItalic$ cd /usr/lib/x86_64-linux-gnu/gconv
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/gconv$ ls -a
.                   EUC-KR.so            IBM1160.so    IBM868.so           ISO8859-8.so
..                  EUC-TW.so            IBM1161.so    IBM869.so           ISO8859-9.so
ANSI_X3.110.so      GB18030.so           IBM1162.so    IBM870.so           ISO8859-9E.so
ARMSCII-8.so        GBBIG5.so            IBM1163.so    IBM871.so           ISO_10367-BOX.so
ASMO_449.so         GBGBK.so             IBM1164.so    IBM874.so           ISO_11548-1.so
BIG5.so             GBK.so               IBM1166.so    IBM875.so           ISO_2033.so
BIG5HKSCS.so        GEORGIAN-ACADEMY.so  IBM1167.so    IBM880.so           ISO_5427-EXT.so
BLUEPRINT           GEORGIAN-PS.so       IBM12712.so   IBM891.so           ISO_5427.so
BRF.so              GOST_19768-74.so     IBM1364.so    IBM901.so           ISO_5428.so
CP10007.so          GREEK-CCITT.so       IBM1371.so    IBM902.so           ISO_6937-2.so
CP1125.so           GREEK7-OLD.so        IBM1388.so    IBM903.so           ISO_6937.so
CP1250.so           GREEK7.so            IBM1390.so    IBM9030.so          JOHAB.so
CP1251.so           HP-GREEK8.so         IBM1399.so    IBM904.so           KOI-8.so
CP1252.so           HP-ROMAN8.so         IBM16804.so   IBM905.so           KOI8-R.so
CP1253.so           HP-ROMAN9.so         IBM256.so     IBM9066.so          KOI8-RU.so
CP1254.so           HP-THAI8.so          IBM273.so     IBM918.so           KOI8-T.so
CP1255.so           HP-TURKISH8.so       IBM274.so     IBM921.so           KOI8-U.so
CP1256.so           IBM037.so            IBM275.so     IBM922.so           LATIN-GREEK-1.so
CP1257.so           IBM038.so            IBM277.so     IBM930.so           LATIN-GREEK.so
CP1258.so           IBM1004.so           IBM278.so     IBM932.so           MAC-CENTRALEUROPE.so
CP737.so            IBM1008.so           IBM280.so     IBM933.so           MAC-IS.so
CP770.so            IBM1008_420.so       IBM281.so     IBM935.so           MAC-SAMI.so
CP771.so            IBM1025.so           IBM284.so     IBM937.so           MAC-UK.so
CP772.so            IBM1026.so           IBM285.so     IBM939.so           MACINTOSH.so
CP773.so            IBM1046.so           IBM290.so     IBM943.so           MIK.so
CP774.so            IBM1047.so           IBM297.so     IBM9448.so          NATS-DANO.so
CP775.so            IBM1097.so           IBM420.so     IEC_P27-1.so        NATS-SEFI.so
CP932.so            IBM1112.so           IBM423.so     INIS-8.so           PT154.so
CSN_369103.so       IBM1122.so           IBM424.so     INIS-CYRILLIC.so    RK1048.so
CWI.so              IBM1123.so           IBM437.so     INIS.so             SAMI-WS2.so
DEC-MCS.so          IBM1124.so           IBM4517.so    ISIRI-3342.so       SHIFT_JISX0213.so
EBCDIC-AT-DE-A.so   IBM1129.so           IBM4899.so    ISO-2022-CN-EXT.so  SJIS.so
EBCDIC-AT-DE.so     IBM1130.so           IBM4909.so    ISO-2022-CN.so      T.61.so
EBCDIC-CA-FR.so     IBM1132.so           IBM4971.so    ISO-2022-JP-3.so    TCVN5712-1.so
EBCDIC-DK-NO-A.so   IBM1133.so           IBM500.so     ISO-2022-JP.so      TIS-620.so
EBCDIC-DK-NO.so     IBM1137.so           IBM5347.so    ISO-2022-KR.so      TSCII.so
EBCDIC-ES-A.so      IBM1140.so           IBM803.so     ISO-IR-197.so       UHC.so
EBCDIC-ES-S.so      IBM1141.so           IBM850.so     ISO-IR-209.so       UNICODE.so
EBCDIC-ES.so        IBM1142.so           IBM851.so     ISO646.so           UTF-16.so
EBCDIC-FI-SE-A.so   IBM1143.so           IBM852.so     ISO8859-1.so        UTF-32.so
EBCDIC-FI-SE.so     IBM1144.so           IBM855.so     ISO8859-10.so       UTF-7.so
EBCDIC-FR.so        IBM1145.so           IBM856.so     ISO8859-11.so       VISCII.so
EBCDIC-IS-FRISS.so  IBM1146.so           IBM857.so     ISO8859-13.so       gconv-modules
EBCDIC-IT.so        IBM1147.so           IBM858.so     ISO8859-14.so       gconv-modules.cache
EBCDIC-PT.so        IBM1148.so           IBM860.so     ISO8859-15.so       libCNS.so
EBCDIC-UK.so        IBM1149.so           IBM861.so     ISO8859-16.so       libGB.so
EBCDIC-US.so        IBM1153.so           IBM862.so     ISO8859-2.so        libISOIR165.so
ECMA-CYRILLIC.so    IBM1154.so           IBM863.so     ISO8859-3.so        libJIS.so
EUC-CN.so           IBM1155.so           IBM864.so     ISO8859-4.so        libJISX0213.so
EUC-JISX0213.so     IBM1156.so           IBM865.so     ISO8859-5.so        libKSC.so
EUC-JP-MS.so        IBM1157.so           IBM866.so     ISO8859-6.so
EUC-JP.so           IBM1158.so           IBM866NAV.so  ISO8859-7.so
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/gconv$ cd BLUEPRINT
ssh-entrypoint: cd: BLUEPRINT: Not a directory
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/gconv$ cat BLUEPRINT
Lucky listing!
The next clue is in: /opt/busybox/busybox-1.33.2/include/config/warn

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/gconv$ ./opt
ssh-entrypoint: ./opt: No such file or directory
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/gconv$ /opt
ssh-entrypoint: /opt: Is a directory
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/gconv$ ./opt
ssh-entrypoint: ./opt: No such file or directory
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/gconv$ cd /opt
hacker@commands~an-epic-filesystem-quest:/opt$ ./busybox
ssh-entrypoint: ./busybox: Is a directory
hacker@commands~an-epic-filesystem-quest:/opt$ cd /opt
hacker@commands~an-epic-filesystem-quest:/opt$ ./busybox
ssh-entrypoint: ./busybox: Is a directory
hacker@commands~an-epic-filesystem-quest:/opt$ cd busybox
hacker@commands~an-epic-filesystem-quest:/opt/busybox$ /busybox-1.33.2
ssh-entrypoint: /busybox-1.33.2: No such file or directory
hacker@commands~an-epic-filesystem-quest:/opt/busybox$ ./busybox-1.33.2
ssh-entrypoint: ./busybox-1.33.2: Is a directory
Connected!                                                                        
hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls
MESSAGE  boot       dev  flag  lib    lib64   media  nix  proc  run   srv  tmp  var
bin      challenge  etc  home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~an-epic-filesystem-quest:/$ cat MESSAGE
Yahaha, you found me!
The next clue is in: /usr/share/javascript/mathjax/unpacked/jax/output/HTML-CSS/fonts/TeX/Math/BoldItalic
hacker@commands~an-epic-filesystem-quest:/$ cd /usr/share/javascript/mathjax/unpacked/jax/output/HTML-CSS/fonts/TeX/Math/BoldItalic
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/unpacked/jax/output/HTML-CSS/fonts/TeX/Math/BoldItalic$ ls 
CUE  Main.js
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/unpacked/jax/output/HTML-CSS/fonts/TeX/Math/BoldItalic$ cat CUE
Great sleuthing!
The next clue is in: /usr/lib/x86_64-linux-gnu/gconv

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/unpacked/jax/output/HTML-CSS/fonts/TeX/Math/BoldItalic$ cd /usr/lib/x86_64-linux-gnu/gconv
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/gconv$ ls
ANSI_X3.110.so      EBCDIC-UK.so         IBM1140.so   IBM423.so     IBM930.so           ISO_6937-2.so
ARMSCII-8.so        EBCDIC-US.so         IBM1141.so   IBM424.so     IBM932.so           ISO_6937.so
ASMO_449.so         ECMA-CYRILLIC.so     IBM1142.so   IBM437.so     IBM933.so           JOHAB.so
BIG5.so             EUC-CN.so            IBM1143.so   IBM4517.so    IBM935.so           KOI-8.so
BIG5HKSCS.so        EUC-JISX0213.so      IBM1144.so   IBM4899.so    IBM937.so           KOI8-R.so
BLUEPRINT           EUC-JP-MS.so         IBM1145.so   IBM4909.so    IBM939.so           KOI8-RU.so
BRF.so              EUC-JP.so            IBM1146.so   IBM4971.so    IBM943.so           KOI8-T.so
CP10007.so          EUC-KR.so            IBM1147.so   IBM500.so     IBM9448.so          KOI8-U.so
CP1125.so           EUC-TW.so            IBM1148.so   IBM5347.so    IEC_P27-1.so        LATIN-GREEK-1.so
CP1250.so           GB18030.so           IBM1149.so   IBM803.so     INIS-8.so           LATIN-GREEK.so
CP1251.so           GBBIG5.so            IBM1153.so   IBM850.so     INIS-CYRILLIC.so    MAC-CENTRALEUROPE.so
CP1252.so           GBGBK.so             IBM1154.so   IBM851.so     INIS.so             MAC-IS.so
CP1253.so           GBK.so               IBM1155.so   IBM852.so     ISIRI-3342.so       MAC-SAMI.so
CP1254.so           GEORGIAN-ACADEMY.so  IBM1156.so   IBM855.so     ISO-2022-CN-EXT.so  MAC-UK.so
CP1255.so           GEORGIAN-PS.so       IBM1157.so   IBM856.so     ISO-2022-CN.so      MACINTOSH.so
CP1256.so           GOST_19768-74.so     IBM1158.so   IBM857.so     ISO-2022-JP-3.so    MIK.so
CP1257.so           GREEK-CCITT.so       IBM1160.so   IBM858.so     ISO-2022-JP.so      NATS-DANO.so
CP1258.so           GREEK7-OLD.so        IBM1161.so   IBM860.so     ISO-2022-KR.so      NATS-SEFI.so
CP737.so            GREEK7.so            IBM1162.so   IBM861.so     ISO-IR-197.so       PT154.so
CP770.so            HP-GREEK8.so         IBM1163.so   IBM862.so     ISO-IR-209.so       RK1048.so
CP771.so            HP-ROMAN8.so         IBM1164.so   IBM863.so     ISO646.so           SAMI-WS2.so
CP772.so            HP-ROMAN9.so         IBM1166.so   IBM864.so     ISO8859-1.so        SHIFT_JISX0213.so
CP773.so            HP-THAI8.so          IBM1167.so   IBM865.so     ISO8859-10.so       SJIS.so
CP774.so            HP-TURKISH8.so       IBM12712.so  IBM866.so     ISO8859-11.so       T.61.so
CP775.so            IBM037.so            IBM1364.so   IBM866NAV.so  ISO8859-13.so       TCVN5712-1.so
CP932.so            IBM038.so            IBM1371.so   IBM868.so     ISO8859-14.so       TIS-620.so
CSN_369103.so       IBM1004.so           IBM1388.so   IBM869.so     ISO8859-15.so       TSCII.so
CWI.so              IBM1008.so           IBM1390.so   IBM870.so     ISO8859-16.so       UHC.so
DEC-MCS.so          IBM1008_420.so       IBM1399.so   IBM871.so     ISO8859-2.so        UNICODE.so
EBCDIC-AT-DE-A.so   IBM1025.so           IBM16804.so  IBM874.so     ISO8859-3.so        UTF-16.so
EBCDIC-AT-DE.so     IBM1026.so           IBM256.so    IBM875.so     ISO8859-4.so        UTF-32.so
EBCDIC-CA-FR.so     IBM1046.so           IBM273.so    IBM880.so     ISO8859-5.so        UTF-7.so
EBCDIC-DK-NO-A.so   IBM1047.so           IBM274.so    IBM891.so     ISO8859-6.so        VISCII.so
EBCDIC-DK-NO.so     IBM1097.so           IBM275.so    IBM901.so     ISO8859-7.so        gconv-modules
EBCDIC-ES-A.so      IBM1112.so           IBM277.so    IBM902.so     ISO8859-8.so        gconv-modules.cache
EBCDIC-ES-S.so      IBM1122.so           IBM278.so    IBM903.so     ISO8859-9.so        libCNS.so
EBCDIC-ES.so        IBM1123.so           IBM280.so    IBM9030.so    ISO8859-9E.so       libGB.so
EBCDIC-FI-SE-A.so   IBM1124.so           IBM281.so    IBM904.so     ISO_10367-BOX.so    libISOIR165.so
EBCDIC-FI-SE.so     IBM1129.so           IBM284.so    IBM905.so     ISO_11548-1.so      libJIS.so
EBCDIC-FR.so        IBM1130.so           IBM285.so    IBM9066.so    ISO_2033.so         libJISX0213.so
EBCDIC-IS-FRISS.so  IBM1132.so           IBM290.so    IBM918.so     ISO_5427-EXT.so     libKSC.so
EBCDIC-IT.so        IBM1133.so           IBM297.so    IBM921.so     ISO_5427.so
EBCDIC-PT.so        IBM1137.so           IBM420.so    IBM922.so     ISO_5428.so
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/gconv$ cat BLUEPRINT
Lucky listing!
The next clue is in: /opt/busybox/busybox-1.33.2/include/config/warn

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/gconv$ ls /opt/busybox/busybox-1.33.2/include/config/warn
MEMO-TRAPPED  simple
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/gconv$ cat MEMO-TRAPPED
cat: MEMO-TRAPPED: No such file or directory
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/gconv$ sudo MEMO-TRAPPED
Connected!                                                                        
hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls
MESSAGE  boot       dev  flag  lib    lib64   media  nix  proc  run   srv  tmp  var
bin      challenge  etc  home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~an-epic-filesystem-quest:/$ cat MESSAGE
Yahaha, you found me!
The next clue is in: /usr/share/javascript/mathjax/unpacked/jax/output/HTML-CSS/fonts/TeX/Math/BoldItalic
hacker@commands~an-epic-filesystem-quest:/$ cd  /usr/share/javascript/mathjax/unpacked/jax/output/HTML-CSS/fonts/TeX/Math/BoldItalic
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/unpacked/jax/output/HTML-CSS/fonts/TeX/Math/BoldItalic$ ls
CUE  Main.js
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/unpacked/jax/output/HTML-CSS/fonts/TeX/Math/BoldItalic$ cat CUE
Great sleuthing!
The next clue is in: /usr/lib/x86_64-linux-gnu/gconv

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/unpacked/jax/output/HTML-CSS/fonts/TeX/Math/BoldItalic$ cd /usr/lib/x86_64-linux-gnu/gconv
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/gconv$ ls
ANSI_X3.110.so     EBCDIC-DK-NO-A.so    HP-ROMAN9.so    IBM1153.so   IBM420.so     IBM880.so           ISO646.so         LATIN-GREEK.so
ARMSCII-8.so       EBCDIC-DK-NO.so      HP-THAI8.so     IBM1154.so   IBM423.so     IBM891.so           ISO8859-1.so      MAC-CENTRALEUROPE.so
ASMO_449.so        EBCDIC-ES-A.so       HP-TURKISH8.so  IBM1155.so   IBM424.so     IBM901.so           ISO8859-10.so     MAC-IS.so
BIG5.so            EBCDIC-ES-S.so       IBM037.so       IBM1156.so   IBM437.so     IBM902.so           ISO8859-11.so     MAC-SAMI.so
BIG5HKSCS.so       EBCDIC-ES.so         IBM038.so       IBM1157.so   IBM4517.so    IBM903.so           ISO8859-13.so     MAC-UK.so
BLUEPRINT          EBCDIC-FI-SE-A.so    IBM1004.so      IBM1158.so   IBM4899.so    IBM9030.so          ISO8859-14.so     MACINTOSH.so
BRF.so             EBCDIC-FI-SE.so      IBM1008.so      IBM1160.so   IBM4909.so    IBM904.so           ISO8859-15.so     MIK.so
CP10007.so         EBCDIC-FR.so         IBM1008_420.so  IBM1161.so   IBM4971.so    IBM905.so           ISO8859-16.so     NATS-DANO.so
CP1125.so          EBCDIC-IS-FRISS.so   IBM1025.so      IBM1162.so   IBM500.so     IBM9066.so          ISO8859-2.so      NATS-SEFI.so
CP1250.so          EBCDIC-IT.so         IBM1026.so      IBM1163.so   IBM5347.so    IBM918.so           ISO8859-3.so      PT154.so
CP1251.so          EBCDIC-PT.so         IBM1046.so      IBM1164.so   IBM803.so     IBM921.so           ISO8859-4.so      RK1048.so
CP1252.so          EBCDIC-UK.so         IBM1047.so      IBM1166.so   IBM850.so     IBM922.so           ISO8859-5.so      SAMI-WS2.so
CP1253.so          EBCDIC-US.so         IBM1097.so      IBM1167.so   IBM851.so     IBM930.so           ISO8859-6.so      SHIFT_JISX0213.so
CP1254.so          ECMA-CYRILLIC.so     IBM1112.so      IBM12712.so  IBM852.so     IBM932.so           ISO8859-7.so      SJIS.so
CP1255.so          EUC-CN.so            IBM1122.so      IBM1364.so   IBM855.so     IBM933.so           ISO8859-8.so      T.61.so
CP1256.so          EUC-JISX0213.so      IBM1123.so      IBM1371.so   IBM856.so     IBM935.so           ISO8859-9.so      TCVN5712-1.so
CP1257.so          EUC-JP-MS.so         IBM1124.so      IBM1388.so   IBM857.so     IBM937.so           ISO8859-9E.so     TIS-620.so
CP1258.so          EUC-JP.so            IBM1129.so      IBM1390.so   IBM858.so     IBM939.so           ISO_10367-BOX.so  TSCII.so
CP737.so           EUC-KR.so            IBM1130.so      IBM1399.so   IBM860.so     IBM943.so           ISO_11548-1.so    UHC.so
CP770.so           EUC-TW.so            IBM1132.so      IBM16804.so  IBM861.so     IBM9448.so          ISO_2033.so       UNICODE.so
CP771.so           GB18030.so           IBM1133.so      IBM256.so    IBM862.so     IEC_P27-1.so        ISO_5427-EXT.so   UTF-16.so
CP772.so           GBBIG5.so            IBM1137.so      IBM273.so    IBM863.so     INIS-8.so           ISO_5427.so       UTF-32.so
CP773.so           GBGBK.so             IBM1140.so      IBM274.so    IBM864.so     INIS-CYRILLIC.so    ISO_5428.so       UTF-7.so
CP774.so           GBK.so               IBM1141.so      IBM275.so    IBM865.so     INIS.so             ISO_6937-2.so     VISCII.so
CP775.so           GEORGIAN-ACADEMY.so  IBM1142.so      IBM277.so    IBM866.so     ISIRI-3342.so       ISO_6937.so       gconv-modules
CP932.so           GEORGIAN-PS.so       IBM1143.so      IBM278.so    IBM866NAV.so  ISO-2022-CN-EXT.so  JOHAB.so          gconv-modules.cache
CSN_369103.so      GOST_19768-74.so     IBM1144.so      IBM280.so    IBM868.so     ISO-2022-CN.so      KOI-8.so          libCNS.so
CWI.so             GREEK-CCITT.so       IBM1145.so      IBM281.so    IBM869.so     ISO-2022-JP-3.so    KOI8-R.so         libGB.so
DEC-MCS.so         GREEK7-OLD.so        IBM1146.so      IBM284.so    IBM870.so     ISO-2022-JP.so      KOI8-RU.so        libISOIR165.so
EBCDIC-AT-DE-A.so  GREEK7.so            IBM1147.so      IBM285.so    IBM871.so     ISO-2022-KR.so      KOI8-T.so         libJIS.so
EBCDIC-AT-DE.so    HP-GREEK8.so         IBM1148.so      IBM290.so    IBM874.so     ISO-IR-197.so       KOI8-U.so         libJISX0213.so
EBCDIC-CA-FR.so    HP-ROMAN8.so         IBM1149.so      IBM297.so    IBM875.so     ISO-IR-209.so       LATIN-GREEK-1.so  libKSC.so
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/gconv$ cat BLUEPRINT
Lucky listing!
The next clue is in: /opt/busybox/busybox-1.33.2/include/config/warn

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/gconv$ ls  /opt/busybox/busybox-1.33.2/include/config/warn
MEMO-TRAPPED  simple
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/gconv$ cat /opt/busybox/busybox-1.33.2/include/config/warn/MEMO-TRAPPED
Tubular find!
The next clue is in: /opt/linux/linux-5.4/include/config/ext4/fs
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/gconv$ cd /opt/linux/linux-5.4/include/config/ext4/fs
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/config/ext4/fs$ ls
DISPATCH  posix  security.h
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/config/ext4/fs$ cat DISPATCH
Yahaha, you found me!
The next clue is in: /usr/share/vim/vim81/lang/de

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/config/ext4/fs$ cd  /usr/share/vim/vim81/lang/de
hacker@commands~an-epic-filesystem-quest:/usr/share/vim/vim81/lang/de$ ls -a
.  ..  .TIP  LC_MESSAGES
hacker@commands~an-epic-filesystem-quest:/usr/share/vim/vim81/lang/de$ cat .TIP
Great sleuthing!
The next clue is in: /opt/linux/linux-5.4/drivers/crypto/ux500

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/share/vim/vim81/lang/de$ ls /opt/linux/linux-5.4/drivers/crypto/ux500
INFO-TRAPPED  Kconfig  Makefile  cryp  hash
hacker@commands~an-epic-filesystem-quest:/usr/share/vim/vim81/lang/de$ cat /opt/linux/linux-5.4/drivers/crypto/ux500/INFO-TRAPPED
Congratulations, you found the clue!
The next clue is in: /opt/linux/linux-5.4/arch/x86/platform/ts5500
hacker@commands~an-epic-filesystem-quest:/usr/share/vim/vim81/lang/de$ cd /opt/linux/linux-5.4/arch/x86/platform/ts5500
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/x86/platform/ts5500$ ls 
INSIGHT  Makefile  built-in.a  ts5500.c
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/x86/platform/ts5500$ cat INSIGHT
Great sleuthing!
The next clue is in: /opt/radare2/shlr/capstone/packages/freebsd/ports

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/x86/platform/ts5500$ cd /opt/radare2/shlr/capstone/packages/freebsd/ports
hacker@commands~an-epic-filesystem-quest:/opt/radare2/shlr/capstone/packages/freebsd/ports$ ls -a
.  ..  .POINTER  devel
hacker@commands~an-epic-filesystem-quest:/opt/radare2/shlr/capstone/packages/freebsd/ports$ cat .POINTER
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{AjgYXKgM_XpY_1aTulKyaC1F1_V.dljM4QDL4ETN0czW}
hacker@commands~an-epic-filesystem-quest:/opt/radare2/shlr/capstone/packages/freebsd/ports$ 

```
