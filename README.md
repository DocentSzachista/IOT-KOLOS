# IOT-KOLOS

# Wykład 1

## Prawa robotyki
### Assimov
1. Robot nie może skrzywdzić człowieka, ani przez zaniechanie działania dopuścić, aby człowiek doznał krzywdy.
2. Robot musi być posłuszny rozkazom człowieka, chyba że stoją one w sprzeczności z Pierwszym Prawem.
3. Robot musi chronić samego siebie, o ile tylko nie stoi to w sprzeczności z Pierwszym lub Drugim Prawem.
4. Robot nie może skrzywdzić ludzkości, lub poprzez zaniechanie działania doprowadzić do uszczerbku dla ludzkości.
### Inne
Robot musi być w stanie wytłumaczyć proces decyzyjny kierujący jego
działaniem


# Wykład 2

## Różnice pomiędzy systemem autonomicznym a automatycznym
|automatyczny|autonomiczny|
|---|---|
|deterministyczny | Niedeterministyczny
|przewidywalny | ograniczona przewidywalność
|mała adaptacyjność | duża percepcja
|ograniczona percepcja | duża adaptacyjność
|specyficzne warunki pracy | zbieranie doświadczenia



## Poziomy automnomiczności
0. brak jakiejkolwiek automatyzacji
1. pomoc kierowcy - tempomat, wspomaganie kierownicy
2. częściowa automatyzacja jazdy - możliwość kierowania sterowania i prędkością przez samochód
3. warunkowa automatyzacja jazdy - auto może samo podejmować decyzje lecz w sytuacjach awaryjnych kierowca ma przejąć ster
4. wysoki poziom autonomii jazdy - auto może interweniować w sytuacjach awaryjnych.człowiek jest tylko dodatkiem ale może przejmowąc ster
5. Całkowity poziom autonomii
![](./zdj%C4%99cia/poziomy.png)

# Wykład 3

## Czujniki
- Czujniki wizyjne (kamery): Są to kamery wizyjne, które rejestrują obraz z otoczenia pojazdu. Wykorzystując technologie takie jak rozpoznawanie obrazu i głębi, pomagają w rozpoznawaniu znaków drogowych, pojazdów, pieszych i innych obiektów na trasie.

- Czujniki radarowe: Radar jest wykorzystywany do wykrywania obiektów na drodze poprzez emisję fal elektromagnetycznych i analizę ich odbicia. Pozwala to na określenie odległości, prędkości i kierunku ruchu innych pojazdów czy przeszkód.

- Czujniki ultradźwiękowe: Czujniki te wykorzystują fale ultradźwiękowe do pomiaru odległości między pojazdem a innymi obiektami. Stosowane są najczęściej do pomiaru odległości przy parkowaniu lub manewrowaniu pojazdem w ciasnych przestrzeniach.

- Czujniki laserowe (LiDAR): LiDAR (Light Detection and Ranging) generuje trójwymiarową mapę otoczenia pojazdu poprzez emisję laserowego promienia i analizę jego odbicia od otaczających obiektów. Zapewnia dokładne dane dotyczące odległości i kształtu obiektów.
![czujniki](./zdj%C4%99cia/rodzaje-skanerow.png)

## Przekazywanie danych statystyki
![Statystyki](./zdj%C4%99cia/statystyki-dane.png)

## Role czujników
![Role](./zdj%C4%99cia/roje-czujnikow.png)

## Jakie są wyzwania w przetwarzaniu danych
- ogromna ilość danych
- komunikacja
- przetwarzanie
- przechowywanie
- bezpieczeństwo
- zarządzanie infrastrukturą
- koszt energetyczny


