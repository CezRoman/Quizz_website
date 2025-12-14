Projekt: Aplikacja Quizowa Full-Stack

🚀 O Projekcie

To jest dynamiczna, interaktywna gra webowa typu quiz, zbudowana przy użyciu nowoczesnego stosu technologicznego. Aplikacja pozwala użytkownikom na branie udziału w quizach z różnych kategorii, odpowiadanie na pytania i śledzenie swoich wyników w czasie rzeczywistym.

Projekt ten został stworzony jako aplikacja typu Single Page Application (SPA), gdzie frontend komunikuje się z backendem poprzez REST API.

🛠️ Architektura i Stos Technologiczny

Aplikacja podzielona jest na trzy główne warstwy: frontend (klient), backend (serwer) oraz bazę danych.

1. Frontend (Warstwa Prezentacji)

Technologia: React

Opis: Interfejs użytkownika został zbudowany przy użyciu biblioteki React. Wykorzystuje ona podejście komponentowe, co zapewnia łatwość w zarządzaniu stanem i budowaniu responsywnego UI.

Kluczowe biblioteki:

React Router: Do obsługi nawigacji po stronie klienta (przechodzenie między widokami logowania, listy quizów, a samą grą).

Axios (lub fetch): Do asynchronicznej komunikacji z backendowym API.

Context API lub Redux/Zustand: Do zarządzania stanem globalnym aplikacji (np. stanem uwierzytelnienia użytkownika lub aktualnym wynikiem).

2. Backend (Warstwa Logiki Biznesowej)

Technologia: FastAPI (Python)

Opis: Backend aplikacji to wydajne REST API napisane w FastAPI. Wybór padł na FastAPI ze względu na jego niesamowitą szybkość (dzięki wsparciu dla asyncio), automatyczną walidację danych (dzięki Pydantic) oraz automatycznie generowaną dokumentację (Swagger UI / ReDoc).

Główne zadania:

Obsługa uwierzytelniania użytkowników (rejestracja, logowanie, zarządzanie sesjami/JWT).

Udostępnianie listy dostępnych quizów i kategorii.

Pobieranie pytań i odpowiedzi dla wybranego quizu.

Walidacja odpowiedzi nadesłanych przez użytkownika.

Zapisywanie wyników w bazie danych i obsługa tablicy wyników.

3. Baza Danych (Warstwa Danych)

Technologia: PostgreSQL

Opis: Jako system zarządzania bazą danych wybrany został PostgreSQL. Jest to potężna, obiektowo-relacyjna baza danych typu open-source, znana ze swojej niezawodności, skalowalności i zgodności ze standardem SQL.

Przechowywane dane (przykładowe tabele):

Uzytkownicy (Users): Przechowuje dane logowania, hashe haseł i profile.

Quizy (Quizzes): Informacje o dostępnych quizach (np. nazwa, kategoria, opis).

Pytania (Questions): Treść pytań, powiązana z konkretnym quizem.

Odpowiedzi (Answers): Dostępne opcje odpowiedzi dla pytań (wraz ze wskazaniem poprawnej).

Wyniki (Scores): Historia wyników osiągniętych przez użytkowników.

ORM: Komunikacja między FastAPI a PostgreSQL odbywa się najczęściej przy użyciu SQLAlchemy (Core lub ORM).

🎯 Główne Funkcjonalności

System rejestracji i logowania użytkowników.

Przeglądanie dostępnych quizów posortowanych według kategorii.

Interaktywny interfejs rozgrywki.

Natychmiastowa informacja zwrotna po udzieleniu odpowiedzi.

Ekran podsumowania wyników po zakończeniu quizu.

(Opcjonalnie) Globalna tablica wyników (High Scores).

Pełna responsywność (RWD) zapewniająca działanie na urządzeniach mobilnych.