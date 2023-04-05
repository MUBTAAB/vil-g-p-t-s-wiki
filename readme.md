# Wikipédia jellegű oldal világépítéshez 
Az alábbi útmutató célja, hogy könnyen, gyorsan egyszerűen tudjunk kisméretű, wikipédia jellegű oldalakat létrehozni. 

Ezek böngészőben megnyithatóak és egymásra, vagy külső linkekre mutathatak, így tökéletesek arra, hogy rendezzük bennük 
pl világépítést tartalmazó infókat. Szükség esetén könnyen (és ingyenesen) publikálhatóak gitubon vagy bitbucketen, 
így nyilvánosan is olvashatóvá tehetők.

Az útmutató azzal a céllal lett megfogalmazva, 
hogy közérthető legyen olyan írók számára, akik egyáltalán nem jártasak informatikai területen, 
nem tudnak és nem is akarnak megtanulni kódolni. 

## Tartalom
- [Létrehozás](#létrehozás)
- [Szerkesztés](#szerkesztés)
- [Megnyitás böngészőben](#megnyitás-böngészőben)
- [A markdown nyelv](#a-markdown-nyelv)
	- [CÍmek, alcímek, paragrafusok](#cimek-alcimek-paragrafusok)
	- [Képek](#képek)
	- [Linkek](#linkek)
	- [Tartalomjegyzék](#tartalomjegyzék)
- [Feltöltés online](#feltöltes-online)

## Létrehozás
1. Létrehozunk egy üres mappát 
2. Létrehozunk benne egy txt file-t (pelda.md)
	- Új -> Szöveges dokumentum
3. Átírjuk a file nevét, és átírjuk a kiterjesztését (tehát a neve végét) .txt-ről .md-re 
4. Így egy ún. markdown file-t hoztunk létre, ilyen a markdown file-ok alkotják majd a wikink oldalait

## Szerkesztés
A markdown file-t sima Notepaddal, vagy Notepad++ segítségével meg tudjuk nyitni. 
- Jobbklikk -> Társítás -> Notepad

Szerkesszük meg az oldalt. Erről részletesebben a [Markdown nyelv](#a-markdown-nyelv) pontban írok, 
de itt egy nagyon nagyon egyszerű példa:

```
# Példa cím
Hello world
```
Ezzel létre is hoztuk az wikink első oldalát. A következő lépésben nézzük meg, hogyan néz ki maga az oldal.

## Megnyitás böngészőben
Hogy a lokális file-ok böngkészőben megnyíljanak, szükség lesz egy markdown olvasó bővítményre. Ez egy gombnyomással telepíthető

Google Chrome-hoz például itt: https://chrome.google.com/webstore/detail/markdown-preview-plus/febilkbfcbhebfnokafefeacimjdckgl

Ha ezt feltelepítettétek böngészővel is meg tudjátok nyitni a Markdown file-t. 
- Jobbklikk -> Társítás -> Google Chrome 
- Avagy csak ráhúzzátok (drag and drop) a file-t a böngészőre

Ha követtétek az instrukciókat, az alábbiakat kell látnotok:
![image](https://user-images.githubusercontent.com/22019900/230039505-dae53a27-4c07-4779-a150-ed35d4131625.png)


## A Markdown nyelv
A Markdown nyelv egy nagyon-nagyon egyszerű szintaxis, mellyel egyszerű weboldalakat (html) lehet generálni. 
Azzal a céllal hozták létre, hogy minimális szerkesztéssel nagyon szép, rendezett dokumentumokat lehessen vele létrehozni. 
Részletesebben a Markdownról [itt](https://hu.wikipedia.org/wiki/Markdown). 

Nagyon jó online tutoriálok léteznek (például [ez](https://www.markdownguide.org/basic-syntax/)), de ez alapokat lentebb is leírom, 
ezeknél nincs is szükség többre. 

### Címek, alcímek, paragrafusok

```
# Ez egy cím
## Ez egy alcím
Ez pedig simán maga a szöveg

Új paragrafusokhoz csak hagyni kell egy üres sort a többi szöveg fölött
A félkövér szöveget **csillagok** közé kell rakni
```

A fenti kód következőket fogja produkálni:
![image](https://user-images.githubusercontent.com/22019900/230035700-0238ea6e-353e-4c91-9952-e018d45b0651.png)

### Képek
Magát a kép file-t közvetlenül a Markdown mellé kell rakni. 
Képeket az alábbi módon tudsz beágyazni.
`![image](./a_kep_file_neve.jpg)`

Egy online kép linkről is beágyazható, egyszerűen a zárójelbe a linket kell rakni.
`![image](https://user-images.githubusercontent.com/22019900/230036697-92001829-dad2-4283-801e-b52b57b5403d.png)`

### Linkek
Ha több oldalunk van, azok mutathatnak egymásra. Ilyenkor egyszerűen egymás mellé rakjuk a markdown file-okat, így:

![image](https://user-images.githubusercontent.com/22019900/230040948-bc82e8f8-4b3c-49a4-ba9f-4541a9dc20e7.png)

A másik oldalra a következőképpen hivatkozunk: 
`A szöveg amelybe a linket ágyazzuk [a szövegrész amelyről kattintható a link](./egy_masik_markdown_file.md) és megy tovább a szöveg blababla`
Ez a következőképpen néz ki majd a wikinkben 

A szöveg amelybe a linket ágyazzuk [a szövegrész amelyről kattintható a link](./egy_masik_markdown_file.md) és megy tovább a szöveg blababla

Természetesen online weboldalakra is lehet hivatkozni:
`A szöveg amelybe a linket ágyazzuk [a szövegrész amelyről kattintható a link](https://www.youtube.com/watch?v=dQw4w9WgXcQ&ab_channel=RickAstley) és megy tovább a szöveg blababla`
Ez pedig így fog kinézni:

A szöveg amelybe a linket ágyazzuk [a szövegrész amelyről kattintható a link](https://www.youtube.com/watch?v=dQw4w9WgXcQ&ab_channel=RickAstley) és megy tovább a szöveg blababla

### Listák

#### Bullet pointos lista

```
- Bullet 
- Pointos
- Lista
    - Persze lehet
    - Alpontokat is
    - Létrehozni
```
Így néz ki:

- Bullet 
- Pointos
- Lista
    - Persze lehet
    - Alpontokat is
    - Létrehozni
  
#### Számozott lista
```
1. Számozott
2. Lista
3. is van
```

A következőt produkálja:

1. Számozott
2. Lista
3. is van

### Tartalomjegyzék
Tartalomjegyzék létrehozása talán a legmacerásabb markdownban, de azért 
