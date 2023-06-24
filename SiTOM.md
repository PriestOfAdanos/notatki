# Przykładowe kolokwium
## Możliwe procesy napływu klientów i Możliwe rozkłady czasu obsługi:
### Możliwe procesy napływu klientów:
- M (Markowian, czyli wykładniczy): Klienci przychodzą zgodnie z procesem Poissona, co oznacza, że czasy pomiędzy kolejnymi przybyciami klientów są niezależne i mają rozkład wykładniczy. Jest to najbardziej powszechny model w teorii kolejkowej.

- D (Deterministyczny): Klienci przychodzą w stałych, z góry określonych odstępach czasu. Na przykład, w systemie D/M/1, klient przybywa co jednostkę czasu.

- G (Ogólny): Klienci przychodzą zgodnie z dowolnym rozkładem prawdopodobieństwa. Jest to najbardziej ogólny model, ale także najtrudniejszy do analizy.

### Możliwe rozkłady czasu obsługi:

- M (Markowian, czyli wykładniczy): Czas obsługi klienta ma rozkład wykładniczy. Tak jak w przypadku procesu napływu klientów, jest to najczęściej stosowany model w teorii kolejkowej.

- D (Deterministyczny): Każdy klient jest obsługiwany dokładnie w określonym czasie. To jest rzadziej stosowany model, ale może być użyteczny w pewnych specyficznych sytuacjach, np. gdy czas obsługi jest z góry określony i niezmienny.

- G (Ogólny): Czas obsługi klienta ma dowolny rozkład prawdopodobieństwa. Jest to najbardziej ogólny model, ale także najtrudniejszy do analizy.

## Przykład 
### Model M/M/1: 
Jest to najprostszy model, który zakłada wykładniczy rozkład czasów przyjścia i obsługi oraz jedno stanowisko obsługi. Przyjmijmy, że λ (intensywność napływu klientów) wynosi 6 na godzinę, a μ (średnia szybkość obsługi) wynosi 8 na godzinę.

Prawdopodobieństwo, że system jest pusty (P0), można obliczyć jako 1 - λ/μ = 1 - 6/8 = 0.25.

Średnia liczba klientów w systemie (L) jest równa λ / (μ - λ) = 6 / (8 - 6) = 3.

Średni czas spędzony przez klienta w systemie (W) jest równy 1 / (μ - λ) = 1 / (8 - 6) = 0.5 godziny = 30 minut.

### Model M/M/2: 
Jest to model z dwoma stanowiskami obsługi. Przyjmijmy, że λ wynosi 6 na godzinę, a μ wynosi 4 na godzinę na jedno stanowisko, co daje łączną szybkość obsługi 8 na godzinę.

Prawdopodobieństwo, że system jest pusty, oblicza się na podstawie bardziej złożonego wzoru, który uwzględnia fakt, że system może obsługiwać dwóch klientów jednocześnie. W tym przypadku P0 = [1 + (λ/μ) + (λ/μ)²/2*(1!)]⁻¹ = [1 + (6/8) + (6/8)²/2]⁻¹ ≈ 0.38.

Średnia liczba klientów w systemie (L) oblicza się jako λ / (μ - λ) + λ² / (2μ * (2μ - λ)) = 6 / (8 - 6) + 6² / (24(8 - 6)) = 3 + 1.5 = 4.5.

Średni czas spędzony przez klienta w systemie (W) jest równy L / λ = 4.5 / 6 = 0.75 godziny = 45 minut.

## Zadania 

###  (1) 
W testowaniu hipotez dotyczących wariancji korzysta się z rozkładu chi-kwadrat. Przyjmujemy hipotezę H0: σ^2 = 1 oraz H1: σ^2 ≠ 1. Odchylenie standardowe w próbie wynosi s = 1.25, a rozmiar próby n = 150.

Wartość statystyki testowej chi-kwadrat wynosi (n-1)*s^2/σ^2 = (150-1)*1.25^2/1^2 = 185.25.

Dla α = 0.05 i n-1 = 149 stopni swobody, z tablic rozkładu chi-kwadrat odczytujemy wartości krytyczne. Dla dwustronnego testu mamy dwie wartości krytyczne, górne i dolne.

Dolna wartość krytyczna wynosi 116.32, a górna 184.25.

Ponieważ wartość statystyki testowej 185.25 jest większa od górnej wartości krytycznej, odrzucamy hipotezę H0 na korzyść H1. Więc, na podstawie naszej próby, istnieją dowody, że odchylenie standardowe populacji różni się od 1.

