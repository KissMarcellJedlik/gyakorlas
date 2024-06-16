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
	
	def kerses:szamolas() -> None:
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
	
	def fuggveny(szoveg, maximum):
	    szam = 0
	    while szam <= 0 or szam > maximum:
	        try:
	            szam = int(input(szoveg))
	        except:
	            print("Ujraa")
	    return szam
	
	def masikfuggveny(ev1, honap1, nap1, ev2, honap2, nap2):
	    datum1 = datetime.date(ev1, honap1, nap1)
	    datum2 = datetime.date(ev2, honap2, nap2)
	    return (datum2 - datum1).days
	
	ev1 = fuggveny("Add meg az első évet: ", 2024)
	honap1 = fuggveny("Add meg az első hónapot: ", 12)
	nap1 = fuggveny("Add meg az első napot: ", 31)
	
	ev2 = fuggveny("Add meg az második évet: ", 2024)
	honap2 = fuggveny("Add meg az második hónapot: ", 12)
	nap2 = fuggveny("Add meg az második napot: ", 31)
	
	print(f"{ev1}.{honap1}.{nap1} illetve {ev2}.{honap2}.{nap2} között eltelt napok számok: {masikfuggveny(ev1, honap1, nap1, ev2, honap2, nap2)}")


ÁTVÁLTÁS:

	def atvaltas(self) -> None:
    return round(self.passzoltyard * 0.9144)

datum: !!!!!!!!!!!!!!!!!!!!!!!!
	
	max_napok = [31, 28, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31]
	
	def number_input(szoveg, maximum):
	    szam = 0
	    while szam <= 0 or szam > maximum:
	        ertek = input(szoveg)
	        try:
	            szam = int(ertek)
	        except:
	            pass
	    return szam
	
	def datum_kulonbseg(ev1, honap1, nap1, ev2, honap2, nap2):
	    napok1 = ev1 * 365
	    for i in range(0, honap1):
	        napok1 += max_napok[i]
	    napok1 += nap1

    napok2 = ev1 * 365
    for i in range(0, honap2):
        napok2 += max_napok[i]
    napok2 += nap2

    return abs(napok1 - napok2)


	datum_ev = number_input('Kérem az első dátum évét: ', 2030)
	datum_honap = number_input('Kérem az első dátum hónapját', 12)
	datum_nap = number_input('Kérem az első dátum napját: ', max_napok[datum_honap-1])
	
	datum_ev2 = number_input('Kérem a második dátum évét: ', 2030)
	datum_honap2 = number_input('Kérem a második dátum hónapját', 12)
	datum_nap2 = number_input('Kérem a második napját: ', max_napok[datum_honap2 - 1])
	
	print(f'A két dátum közötti különbség: {datum_kulonbseg(datum_ev, datum_honap, datum_nap, datum_ev2, datum_honap2, datum_nap2)}')



HARMADIK

	def main():
	    beolvasas_fajlbol('szszb (1).csv')
	    szamolas()
	    emberek()
	    legkisebb()
	    nagykozseg()
	    fajlbairas('varosok.csv')
	main()
