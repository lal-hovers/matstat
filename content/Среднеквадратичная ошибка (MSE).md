
Пусть мы оцениваем параметр $\theta$ с помощью статистики (оценки) $\hat{\theta}$. **Среднеквадратичная ошибка** (mean squared error) определяется как
$$
\mathrm{MSE}(\hat{\theta}) 
\;=\; E\bigl[(\hat{\theta} - \theta)^2\bigr].
$$

## 2. Разложение MSE через смещение и дисперсию

Рассмотрим смещение $\mathrm{Bias}(\hat{\theta}) = E(\hat{\theta}) - \theta$. Тогда
$$
(\hat{\theta} - \theta)^2 
= (\hat{\theta} - E(\hat{\theta}) + E(\hat{\theta}) - \theta)^2
= \bigl[\hat{\theta} - E(\hat{\theta})\bigr]^2 + 2\bigl[\hat{\theta} - E(\hat{\theta})\bigr]\bigl[E(\hat{\theta}) - \theta\bigr] + \bigl[E(\hat{\theta}) - \theta\bigr]^2.
$$
Берём математическое ожидание:
$$
E\bigl[(\hat{\theta} - \theta)^2\bigr] 
= E\bigl[\hat{\theta} - E(\hat{\theta})\bigr]^2 \;+\; 2\bigl[E(\hat{\theta}) - \theta\bigr] \, E\bigl[\hat{\theta} - E(\hat{\theta})\bigr] \;+\; \bigl[E(\hat{\theta}) - \theta\bigr]^2.
$$
Но $E\bigl[\hat{\theta} - E(\hat{\theta})\bigr] = 0$, поэтому второй член зануляется. Получаем **классическую формулу**:

$$
\mathrm{MSE}(\hat{\theta})
= E\bigl[(\hat{\theta} - \theta)^2\bigr]
= \mathrm{Var}(\hat{\theta}) + \bigl[\mathrm{Bias}(\hat{\theta})\bigr]^2.
$$
