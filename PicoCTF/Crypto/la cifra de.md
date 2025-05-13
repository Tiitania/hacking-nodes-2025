#### Description

I found this cipher in an old book. Can you figure out what it says? Connect with `nc jupiter.challenges.picoctf.org 32411`.
#### Hints 
- There are tools that make this easy.
- Perhaps looking at history will help

```

input: Ne iy nytkwpsznyg nth it mtsztcy vjzprj zfzjy rkhpibj nrkitt ltc tnnygy ysee itd tte cxjltk

Ifrosr tnj noawde uk siyyzre, yse Bnretèwp Cousex mls hjpn xjtnbjytki xatd eisjd

Iz bls lfwskqj azycihzeej yz Brftsk ip Volpnèxj ls oy hay tcimnyarqj dkxnrogpd os 1553 my Mnzvgs Mazytszf Merqlsu ny hox moup Wa inqrg ipl. Ynr. Gotgat Gltzndtg Gplrfdo 

Ltc tnj tmvqpmkseaznzn uk ehox nivmpr g ylbrj ts ltcmki my yqtdosr tnj wocjc hgqq ol fy oxitngwj arusahje fuw ln guaaxjytrd catizm tzxbkw zf vqlckx hizm ceyupcz yz tnj fpvjc hgqqpohzCZK{m311a50_0x_a1rn3x3_h1ah3x7g996649}

Ehk ktryy herq-ooizxetypd jjdcxnatoty ol f aordllvmlbkytc inahkw socjgex, bls sfoe gwzuti 1467 my Rjzn Hfetoxea Gqmexyt.

Tnj Gimjyèrk Htpnjc iy ysexjqoxj dosjeisjd cgqwej yse Gqmexyt Doxn ox Fwbkwei Inahkw.

Tn 1508, Ptsatsps Zwttnjxiax tnbjytki ehk xz-cgqwej ylbaql rkhea (g rltxni ol xsilypd gqahggpty) ysaz bzuri wazjc bk f nroytcgq nosuznkse ol yse Bnretèwp Cousex.

Gplrfdo’y xpcuso butvlky lpvjlrki tn 1555 gx l cuseitzltoty ol yse lncsz. Yse rthex mllbjd ol yse gqahggpty fce tth snnqtki cemzwaxqj, bay ehk fwpnfmezx lnj yse osoed qptzjcs gwp mocpd hd xegsd ol f xnkrznoh vee usrgxp, wnnnh ify bk itfljcety hizm paim noxwpsvtydkse.

recipe: Vigenere Decode Key: Flag
output: It is interesting how in history people often receive credit for things they did not create

During the course of history, the Vigenère Cipher has been reinvented many times

It was falsely attributed to Blaise de Vigenère as it was originally described in 1553 by Giovan Battista Bellaso in his book La cifra del. Sig. Giovan Battista Bellaso 

For the implementation of this cipher a table is formed by sliding the lower half of an ordinary alphabet for an apparently random number of places with respect to the upper halfpicoCTF{b311a50_0r_v1gn3r3_c1ph3r7b996649}

The first well-documented description of a polyalphabetic cipher however, was made around 1467 by Leon Battista Alberti.

The Vigenère Cipher is therefore sometimes called the Alberti Disc or Alberti Cipher.

In 1508, Johannes Trithemius invented the so-called tabula recta (a matrix of shifted alphabets) that would later be a critical component of the Vigenère Cipher.

Bellaso’s second booklet appeared in 1555 as a continuation of the first. The lower halves of the alphabets are now shifted regularly, but the alphabets and the index letters are mixed by means of a mnemonic key phrase, which can be different with each correspondent.


picoCTF{b311a50_0r_v1gn3r3_c1ph3r7b996649}




```

