# Pumpa DanaRS a Dana-i

*Tyto pokyny slouží k nastavení aplikace a pumpy DanaRS od roku 2017 nebo nejnovější Dana-i. Pokud máte původní DanaR, navštivte [Pumpa DanaR](./DanaR-Insulin-Pump).*

**Pumpu Dana RS s firmwarem v3 lze použít pouze s AndroidAPS verze 2.7 a vyšší.**

**Novou pumpu Dana-i lze použít pouze s AndroidAPS verze 3.0 a vyšší.**

* V pumpě DanaRS/i je aplikací používán "BAZÁL A". Stávající data budou přepsána.

## Párování pumpy

* Na domovské obrazovce AndroidAPS klikněte na hamburger menu v levém horním rohu a přejděte do Konfigurace.
* V sekci pumpy vyberte 'Dana-i/RS'.
* Kliknutím na ozubené kolo se dostanete přímo do nastavení pumpy nebo se vrátíte na hlavní obrazovku.
    
    ![Konfigurace AAPS Dana-i/RS](../images/DanaRS_i_ConfigB.png)

* Přejít na záložku 'DANA-i/RS'.

* Vyberte nabídku nastavení klepnutím na 3 tečky v pravém horním rohu. 
* Zvolte 'Rozšířená nastavení Dana-i/RS'.
* Klikněte na "Vybranou pumpu".
* V okně párování vyberte vaší pumpu.
    
    ![AAPS párování Dana-i/RS](../images/DanaRS_i_Pairing.png)

* **Je třeba potvrdit párování na pumpě!** Stejný způsob, na který jste zvyklí z párování ostatních BT zařízení (např. telefonů a auta).
    
    ![Potvrzování Dana RS párování](../images/DanaRS_Pairing.png)

* Postupujte podle procesu párování na základě typu a firmwaru vaší pumpy:
    
    * Pro DanaRS v1 vyberte v nastavení heslo pumpy a nastavte si ho.
    * Pro DanaRS v3 musíte zadat 2 sekvence čísel a písmen zobrazených na pumpě do dialogu párování AndroidAPS.
    * Pro Dana-i se zobrazí standardní dialogové okno párování Android a musíte zadat 6-místné číslo zobrazené na pumpě.

* Vyberte rychlost bolusu, abyste změnili výchozí rychlost bolusu (12sec na 1U, 30sec na 1U nebo 60sec na 1U).

* Nastavte bazální dávkování na 0,01 U/h pomocí lékařského menu (viz uživatelská příručka pumpy).
* Nastavte krok bolusu na 0.05 U/h pomocí lékařského menu (viz uživatelská příručka pumpy).
* Na pumpě povolte rozšířené bolusy

### Výchozí heslo

* DanaRS s firmwarem v1 a v2 má výchozí heslo 1234.
* Pro DanaRS s firmwarem v3 nebo Dana-i je výchozím heslem kombinace měsíce a data výroby (tj. měsíc 01 a den 24).
    
    * Otevřete hlavní menu na pumpě > Přehled > Informace. 
    * Číslo 3 je datum výroby. 
    * Pro v3/i se toto heslo používá pouze pro uzamčení nabídky na pumpě. Nepoužívá se pro komunikaci a není nutné jej zadat v AndroidAPS.

## Změna hesla pumpy

* Stiskněte tlačítko OK na pumpě
* V hlavní nabídce zvolte "Možnosti" (posuňte se vpravo několikrát stisknutím šipky)
    
    ![Hlavní menu DanaRS](../images/DanaRSPW_01_MainMenu.png)

* V nabídce možností vyberte "UŽIV. FUNKCE"
    
    ![Nastavení DanaRS](../images/DanaRSPW_02_OptionMenu.png)

* Pomocí tlačítka šipky přejdete dolů na "11. heslo"
    
    ![DanaRS 11. Heslo](../images/DanaRSPW_03_11PW.png)

* Stiskněte OK pro zadání starého hesla.

* Zadejte **staré heslo** (Výchozí heslo viz [nahoře](#default-password)) a stiskněte tlačítko OK
    
    ![DanaRS Zadejte staré heslo](../images/DanaRSPW_04_11PWenter.png)

* Je-li zde zadáno chybné heslo, nebude zde žádná zpráva indikující selhání!

* Nastavte **nové heslo** (Změňte čísla pomocí + & - tlačítka / Přesunout vpravo pomocí šipky).
    
    ![Nové heslo pro DanaRS](../images/DanaRSPW_05_PWnew.png)

* Potvrďte pomocí tlačítka OK.

* Uložte opětovným stisknutím tlačítka OK.
    
    ![DanaRS Uložení nového hesla](../images/DanaRSPW_06_PWnewSave.png)

* Přejděte dolů na "14. UKONČIT" a stiskněte tlačítko OK.
    
    ![Ukončit DanaRS](../images/DanaRSPW_07_Exit.png)

## Specifické chyby Dana RS

### Chyba během vydávání inzulinu

V případě, že dojde k přerušení spojení mezi AAPS a pumpou Dana RS v průběhu vydávání bolusu (např. odejdete mimo dosah telefonu, zatímco pumpa Dana RS vydává inzulin), zobrazí se následující zpráva a zazní akustická výstraha.

![Oznámení chyby podávání inzulínu](../images/DanaRS_Error_bolus.png)

* Ve většině případů se jedná pouze o problém s komunikací, který se netýká vydaného inzulinu (je vydáno správné množství).
* Podívejte se do historie pumpy (buď v pumpě, nebo na kartě Dana > Historie pumpy > Bolusy), zda byl vydán správný bolus.
* Pokud chcete, odstraňte chybový záznam v záložce [ošetření](../Getting-Started/Screenshots#carb-correction).
* Skutečně vydaný bolus se načte a zaznamená při příštím připojení. Chcete-li vynutit připojení okamžitě, klikněte na ikonu BT na kartě Dana, nebo prostě počkejte na příští připojení.

## Zvláštní poznámka, pokud měníte telefon

Pokud měníte telefon za nový, je nezbytné, abyste provedli následující kroky:

* [Exportujte nastavení](../Usage/ExportImportSettings#export-settings) na svém starém telefonu
* Přesuňte nastavení ze starého do nového telefonu

### DanaRS v1

* **Ručně spárujte** Danu RS s novým telefonem
* Vzhledem k tomu, že nastavení týkající se připojení pumpy jsou také importována, AAPS na vašem novém telefonu již pumpu „zná“, a proto nezahájí skenování bluetooth. Proto je třeba nový telefon a pumpu spárovat ručně.
* Nainstalujte AndroidAPS v novém telefonu.
* [Importujte nastavení](../Usage/ExportImportSettings#import-settings) v novém telefonu

### DanaRS v3, Dana-i

* Zahajte proces párování, jak je popsáno [výše](#pairing-pump).
* Někdy může být nutné vymazat informace o párování v AndroidAPS dlouhým kliknutím na ikonu BT na kartě Dana-i/RS.

## Cestování mezi časovými pásmy s pumpou Dana RS

Více informací o cestování přes více časových pásem najdete v části [Cestování s pumpou mezi časovými pásmy](../Usage/Timezone-traveling#danarv2-danars).