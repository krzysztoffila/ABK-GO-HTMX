# Książka Adresowa

Prosta aplikacja do zarządzania kontaktami, stworzona w Go i HTMX.

## Funkcje

- Dodawanie nowego kontaktu
- Edytowanie istniejącego kontaktu
- Usuwanie kontaktu
- Wyświetlanie listy kontaktów
- Wyszukiwanie kontaktów

## Technologie

- Backend: Go
- Frontend: HTMX, HTML, CSS

## Instalacja

1. **Zainstaluj Go:**

    Upewnij się, że masz zainstalowany Go. Możesz pobrać Go z [oficjalnej strony](https://golang.org/dl/).

2. **Skonfiguruj projekt:**

    ```bash
    git clone https://github.com/TwojeKonto/adresowa-ksiazka.git
    cd adresowa-ksiazka
    go mod init adresowa-ksiazka
    ```

## Struktura Projektu

- `main.go` - punkt wejścia aplikacji.
- `handlers/` - obsługa żądań HTTP.
- `models/` - struktury danych.
- `templates/` - szablony HTML.
- `static/` - pliki statyczne (CSS, JS).

## Implementacja

### 1. Konfiguracja Serwera HTTP

W pliku `main.go`, skonfiguruj serwer HTTP przy użyciu pakietu `net/http`.

### 2. Stworzenie Modelu Danych

W pliku `models/contact.go`, zdefiniuj strukturę `Contact`:

```go
package models

type Contact struct {
    ID        int
    FirstName string
    LastName  string
    Phone     string
    Email     string
    Address   string
}
```
## Implementacja

### 3. Implementacja CRUD

#### a. Dodawanie Kontaktów

1. **Stwórz formularz dodawania kontaktów:**
   - Utwórz szablon HTML zawierający formularz do wprowadzania danych kontaktu (imię, nazwisko, numer telefonu, e-mail, adres).

2. **Obsłuż żądania POST:**
   - Na backendzie, w Go, stwórz funkcję, która będzie obsługiwać żądania POST i zapisywać nowe kontakty w pamięci lub bazie danych.

#### b. Edytowanie Kontaktów

1. **Stwórz formularz edytowania kontaktów:**
   - Utwórz szablon HTML, który będzie wypełniony danymi istniejącego kontaktu do edycji.

2. **Obsłuż żądania POST dla edycji:**
   - Na backendzie, w Go, stwórz funkcję, która będzie obsługiwać żądania POST do aktualizacji istniejących kontaktów.

#### c. Usuwanie Kontaktów

1. **Stwórz funkcję usuwania:**
   - Na backendzie, w Go, stwórz funkcję, która będzie obsługiwać żądania usuwania kontaktów z pamięci lub bazy danych.

2. **Dodaj przyciski usuwania:**
   - W szablonie HTML listy kontaktów dodaj przyciski lub linki umożliwiające usunięcie kontaktu.

#### d. Wyświetlanie Listy Kontaktów

1. **Stwórz szablon listy kontaktów:**
   - Utwórz szablon HTML, który będzie wyświetlał wszystkie kontakty w formie listy.

2. **Obsłuż żądania GET:**
   - Na backendzie, w Go, stwórz funkcję, która będzie obsługiwać żądania GET i renderować listę kontaktów za pomocą szablonu HTML.

#### e. Wyszukiwanie Kontaktów

1. **Stwórz formularz wyszukiwania:**
   - Utwórz szablon HTML z polem wyszukiwania, w którym użytkownik może wprowadzać kryteria wyszukiwania.

2. **Obsłuż żądania wyszukiwania:**
   - Na backendzie, w Go, stwórz funkcję, która będzie obsługiwać żądania wyszukiwania i filtrować kontakty według wprowadzonych kryteriów.

### 4. Szablony HTML

1. **Utwórz katalog szablonów:**
   - Stwórz katalog `templates` i umieść w nim pliki HTML dla różnych widoków (np. lista kontaktów, formularz dodawania, formularz edytowania).

2. **Dynamiczne renderowanie:**
   - Wykorzystaj mechanizm szablonów Go (`html/template`) do dynamicznego generowania stron na podstawie danych.

### 5. Stylizacja i Interaktywność

1. **Dodaj pliki CSS:**
   - Stwórz katalog `static` i umieść w nim pliki CSS do stylizacji stron.

2. **Użyj HTMX:**
   - Wykorzystaj HTMX do dynamicznego ładowania i aktualizacji elementów strony bez pełnego przeładowania strony.

### 6. Testowanie

1. **Testy jednostkowe:**
   - Napisz testy jednostkowe dla funkcji CRUD w Go, aby upewnić się, że działają poprawnie.

2. **Testy end-to-end:**
   - Przetestuj całą aplikację, aby upewnić się, że wszystkie funkcje (dodawanie, edytowanie, usuwanie, wyświetlanie i wyszukiwanie kontaktów) działają zgodnie z oczekiwaniami.

### 7. Deployment

1. **Przygotowanie do wdrożenia:**
   - Skonfiguruj serwer produkcyjny (np. VPS, Docker).

2. **Uruchomienie aplikacji:**
   - Skopiuj pliki projektu na serwer i upewnij się, że serwer jest poprawnie skonfigurowany do obsługi aplikacji Go.
   - Skonfiguruj Nginx lub inny reverse proxy do obsługi ruchu HTTP/HTTPS.

### 8. Monitorowanie i Utrzymanie

1. **Monitorowanie aplikacji:**
   - Użyj narzędzi monitorujących, aby śledzić działanie aplikacji.

2. **Aktualizacje i poprawki:**
   - Regularnie aktualizuj aplikację, dodawaj nowe funkcje i poprawiaj błędy.

## Podsumowanie

Podzielając projekt na mniejsze kroki i realizując je po kolei, będziesz w stanie stworzyć funkcjonalną książkę adresową w Go i HTMX. Każdy krok jest istotny i wymaga skupienia, ale jednocześnie pozwoli na stopniowe budowanie umiejętności i doświadczenia w pracy z tymi technologiami.
