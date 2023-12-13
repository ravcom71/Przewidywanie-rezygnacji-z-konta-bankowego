# Przewidywanie-rezygnacji-z-konta-bankowego
Przewidywanie rezygnacji z konta bankowego

Zbiór ten zawiera dane dotyczące klientów banku, a zmienną docelową jest zmienna binarna Exited odzwierciedlająca fakt, czy klient opuścił bank (zamknął konto), czy też nadal jest klientem.

<h3 align="left"><a id = "R5">Wnioski:</a></h3>
    <ol>
        <li>Otrzymane dane są kompletne, bez braków.</li>
        <li>Istnieją ogromne dysproporcje w zmiennej objaśnianej Exited - tylko 20% danych zawiera informacje na temat rezygnacji klientów z usług.</li>
        <li>Ponad 50% rekordów dotyczy klientów z Francji, Niemcy i Hiszpanie stanowią po ok. 25% zasobów.</li>
        <li>Spośród wszystkich klientów w 3 państwach największa liczba osób została utracona w Niemczech, bo aż 8.14%.</li>
        <li>Ponad 3600 rekordów zawiera prawdopodobnie błędną informację o zerowym saldzie konta (tylko dane z Francji i Hiszpanii).</li>
        <li>Najlepsze wyniki zbudowanych modeli otrzymano przy wykorzystaniu wszystkich danych odpowiednio przetransformowanych do rozkładów zbliżonych do rozkładu Gaussa i uzupełnieniu zerowych wartości zmiennej Balance.</li>
        <li>Najlepszą dokładność przewidywania rezygnacji klientów osiągnęły modele RandomForestClassifier - na poziomie ok. 84-85%.</li>
        <li>Model zbudowany w oparciu o dane z Niemiec pozwolił na trafne przewidywanie odejść we Francji i Hiszpanii na poziomie 84%.</li>
        <li>Model zbudowany w oparciu o wszystkie dane pozwolił na trafne przewidywanie na poziomie 85%.</li>
        <li>Zwiększenie liczebności zmiennej objaśnianej Exited metodą SMOTE nie przyniosło zamierzonych efektów w postaci zwiąkszenia dokładności całkowitego przewidywania rezygnacji klientów, natomiast pozwoliło na zwiększenie różnicy pomiędzy prawidłowym i negatywnym typowaniem odejścia klientów ze wskazaniem na wartość prawidłowego typowania rezygnacji.</li>
        <li>Modele uczenia głębokiego zbudowane w oparciu o bibliotekę tensorflow, pomimo wysokiego stopnia doboru parametrów i dokładności uczenia powyżej 95% osiągały każdorazowo gorsze wskaźniki przewidywania wartości testowych niż model zbudowany w oprciu o drzewa losowe.
