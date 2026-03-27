## Technologie Chmurowe — Laboratorium 5

## Autor - Kinga Kowalska

## Opis 
Aplikacja jest prostą stroną internetową uruchamianą w kontenerze Docker, która wyświetla podstawowe informacje o serwerze, takie jak adres IP, hostname oraz wersja aplikacji. W pierwszym etapie budowania obrazu wykorzystano minimalny system plików Alpine dostarczony w postaci archiwum `.tar`, które zostało rozpakowane na obrazie bazowym `scratch`. Następnie gotowa strona jest kopiowana do kontenera z serwerem Nginx, który udostępnia ją w przeglądarce.


## Polecenie - Budowa obrazu 
docker build --build-arg VERSION=2.5.0 -t lab5-app .
![Zrzut ekranu z budowania](build.png)

## Polecenie - Uruchomienie serwera
docker run -d -p 8080:80 --name moj_serwer lab5-app


##  Polecenie potwierdzające działanie kontenera i poprawne funkcjonowanie opracowanej aplikacji
docker ps
![Zrzut ekranu z przeglądarki](ps.png)
![Zrzut ekranu z przeglądarki](przegladarka.png)