### (2)
W tym przypadku używamy testu dla dwóch proporcji. W próbie 1, n1 = 300, a x1 = 0.15 * 300 = 45. W próbie 2, n2 = 300, a x2 = 0.20 * 300 = 60.

Podstawiamy do wzoru dla statystyki Z:
Z = (p1 - p2) - 0 / sqrt( p * ( 1 - p ) * [ (1/n1) + (1/n2) ] )
gdzie p = (x1 + x2) / (n1 + n2) = (45 + 60) / (300 + 300) = 0.175.

Obliczamy Z i porównujemy z wartością krytyczną dla α = 0.01 (Z_critical = 2.58 dla dwustronnego testu). Jeżeli wartość bezwzględna Z będzie większa od wartości krytycznej, odrzucamy H0 na korzyść H1, że odsetek osób palących jest różny w obu populacjach.

### (3)
Współczynnik korelacji Pearsona ρ (rho) jest równy kowariancji podzielonej przez iloczyn odchyleń standardowych, więc ρ = Cov(X,Y) / (σ_x * σ_y) = 0.4 / (1 * 0.5) = 0.8.

Współczynnik kierunkowy prostej regresji β wynosi ρ * (σ_y / σ_x) = 0.8 * (0.5 / 1) = 0.4.

Współczynnik przecięcia prostej regresji α wynosi średnia Y - β * średnia X = 2 - 0.4 * 2 = 1.2.

Więc równanie prostej regresji Y względem X to Y = 0.4X + 1.2.

### (4)
W modelu M/M/1:

λ (intensywność napływu klientów) = 5/h
1/μ (średni czas obsługi) = 10 minut = 1/6 h, więc μ = 6/h
P0 (bezczynność serwera) = 1 - λ/μ = 1 - 5/6 ≈ 0.167, czyli stanowisko obsługi pozostaje bezczynne około 16,7% czasu.

L (średnia liczba klientów w systemie) = λ / (μ - λ) = 5 / (6 - 5) = 5, więc średnia liczba klientów w systemie wynosi 5.

### (5) 
Przykładem modelu D/M/2/1 w praktyce może być mały punkt obsługi klienta na stacji benzynowej, gdzie są dwie kasy. Klienci, którzy kończą tankowanie, podchodzą do kasy w regularnych, deterministycznych odstępach czasu - na przykład co minutę, ponieważ tyle średnio trwa tankowanie samochodu.

Czas obsługi klienta przez kasjera, czyli czas potrzebny na zapłatę i ewentualne dodatkowe czynności, takie jak kupno dodatkowych produktów, ma rozkład wykładniczy. Oznacza to, że niektóre transakcje są szybkie (tylko zapłata za paliwo), ale niektóre mogą trwać dłużej (klient decyduje się na dodatkowe zakupy).

Ponieważ mamy tylko dwie kasy, jeżeli obie są zajęte, każdy następny klient, który skończył tankowanie, nie ma możliwości dołączenia do kolejki - musi czekać przy swoim samochodzie, aż jedno z miejsc się zwolni. W praktyce może to oznaczać, że klienci, którzy nie mają możliwości natychmiastowej obsługi, mogą zdecydować się na opuszczenie stacji bez dokonywania płatności, co wprowadza dodatkowe komplikacje w obsłudze takiego punktu.

### Bonus: Regresja wieloraka

Rozważmy następującą sytuację. Na podstawie próby losowej trzech cech X1, X2 i Y, otrzymano średnie wartości dla tych cech, które wynoszą odpowiednio 2, 3 i 4. Odchylenia standardowe dla X1, X2 i Y wynoszą odpowiednio 1, 1.5 i 2.

Dodatkowo, otrzymano następujące kowariancje:

kowariancja między X1 i Y wynosi 0.6,
kowariancja między X2 i Y wynosi 0.8,
kowariancja między X1 i X2 wynosi 0.5.
Wyznacz równanie wielokrotnej regresji liniowej cechy Y względem cech X1 i X2.

Do rozwiązania tego problemu, musimy znać zarówno wariancje dla X1 i X2, jak i kowariancje między nimi, aby móc zastosować wzory na współczynniki regresji dla regresji wielorakiej. Możemy to zrobić przy użyciu technik takich jak metoda najmniejszych kwadratów, ale wymaga to bardziej zaawansowanych obliczeń.

Na początek, musimy sobie przypomnieć, że nasz cel polega na znalezieniu współczynników β0, β1, β2 dla modelu regresji wielorakiej, który wygląda tak:

$$
Y = β0 + β1\*X1 + β2\*X2 + ε
$$