# Wykład 4, 5, 6
## LoRa
to technologia komunikacyjna używana w sieciach IoT (Internetu rzeczy), umożliwiająca przesyłanie danych na duże odległości przy minimalnym zużyciu energii.  Infrastruktura LoRa składa się z bramek (gateway) umieszczonych na różnych lokalizacjach, które odbierają dane z urządzeń LoRa i przekazują je do chmury lub serwera aplikacyjnego, gdzie dane są przetwarzane i analizowane.
### Struktura LORA
- Urządzenia końcowe (end device) -Czujniki lub siłowniki wysyłają bezprzewodowe komunikaty z modulacją LoRa do bramek lub odbierają bezprzewodowo komunikaty z powrotem z bramek.

- Bramy (Gateway) - Specjalistyczne urządzenia, które odbierają wiadomości od urządzeń końcowych i przekazują je do serwera sieciowego, a także przekazują wiadomości z serwera sieciowego do urządzeń końcowych.

- Serwer sieciowy - Oprogramowanie działające na serwerze, które zarządza całą siecią. Nazywany również LoRaWAN Network Server/LNS lub po prostu oprogramowaniem sieciowym.

- Serwery aplikacji - Oprogramowanie działające na serwerze, które jest odpowiedzialne za bezpieczne przetwarzanie danych aplikacji

### Cechy
- **Modulacja**: LoRa korzysta z modulacji Chirp Spread Spectrum (CSS). Dane są kodowane w postaci długich chirpów radiowych, które są odporniejsze na zakłócenia i mają większy zasięg w porównaniu z innymi technologiami komunikacyjnymi.
- **Zasięg**: Jedną z głównych zalet LoRa jest jego zdolność do przesyłania danych na duże odległości. Może sięgać kilkunastu kilometrów w warunkach miejskich i nawet kilkudziesięciu kilometrów w warunkach bardziej otwartych.

- **Niska moc i oszczędność energii**: Urządzenia LoRa zużywają niewielką ilość energii, co jest kluczowe dla urządzeń IoT, które często działają na bateriach. Dzięki temu możliwe jest długotrwałe działanie bez konieczności częstej wymiany baterii.

- **Szeroki zakres zastosowań**: LoRa jest wykorzystywane w różnych obszarach, takich jak monitorowanie środowiska, inteligentne rolnictwo, zarządzanie smart city, systemy alarmowe, monitorowanie zdrowia, logistyka i wiele innych.

## Bluetooth low energy
Blueetoth który przesyła dane z niskim kosztem energii.
Ma krótszy zasięg niż tradycyjny bluetooth.

## Cechy niskich kosztów
- przesyłanie mniejszych pakietów danych niż w przypadku zwykłego bluetootha
- mały czas aktywności radiowej, są aktywowane tylko w momencie odbierania lub wysyłania danych
- ogłasza się bezpołączeniowo aby inne urządzenia wiedziały że istnieje, dzięki czemu nie musi być cały czas aktywny.
- wykorzystywane technologii kompresji w celu optymalizacji transmisji
- struktura urządzeń korzystających z tego protokołu

## Bluetooth mesh
  jest to rozszerzenie BLE które umożliwia komunikację w sieciach typu mesh, kdzie każde urządzenie może bezpośrednio komunikować się z innymi urządzeniami w sieci zamiast polegać tylko na centralnym punkcie zarządzającym.
## Cechy BLE MESH
- skalowalność (łatwo można dodać nowe urządzenia)
- mesh (bezpośrednia komunikacja, większa niezawodnosć)
- niskie zużycie energii (powody jak w BLE)

