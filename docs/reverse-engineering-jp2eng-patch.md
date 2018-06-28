# Reverse engineering Someone 1.00's Jap2Eng Patcher

Someone 1.00's, a hacker from the early NEX hacking scene, built a few years ago a patcher that could alter camera region so that the camera language could be set to English if it was bought in Japan. The patcher was a Windows executable available on the [nex-hack website (archive.org link)](https://web.archive.org/web/20160305005438/http://nex-hack.info/wiki/_media/nex3.jap2eng.patcher.zip).

    * md5(nex3.jap2eng.patcher.zip) = 33b2bb7969d7ce7881b2263a80b0cd48
    * md5(Nex3.Jap2Eng.Patcher.exe) = e485aa28c2fc67cbfca0cf5d46523370

I tried to load it into a disassembler, and found the following strings :

```
.data:0053708C dword_53708C    dd 300030h              ; DATA XREF: sub_41E578+C0r
.data:0053708C                                         ; sub_41E578+D9r ...
.data:00537090 a01020304050607:
.data:00537090                 unicode 0, <010203040506070809101112131415161718192021222324252627282>
.data:00537090                 unicode 0, <930313233343536373839404142434445464748495051525354555657>
.data:00537090                 unicode 0, <585960616263646566676869707172737475767778798081828384858>
.data:00537090                 unicode 0, <687888990919293949596979899>
.data:0053721C dword_53721C    dd 300030h              ; DATA XREF: sub_41EA20+DFr
.data:0053721C                                         ; sub_41EA20+FBr ...
.data:00537220 a010203040506_0:
.data:00537220                 unicode 0, <0102030405060708090A0B0C0D0E0F101112131415161718191A1B1C1>
.data:00537220                 unicode 0, <D1E1F202122232425262728292A2B2C2D2E2F30313233343536373839>
.data:00537220                 unicode 0, <3A3B3C3D3E3F404142434445464748494A4B4C4D4E4F5051525354555>
.data:00537220                 unicode 0, <65758595A5B5C5D5E5F606162636465666768696A6B6C6D6E6F707172>
.data:00537220                 unicode 0, <737475767778797A7B7C7D7E7F808182838485868788898A8B8C8D8E8>
.data:00537220                 unicode 0, <F909192939495969798999A9B9C9D9E9FA0A1A2A3A4A5A6A7A8A9AAAB>
.data:00537220                 unicode 0, <ACADAEAFB0B1B2B3B4B5B6B7B8B9BABBBCBDBEBFC0C1C2C3C4C5C6C7C>
.data:00537220                 unicode 0, <8C9CACBCCCDCECFD0D1D2D3D4D5D6D7D8D9DADBDCDDDEDFE0E1E2E3E4>
.data:00537220                 unicode 0, <E5E6E7E8E9EAEBECEDEEEFF0F1F2F3F4F5F6F7F8F9FAFBFCFDFEFF>
```

It appears that the patching utility is just patching binary.
