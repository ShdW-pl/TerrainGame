Modul Zadan - Gra Terenowa

Modul odpowiedzialny za tworzenie zestawow zadan, ich wykonywanie przez gracza oraz weryfikacje odpowiedzi. Zrealizowany w technologii .NET MAUI z lokalna baza danych SQLite.

Zakres modulu
- Tworzenie i zarzadzanie zestawami lokalizacji
- Tworzenie zadan pieciu typow: pytanie otwarte, pytanie A/B/C/D, wielokrotny wybor, skanowanie QR, potwierdzenie czynnosci
- Wykonywanie zadan przez gracza z weryfikacja odpowiedzi
- Generowanie i eksport kodow QR do wydruku
- Import zadan zbiorczy z plikow JSON i CSV
- Integracja z modulem mapy przez GameStateService

Technologie
- .NET MAUI / C# / XAML
- SQLite (sqlite-net-pcl)
- CommunityToolkit.Mvvm
- QRCoder
- ZXing.Net.Maui

Struktura
Models      - modele bazy danych i klasy Payload (JSON)
Services    - logika biznesowa, dostep do SQLite, generowanie QR
ViewModels  - warstwa MVVM
Views       - interfejs uzytkownika XAML
Converters  - konwertery wartosci dla bindingow

Baza danych
Trzy tabele SQLite tworzone automatycznie przy pierwszym uruchomieniu:
- LocationSets     - zestawy lokalizacji
- LocationTasks    - zadania przypisane do zestawow (dane w polu Payload jako JSON)
- TaskCompletions  - wyniki zaliczonych zadan
