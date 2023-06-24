### Dane do przykładów:
- Grupa 1: średnia = 85, odchylenie standardowe = 10
- Grupa 2: średnia = 90, odchylenie standardowe = 12
- Poziom istotności testu α = 0.05


### Test statystyczny: 
Weryfikację hipotezy zerowej przeprowadzamy na podstawie wyników próby losowej. Konieczny jest wybór odpowiedniej funkcji T(X1, ..., Xn), której wartości przyjęte dla realizacji próby świadczą na korzyść lub przeciw testowanej hipotezie. Funkcję taką nazywamy statystyką testową. Hipoteza alternatywna nie musi być zaprzeczeniem hipotezy zerowej. Na przykład, wiedząc, że rozkład cechy X w populacji jest rozkładem normalnym N(m, 1), możemy sformułować hipotezy zerową i alternatywną w następujący sposób: H0 : m = 0, H1 : m = 1.

Test statystyczny jest procedurą, która pozwala na ocenę hipotezy na podstawie próby danych. Przykładem może być test t-Studenta, który jest używany do porównania średnich dwóch grup. Wzór na statystykę t jest następujący:

t = (X̄ - μ) / (s/√n)

gdzie:

- X̄ to średnia próbkowa,
- μ to średnia w populacji lub wartość oczekiwana,
- s to odchylenie standardowe próbki,
- n to rozmiar próbki.

##### Przykład praktyczny

Obliczmy wartość t-statystyki:
t = (X̄1 - X̄2) / sqrt[(s1^2/n1) + (s2^2/n2)]
gdzie:
- X̄1, X̄2 to średnie dla grupy 1 i 2,
- s1, s2 to odchylenia standardowe dla grupy 1 i 2,
- n1, n2 to rozmiary próbek dla grupy 1 i 2.
- Podstawiając wartości do wzoru, otrzymujemy:

t = (85 - 90) / sqrt[(10^2/10) + (12^2/10)] = -5 / sqrt[10 + 14.4] = -5 / 4.9 = -1.02


### Zbiór krytyczny: 
Zbiór krytyczny: Zbiór krytyczny to zbiór wartości, które prowadzą do odrzucenia hipotezy zerowej. Na przykład, dla testu t-Studenta z poziomem istotności 0.05 i stopniami swobody df = n - 1, zbiór krytyczny to zbiór wszystkich wartości t, które są większe od wartości t-krytycznej (można ją znaleźć w tabeli rozkładu t-Studenta dla danego poziomu istotności i stopni swobody).
W praktyce wybiera się taki zbiór krytyczny, który przy ustalonym wcześniej poziomie istotności testu α minimalizuje prawdopodobieństwo β popełnienia błędu II rodzaju: β = P{T(X1, ..., Xn) ∈ K′ | H1}, gdzie H1 jest ustaloną hipotezą alternatywną względem H0.

##### Przykład praktyczny 

Załóżmy, że używamy dwustronnego testu t-Studenta z poziomem istotności α = 0.05. Dla 18 stopni swobody (n1 + n2 - 2), wartość t-krytyczna wynosi około ±2.10 (można ją znaleźć w tabeli rozkładu t-Studenta). Zatem zbiór krytyczny to zbiór wszystkich wartości t, które są mniejsze od -2.10 lub większe od 2.10.

### Poziom istotności testu: 
W praktyce stosuje się następującą regułę postępowania. Ustala się niewielki poziom istotności testu α (równy najczęściej 0.01, 0.05 lub 0.1) i wyznacza się taki zbiór krytyczny K, by P{T(X1, ..., Xn) ∈ K | H0} = α.
Poziom istotności testu (α) to prawdopodobieństwo odrzucenia hipotezy zerowej, gdy jest ona prawdziwa. Jest to wartość, którą ustalamy przed przeprowadzeniem testu. Często używane wartości to 0.01, 0.05 lub 0.1.

Stopnie swobody (df) to liczba wartości w zestawie danych, które mogą swobodnie zmieniać się, podczas gdy inne wartości są ustalone. Wzór na obliczenie stopni swobody zależy od kontekstu:

- Dla testu t-Studenta dla jednej próbki: 
Stopnie swobody są równe rozmiarowi próbki minus 1. Wzór to:
df = n - 1
gdzie n to rozmiar próbki.
- Dla testu t-Studenta dla dwóch niezależnych próbek: 
Stopnie swobody są równe sumie rozmiarów obu próbek minus 2. Wzór to:
df = n1 + n2 - 2

gdzie n1 i n2 to rozmiary próbek.

