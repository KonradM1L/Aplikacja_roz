# Aplikacja_roz
Praca dla Projektowanie aplikacji rozproszonych, Konrad Milewski 159826
-----------
Oto podstawowa struktura:

Serwer: będzie obsługiwać żądania od klientów i dostarczać odpowiedzi.
Klienci: będą wysyłać żądania do serwera i przetwarzać odpowiedzi.

Aplikacja wykorzystuje następujące protokoły i narzędzia:

HTTP - do komunikacji między klientem webowym a serwerem.
OAuth 2.0 - do uwierzytelniania użytkowników.
Google Sheets API - do uzyskiwania dostępu do danych z arkuszy Google.
Flask - do tworzenia aplikacji internetowej.
requests - do wysyłania żądań HTTP do zewnętrznych API.
google-api-python-client - do interakcji z Google Sheets API.

Kod wykorzystuje protokół TCP/IP do komunikacji. Jest to widoczne z użycia socket.AF_INET i socket.SOCK_STREAM. TCP zapewnia niezawodny protokół zorientowany na połączenie do wysyłania danych.
Tworzenie gniazda: socket.socket(socket.AF_INET, socket.SOCK_STREAM) tworzy gniazdo TCP.
Przyłączanie: s.bind((HOST, PORT)) przyłącza gniazdo do podanego adresu i portu.
Nasłuchiwanie: s.listen() przełącza gniazdo w tryb nasłuchiwania.
Akceptowanie połączeń: conn, addr = s.accept() akceptuje połączenie od klienta.
Wymiana danych: Pętla while True odbiera dane od klienta (conn.recv(1024)), wyświetla je i odbija je z powrotem (conn.sendall(data)).
Kod przedstawia prosty serwer TCP. Moduł socket zapewnia podstawowe elementy do implementacji komunikacji sieciowej.
-----------
Błąd „Module level import not at top of file” w wersie 'import socket' oznacza, że ​​próbuję zaimportować moduł w ramach funkcji lub bloku kodu, który nie znajduje się na najwyższym poziomie pliku. Python wymaga, aby wszystkie polecenia importu znajdowały się na najwyższym poziomie skryptu przed jakimkolwiek innym kodem.
