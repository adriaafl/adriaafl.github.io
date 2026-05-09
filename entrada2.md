## Explicació del codi

He triat Python perquè és un llenguatge senzill i està suportat a VSCode.

---

## Eines utilitzades

Per poder programar i executar correctament he instal·lat:

- Extensió de Python
- Python Debugger
- Pylance
- Python instal·lat al sistema

Aquestes eines permeten escriure codi, detectar errors i executar programes. Sense això no es pot treballar correctament amb Python.

---

## Codi utilitzat


dni = int(input("Introdueix el número del DNI (sense lletra): "))

lletres = "TRWAGMYFPDXBNJZSQVHLCKE"
lletra = lletres[dni % 23]

print("La lletra del DNI és:", lletra)

## Explicació Codi


dni = int(input("Introdueix el número del DNI (sense lletra): "))

Primer demano a l’usuari que escrigui el número del DNI.  
Amb input() es llegeix el que escriu per teclat, però això entra com a text, així que amb int() ho converteixo a número per poder fer càlculs.  

En C# seria semblant, però una mica més llarg:  
int dni = int.Parse(Console.ReadLine());

---

lletres = "TRWAGMYFPDXBNJZSQVHLCKE"

Aquí guardo totes les lletres possibles del DNI dins d’una cadena de text.  
L’ordre és important perquè després segons el número sortirà una lletra o una altra.  

En C# seria pràcticament igual:  
string lletres = "TRWAGMYFPDXBNJZSQVHLCKE";

---

lletra = lletres[dni % 23]

En aquesta línia faig el càlcul de la lletra.  
El % 23 serveix per obtenir el residu de dividir el número entre 23, i aquest resultat indica quina posició de la cadena hem d’agafar.  
Bàsicament, el número dóna una posició i d’allà surt la lletra correcta.  

En C# funciona gairebé igual:  
char lletra = lletres[dni % 23];

---

print("La lletra del DNI és:", lletra)

Per acabar, mostro per pantalla la lletra calculada.  

  Proves d’execució
Prova 1:

Entrada:
12345678

Sortida:
La lletra del DNI és: Z

Prova 2:

Entrada:
87654321

Sortida:
La lletra del DNI és: X

  Explicació
El programa demana el número del DNI, calcula la posició amb % 23 i retorna la lletra corresponent.

---

## Vídeo

(Aquí enganxes el vídeo de Google Vids)
En C# seria:  
Console.WriteLine("La lletra del DNI és: " + lletra);