### Funkcja mocy testu: 
Weźmy pod uwagę ogólną postać zerowej hipotezy parametrycznej, mianowicie H0 : θ = θ0, gdzie θ jest nieznanym parametrem rozkładu pewnej zmiennej losowej (cechy statystycznej) X. Niech K będzie zbiorem krytycznym testu hipotezy zerowej, a zatem P{T(X1, ..., Xn) ∈ K | H0} = α. Funkcję zdefiniowaną w następujący sposób: M(θ, K) = P{T(X1, ..., Xn) ∈ K | θ} nazywamy funkcją mocy testu (mocą testu).

W praktyce zamiast funkcji mocy testu wykorzystuje się często tzw. funkcję operacyjno-charakterystyczną (OC), zwaną także charakterystyką testu. Funkcję tę definiuje się w następujący sposób: L(θ, K) = 1 − M(θ, K). Oczywiście, jeżeli H0 : θ = θ0 oraz H1 : θ = θ1 ≠ θ0, wówczas spełnione są warunki L(θ0, K) = 1 − α, L(θ1, K) = β.

Wartość funkcji operacyjno-charakterystyczną `P` wyliczamy następująco:
- Wyliczamy wartość rozkładu `t` 
- W tabeli rozkładów zbiorów krytycznych patrzymy jakie wartości są najbliższe naszemu `t`
- Mnożymy razy 2 i otrzymujemy `P`
- Jeśli `P` jest mniejsze od α (0.05) to odrzucamy hipotezę zerową



##### Przykład praktyczny

Załóżmy, że przeprowadzamy test t-Studenta dla jednej próbki, gdzie hipoteza zerowa mówi, że średnia populacji wynosi 0. Mamy próbkę o rozmiarze 10, ze średnią 3 i odchyleniem standardowym 1. Chcemy przeprowadzić test z poziomem istotności 0.05.

- Najpierw obliczamy t-statystykę:
  Z=(11,9,10,10), n=4, X̄=10 , μ=9.5, s=1/2,   t=(10-9.5) / ((1/2)/√4)= (1/2)/(1/4)=2

- - W tabeli rozkładów zbiorów krytycznych patrzymy jakie wartości są najbliższe naszemu `t` (dla (n-1)=9, t=2 będzie to wartość tail = 0.05 )

- Mnożymy razy 2 i otrzymujemy `P = 0.1`
- `0.1 > 0.05`  i nie odrzucamy hipotezy zerowej


### Rozkład normalny: 
Rozkład normalny, znany również jako rozkład Gaussa, jest jednym z najważniejszych rozkładów w teorii prawdopodobieństwa i statystyce. Jego gęstość prawdopodobieństwa jest dana przez wzór:

$$
f(x) = \frac{1}{\sqrt{2\pi}\sigma} e^{ -\frac{(x-\mu)^2}{2\sigma^2} }
$$

gdzie μ to wartość oczekiwana (średnia), a σ to odchylenie standardowe.

### Rozkład t-Studenta: 
Rozkład t-Studenta jest używany w statystyce, gdy próbka jest mała. Jego gęstość prawdopodobieństwa jest dana przez wzór:

$$
f_n(x) = \frac{\Gamma(\frac{n+1}{2})}{\sqrt{n\pi}\Gamma(\frac{n}{2})} \left(1 + \frac{x^2}{n}\right)^{-\frac{n+1}{2}}
$$

gdzie n to liczba stopni swobody, a Γ to funkcja gamma.
### Rozkład chi kwadrat: 
Rozkład chi kwadrat jest stosowany w statystyce, szczególnie w testach zgodności. Jego gęstość prawdopodobieństwa jest dana przez wzór:

$$
f(x;n) = \frac{1}{2^{n/2}\Gamma(n/2)} x^{n/2-1} e^{-x/2}
$$

### Rozkład F Snedecora: 
Rozkład F Snedecora jest stosowany w analizie wariancji i regresji. Jego gęstość prawdopodobieństwa jest dana przez wzór:
$$
f(x;d_1,d_2) = \frac{\sqrt[(d_1x)^{d_1} \cdot d_2^{d_2} / (d_1x + d_2)^{d_1+d_2}]}{xB(\frac{d_1}{2},\frac{d_2}{2})}
$$

gdzie d1 i d2 to liczby stopni swobody, a B to funkcja beta.

### Statystyczne testy zgodności: 
Testy zgodności są używane do sprawdzenia, czy dane empiryczne pasują do określonego rozkładu teoretycznego. Przykłady to test chi kwadrat Pearsona i test t-Studenta.

### Test zgodności χ2 Pearsona:
Test zgodności χ2 Pearsona jest jednym z najważniejszych testów zgodności. Hipoteza zerowa w teście χ2 Pearsona ma postać:

$$
H_0 : X \sim F_0(·)
$$


