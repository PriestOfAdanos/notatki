### KorelacjaPearsona 

$$
r = \frac{\sum_{i=1}^{n} (x_i - \bar{x})(y_i - \bar{y})}{\sqrt{\sum_{i=1}^{n} (x_i - \bar{x})^2 \sum_{i=1}^{n} (y_i - \bar{y})^2}}
$$

gdzie:
- \(x_i\) i \(y_i\) to wartości punktów danych,
- \(\bar{x}\) i \(\bar{y}\) to średnie wartości punktów danych,
- \(n\) to liczba punktów danych.

W praktyce, obliczanie współczynnika korelacji Pearsona często jest uproszczone do następującego wzoru:

$$
r = \frac{n(\sum xy) - (\sum x)(\sum y)}{\sqrt{[n\sum x^2 - (\sum x)^2][n\sum y^2 - (\sum y)^2]}}
$$

gdzie:
- \(\sum xy\) to suma iloczynów par punktów danych,
- \(\sum x\) i \(\sum y\) to sumy wartości punktów danych,
- \(\sum x^2\) i \(\sum y^2\) to sumy kwadratów wartości punktów danych.


### Test t-Studenta jest stosowany do testowania hipotez dotyczących średniej populacji.
t = \frac{\bar{X} - \mu_0}{s / \sqrt{n}}
$$

gdzie:
- \(\bar{X}\) to średnia próby,
- \(\mu_0\) to założona średnia w populacji,
- \(s\) to odchylenie standardowe próby,
- \(n\) to rozmiar próby.

Wartość statystyki testowej jest porównywana z wartością krytyczną z rozkładu t-Studenta o \(n-1\) stopniach swobody. Jeżeli wartość statystyki testowej jest większa od wartości krytycznej, hipoteza zerowa jest odrzucana.

W kontekście testowania różnicy między dwiema średnimi, statystyka testowa ma postać:

$$
t = \frac{\bar{X}_1 - \bar{X}_2}{\sqrt{s_1^2/n_1 + s_2^2/n_2}}
$$

gdzie:
- \(\bar{X}_1\) i \(\bar{X}_2\) to średnie dwóch prób,
- \(s_1\) i \(s_2\) to odchylenia standardowe dwóch prób,
- \(n_1\) i \(n_2\) to rozmiary dwóch prób.

### Test chi-kwadrat jest stosowany do testowania hipotez dotyczących rozkładu zmiennej losowej. 
Istnieje kilka różnych typów testów chi-kwadrat, ale wszystkie opierają się na tej samej statystyce testowej. Statystyka testu chi-kwadrat ma postać:

$$
X^2 = \sum \frac{(O_i - E_i)^2}{E_i}
$$

gdzie:
- \(O_i\) to obserwowane częstości,
- \(E_i\) to oczekiwane częstości.

W kontekście testowania hipotez o odchyleniu standardowym, statystyka testowa ma postać:

$$
X^2 = \frac{(n-1)s^2}{\sigma_0^2}
$$

gdzie:
- \(n\) to rozmiar próby,
- \(s\) to odchylenie standardowe próby,
- \(\sigma_0\) to założone odchylenie standardowe w populacji.

Wartość statystyki testowej jest porównywana z wartością krytyczną z rozkładu chi-kwadrat o \(n-1\) stopniach swobody. Jeżeli wartość statystyki testowej jest większa od wartości krytycznej, hipoteza zerowa jest odrzucana.

### Z-score

Z-score, zwany również standardowym wynikiem Z, jest miarą, która opisuje, jak daleko dany punkt danych jest od średniej, wyrażonej w jednostkach odchylenia standardowego. 

Podstawowy wzór na obliczenie Z-score jest następujący:

$$
Z = \frac{X - \mu}{\sigma}
$$

gdzie:
- \(X\) to wartość punktu danych,
- \(\mu\) to średnia populacji lub próby,
- \(\sigma\) to odchylenie standardowe populacji lub próby.

W kontekście testowania hipotez, Z-score jest często używany do porównania obserwowanej wartości statystyki testowej z wartością oczekiwaną pod hipotezą zerową. W takim przypadku, Z-score jest obliczany jako:

