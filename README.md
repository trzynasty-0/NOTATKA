# NOTATKA
Notatka z aplikacji Mobilnych - Android Studio, made by Maja and Szymon
<pre>
==================== GIT ====================
   1. git init

   2. git config user.name "username"
   3. git config user.email "email"

   4. git add . - dodaje wszystkie pliki
   5. git commit -m "commit name"

   6. stwórz puste repozytorium na githubie
   7. skopiuj link

   8. git push -u origin master (!!!MUSI BYĆ MASTER A NIE MAIN!!!)


potem tylko:
   1. git add .
   2. git commit -m "pusty projekt"
   3. 3. git push


inne komendy:
   • git status - sprawdza czy coś jest do zapisania (commitowania)
   • git add/rm - zapisuje plik (commituje)
   • git restore - usuwa niezapisane pliki (które nie były commitowane) -> wraca do poprzedniej wersji
   • mechaniktgmobilne - konto Pani na gicie


==================== Windows ====================

   • menedżer poświadczeń -> Pświadczenia systemu -> git.hub -> usuń dane!


==================== .XML ====================

Budowa:
   • app -> java -> com.example.NazwaProjektu -> MainActivity
   • app -> res  -> layout   -> activity_main.xml
   • app -> res  -> drawable -> obrazy (najlepiej jpg)
   • app -> res  -> values   -> colors.xml - dodawaj i korzystaj z własnych kolorków
   • app -> res  -> values   -> strings.xml - dodawaj stringi, które możesz potem tłumaczyć automatycznie

Komendy widoku: 
   • gravity            -> ustawia dziecko
   • layout_gravity     -> ustawia rodzica
   • backgroundTint     -> kolor tła dla przycisków
   • background         -> kolor tła
   • "wrap_content"     -> skraca do minimalnej szerokości, którą potrzebuje (z wysokością tak samo)
   • "match_parent"     -> wydłuża szerokość do szerokości rodzica (z wysokością tak samo)
   • adjustViewBounds   -> dostosowuje marginesy obrazu jego do szerokoścki
   • sp -> do tekstu
   • dp -> do rozmiarów, marginów itp


Komendy w java:
----- podstawowe
   
   • Toast (za stempelkiem)                  -> powiadomienie dymkowe, alert
   • obiekt = findViewById(R.id.idObiektu)   -> stworzenie obiektu z elementu z XML (w funkcji onCreate)

   • klikanie przycisków, jak ma wyglądać:
      przycisk.setOnClickListner(       
         new View.OnClickListner(){    <=>    View -> {
             .
             .
             .
          }
      ) 

----- Zapis
            
   • protected void onSaveInstanceState(...)   -> możliwość zapisywania rzeczy 
   • outState.put...()                         -> wymagane zdefiniowanie w powyższej funkcji co zapisujemy
                                                      np. putInt("KLUCZ", zmiennaZWaroscia)
   • jak ma wyglądać: 
      protected void onSaveInstanceState(@NonNull Bundle outState) {
         super.onSaveInstanceState(outState);
         outState.putInt("wartoscZapisanychPolubien", iloscPolubien);
      }
            
----- Działania na zapisie
            
   • savedInstanceState            -> to obiekt, który ma wszystkie zapisane informacje
                                          z powyższej funkcji onSaveInstanceState(...)
   • savedInstanceState.get...()   -> pobiera zapisaną wartość po kluczu, należy podać
                                          typ pobieranej wartości np getInt("KLUCZ")
   • przykład użycia:
      if(savedInstanceState != null){
         wartosc =  savedInstanceState.getInt("ZAPISANA_WARTOSC");
         jakisTekst.setText(Integer.toString(wartosc) + " - to zapisana wartosc");
      }
            
----- Nowe okienko w main
            
   • startActivity(intencja)                          -> otwiera nowe oknienko, dajesz w dowolnym miejscu
                                                             w main, gdzie chcesz aby się otwarło
   • Intencja                                        -> znaczy co chcesz wykonać
   • Intent intencja = new Intent(Skąd, dokąd)       -> np (MainActivity.this, InneActivity.class)
   • intencja.putExtra('KLUCZ', zmienna)             -> możliwość dodania argumentu (dajesz zmienną jaką
                                                             chcesz wyeksportować do klasy nowego okienka)

----- Nowe okienko w swojej klasie
            
   • zmienna = getIntent().get...Extra("KLUCZ", wartośćDomyślna) -> pobierasz argumenty, które 
                       np. getIntExtra("KLUCZ", wartośćDomyślna)        wyeksportowałeś we wcześniejszej
                                                                        klasie tworząc nowe okienko.
                                                

</pre>