Znamy średnie i odchylenia standardowe dla każdej z cech (X1, X2, Y), a także kowariancje między nimi. Z tego możemy obliczyć współczynniki kierunkowe (β1 i β2) oraz wyraz wolny (β0). Pamiętaj jednak, że w praktyce, te obliczenia są często wykonywane przez oprogramowanie statystyczne, takie jak R czy Python.

Zacznijmy od obliczenia β1 i β2.

β1 i β2 są współczynnikami regresji dla X1 i X2, odpowiednio, i mogą być obliczone przy użyciu następujących wzorów, które są wynikiem metody najmniejszych kwadratów:

$$
β1 = \frac{Cov(Y,X2)*Cov(X1,X2) - Cov(Y,X1)*Var(X2)}{Var(X1)*Var(X2) - (Cov(X1,X2))^2}
$$

$$
β2 = \frac{Cov(Y,X1)*Cov(X1,X2) - Cov(Y,X2)*Var(X1)}{Var(X1)*Var(X2) - (Cov(X1,X2))^2}
$$

Pierwszym krokiem jest wyliczenie wariancji dla X1 i X2. Wariancja to kwadrat odchylenia standardowego, więc Var(X1) = 1^2 = 1 i Var(X2) = 1.5^2 = 2.25.

Następnie, możemy obliczyć β1 i β2:

$$
β1 = \frac{0.8\*0.5 - 0.6\*2.25}{1\*2.25 - 0.5^2}= -0.35
$$

$$
β2 = \frac{0.6\*0.5 - 0.8\*1}{1\*2.25 - 0.5^2} = 0.1
$$

Mamy teraz nasze współczynniki kierunkowe, więc pozostało nam tylko obliczyć wyraz wolny β0. Wyliczamy go używając średnich wartości X1, X2 i Y:

$$
β0 = E(Y) - β1\*E(X1) - β2\*E(X2) = 4 - (-0.35\*2) - (0.1\*3) = 4.1
$$

Więc równanie naszej regresji wielorakiej to:

$$
Y = 4.1 - 0.35\*X1 + 0.1\*X2
$$

# Wykłady

### Dane do przykładów:
- Grupa 1: średnia = 85, odchylenie standardowe = 10
- Grupa 2: średnia = 90, odchylenie standardowe = 12
- Poziom istotności testu α = 0.05


### Test statystyczny: 
Weryfikację hipotezy zerowej przeprowadzamy na podstawie wyników próby losowej. Konieczny jest wybór odpowiedniej funkcji T(X1, ..., Xn), której wartości przyjęte dla realizacji próby świadczą na korzyść lub przeciw testowanej hipotezie. Funkcję taką nazywamy statystyką testową. Hipoteza alternatywna nie musi być zaprzeczeniem hipotezy zerowej. Na przykład, wiedząc, że rozkład cechy X w populacji jest rozkładem normalnym N(m, 1), możemy sformułować hipotezy zerową i alternatywną w następujący sposób: H0 : m = 0, H1 : m = 1.

Test statystyczny jest procedurą, która pozwala na ocenę hipotezy na podstawie próby danych. Przykładem może być test t-Studenta, który jest używany do porównania średnich dwóch grup. Wzór na statystykę t jest następujący:

$$
t = (X̄ - μ) / (s/√n)
$$
gdzie:

- X̄ to średnia próbkowa,
- μ to średnia w populacji lub wartość oczekiwana,
- s to odchylenie standardowe próbki,
- n to rozmiar próbki.

##### Przykład praktyczny

Obliczmy wartość t-statystyki:

$$
t = \frac{X1 - X2}{\sqrt{\frac{s_{1}^{2}}{n_{1}} + \frac{s_{2}^2}{n_{2}}}}
$$

gdzie:
- X̄1, X̄2 to średnie dla grupy 1 i 2,
- s1, s2 to odchylenia standardowe dla grupy 1 i 2,
- n1, n2 to rozmiary próbek dla grupy 1 i 2.
- Podstawiając wartości do wzoru, otrzymujemy:

$$
t = \frac{90-85}{\sqrt{\frac{10^{2}}{10} + \frac{12^2}{10}}}= -5 / \sqrt{10 + 14.4} = \frac{-5}{4.9} = 1.02
$$

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
Jest to jeden z najważniejszych rozkładów w statystyce i jest często używany w naukach przyrodniczych do reprezentowania losowych zmiennych, które mają tendencję do grupowania się wokół średniej. Charakteryzuje się dzwonowatym kształtem i jest symetryczny wokół swojej średniej. Wzór na gęstość prawdopodobieństwa rozkładu normalnego to:

