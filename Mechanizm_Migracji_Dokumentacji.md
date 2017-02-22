1. Migracja istniejącej dokumentacji
====================================

* Eksport z programu *Help&Manual* do pliku *RTF*.
* Eksport pliku *RTF* do pliku *DOCX* za pomocą LibreOffice przy pomocy poniższej komendy w konsoli:
*libreoffice --headless --convert-to docx nazwa_pliku.rtf*

* Wypakowanie z pliku *docx*(np. menadżerem archiwum) katalogu **/word/media** (jeśli dokumentacja posiada multimedia).

* Eksport za pomocą Pandoc'a pliku *docx* do pliku *markdown* lub *RST*.
W pliku wynikowym obrazy są zlinkowane w odpowiednich miejscach.
*pandoc plik_zrodlowy.docx -o plik_wynikowy.md/rst*

2. Formatowanie zmigrowanej dokumentacji
========================================
**Pliki wynikowe po zmigrowaniu wymagają ponownego formatowania całego tekstu, ze względu na utratę poniżej wymienionych elementów:**

* Wcięć
* Nagłówki mają zmienioną formę.
* Tabele mają zmienioną formę.
* Położenie opisów obrazów jest zmienione względem pierwotnej wersji, np. obrazek i opis znajdują się na tym samym poziomie, zamiast równolegle jeden pod drugim.

**Wszystkie te elementy muszą zostać poprawione w jednym z markup'ów (np. Markdown).**

3. Przechowywanie dokumentacji w systemie kontroli wersji
=========================================

Niezależnie od wybranego markup'u dokumenty mogą być przechowywane w systemie kontroli wersji, oraz w nim przeglądane, w zinterpretowanej przez git'a formie. Umożliwia to łatwość przechowywania dokumentacji i porównywania pomiędzy poszczególnymi wersjami.
Wraz z dokumentacją powinny być przechowywane szablony, oraz pliki konfiguracyjne, aby umożliwić sprawne generowanie dokumentacji w formatach docelowych, np. PDF, HTML.

4. Wybór narzędzi do edycji dokumentów
========================================

* Istnieje możliwość wyboru spośród wielu edytorów tekstu, do edycji zarówno plików *markdown* jak i *RST*, np. *ReText*, czy *Haroopad*. Obydwa programy udostępniają m.in. podgląd w czasie rzeczywistym, a dodatkowo ReText w przypadku plików *RST* wyświetla ostrzeżenia, gdy składnia jest błędna.

5. Generacja dokumentacji
========================================

Generacja i przechowywanie dokumentacji jest opisane w pliku Generacja_Dokumentacji_Tutorial.md. W zależności od wymagań należy napisać właśny szablon LaTeX, określający wygląd dokumentu wygenerowanego na podstawie dokumentacji w Markdownie. 