## Cechy technologii radiowych IOT
  -  **Zasięg**: Technologie radiowe IoT różnią się pod względem zasięgu transmisji danych. Niektóre z nich, jak na przykład LoRa, Sigfox czy NB-IoT, oferują większy zasięg w porównaniu do tradycyjnych sieci bezprzewodowych, co pozwala na komunikację na większe odległości, nawet kilkudziesięciu kilometrów w warunkach otwartych.

  -  **Przepustowość**: Przepustowość odnosi się do ilości danych, które można przesłać w danym czasie. Technologie radiowe IoT mogą różnić się pod względem przepustowości, gdzie niektóre umożliwiają szybką transmisję danych (np. NB-IoT), podczas gdy inne oferują mniejszą przepustowość, ale na rzecz większego zasięgu (np. LoRa).

 -   **Koszt energetyczny**: Efektywność energetyczna jest istotnym czynnikiem w przypadku urządzeń IoT, często zasilanych bateriami. Niektóre technologie radiowe IoT, jak LoRa, charakteryzują się niskim zużyciem energii, umożliwiając długotrwałą pracę urządzeń bez konieczności częstej wymiany baterii.

  -  **Rozmiar ramki danych:** Technologie radiowe IoT różnią się pod względem maksymalnego rozmiaru ramki danych, który może zostać przesłany w jednym pakiecie. Niektóre standardy mają ograniczenia dotyczące rozmiaru pakietów danych, co wpływa na sposób przesyłania informacji między urządzeniami.

  -  **Asymetria komunikacji**: W niektórych technologiach radiowych IoT komunikacja między urządzeniami a siecią może być asymetryczna, co oznacza, że przepływ danych w jednym kierunku może być inny niż w drugim. Na przykład, w standardzie LoRaWAN, nadawane dane z urządzenia do bramki mogą być przesyłane na dłuższy dystans niż dane z bramki do urządzenia.

  -  **Opóźnienie:** Czas, jaki jest potrzebny na przesłanie danych od nadawcy do odbiorcy, może być różny w zależności od technologii radiowej IoT. W niektórych przypadkach, jak na przykład w standardzie NB-IoT, opóźnienia mogą być krótkie, podczas gdy inne technologie mogą charakteryzować się dłuższym opóźnieniem ze względu na potrzebę optymalizacji energii czy zasięgu.

  -  **Pojemność sieci**: Pojemność sieci odnosi się do ilości urządzeń, które mogą być obsługiwane przez sieć w danym obszarze jednocześnie. Niektóre technologie radiowe IoT mogą obsługiwać większą liczbę urządzeń w jednym obszarze niż inne, co jest istotne w przypadku rozbudowanych sieci IoT.

   - **Niezawodność transmisji**: Niezawodność transmisji oznacza zdolność systemu do przekazywania danych bez błędów i zapewniania stabilnej komunikacji między urządzeniami a siecią. Niektóre technologie radiowe mogą zapewniać większą niezawodność transmisji poprzez różne mechanizmy korekcji błędów lub redundancji danych.


# Potencjalne pytania na kolosa
Komentarz: Rzucił dość ciekawym komentarzem na temat pytań jakie mogą się pojawić na kolosie
- ile dziennie danych jest przesyłanych z pojazdu autonomicznego

   4000 GB dziennie 
- Jak bluetooth unika kolizji
- Skąd się wziął znaczek bluetooth
  ![nordic h i nordic b](./zdj%C4%99cia/blueetooth.png)

- Czy wykorzystanie jednego rodzaju czujników jest wystarczające do utworzenia samochodu autonomicznego?
  - losowy czas dodawany do ADV. INTERVAL,
  - procedura „back-off” przy Scan Request,
  - frequency hopping w trakcie połączenia

  Zaleca się aby korzystać z wielu różnych czujników podczas tworzenia auta autonomicznego. Każdy z czujników ma swoje wady, które mogą zostać uzupełnione przez inny zestaw czujników.
  Nie każda firma się do tego stosuje, chociażby Tesla, w której główną rolę przy autonomiczności pojazdu odgrywają kamery wizyjne. 
- Jak można unikać kolizję w protokołach?
  - random access
  - cykliczny okres wysyłania sygnału
  - Dodawanie dodatkowego przekaźnika do którego się urządzenia bezpośrednio komunikują
  - Wyznaczanie momentu nadawania
  - wykorzystywanie z góry określonych kanałów do rozgłaszania się i do przesyłania danych
