# python1
def fun(o):
    return len(o)


with open("lekseis.txt", "r") as f:
    words = f.read()
words = words.split()
words = [word.strip(",").strip(".").strip("!") for word in words]
words = list(dict.fromkeys(words))  
words.sort(key = fun)
leksi = words[::-1]
fonienta = ('a', 'e', 'i', 'o', 'u', 'A', 'E', 'I', 'O', 'U')

#ελεγχος για φωνηεντα
try:
    proti = leksi[0]
    for i in proti:
        if i in fonienta:
            proti = proti.replace(i, '')
    print ("Η πρωτη μεγαλυτερη λεξη ειναι: " + proti[::-1])
    try:
        deyteri = leksi[1]
        for i in deyteri:
            if i in fonienta:
                deyteri = deyteri.replace(i, '')
        print("Η δευτερη μεγαλυτερη λεξη ειναι: " + deyteri[::-1])
        try:
            triti = leksi[2]
            for i in triti:
                if i in fonienta:
                    leksi = leksi.replace(i, '')
            print("Η τριτη μεγαλυτερη λεξη ειναι: " + triti[::-1])
            try:
                tetarti = leksi[3]
                for i in tetarti:
                    if i in fonienta:
                        tetarti = tetarti.replace(i, '')
                print("Η τεταρτη μεγαλυτερη λεξη ειναι: " + tetarti[::-1])
                try:
                    pempti = leksi[4]
                    for i in pempti:
                        if i in fonienta:
                            pempti = pempti.replace(i, '')
                    print("Η πεμπτη μεγαλυτερη λεξη ειναι: " + pempti[::-1])
                except:
                    print("λιγοτερες απο 5 λεξεις")
                except:
                        print("λιγοτερες απο 4 λεξεις")
                    except:
                           print("λιγοτερες απο 3 λεξεις")
                            except:
                                print("λιγοτερες απο 2 λεξεις")
                                except:
                                    print("Κενος φακελος")
