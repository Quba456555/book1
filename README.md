# book1
ksiazka = {
    'tytuł': 'LOTR',
    'autor': 'Tolkien',
    'liczba stron': 500,
    'rok wydania': 1997
}

# Funkcja wyświetlająca informacje o książce
def wyswietl_ksiazke(ksiazka):
    for key, value in ksiazka.items():
        print(f"{key}: {value}")

# Funkcja edytująca dane książki
def edytuj_dane(ksiazka, klucz, nowa_wartosc):
    if klucz in ksiazka:
        ksiazka[klucz] = nowa_wartosc
        print("Dane zostały zaktualizowane.")
    else:
        print("Podany klucz nie istnieje.")


print("Początkowe informacje o książce:")
wyswietl_ksiazke(ksiazka)

klucz_do_edytowania = input("Podaj klucz do edycji: ")
nowa_wartosc = input("Podaj nową wartość: ")

edytuj_dane(ksiazka, klucz_do_edytowania, nowa_wartosc)

print("Zaktualizowane informacje o książce:")
wyswietl_ksiazke(ksiazka)
