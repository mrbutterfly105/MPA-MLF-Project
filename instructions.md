## Úvod

Všichni denně používáme mobilní telefony. Jsou naším spojením s rodinou a přáteli, pomáhají nám vyhledávatvyhledávat informace atd. Mobilní telefon musí být vždy připojen k síti, a to prostřednictvím tzv. základnové stanice (jako je např.
telekomunikační inženýři, jim říkáme eNodeB nebo gNodeB).

V mobilních sítích však mohou existovat útočníci, kteří využívají bezpečnostních slabin. S využitím
specializovaného hardwaru a softwaru mohou ukrást některé informace, odesílat škodlivé zprávy nebo sledovat uživatele. Jedním z nich je např.
známých nástrojů je takzvaná falešná základnová stanice (False Base Station, FBS), někdy nazývaná Rogue Base Station (RBS) nebo International
Mobile Subscriber Identifier (IMSI) Catcher. Jedná se o zařízení, které se vydává za legitimní základnovou stanici a snaží se
mobilní terminály připojit.


Falešná základnová stanice se tedy musí chovat jako legitimní stanice, tj. musí vysílat stejné informace jako legitimní stanice.
do rádiového kanálu.



## Popis zadání

Struktura rámce signálu 4G/LTE vysílaného ze základnové stanice je znázorněna v levé části obr. 1. Rozhodující část
přenášených informací jsou tzv. synchronizační sekvence. Existují dvě z nich - primární synchronizace
(PSS) a sekundární synchronizační sekvence (SSS). Během naší měřicí kampaně jsme zachytili
obrovské množství takových sekvencí a použili je k výpočtu frekvenčních odezv kanálu. Z těchto kanálových
frekvenčních odezv jsme vytvořili vzorky, které budete zpracovávat. Příklad jednoho vzorku vizualizovaného ve 2D je uveden na obrázku
v pravé části obrázku 1. Všimněte si, že se skládá ze 72 řádků (odpovídajících 72 subnosným přiděleným PSS/SSS) a 48
sloupců (odpovídajících 48 opakováním frekvenční odezvy kanálu).

Cílem vašeho projektu je klasifikovat, zda existuje pouze legitimní základnová stanice (gNodeB) společnosti T-mobile.
operátora (třída 0) vysílá ze sousední budovy, nebo zda útočník přivedl svůj vysílač do sousední budovy.
a snaží se ukrást informace uživatelům (třída 1 a třída 2). Falešná/útočníkova základnová stanice
může být umístěna na jedné ze dvou pozic - třída 1 odpovídá první pozici a třída 2 odpovídá druhé pozici.
2.