$$
f(x) = \frac{1}{\sqrt{2\pi}\sigma} e^{ -\frac{(x-\mu)^2}{2\sigma^2} }
$$

gdzie μ to wartość oczekiwana (średnia), a σ to odchylenie standardowe.

### Rozkład t-Studenta: 
Jest to rozkład prawdopodobieństwa, który jest używany do estymacji populacji, gdy rozmiar próbki jest mały. Jest szeroko stosowany w testach statystycznych, takich jak test t-Studenta. Wzór na gęstość prawdopodobieństwa rozkładu t-Studenta to:

$$
f_n(x) = \frac{\Gamma(\frac{n+1}{2})}{\sqrt{n\pi}\Gamma(\frac{n}{2})} \left(1 + \frac{x^2}{n}\right)^{-\frac{n+1}{2}}
$$

gdzie n to liczba stopni swobody, a Γ to funkcja gamma.
### Rozkład chi kwadrat: 
 Jest to rozkład prawdopodobieństwa zmiennej losowej, która jest sumą kwadratów n niezależnych standardowych zmiennych normalnych. Jest używany w testach statystycznych, w tym w teście chi kwadrat. Wzór na gęstość prawdopodobieństwa rozkładu chi kwadrat to:
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
Testy zgodności są używane do sprawdzenia, czy dane empiryczne pasują do określonego rozkładu teoretycznego. Przykłady to test chi kwadrat Pearsona i test t-Studenta. Testy te są szczególnie ważne w statystyce, ponieważ pozwalają na ocenę, czy dane są zgodne z oczekiwaniami teoretycznymi. Jeśli dane nie są zgodne, może to sugerować, że istnieje jakiś nieznany czynnik wpływający na dane.

### Test zgodności χ2 Pearsona:
Test zgodności χ2 Pearsona jest jednym z najważniejszych testów zgodności. Jest używany do sprawdzenia, czy obserwowane częstości kategorii zmiennej kategorycznej różnią się od tego, czego byśmy oczekiwali na podstawie teorii. Hipoteza zerowa w teście χ2 Pearsona ma postać:

$$
H_0 : X \sim F_0(·)
$$

### P-wartość testu statystycznego: 
P-wartość jest używana w statystyce do określenia istotności wyników testu statystycznego. P-wartość to prawdopodobieństwo, że otrzymalibyśmy obecne lub bardziej ekstremalne wyniki, gdy hipoteza zerowa jest prawdziwa. Jeśli p-wartość jest mniejsza od ustalonego poziomu istotności (zazwyczaj 0,05), odrzucamy hipotezę zerową. Jeśli p-wartość jest większa, nie możemy odrzucić hipotezy zerowej. Pamiętaj, że p-wartość nie mówi nam o wielkości efektu ani o jego praktycznym znaczeniu - tylko o tym, czy efekt jest statystycznie istotny.

### Test Kołmogorowa:
Test Kołmogorowa jest testem hipotezy zerowej 
$H_0 : X \sim F_0(\cdot)$, gdzie dystrybuanta $F_0(\cdot)$ jest dystrybuantą typu ciągłego w pełni określoną. Statystyka testowa ma postać:

$$
D_n = sup_{x in R} |F_0(x) - F_n(x)|,
$$

gdzie $F_n(\cdot)$ jest dystrybuantą empiryczną cechy $X$ utworzoną na podstawie próby losowej prostej $(X_1, ..., X_n)$.

#### Przykład
Załóżmy, że mamy próbę 5 liczb: 1, 2, 3, 4, 5. Chcemy sprawdzić, czy te liczby pochodzą z rozkładu jednostajnego na przedziale [1, 5]. W tym przypadku, $F_0(x)$ to dystrybuanta rozkładu jednostajnego, a $F_n(x)$ to dystrybuanta empiryczna naszej próby. Obliczamy wartość $D_n$ i porównujemy ją z wartością krytyczną dla danego poziomu istotności.

W przypadku rozkładu jednostajnego, dystrybuanta $F_0(x)$ to $(x - 1) / 4$ dla $x$ w przedziale [1, 5]. Dystrybuanta empiryczna $F_n(x)$ to liczba obserwacji w próbie mniejszych lub równych $x$, podzielona przez liczbę wszystkich obserwacji. Dla naszej próby, $F_n(x)$ to $x / 5$ dla $x$ w przedziale [1, 5].

Obliczamy $D_n$ jako największą różnicę między $F_0(x)$ a $F_n(x)$ dla $x$ w przedziale [1, 5]. W tym przypadku, $D_n$ to największa wartość z $|(x - 1) / 4 - x / 5|$ dla $x$ równego 1, 2, 3, 4, 5. Obliczamy te różnice i bierzemy największą z nich.

