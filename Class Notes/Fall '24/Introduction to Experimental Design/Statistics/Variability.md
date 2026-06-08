>[!quote]
>According to Gemini:
>
>*Variability in statistics, also known as dispersion or spread, describes how spread out or clustered together data points are within a dataset. It tells you how much individual data points deviate from the central tendency (mean, median, or mode).*
>
>*Here's why understanding variability is important:*
>- *__Provides context to the central tendency__: Knowing the average is useful, but understanding how much the data points vary around that average gives you a more complete picture.*
>- *__Helps compare datasets__: Two datasets can have the same mean but very different variability, indicating different underlying patterns.*
>- *__Essential for decision-making__: High variability might indicate greater risk or uncertainty, influencing decisions in fields like finance or healthcare.*

There are different ways of measuring variability, including:
- __Variance__
$$
Var(x) = \frac{1}{N} \sum^{N}_{i = 1}(x - \bar{x})^2
$$
- __Standard Deviation__
$$
s = \sqrt{\frac{1}{N - 1}\sum^{N}_{i = 1}(x-\bar{x})^2}
$$
>[!note]
>Variance and Standard Deviation formulas are *almost* the same except N (the number of data points) is subtracted by one in the Standard Deviation equation

- __Range__ (difference from minimum and maximum)
- __Interquartile Range__ (difference from 75th percentile and 25th percentile)