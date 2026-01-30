# Projekt `Balbinka`

## Zadanie 1

Proces CICD zawiera kilka etapów:

1. __Checkout repository__: Pobranie kodu źródłowego na maszynę GitHub Actions.

1. __pip audit__: Skanowanie bibliotek Pythona pod kątem znanych luk.

1. __Perform Bandit Analysis__: Statyczna analiza kodu pod kątem błędów bezpieczeństwa.

1. __Deploy for DAST analysis__: Zdalne uruchomienie aplikacji w Dockerze na serwerze zewnętrznym.

1. __zap scan__: Przeprowadzenie aktywnego ataku na działającą aplikację w celu wykrycia podatności runtime.

1. __Teardown after DAST__: Usunięcie kontenera, obrazu i plików projektu z zewnętrznego serwera po zakończeniu testów.

1. __Log in to Docker Hub__: Autoryzacja w rejestrze w celu  wysyłania obrazu.

1. __Extract metadata__: Automatyczne generowanie tagów i etykiet dla obrazu Docker.

1. __Build and push__: Zbudowanie finalnego obrazu i wypchnięcie go do rejestru Docker Hub.