## Referencias
https://gchq.github.io/CyberChef/#recipe=Vigen%C3%A8re_Decode('flag')&input=TmUgaXkgbnl0a3dwc3pueWcgbnRoIGl0IG10c3p0Y3kgdmp6cHJqIHpmemp5IHJraHBpYmogbnJraXR0IGx0YyB0bm55Z3kgeXNlZSBpdGQgdHRlIGN4amx0aw0KDQpJZnJvc3IgdG5qIG5vYXdkZSB1ayBzaXl5enJlLCB5c2UgQm5yZXTDqHdwIENvdXNleCBtbHMgaGpwbiB4anRuYmp5dGtpIHhhdGQgZWlzamQNCg0KSXogYmxzIGxmd3NrcWogYXp5Y2loemVlaiB5eiBCcmZ0c2sgaXAgVm9scG7DqHhqIGxzIG95IGhheSB0Y2ltbnlhcnFqIGRreG5yb2dwZCBvcyAxNTUzIG15IE1uenZncyBNYXp5dHN6ZiBNZXJxbHN1IG55IGhveCBtb3VwIFdhIGlucXJnIGlwbC4gWW5yLiBHb3RnYXQgR2x0em5kdGcgR3BscmZkbyANCg0KTHRjIHRuaiB0bXZxcG1rc2Vhem56biB1ayBlaG94IG5pdm1wciBnIHlsYnJqIHRzIGx0Y21raSBteSB5cXRkb3NyIHRuaiB3b2NqYyBoZ3FxIG9sIGZ5IG94aXRuZ3dqIGFydXNhaGplIGZ1dyBsbiBndWFheGp5dHJkIGNhdGl6bSB0enhia3cgemYgdnFsY2t4IGhpem0gY2V5dXBjeiB5eiB0bmogZnB2amMgaGdxcXBvaHpDWkt7bTMxMWE1MF8weF9hMXJuM3gzX2gxYWgzeDdnOTk2NjQ5fQ0KDQpFaGsga3RyeXkgaGVycS1vb2l6eGV0eXBkIGpqZGN4bmF0b3R5IG9sIGYgYW9yZGxsdm1sYmt5dGMgaW5haGt3IHNvY2pnZXgsIGJscyBzZm9lIGd3enV0aSAxNDY3IG15IFJqem4gSGZldG94ZWEgR3FtZXh5dC4NCg0KVG5qIEdpbWp5w6hyayBIdHBuamMgaXkgeXNleGpxb3hqIGRvc2plaXNqZCBjZ3F3ZWogeXNlIEdxbWV4eXQgRG94biBveCBGd2Jrd2VpIEluYWhrdy4NCg0KVG4gMTUwOCwgUHRzYXRzcHMgWnd0dG5qeGlheCB0bmJqeXRraSBlaGsgeHotY2dxd2VqIHlsYmFxbCBya2hlYSAoZyBybHR4bmkgb2wgeHNpbHlwZCBncWFoZ2dwdHkpIHlzYXogYnp1cmkgd2F6amMgYmsgZiBucm95dGNncSBub3N1em5rc2Ugb2wgeXNlIEJucmV0w6h3cCBDb3VzZXguDQoNCkdwbHJmZG/igJl5IHhwY3VzbyBidXR2bGt5IGxwdmpscmtpIHRuIDE1NTUgZ3ggbCBjdXNlaXR6bHRvdHkgb2wgeXNlIGxuY3N6LiBZc2UgcnRoZXggbWxsYmpkIG9sIHlzZSBncWFoZ2dwdHkgZmNlIHR0aCBzbm5xdGtpIGNlbXp3YXhxaiwgYmF5IGVoayBmd3BuZm1lenggbG5qIHlzZSBvc29lZCBxcHR6amNzIGd3cCBtb2NwZCBoZCB4ZWdzZCBvbCBmIHhua3J6bm9oIHZlZSB1c3JneHAsIHdubm5oIGlmeSBiayBpdGZsamNldHkgaGl6bSBwYWltIG5veHdwc3Z0eWRrc2UuDQo&oenc=65001&ieol=CRLF&oeol=CRLF