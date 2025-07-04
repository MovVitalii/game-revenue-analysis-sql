Opis
To zapytanie SQL analizuje miesięczne powtarzalne przychody (MRR - Monthly Recurring Revenue) dla płatności w grach, obliczając kluczowe metryki dla każdego użytkownika i gry.
Co robi zapytanie
1. Agregacja płatności (payment_summary)

Grupuje płatności według miesięcy, gier i użytkowników
Sumuje całkowity przychód w dolarach amerykańskich

2. Dodanie znaczników czasowych (payment_with_months)

Oblicza poprzednie i następne miesiące kalendarzowe
Używa funkcji okiennych do pobierania danych z poprzednich okresów

3. Obliczanie metryk MRR (metrics)

New MRR: Przychód od nowych użytkowników
Expansion Revenue: Wzrost przychodów od istniejących użytkowników
Contraction Revenue: Spadek przychodów od istniejących użytkowników
Churned Revenue: Przychód od użytkowników, którzy zrezygnowali z usług
Churn Month: Miesiąc rezygnacji użytkownika

4. Finalne połączenie

Dodaje dane demograficzne użytkowników (język, model urządzenia, wiek)
Sortuje wyniki według użytkownika, gry i miesiąca

Dane wyjściowe
Zapytanie zwraca szczegółowe informacje o każdej płatności z obliczonymi metrykami MRR i charakterystykami użytkowników.
Zastosowanie
Wyniki można wykorzystać do:

Analizy dynamiki przychodów
Identyfikacji trendów utrzymania użytkowników
Segmentacji użytkowników według zachowań płatniczych
Planowania przychodów i prognozowania