### Test Craméra-von Misesa:
Statystyka testowa tego testu ma postać: 

$$
W^2 = n int_{-infty}^{infty} [F_0(x) - F_n(x)]^2 dF_0(x) = 1/(12n) + sum_{i=1}^{n} (2i - 1)/(2n) - F_0(X_i))^2.
$$

Zbiór krytyczny testu Craméra-von Misesa jest zbiorem prawostronnym i ma postać $K = [c_{n,1-\alpha}, \infty)$, gdzie $c_{n,1-\alpha}$ jest kwantylem rzędu $1 - \alpha$ statystyki $W^2$ (strona 37).

#### Przykład 
Załóżmy, że mamy próbę 5 liczb: 1, 2, 3, 4, 5. Chcemy sprawdzić, czy te liczby pochodzą z rozkładu jednostajnego na przedziale [1, 5]. W tym przypadku, $F_0(x)$ to dystrybuanta rozkładu jednostajnego, a $F_n(x)$ to dystrybuanta empiryczna naszej próby. Obliczamy wartość $W^2$ i porównujemy ją z wartością krytyczną dla danego poziomu istotności.

W przypadku rozkładu jednostajnego, dystrybuanta $F_0(x)$ to $(x - 1) / 4$ dla $x$ w przedziale [1, 5]. Dystrybuanta empiryczna $F_n(x)$ to liczba obserwacji w próbie mniejszych lub równych $x$, podzielona przez liczbę wszystkich obserwacji. Dla naszej próby, $F_n(x)$ to $x / 5$ dla $x$ w przedziale [1, 5].

Obliczamy $W^2$ jako sumęPrzykro mi za wcześniejsze nieporozumienie. Poniżej znajdują się przykładowe obliczenia dla każdego z testów statystycznych, które opisałem wcześniej. Przyjmijmy, że mamy próbę 5 liczb: 1, 2, 3, 4, 5. Chcemy sprawdzić, czy te liczby pochodzą z rozkładu jednostajnego na przedziale [1, 5].

### Test Kołmogorowa-Lillieforsa:
Test Kołmogorowa-Lillieforsa jest testem normalności rozkładu, a zatem jego stosowalność jest ograniczona do weryfikacji hipotez o zgodności rozkładu badanej cechy $X$ z rozkładem normalnym. Hipoteza zerowa ma postać:

$$
H_0 : X ~ N(x_bar, s^2(x_bar)),
$$

gdzie $s^2(\bar{x}) = \frac{1}{n-1} \sum_{i=1}^{n} (x_i - \bar{x})^2$.

#### Przykład 
W przypadku rozkładu jednostajnego, dystrybuanta $F_0(x)$ to $(x - 1) / 4$ dla $x$ w przedziale [1, 5]. Dystrybuanta empiryczna $F_n(x)$ to liczba obserwacji w próbie mniejszych lub równych $x$, podzielona przez liczbę wszystkich obserwacji. Dla naszej próby, $F_n(x)$ to $x / 5$ dla $x$ w przedziale [1, 5].
Obliczamy $D_n$ jako największą różnicę między $F_0(x)$ a $F_n(x)$ dla $x$ w przedziale [1, 5]. W tym przypadku, $D_n$ to największa wartość z $|(x - 1) / 4 - x / 5|$ dla $x$ równego 1, 2, 3, 4, 5. Obliczamy te różnice i bierzemy największą z nich.

### Test Shapiro-Wilka:
Test Shapiro-Wilka jest, podobnie jak test Kołmogorowa-Lillieforsa, testem normalności rozkładu. Test ten oparty jest na statystyce testowej postaci:

$$
W = (sum_{i=1}^{[n/2]} a_i(n)[X(n-i+1) - X(i)])^2 / sum_{i=1}^{n} (X_i - X_bar)^2,
$$

gdzie $[n/2]$ oznacza część całkowitą liczby $n/2$, a $n$ jest liczebnością próby losowej

#### Przykład 
W tym teście, obliczamy wartość statystyki testowej $W$ jako kwadrat sumy różnic między kolejnymi liczbami w próbie a ich średnią, podzielony przez sumę kwadratów odchyleń odPrzykro mi za wcześniejsze nieporozumienie. Poniżej znajdują się przykładowe obliczenia dla każdego z testów statystycznych, które opisałem wcześniej. Przyjmijmy, że mamy próbę 5 liczb: 1, 2, 3, 4, 5. Chcemy sprawdzić, czy te liczby pochodzą z rozkładu jednostajnego na przedziale [1, 5].
