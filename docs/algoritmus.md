---
title: Az algoritmus
---

## Célkitűzés

**Olyan algoritmus, ami külső értékíteletek jövőbeli hasznossága alapján rangsololja a csomópontok fontosságát, hatását más csomópontok vélekedésére és megjósolja jövőbeli értékíteiket.**

Belső dinamikai elemzés: a hálózat struktúrájából és a struktúrához tartozó cselekvés elemzésével jósoljuk előre a változó struktúra alapján a jövőbeli viselkedést.

## Beauty contest kritika

[A beauty contest kísérletekből](beautycontest.md#Beauty contest game) tudjuk, hogy a játékokban a nyerő szám mindig lényegesen magasabb, mint a 0, vagyis a játék szereplői sosem jutnak el a magasabb szintű gondolkosáig (vagy nem feltételezik, hogy a többiek eljutnak).

A tőkepiaci spekuláció fogalmát át kell alakítani:

- **"Azt próbálom kitalálni, hogy mások mit fognak gondolni"** -> magas színtű gondolkozás, a játékosk kis részére jellemző
- **"Az addja a (látens) árupiaci értéket, hogy mások mit gondolnak róla"** -> alacson szintű gondolkozás, ahol klasszikus döntési eljárások alapján alkotnak véleményt a játékosok csak a preferenciáik más játékosok hatása

Ez az elv a közös tudást [a BCG játék csak a közös tudás feltételezésével olható meg] (remélem) képes kizárólag hálózati topológiaként leírni. 

Az algortmunak magába kell foglalni, hogy a különböző szereplők más szinteken játszanak és ezeket univerzálisan tudnia kell kezelni. 

## Az algoritmus dinamikája

Alapelvek:

1. A látens értéket a közös vélekedés határozza meg
2. A vélekedés kifejeződése a cselekedet
3. A cselekedet hatással van az összes többi csomópontot vélekedésre

Létrehozok egy hálózatot. A hálózat nem egy kalsszikus kapcsolati háló, hanem egy hatás struktúra hálózat. Erre a speciális hálózatra írt (jelenleg fojuk fel így) centralitás mutató képes meghatározni melyik csomópont milyen és mekkora hatással van a többi csomópontra. 

Minden csomópontak vagy egy egyedi vélekedése az értékről, amit preferencia rendezéssel hoz meg melyben más csomópontok vélt fontossága és általuk hozott értékítele a döntés alapja. Ha az aktuális érték alacsonyabb mint vélt érték akkor vásárol (ezzel kinyilatkoztatja értékítéletét), ha alacsonabb akkor eladat (ezzel szintén kinyilatkoztatja értékítéletét). A cselekvésével hatással van a hálózat összes többi szereplőjere, akik az értékítélet után frissítik szubkejtív véleményüket az értékről, majd véleményt alkotnak az cselekvő csomópont rájuk gyakorolt hatásáról az alapján, hogy a jövő tekintetében mennyire tett helyes cselekvést a cselekvő a saját értékítelete alapján.

Az egyének súlya mindenkihez másodrendű rendezés.

Az egyéni értékek maximuma határozza meg az árfolyamot. Leegyszerűsítve: ha valakinek többet ér mint amennyiért megkaphaja akkor megveszi. 

Bináris vélekedés egy cselekvésről. Ha valaki adott árfolyamon vásárol akkor a többiek gondolhatják 1. ez hülye 2. helyesen járt el. Mindezt az előtt, hogy valóban kiderülni az eredmény. A cselekedet helyessége persze sosem fog véglegesen kiserülni mivel az árfolyamok folyamatosan változnak. Vagyis minden idő pillanatban az adott árolyam alapján megítélhetjük az összes múltbeli cselekedet jelen pillanatban mért helyességét. És ez alapján újra tudunk számolni mindent. 



## Befolyásolási hálózatok a szakirodalomban

*.... szakirodalom ismertetése ...*

Skálafüggetlen hálózatok -> kialakulnak nagy vélemény befolyásoló hatással rendelkező csomópontok "ha ő jónak tartja akkor én is" elv alapján. 

Ez felvet egy logikai problémát:

1. az értékre az van hatással, hogy ez a nagy befolyású egyén hogyan vélekedik (pl. vásárol)

   vagy

2. azért vásárol ez az illető mert ő valamilyen belő információ birtokában van. És a többiek azért tartják nagy befolyású egyénnek mert az ő viselkedésével előrejelezhető az árfolyam

Vagyis: valóban ő határzza meg az értéket, vagy csak informális előnyben van. 

Social Power: akik sokakra hatott korábban, annak véleményét később még nagyobb súlyal veszik figyelembe a többiek



---



Kulcsszavak (mindegyikből lesz egy fejezet)
- Preferencia súlyozás
- másodrendű rangsorolás
- Modális logika
- közös tudás
- Bizánciz tábornokok logika



