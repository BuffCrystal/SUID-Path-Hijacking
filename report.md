# SUID-Path-Hijacking
Využil jsem zranitelnost SUID binárky spolu s chybným používáním PATH.
Program syscheck spouštěl příkaz date bez absolutní cesty, takže se dal nahradit vlastním souborem. 
Díky SUID běžel program s právy rootu, i když jsem byl běžný uživatel student. 
Rozdíl mezi UID a EUID je v tom, že UID určuje uživatele, ale EUID určuje práva, se kterými program reálně běží. 
Jako opravu by měl administrátor používat vždy absolutní cesty k příkazům a dávat si pozor na to, aby se v privilegovaných programech nepoužíval nezabezpečený PATH.
