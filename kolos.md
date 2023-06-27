(1) Weryfikacja hipotezy o odchyleniu standardowym w populacji wymaga zastosowania testu chi-kwadrat. W tym przypadku, hipoteza zerowa (H0) mówi, że odchylenie standardowe w populacji wynosi 1, a hipoteza alternatywna (H1) mówi, że odchylenie standardowe w populacji różni się od 1. 

Znamy następujące wartości:
- n (rozmiar próby) = 150,
- s (odchylenie standardowe próby) = 1.25,
- σ (odchylenie standardowe w populacji według H0) = 1,
- α (poziom istotności) = 0.05.

Statystyka testowa dla testu chi-kwadrat to (n-1)*s^2/σ^2. Wartość krytyczną dla testu dwustronnego z poziomem istotności α znajdujemy w tablicach rozkładu chi-kwadrat dla stopni swobody df = n - 1.

Obliczmy wartość statystyki testowej:

$$
(n-1)\*s^2/σ^2 = (150-1)\*1.25^2/1^2 = 232.8125
$$

Teraz obliczmy wartość krytyczną dla rozkładu chi-kwadrat z 149 stopniami swobody i poziomem istotności 0.05. Wartość ta wynosi około 178.49.

Ponieważ wartość statystyki testowej jest większa od wartości krytycznej, odrzucamy hipotezę zerową. Możemy więc stwierdzić, że na poziomie istotności 0.05 odchylenie standardowe cechy w populacji różni się istotnie od 1.

(2) W tym przypadku mamy do czynienia z testem proporcji dla dwóch populacji. Hipoteza zerowa (H0) mówi, że proporcje palących w obu populacjach są takie same, a hipoteza alternatywna (H1) mówi, że proporcja palących w drugiej populacji jest większa.

Znamy następujące wartości:
- n1, n2 (rozmiary prób) = 300,
- p1, p2 (proporcje palących w próbach) = 0.15, 0.20,
- α (poziom istotności) = 0.01.

Statystyka testowa dla testu proporcji to (p1 - p2) / sqrt(p*(1-p)*(1/n1 + 1/n2)), gdzie p to proporcja palących w obu próbach połączonych. Wartość krytyczną dla testu jednostronnego z poziomem istotności α znajdujemy w tablicach rozkładu normalnego.

Obliczmy wartość statystyki testowej:

$$
(p1 - p2) / sqrt(p\*(1-p)\*(1/n1 + 1/n2)) = (0.15 - 0.20) / sqrt((0.15\*300 +
$$
Wartość statystyki testowej wynosi około -0.000048. Wartość krytyczna dla rozkładu normalnego z poziomem istotności 0.01 wynosi około -2.33 (dla testu jednostronnego). Ponieważ wartość statystyki testowej jest większa od wartości krytycznej, nie odrzucamy hipotezy zerowej. Możemy więc stwierdzić, że na poziomie istotności 0.01 nie ma podstaw do twierdzenia, że odsetek osób palących w drugiej populacji jest wyższy.

(3) Równanie prostej regresji Y względem X ma postać Y = a + bX, gdzie b to współczynnik kierunkowy, a to wyraz wolny. Współczynnik kierunkowy b można obliczyć jako kowariancję cech X i Y podzieloną przez wariancję cechy X. Wyraz wolny a to średnia cechy Y minus b pomnożone przez średnią cechy X.

Znamy następujące wartości:
- X_bar, Y_bar (średnie cech X i Y) = 2,
- s_X, s_Y (odchylenia standardowe cech X i Y) = 1, 0.5,
- Cov(X,Y) (kowariancja cech X i Y) = 0.4.

Obliczmy współczynniki a i b:

$$
b = Cov(X,Y) / s_X^2 = 0.4 / 1^2 = 0.4
$$

$$
a = Y_bar - b*X_bar = 2 - 0.4*2 = 1.2
$$

Więc równanie prostej regresji to Y = 1.2 + 0.4X.

(4) Model M/M/1 to model kolejkowy, w którym czas między przybyciami klientów (interarrival time) ma rozkład wykładniczy (M), czas obsługi ma rozkład wykładniczy (M), jest jedno stanowisko obsługi (1). Intensywność napływu klientów oznaczamy przez λ, a średni czas obsługi pojedynczego klienta przez 1/μ.

Znamy następujące wartości:
- λ = 5/h,
- μ = 1 / (10 min) = 6/h.

Obliczmy intensywność ruchu (ρ), czyli stosunek intensywności napływu do intensywności obsługi:

$$
ρ = λ / μ = 5/6
$$

Prawdopodobieństwo, że stanowisko obsługi jest bezczynne (P0), obliczamy jako 1 - ρ:

$$
P0 = 1 - ρ = 1 - 5/6 = 1/6
$$

Średnia liczba klientów w systemie (L) obliczamy jako ρ / (1 - ρ):

$$
L = ρ / (1 - ρ) = (5/6) / (1 - 5/6) = 5
$$
