## Symfony egyszerű tesztfeladat

Ez a repository egy tesztfeladat kiírása, melyenk keretében egy parancssorból használható TODO alkalmazást kell létrehoznod. 

Elvárások:

- A megvalósításhoz használj olyan Symfony keretrendszer verziót és csomagokat, amik jelenleg is támogatottak.  
 - A git clone utáni első elindítás laikusként is egyszerű legyen: ne kelljen xy parancsokat lefuttatni csomagok telepítéséhez, adatbázis inicializálásához külön, hanem legyen erre egy, valamilyen build script. (feltételezhetjük, hogy elérhetőek lesznek ezek futtatásához szükséges függőségek: php, make, ant, stb, de akár a docker compose fájlt is módosíthatod)
 - Ne legyen szükség adatbázist létrehozni külső adatbázimotorhoz kapcsolódva, hanem oldja meg az alkalmazás az adatok tárolását valamilyen fájl alapú tárolóban.
 - A feladatokról a következő információkat tárolja:
   - description
   - creation date
   - status (NEW, INPROGRESS, ONHOLD, DONE)
 - a feladatok kezelése parancssorból legyen elérhető (pl `php bin/console list`), és a következő műveleteket lehessen végezni az elemekkel:
   - `list`
   - `create {DESCRIPTION}`
   - `update-status {STATUS}`
 - A státuszok változtatása során (pl `php`) a következő átmenetek legyenek elérhetőek. (más esetben jelezzen hibát az alkalmazás)
   - új létrehozása esetén: `NEW`
   - `NEW` => `INPROGRESS`
   - `INPROGRESS` => `ONHOLD`
   - `INPROGRESS` => `DONE`
 - Az elemeken végzett műveletekről készüljön tevékenységnapló, és ezt az egyet webes felületen is tudja listázni az alkalmazás. Ez a funkció különálló modulként legyen megvalósítva, ami nélkül tud működni az alkalmazás.

A feladat megoldását tetszőleges módon elküldheted, de szívesen vesszük, ha ezt PR formájában teszed github-on.   
Ha nem tudod megoldani a teljes működést, küldd el ameddig jutottál, és írd meg a hogyan folytattad volna, miben akadtál el!



