# Archi Helper
Fontosabb assembly utasítások, Dosboxban való programok futtatása.

## Jelek értelmezése az "ArchiHelper.txt" állományban:

|<center>Jelölés</center>|<center>Mit jelent</center>|<center>Példa:</center>|
|----|----|----|
|<center>3 sor '#'</center>|Nagyobb témák elválasztása.|<center>-</center>|
|<center>1 sor '#'</center>|Egy nagy témát több kisebb alrészre bont.|<center>-</center>|
|<center>Szöveg/szám '*' között</center>|Gyors elérésm témák száma, neve. Ezekre ha rákeresünk egyből az adott témához ugorhatunk.|<center>\*6.5\* - \*shr\*</center>|
|<center>Egy sor '.'</center>|Elválasztó jel, 2 ilyen sor között programkód található|<center>-</center>|
|<center>{SZOVEG}</center>|Behelyettesítendő szöveg|<center>shr {MIT},{MENNYIVEL}</center>|
|<center>...</center>|Nem lényeges kód sorok, ez akár több sort is reprezentálhat, de nem lényeges a bemutató szempontjából|<center>...</center>|

## Témák gyors elérése:
### Használata:
Az "ArchiHelper.txt" állományban keressünk rá az adott számú elem számára vagy nevére.

Pl.: Kíváncsiak vagyunk hogy hogyan néz ki a program váza: 
    keresés szövege: \*2\* vagy \*program váz\* vagy \*2\* - \*program váz\*

1. exe létrehozása
2. program váz
3. karakter kiíratás
4. szöveg kiíratás
5. műveletek
    1. mov
    2. add
    3. sub
    4. cmp
    5. jmp
    6. jz
    7. jnz
    8. jc
    9. jnc
    10. többi jump
6. bináris műveletek
    1. and
    2. or
    3. xor
    4. shl
    5. shr
    6. rol
    7. ror

## Dosboxban programok futtatása

1. Hozzunk létre egy mappát a számítógépünkön amiben majd a programunkat fogjuk elkészíteni, ebben a mappában előnyös ha benne van a **masm.exe** és a **link.exe**.
2. Hozzunk létre egy programot **.asm** kiterjesztéssel a mappában.
3. Nyissuk meg a Dosboxot.
4. írjuk be a következőt: **<code>mount c {mappánk elérési utvonala}</code>**
5. Váltsunk a felcsatolt mappába: **<code>C:</code>**
6. (Opcionális) Győződjünk meg hogy az adott filejaink a mappában vannak-e: **<code>dir</code>**
7. EXE létrehozása Dosboxban: **<code>masm.exe program.asm,,,,</code>** majd **<code>link.exe program.obj,,,,</code>**
8. EXE futtatása: **<code>program.exe</code>**

A megosztott mappában tudunk tovább dolgozni, **nem kell minden egyes mappában történő változtatás, fájl létrehozás után újra felcsatolni mount-al**!