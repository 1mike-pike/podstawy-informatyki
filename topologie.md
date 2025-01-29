# Topologie Sieci

## Sieci Fizyczne
Sieci fizyczne odnoszą się do fizycznego ułożenia kabli, urządzeń i połączeń. Przykłady:
- **Topologia magistrali** (Bus) : 
- W topologii magistrali wszystkie urządzenia w sieci są 
podłączone do jednego, wspólnego przewodu 
komunikacyjnego (tzw. magistrali). Dane przesyłane są w 
obu kierunkach, a każde urządzenie monitoruje przesył i 
odbiera dane przeznaczone dla siebie.

  - Wady: 
    - Awaria głównej magistrali powoduje zatrzymanie 
    pracy całej sieci.
    - Ograniczona wydajność – im więcej urządzeń, tym 
    większe przeciążenie magistrali.

  - Zalety: 
    - Prosta implementacja i niski koszt.
    - Łatwa rozbudowa poprzez dodanie nowych 
    urządzeń.

  - Gdzie stosowane:
    - W starszych sieciach LAN, które miały ograniczoną 
    liczbę urządzeń.
    - Do celów edukacyjnych i testowych

- **Topologia pierścienia** (Ring):
- W tej topologii urządzenia są połączone w zamkniętą 
pętlę. Dane przesyłane są w jednym kierunku (lub w obu w 
przypadku pierścieni dwukierunkowych), a każde 
urządzenie działa jako wzmacniacz sygnału.

  - Wady: 
    - Awaria jednego urządzenia lub połączenia 
    powoduje przerwanie działania całej sieci.
    - Trudniejsza diagnostyka i naprawa w porównaniu z 
    innymi topologiami.

  - Zalety:
    - Brak kolizji danych, ponieważ ruch odbywa się w 
    sposób uporządkowany.
    - Stabilna wydajność przy dużej liczbie urządzeń.

  - Zastosowanie:
    - 
- **Topologia gwiazdy** (Star):
- Wszystkie urządzenia w sieci są połączone z jednym 
centralnym punktem, którym najczęściej jest switch lub 
router. Każde urządzenie komunikuje się z innymi za 
pośrednictwem tego punktu.

  - Wady: 
    - Awaria centralnego węzła powoduje zatrzymanie 
    całej sieci.
    - Wysokie koszty wdrożenia ze względu na potrzebę 
    większej ilości okablowania.

  - Zalety:
    - Łatwe diagnozowanie problemów – awaria jednego 
    urządzenia nie wpływa na całą sieć.
    - Prosta rozbudowa – dodanie nowego urządzenia 
    wymaga podłączenia go do centralnego węzła.

  - Gdzie stosowane:
    - Nowoczesne sieci LAN w biurach i szkołach.
    - Sieci domowe z routerem jako centralnym punktem.


## Sieci Logiczne
Sieci logiczne opisują sposób przesyłania danych między urządzeniami, niezależnie od fizycznej struktury. Przykłady:
Sieci logiczne opisują sposób przesyłania danych między urządzeniami, niezależnie od fizycznej struktury. Oznacza to, że skupiają się na sposobie komunikacji oraz metodzie dostępu do medium transmisyjnego, nie zwracając uwagi na fizyczną topologię sieci.

**Punkt-punkt** (Point-to-Point)
Jest to metoda, w której dwa urządzenia (komputery, routery itp.) łączą się bezpośrednio, a komunikacja odbywa się tylko pomiędzy nimi.

- Wady:
  - Brak skalowalności – tylko dwa urządzenia mogą się komunikować.
  - Ograniczona przepustowość, ponieważ tylko dwa urządzenia dzielą łącze.

- Zalety:
  - Prostota – łatwa konfiguracja i zarządzanie.
  - Niska latencja – komunikacja odbywa się bez pośredników.

- Zastosowanie:
  - Połączenia między dwoma urządzeniami w sieciach prywatnych, np. łącza punkt-punkt w telekomunikacji.

---

### 2. **Przekazywanie żetonu** (Token Passing)
Jest to metoda dostępu do medium, w której urządzenia komunikujące się w sieci muszą uzyskać specjalny "żeton", który daje im prawo do przesyłania danych. W sieci przesuwa się jeden żeton, który przechodzi z urządzenia do urządzenia, aż do momentu, gdy jedno z nich zacznie transmisję.

- Wady:
  - Może wystąpić opóźnienie, jeżeli żeton jest daleko od urządzenia, które chce nadawać.
  - Możliwość utraty żetonu, co może spowodować problemy z komunikacją.

- Zalety:
  - Zapobiega kolizjom, ponieważ tylko jedno urządzenie może nadawać dane w danym momencie.
  - Działa dobrze w sieciach o dużym natężeniu ruchu.

- Zastosowanie:
  - Stosowane w sieciach takich jak Token Ring, gdzie żeton krąży po sieci i kontroluje dostęp do medium.

---

### 3. **Wielodostępowa** (Multiple Access)
Metoda ta polega na tym, że wiele urządzeń współdzieli jedno medium transmisyjne, a każde z nich może nadawać dane. W tej metodzie często stosuje się różne mechanizmy zarządzania dostępem, aby zapobiec kolizjom danych.

- Wady:
  - Kolizje mogą występować, szczególnie w sieciach o dużym natężeniu ruchu.
  - Wymaga zastosowania algorytmów detekcji kolizji (np. CSMA/CD), co może generować dodatkowe opóźnienia.

- Zalety:
  - Efektywne wykorzystanie medium – wiele urządzeń może korzystać z tego samego łącza.
  - Niskie koszty infrastruktury, ponieważ nie jest wymagane osobne łącze dla każdego urządzenia.

- Zastosowanie:
  - Typowe dla sieci LAN, takich jak Ethernet (CSMA/CD) czy Wi-Fi (CSMA/CA).

--- 

Każda z tych sieci logicznych ma swoje specyficzne właściwości, które sprawiają, że są one bardziej odpowiednie w różnych środowiskach i zastosowaniach.