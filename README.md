# gyakorlas

ELSŐ

	class Varos:
	    def __init__(self, sor:str) -> None:
	        splitted = sor.strip().split(';')
	        self.telepules = splitted[0]
	        self.rang = splitted[1]
	        self.terseg = splitted[2]
	        self.terulet = int(splitted[3])
	        self.lakossag = int(splitted[4])



MÁSODIK

	telepulesek_listaja : list[Varos] = []
	
	def beolvasas_fajlbol(fajlnev: str) -> None:
	    file = open(fajlnev, "r", encoding="utf-8")
	    file.readline()
	    for sor in file:
	        telepulesek_listaja.append(Varos(sor.strip()))
	    file.close()
	
	def szamolas() -> None:
	    d = 0
	    d = len(telepulesek_listaja)
	    print(f'3. feladat: Települések száma: {d} db')

	 def ember_szamolas() -> None:
	    a = 0
	    for i in telepulesek_listaja:
	        a += i.lakossag
	    print(f'4. feladat: A megye lakossága: {a} fő')
	        
	def legkisebb() -> None: 
	    a = telepulesek_listaja[0]
	    for i in telepulesek_listaja:
	        if i.terulet < a.terulet:
	            a = i
	    print(f'5. feladat: A legkisebb területű település:\n\tTelepülés neve: {a.telepules}\n\tTerülete: {a.terulet} ha')
	
	def kersesszamolas() -> None:
	    a = 0
	    for i in telepulesek_listaja:
	        if i.rang == 'nagyközség':
	            a += 1
	    print(f'6. feladat: A megyében {a} nagyközség található')
	
	def fajlbairas(fajlnev: str) -> None:
	    f = open(fajlnev, 'w', encoding='utf-8')
	    for t in telepulesek_listaja:
	        if t.rang == 'város':
	            f.write(f'{t.telepules};{t.rang};{t.terseg};{t.terulet}.{t.terulet}\n')
	            f.close
FÜGGVÉNYEK:
	
 	legnagyobb_elem = max(myList, key=lambda x: x.xxxxxxxxxxxx) # x. után az kell, amire szeretnél max-ot keresni pl: x.ar
	
	legkisebb_elem = min(myList, key=lambda x: x.xxxxxxxxxxxx) # x. után az kell, amire szeretnél min-t keresni pl: x.ar
	
	xxxxxxxxx_elemek_osszeadasa = sum(i.xxxxxxxxxxxx for i in myList if xxxxxxxxxxx) # xxxxxxxxxxx helyére feltételt kell írni 
	# Ha nincs feltétel akkor töröld ki: if xxxxxxxxxxxxx
	
	
	xxxxxxxx_felteteles_kereses_count = 0
	
	for i in myList:
	    if xxxxxxxxxxx: # xxxxxxxxxxx helyére feltétel
	        xxxxxxxx_felteteles_kereses_count += 1
	
	myDict = {}
	for i in myList:
	    myDict[i.xxxxxxxxxxxx] = myDict.get(i.xxxxxxxxxxxx, 0) + 1 
	# xxxxxxxxxxxx helyére a classnak kell a tulajdonsága.
	# a get fogja a i.xxxxxxxxxxxx értéket, hozzáad 1-et, ha nincs akkor 0
	# + 1 helyett lehet más is


DICTIONARY:

	def egyetemes() -> None:
    egyetemek = {}
    for i in iranyitok_listaja:
        if i.egyetem in egyetemek:
            egyetemek[i.egyetem] += 1
        else:
            egyetemek[i.egyetem] = 1
    sikeres_egyetemek = {egyetem: jatekosok_szama for egyetem, jatekosok_szama in egyetemek.items() if jatekosok_szama > 1}

    print("8. feladat: Legsikeresebb egyetemek")
    for egyetem, jatekosok_szama in sikeres_egyetemek.items():
        print(f"\t{egyetem} - {jatekosok_szama}\t")


DATETIME:
	
 
 	import datetime

	# Függvény a felhasználói bemenet validálásához
	def fuggveny(szoveg, maxiszam):
	    while True:
	        try:
	            szam = int(input(szoveg))
	            if 1 <= szam <= maxiszam:  # Ellenőrzi, hogy a szám az elfogadható tartományban van-e
	                return szam
	            else:
	                print(f"A számnak 1 és {maxiszam} között kell lennie.")
	        except ValueError:
	            print("Érvénytelen bemenet. Kérlek, adj meg egy számot!")
	
	# Függvény a két dátum közötti napok számának kiszámításához
	def masikfuggveny(ev1, honap1, nap1, ev2, honap2, nap2):
	    try:
	        datum1 = datetime.date(ev1, honap1, nap1)
	        datum2 = datetime.date(ev2, honap2, nap2)
	        return abs((datum2 - datum1).days)  # A különbség abszolút értéke
	    except ValueError as e:
	        print(f"Hiba a dátumokkal: {e}")
	        return None
	
	# Bemeneti adatok bekérése
	ev1 = fuggveny("Add meg az első évet (1-9999): ", 9999)
	honap1 = fuggveny("Add meg az első hónapot (1-12): ", 12)
	nap1 = fuggveny("Add meg az első napot (1-31): ", 31)
	
	ev2 = fuggveny("Add meg a második évet (1-9999): ", 9999)
	honap2 = fuggveny("Add meg a második hónapot (1-12): ", 12)
	nap2 = fuggveny("Add meg a második napot (1-31): ", 31)
	
	# Napok számának kiszámítása és kiírása
	napok_szama = masikfuggveny(ev1, honap1, nap1, ev2, honap2, nap2)
	if napok_szama is not None:
	    print(f"{ev1}.{honap1}.{nap1} és {ev2}.{honap2}.{nap2} között eltelt napok száma: {napok_szama} nap.")
	


ÁTVÁLTÁS:

	def atvaltas(self) -> None:
    return round(self.passzoltyard * 0.9144)

RANDOM.CHOICE
	
 	import math
	import random
	
	
	d = int(input('Kérem a kör átmérőjét:'))
	
	allatok = ['elefánt', 'macska', 'kutya', 'zsiráf', 'oroszlán']
	randomallat = random.choice(allatok)
	
	def korszamitas(d):
	    r = d / 2
	    print(r)
	    terulet = math.pi * r * r
	    return terulet

	print(f'{korszamitas(d):.2f}  cm^2 és az állat rajta {randomallat}')





HARMADIK

	def main():
	    beolvasas_fajlbol('szszb (1).csv')
	    szamolas()
	    emberek()
	    legkisebb()
	    nagykozseg()
	    fajlbairas('varosok.csv')
	main()
