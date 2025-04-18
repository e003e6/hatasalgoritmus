**Olyan algoritmus, ami külső értékíteletek jövőbeli hasznossága alapján rangsololja a csomópontok fontosságát, hatását más csomópontok vélekedésére és megjósolja jövőbeli értékíteiket.**

Belső dinamikai elemzés: a hálózat struktúrájából és a struktúrához tartozó cselekvés elemzésével jósoljuk előre a változó struktúra alapján a jövőbeli viselkedést.

---



Alapelvek:

1. A látens értéket a közös vélekedés határozza meg
2. A vélekedés kifejeződése a cselekedet
3. A cselekedet hatással van az összes többi csomópontot vélekedésre 

A hálózat nem egy kalsszikus kapcsolati háló, hanem egy hatás struktúra hálózat.

Minden csomópontak vagy egy egyedi vélekedése az árról, amit preferencia rendezéssel hoz meg melyben más csomópontok vélt fontossága és általuk hozott értékítele a döntés alapja. Ha az ár alacsonyabb mint vélt érték akkor vásárol (kinyilatkoztatja értékítéletét), ha alacsonabb akkor eladat (kinyilatkoztatja értékítéletét). Ezzel a cselekvéssel hatással van a hálózat összes többi szereplőjere akik az értékítélet után frissítik szubkejtív véleményüket az árról, majd véleményt alkotnak az cselekvő csomópont rájuk gyakorolt hatásáról az alapján hogy a jövő függvényében mennyire tett helyes cselekvést a saját értékítelete alapján.

## Beauty contest kritika

[A beauty contest kísérletekből](beautycontest.md#Beauty contest game) tudjuk, hogy a játékokban a nyerő szám mindig lényegesen magasabb, mint a 0, vagyis a játék szereplői sosem jutnak el a magasabb szintű gondolkosáig. 

A tőkepiaci spekuláció fogalmát át kell alakítani:

- **"Azt próbálom kitalálni, hogy mások mit fognak gondolni"** -> magas színtű gondolkozás, a játékosk kis részére jellemző
- **"Az addja a (látens) árupiaci értéket, hogy mások mit gondolnak róla"** -> alacson szintű gondolkozás, ahol klasszikus döntési eljárások alapján alkotnak véleményt a játékosok csak a preferenciájik más játékosok hatása

Ez az elv a közös tudást (remélem) képes kizárólag hálózati topológiaként leírni. 



