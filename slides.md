---
title-slide: false
bibliography: references.bib
csl: vancouver.csl
citeproc: true
theme: serif
background-color: "#ffffff"
transition: slide
navigationMode: linear
hash: true
---

:::: {.columns}
::: {.column width="50%"}

## Sample slides
#### PlaceHolderName
#### Universiti Malaysia Perlis
#### [placeholder@email.com](mailto:placeholder@email.com)

<!-- __AUDIO_INTRO_DO_NOT_TOUCH__ -->

:::

::: {.column width="50%"}
![](media/pics/logo1.png)
:::

::::

---

:::: {.columns}
::: {.column width="50%"}
### Slide one
**Key Concepts:**
- Energy conservation per @carnot1824.
- $\Delta U = Q - W$
:::

::: {.column width="50%"}
![](media/pics/sample.png)
:::
::::

---

<span class="slide-title" data-title="My Hidden Slide Name"></span>

![](media/pics/wide.jpeg)

---

:::: {.columns}
::: {.column width="50%"}
### The Master Equation
The fundamental relation of thermodynamics:

$$\Delta U = Q - W$$

The work done $W$ is positive when the system expands against an external pressure.
:::

::: {.column width="50%"}
<video data-src="media/videos/sample.mp4" data-autoplay loop muted width="100%"></video>
:::

::::

---

:::: {.columns}
::: {.column width="50%"}
### Visualizing the Gas Law
**Interactive Model:**

- P, V, and T relationships.
- Use the slider to adjust pressure.
- Observe the phase boundary.
:::

::: {.column width="50%"}
<iframe 
  data-src="media/plots/sample.html" 
  width="100%" 
  height="500px" 
  style="border:none;" 
  scrolling="no">
</iframe>
:::
::::

-----

:::: {.columns}
::: {.column width="50%"}
### Impact of Pressure on Part Resistance (Machine 1)

An ANOVA was performed to evaluate the effect of varying `Pressure` on `PartResistance` for `Machine 1`. The results indicate a statistically significant influence of pressure levels on the part resistance.

The boxplot visually confirms these findings, showing distinct distributions of `PartResistance` across different `Pressure` settings. Lower resistance values are generally preferred, with an Upper Specification Limit (USL) of 10.

This analysis highlights the importance of optimizing pressure settings to achieve desired product quality and minimize variability in part resistance.

:::

::: {.column width="50%"}
<iframe data-src='media/plots/machine1_resistance_boxplot_pressure_anova.html' width='100%' height='500px' style='border:none;'></iframe>
:::
::::

-----

:::: {.columns}
::: {.column width="50%"}
### Impact of Temperature on Part Resistance (Machine 1)

An ANOVA was performed to evaluate the effect of varying `Temperature` on `PartResistance` for `Machine 1`. The results indicate a statistically significant influence of temperature levels on the part resistance.

The boxplot visually confirms these findings, showing distinct distributions of `PartResistance` across different `Temperature` settings. Lower resistance values are generally preferred, with an Upper Specification Limit (USL) of 10. There is no Lower Specification Limit (LSL).

This analysis highlights the importance of optimizing temperature settings to achieve desired product quality and minimize variability in part resistance.

:::

::: {.column width="50%"}
<iframe data-src='media/plots/machine1_resistance_boxplot_temperature_anova.html' width='100%' height='500px' style='border:none;'></iframe>
:::
::::

-----

:::: {.columns}
::: {.column width="50%"}
### Impact of Pressure and Temperature Interaction on Part Resistance (Machine 1)

An ANOVA was performed to evaluate the combined effect of `Pressure` and `Temperature` on `PartResistance` for `Machine 1`. The results indicate a statistically significant interaction effect, meaning the effect of temperature on part resistance depends on the pressure level, and vice-versa.

The boxplot visually confirms these findings, showing varying distributions of `PartResistance` across different `Pressure:Temperature` combinations. Lower resistance values are generally preferred, with an Upper Specification Limit (USL) of 10. There is no Lower Specification Limit (LSL).

This analysis underscores the importance of considering both factors simultaneously for optimizing manufacturing conditions to achieve desired product quality and minimize variability in part resistance.

:::

::: {.column width="50%"}
<iframe data-src='media/plots/machine1_resistance_boxplot_pressure_temperature_anova.html' width='100%' height='500px' style='border:none;'></iframe>
:::
::::