$$
Z = \frac{\text{statystyka testowa} - \text{oczekiwana wartość statystyki testowej}}{\text{standardowy błąd statystyki testowej}}
$$

W przypadku porównania dwóch proporcji, Z-score jest obliczany za pomocą następującego wzoru:

$$
Z = \frac{(\hat{p}_1 - \hat{p}_2) - 0}{\sqrt{\hat{p}(1 - \hat{p})(\frac{1}{n_1} + \frac{1}{n_2})}}
$$

gdzie:
- \(\hat{p}_1\) i \(\hat{p}_2\) to proporcje w dwóch grupach,
- \(\hat{p}\) to proporcja w całej populacji,
- \(n_1\) i \(n_2\) to rozmiary dwóch grup.

W przypadku testu dla jednej średniej, Z-score jest obliczany za pomocą następującego wzoru:

$$
Z = \frac{\bar{X} - \mu_0}{\sigma / \sqrt{n}}
$$

gdzie:
- \(\bar{X}\) to średnia próby,
- \(\mu_0\) to założona średnia w populacji,
- \(\sigma\) to odchylenie standardowe populacji,
- \(n\) to rozmiar próby.


Jeśli chcesz obliczyć Z-score dla dwóch wartości z dwóch różnych populacji lub prób, możesz to zrobić, porównując różnicę między dwoma wartościami do oczekiwanej różnicy pod hipotezą zerową. W takim przypadku, Z-score jest obliczany za pomocą następującego wzoru:

$$
Z = \frac{(X_1 - X_2) - D_0}{\sqrt{\sigma_1^2/n_1 + \sigma_2^2/n_2}}
$$

gdzie:
- \(X_1\) i \(X_2\) to wartości punktów danych,
- \(D_0\) to oczekiwana różnica pod hipotezą zerową (często jest to 0, jeśli hipoteza zerowa mówi, że dwie wartości są równe),
- \(\sigma_1\) i \(\sigma_2\) to odchylenia standardowe populacji lub prób,
- \(n_1\) i \(n_2\) to rozmiary prób.

Wartość Z-score jest następnie porównywana z wartością krytyczną z rozkładu normalnego standardowego, aby zdecydować, czy odrzucić hipotezę zerową.

### Modele kolejkowe 
1. **M/M/1**:
   - Średnia liczba klientów w systemie (L): \( L = \frac{\rho}{1 - \rho} \)
   - Średni czas spędzony przez klienta w systemie (W): \( W = \frac{1}{\mu - \lambda} \)
   - Prawdopodobieństwo, że system jest pusty (P0): \( P0 = 1 - \rho \)
   - Prawdopodobieństwo, że w systemie jest n klientów (Pn): \( Pn = (1 - \rho) * \rho^n \)

2. **M/M/c** (gdzie c > 1):
   - Prawdopodobieństwo, że system jest pusty (P0): \( P0 = \left[ \sum_{k=0}^{c-1} \frac{(c\rho)^k}{k!} + \frac{(c\rho)^c}{c!(1-\rho)} \right]^{-1} \)
   - Średnia liczba klientów w systemie (L): \( L = \frac{(c\rho)^c}{c!(1-\rho)^2} * P0 + c\rho \)
   - Średni czas spędzony przez klienta w systemie (W): \( W = \frac{L}{\lambda} \)

3. **M/D/1**:
   - Średnia liczba klientów w systemie (L): \( L = \frac{\rho^2 + \rho}{2(1-\rho)} \)
   - Średni czas spędzony przez klienta w systemie (W): \( W = \frac{L}{\lambda} + \frac{1}{\mu} \)

4. **M/G/1**:
   - Średnia liczba klientów w systemie (L): \( L = \rho + \frac{\rho^2 + \lambda^2 \sigma^2_s}{2(1-\rho)} \)
   - Średni czas spędzony przez klienta w systemie (W): \( W = \frac{L}{\lambda} \)

gdzie:
- \(\lambda\) to średni czas między przybyciem klientów (intensywność napływu),
- \(\mu\) to średni czas obsługi,
- \(\rho = \lambda / (\mu c)\) to intensywność ruchu na serwer,
- \(\sigma^2_s\) to wariancja czasu obsługi.
