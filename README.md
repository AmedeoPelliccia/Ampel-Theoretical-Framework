# Ampel Theoretical Framework
## Capa de Límite Físico, Puente Termodinámico, Gobernanza SICO.CA y Validación por Simulación

**Versión 3.0.0** — Puerta de responsabilidad sobre el balance neto regional, formulación en flujos (tasas), vulnerabilidad como contexto y no como compuerta.

`v3.0.0` corrige un defecto estructural de `v2.1.0`: la puerta comparaba una externalidad **global** contra una capacidad regenerativa **regional**, lo que la volvía **degenerada** (la licencia nunca podía abrirse bajo ninguna política). Esta versión vuelve a anclar la puerta al **balance neto europeo** (responsabilidad sobre la propia contribución), adopta una **formulación dimensionalmente consistente en flujos** (W/m²/año), y reincorpora la vulnerabilidad como **contexto exógeno** que puede endurecer normativamente la tolerancia, no como la magnitud que acciona la puerta.

> **Confirmación numérica (§13.2).** Con los parámetros de `v2.1.0`, el sobrepaso mínimo alcanzable es ≈ 1.38 W/m² y χ ≈ 1.3×10⁻³⁰ incluso con mitigación y remoción al máximo: no existe atractor regenerativo. Con la puerta de responsabilidad de `v3.0.0`, χ → 1.000 es alcanzable con esfuerzo regenerativo suficiente.

---

# 0. Doctrina Operativa: `SICO.CA`

`SICO.CA` no es un acrónimo descriptivo. Es una **condición de autorización industrial y algorítmica**.

```yaml
acronym: SICO.CA
SICO: Sustainable Industrial Competitive Operations
CA: Chained Algorithms
status: controlled_acronym
doctrine: "No more wars. Regeneration now."
```

## 0.1 Significado exacto

> **Operaciones industriales competitivas solo son admisibles si son sostenibles.**
> La sostenibilidad no es una etiqueta descriptiva. Es un límite operativo medible: una región mantiene su licencia si compensa al menos su propia contribución neta al forzamiento.

## 0.2 Expansión semántica

| Elemento | Significado |
| :--- | :--- |
| **S** | `Sustainable`: sin externalización irreversible de daño, y con compensación del daño propio inevitable dentro de la propia región. |
| **I** | `Industrial`: producción de energía, materiales, logística, manufactura, datos y cadenas de valor. |
| **C** | `Competitive`: mejora sistémica sin guerras, destrucción, heridos, muertes ni colapso ecológico; competición generativa y regenerativa. |
| **O** | `Operations`: ejecución medible en tiempo operacional, validada por métricas y trazabilidad. |
| **CA** | `Chained Algorithms`: algoritmos encadenados, auditables, gobernados, extraíbles y reproducibles. |

## 0.3 Línea doctrinal

> **SICO.CA:** industria solo si es sostenible; competición solo si es regenerativa; algoritmos solo si rinden cuentas. La región mantiene su licencia si regenera al menos su propia huella neta; puede elegir, además, un margen de solidaridad para ayudar a compensar el daño global heredado.

---

# 1. Arquitectura del Marco — Responsabilidad Regional bajo Contexto Global

El flujo de información es cerrado pero **asimétrico en escala**: la física global es el **contexto**, la responsabilidad europea es lo que la puerta **gobierna**.

```text
        ┌───────────────────────────────────────────────┐
        │     CONTEXTO FÍSICO GLOBAL (L1, exógeno)        │
        │  EBM 0-D planetario → T_s(t)                    │
        │  Q_anth = Q_resto(t) + Q_UE(t)   [W/m², nivel]  │
        └───────────────┬───────────────────────────────┘
                        │ contexto: T_s, Q_resto (no controlables por la región)
                        │ (pueden endurecer normativamente la tolerancia)
                        ▼
        ┌───────────────────────────────────────────────┐
        │     PUENTE TERMODINÁMICO REGIONAL (L2)          │
        │  x_phys = tasa de forzamiento añadido por la UE │
        │  r_phys = tasa de compensación de la UE         │
        │  Δ_phys = max(0, x_phys + m − r_phys)  [W/m²/yr]│
        │  (todo en TASAS; m = margen de solidaridad)     │
        └───────────────┬───────────────────────────────┘
                        │ Δ_phys (W/m²/yr)
                        ▼
        ┌───────────────────────────────────────────────┐
        │   PUERTA SICO.CA (L2-L3)                        │
        │  dD_reg/dt = Δ_phys − ρ·D_reg   [D_reg en W/m²] │
        │  D_reg = forzamiento europeo NO compensado      │
        │  latch h con umbral móvil                       │
        │  χ = exp(− D_reg·(1+ξ·h) / F_ref )              │
        └───────────────┬───────────────────────────────┘
                        │ χ(t)
                        ▼
        ┌───────────────────────────────────────────────┐
        │   CAPA SOCIO-TÉCNICA REGIONAL (L3)              │
        │  I_EU, E_mitig, E_remove, E_digi, D_ID          │
        │  E_mitig ↓ tasa de forzamiento europea          │
        │  E_remove ↑ tasa de compensación europea        │
        │  E_digi → impulsa D_ID, I_EU                    │
        └───────────────┬───────────────────────────────┘
                        │ E_mitig, E_remove
                        └──► retroalimentación a L2 (no a Q_resto)
```

**La diferencia central con `v2.1.0`.** La puerta ya **no** resta una capacidad regional de un forzamiento global (lo que la hacía degenerada). La puerta keyea el **balance neto europeo**: ¿está Europa compensando al menos el forzamiento que ella misma añade? Eso *sí* lo controla la región, y por tanto *sí* puede ser objeto de una licencia. El forzamiento del resto del mundo y la temperatura global son el **contexto** —el mundo en el que Europa opera— y solo entran en la puerta de forma **normativa**, a través de un margen de solidaridad opcional (§6.4).

---

# 2. Capa Física I — Relatividad General como Marco de Conservación

La relatividad general se mantiene como marco conceptual y para la separación de escalas:

$$
G_{\mu\nu} + \Lambda g_{\mu\nu} = \frac{8\pi G}{c^4}\, T_{\mu\nu}
$$

La contribución antropogénica se elimina del tensor por ser despreciable como fuente de curvatura. La conservación se mantiene como principio rector. **El cómputo operativo recae enteramente en el balance energético y en el puente de flujos.**

---

# 3. Contexto Físico Global — Modelo de Balance Energético (EBM 0‑D)

El EBM proporciona el **contexto climático global** en el que opera la región. No es la magnitud que acciona la puerta.

$$
C_{\mathrm{eff}}\,\frac{dT_s}{dt} = \frac{S_0}{4}\big(1 - A_{\mathrm{alb}}\big) - \epsilon\,\sigma\,T_s^{4} + Q_{\mathrm{anth}}(t)
$$

| Símbolo | Descripción | Valor de referencia |
| :--- | :--- | :--- |
| \(C_{\mathrm{eff}}\) | Capacidad calorífica efectiva | \(\sim 4\times10^{8}\ \mathrm{J\,m^{-2}\,K^{-1}}\) |
| \(S_0\) | Constante solar | \(1361\ \mathrm{W\,m^{-2}}\) |
| \(A_{\mathrm{alb}}\) | Albedo planetario | \(0.30\) |
| \(\epsilon\) | Emisividad efectiva | \(0.61\) (calibra \(T_{eq}\approx 288\ \mathrm{K}\)) |
| \(\sigma\) | Stefan–Boltzmann | \(5.670\times10^{-8}\ \mathrm{W\,m^{-2}\,K^{-4}}\) |
| \(Q_{\mathrm{anth}}\) | Forzamiento antropogénico global neto (**nivel**, W/m²) | \(\sim 2.7\) en 2019 |

El forzamiento global se descompone:

$$
Q_{\mathrm{anth}}(t) = Q_{\mathrm{resto}}(t) + Q_{\mathrm{UE}}(t), \qquad Q_{\mathrm{UE}}(t) = Q_{0,\mathrm{UE}}\,\Theta_{\mathrm{UE}}(t)\,\big(1 - \mu\, E_{\mathrm{mitig}}(t)\big)
$$

donde \(Q_{\mathrm{resto}}\) (el forzamiento del resto del mundo) es una **señal exógena de escenario**. El EBM responde al **nivel** de forzamiento; el puente de §5 opera en **tasas**. La distinción nivel/tasa es deliberada y se justifica en §5.

> Nota de consistencia: \(D_{\mathrm{reg}}\) (§6, el forzamiento europeo acumulado no compensado, W/m²) es, físicamente, la fracción del nivel \(Q_{\mathrm{anth}}\) atribuible a la contribución neta europea no compensada. Las dos magnitudes son coherentes: una es nivel global, la otra es la componente regional de ese nivel.

---

# 4. Transferencia Radiativa (Formulación Estándar)

Se utiliza la ecuación clásica sin acoplamientos especulativos. La generalización relativista (intensidad invariante, transporte geodésico) se conserva para consistencia formal. Sin cambios respecto a v2.x.

---

# 5. Puente Termodinámico — Formulación en Flujos (Tasas)

**Corrección dimensional de `v3.0.0`.** En `v2.x`, tanto \(X_{\mathrm{phys}}\) como \(R_{\mathrm{phys}}\) se trataban como **niveles** de forzamiento (W/m²). Pero un sumidero o una remoción es físicamente un **flujo** (retira carbono a una tasa), no un nivel. Restar un flujo de un nivel es un error de categoría. `v3.0.0` formula el puente enteramente en **tasas de cambio del forzamiento (W/m²/año)**, y deja que la **acumulación** produzca el nivel de deuda.

### 5.1 Tasa de externalidad europea (flujo de forzamiento añadido)

$$
\boxed{x_{\mathrm{phys}}(t) = \kappa_{\mathrm{rad}}\,\Theta_{\mathrm{UE}}(t)\,\big(1 - \mu\, E_{\mathrm{mitig}}(t)\big) \quad [\mathrm{W\,m^{-2}\,yr^{-1}}]}
$$

\(x_{\mathrm{phys}}\) es la **tasa** a la que las emisiones europeas añaden forzamiento. \(\kappa_{\mathrm{rad}}\) agrupa intensidad de emisión × fracción aerotransportada × eficacia radiativa marginal (Apéndice C).

### 5.2 Tasa de compensación europea (flujo de forzamiento retirado)

$$
\boxed{r_{\mathrm{phys}}(t) = \varphi_{\mathrm{bio,UE}}(t) + k_{\mathrm{tech}}\,E_{\mathrm{remove}}(t) \quad [\mathrm{W\,m^{-2}\,yr^{-1}}]}
$$

| Término | Descripción | Fuente |
| :--- | :--- | :--- |
| \(\varphi_{\mathrm{bio,UE}}\) | Tasa de sumidero biosférico regional (W/m²/yr) | LULUCF, RECCAP2, GCB regionalizado |
| \(k_{\mathrm{tech}}\,E_{\mathrm{remove}}\) | Tasa de remoción ingenierizada (DACCS, BECCS, biochar), W/m²/yr; hoy ≈ 0 | Escalamiento tecnológico |

**Se elimina cualquier término de respuesta radiativa (\(\Phi_{\mathrm{rad}}\)).** El calentamiento ya realizado no es capacidad regenerativa; es la firma del daño. (Corrección conservada de v2.0.0.)

### 5.3 Sobrepaso neto y margen de solidaridad

$$
\boxed{\Delta_{\mathrm{phys}}(t) = \max\big(0,\; x_{\mathrm{phys}}(t) + m(t) - r_{\mathrm{phys}}(t)\big) \quad [\mathrm{W\,m^{-2}\,yr^{-1}}]}
$$

donde \(m(t) \ge 0\) es el **margen de solidaridad** (parámetro normativo, §6.4). Con \(m = 0\), la puerta exige solo que Europa compense **su propia huella**. Con \(m > 0\), Europa se compromete a remover **más** de lo que emite, ayudando a compensar el daño global.

> **Por qué esto no es degenerado.** \(x_{\mathrm{phys}}\) y \(r_{\mathrm{phys}}\) son ambas tasas **europeas**. Con mitigación y remoción suficientes, \(r_{\mathrm{phys}}\) puede **superar** a \(x_{\mathrm{phys}} + m\), de modo que \(\Delta_{\mathrm{phys}} = 0\), la deuda decae y \(\chi \to 1\). La región controla ambos lados del balance. (Confirmado en §13.2.)

---

# 6. Función de Autorización SICO.CA — con Retardo e Histéresis

### 6.1 Deuda regenerativa (acumulación del sobrepaso neto)

$$
\frac{dD_{\mathrm{reg}}}{dt} = \Delta_{\mathrm{phys}}(t) - \rho\,D_{\mathrm{reg}}(t)
$$

\(D_{\mathrm{reg}}\) tiene unidades de **W/m²** (la integral de una tasa) y mide el **forzamiento europeo acumulado no compensado** — la "deuda climática" de la región. El término \(\rho\,D_{\mathrm{reg}}\) representa el lento drenaje natural del forzamiento (ajuste del ciclo del carbono); \(\rho\) tiene un anclaje físico en el tiempo de ajuste del ciclo del carbono, aunque se trata como calibrable (zona gris descriptiva/normativa, §7.3).

### 6.2 Latch de histéresis (umbral móvil)

$$
\theta_{\mathrm{eff}}(h) = \theta_{\mathrm{off}} + (\theta_{\mathrm{on}} - \theta_{\mathrm{off}})\,(1 - h)
$$

$$
\frac{dh}{dt} = \frac{1}{\tau_h}\Big[\,\varsigma\big(D_{\mathrm{reg}} - \theta_{\mathrm{eff}}(h)\big) - h\,\Big], \qquad \varsigma(z) = \frac{1}{1 + e^{-k\,z}}
$$

La liberación chasquea por encima de \(\theta_{\mathrm{off}}\) debido al umbral móvil (snap; ver el resultado validado en versiones previas: la liberación precede al cruce de \(\theta_{\mathrm{off}}\), y \(\theta_{\mathrm{off}}\) marca la recuperación plena, no el instante de liberación).

### 6.3 Puerta efectiva

$$
\boxed{\;\chi(t) = \exp\!\Big[-\frac{1}{F_{\mathrm{ref}}}\,D_{\mathrm{reg}}(t)\,\big(1 + \xi\,h(t)\big)\Big]\;}
$$

\(D_{\mathrm{reg}}\) y \(F_{\mathrm{ref}}\) en W/m², exponente adimensional. \(F_{\mathrm{ref}}\) es el nivel de deuda al que χ cae por un factor \(1/e\) (latch apagado).

### 6.4 La vulnerabilidad entra solo como normatividad

La intuición de **vulnerabilidad** de `v2.1.0` —que un mundo más caliente debería exigir más a la región— es correcta, pero **no puede accionar la puerta**: si la puerta estrangulara el crecimiento tecnológico en función del forzamiento global (no controlable), penalizaría a la región por las emisiones del mundo y bloquearía justamente la mitigación y la remoción que constituyen la acción responsable (un bucle perverso). Por eso la vulnerabilidad entra **solo** a través del margen de solidaridad normativo:

$$
m(t) = m_0 + m_1 \cdot \max\big(0,\; T_s(t) - T_{\mathrm{ref}}\big)
$$

con \(m_0, m_1 \ge 0\) **elegidos por los actores**. \(m_1 > 0\) codifica "Europa hace más cuanto más caliente está el mundo" — una decisión de valor, no un hecho físico. Con \(m_0 = m_1 = 0\), la puerta es de pura responsabilidad sobre la propia huella.

> Síntesis de las dos lecturas: el **núcleo descriptivo** mide responsabilidad (balance propio); la **capa normativa** puede añadir solidaridad ante la vulnerabilidad global. La vulnerabilidad es contexto y elección, nunca compuerta automática sobre operaciones.

---

# 7. Variables Controladas

## 7.1 Núcleo descriptivo (respaldable empíricamente)

| Símbolo | Descripción | Unidad |
| :--- | :--- | :--- |
| \(T_s\) | Temperatura superficial global (contexto) | K |
| \(Q_{\mathrm{anth}}\) | Forzamiento global neto (contexto, nivel) | W/m² |
| \(Q_{\mathrm{resto}}\) | Forzamiento del resto del mundo (exógeno) | W/m² |
| \(x_{\mathrm{phys}}\) | Tasa de forzamiento añadido por la UE | W/m²/yr |
| \(r_{\mathrm{phys}}\) | Tasa de compensación de la UE | W/m²/yr |
| \(\Delta_{\mathrm{phys}}\) | Tasa de sobrepaso neto regional | W/m²/yr |
| \(D_{\mathrm{reg}}\) | Forzamiento europeo acumulado no compensado (deuda climática) | W/m² |
| \(h\) | Estado del latch | adimensional |
| \(\varphi_{\mathrm{bio,UE}}\) | Tasa de sumidero biosférico regional | W/m²/yr |
| \(E_{\mathrm{mitig}}\) | Descarbonización europea (eficiencia, renovables) | [0,1] |
| \(E_{\mathrm{remove}}\) | Despliegue de remoción ingenierizada europea | [0,1] |
| \(E_{\mathrm{digi}}\) | Eficacia tecnológica digital | [0,1] |
| \(I_{\mathrm{EU}}\) | Integración institucional europea | [0,1] |
| \(D_{\mathrm{ID}}\) | Adopción de identidad digital europea | [0,1] |

## 7.2 Capa normativa (juicios de valor, a fijar por los actores)

| Símbolo | Significado |
| :--- | :--- |
| \(F_{\mathrm{ref}}\) | Tolerancia a la deuda (W/m²) — escala de penalización |
| \(\theta_{\mathrm{on}}\) | Umbral de activación del latch (W/m²) |
| \(\theta_{\mathrm{off}}\) | Umbral de recuperación plena (W/m²) |
| \(\xi\) | Amplificación de penalización con latch activo |
| \(\tau_h\) | Escala temporal del latch |
| \(k\) | Pendiente del smoothstep |
| \(m_0\) | Margen de solidaridad base (W/m²/yr) |
| \(m_1\) | Sensibilidad del margen a la temperatura global (W/m²/yr/K) |

## 7.3 Parámetro de zona gris

\(\rho\) (tasa de recuperación de la deuda) tiene un **anclaje físico** (tiempo de ajuste del ciclo del carbono, ~décadas a siglos) pero su valor efectivo en un modelo de orden cero es calibrable. Se declara explícitamente como descriptivo-con-elección, no puramente normativo ni puramente físico.

---

## 8. Sistema Socio-Técnico Acoplado

### Acotado por construcción

Todas las variables socio-técnicas están acotadas en el intervalo:

```math
[0,1]
```

por construcción. El sistema se formula como un conjunto de ecuaciones diferenciales acopladas.

#### Integración institucional europea

```math
\frac{dI_{\mathrm{EU}}}{dt}
=
\left(
aC
+ bR_{\mathrm{reg}}
+ cA_{\mathrm{inst}}
+ d
\right)
\left(1 - I_{\mathrm{EU}}\right)
+
\kappa_{E_{\mathrm{digi}},I}
E_{\mathrm{digi}}
\left(1 - I_{\mathrm{EU}}\right)
-
\gamma_I I_{\mathrm{EU}}
```

#### Tecnología de mitigación

```math
\frac{dE_{\mathrm{mitig}}}{dt}
=
\chi(t)
\eta_{\mathrm{mit}}
\left(UA_{\mathrm{adopt}}\right)^{\alpha_{\mathrm{mit}}}
I_{\mathrm{EU}}^{\beta_{\mathrm{mit}}}
\left(1 - E_{\mathrm{mitig}}\right)
-
\delta_{\mathrm{mit}} E_{\mathrm{mitig}}
```

#### Tecnología de remoción

```math
\frac{dE_{\mathrm{remove}}}{dt}
=
\chi(t)
\eta_{\mathrm{rem}}
\left(UA_{\mathrm{adopt}}\right)^{\alpha_{\mathrm{rem}}}
I_{\mathrm{EU}}^{\beta_{\mathrm{rem}}}
\left(1 - E_{\mathrm{remove}}\right)
-
\delta_{\mathrm{rem}} E_{\mathrm{remove}}
```

#### Tecnología digital

```math
\frac{dE_{\mathrm{digi}}}{dt}
=
\chi(t)
\eta_{\mathrm{dig}}
\left(UA_{\mathrm{adopt}}\right)^{\alpha_{\mathrm{dig}}}
I_{\mathrm{EU}}^{\beta_{\mathrm{dig}}}
\left(1 - E_{\mathrm{digi}}\right)
+
\kappa_{D_{\mathrm{ID}},E_{\mathrm{digi}}}
D_{\mathrm{ID}}
\left(1 - E_{\mathrm{digi}}\right)
-
\delta_{\mathrm{dig}} E_{\mathrm{digi}}
```

#### Identidad digital

```math
\frac{dD_{\mathrm{ID}}}{dt}
=
\sigma_D
\left[
\frac{1}
{
1 + e^{-\left(
uI_{\mathrm{EU}}
+ vS
+ wE_{\mathrm{digi}}
+ x
\right)}
}
-
D_{\mathrm{ID}}
\right]
```

---

### Notas de diseño

* `E_mitig` reduce únicamente la tasa de forzamiento europea `x_phys`, vía `mu`.
  No modifica la compensación.

* `E_remove` aumenta únicamente la tasa de compensación `r_phys`, vía `k_tech`.
  No modifica las emisiones.

* La descarbonización y la remoción son tecnologías distintas y no co-mueven por construcción.
  Se conserva así la corrección estructural introducida mediante la separación de `E_clean`.

* `E_digi` impulsa la adopción digital y la integración institucional.
  No afecta directamente al balance físico.

* La puerta `chi(t)` estrangula el crecimiento primario de las tres variables tecnológicas:

```math
E_{\mathrm{mitig}}, \quad
E_{\mathrm{remove}}, \quad
E_{\mathrm{digi}}
```

* Los canales cruzados, por ejemplo:

```math
\kappa_{D_{\mathrm{ID}},E_{\mathrm{digi}}}
```

pueden permanecer libres o ser estrangulados según el modo de gobernanza definido en §13.3.
La fuga de momento institucional resultante afecta a la forma de la separatriz.

* `Theta_UE` es, en la versión base, una entrada exógena.
  Su endogenización queda reservada como extensión experimental.

---

### Vector de estado

El vector de estado del sistema se define como:

```math
\mathbf{y}(t)
=
\left[
I_{\mathrm{EU}},
E_{\mathrm{mitig}},
E_{\mathrm{remove}},
E_{\mathrm{digi}},
D_{\mathrm{ID}},
T_s,
D_{\mathrm{reg}},
h
\right]^{\mathsf{T}}
```

donde:

| Variable   | Descripción resumida                                 |
| ---------- | ---------------------------------------------------- |
| `I_EU`     | Integración institucional europea                    |
| `E_mitig`  | Capacidad tecnológica de mitigación                  |
| `E_remove` | Capacidad tecnológica de remoción                    |
| `E_digi`   | Adopción e integración digital                       |
| `D_ID`     | Adopción de identidad digital                        |
| `T_s`      | Temperatura o estado térmico sistémico               |
| `D_reg`    | Densidad o presión regulatoria                       |
| `h`        | Variable auxiliar de horizonte, memoria o histéresis |

---

# 9. Bucles de Retroalimentación

| Bucle | Mecanismo | Efecto sistémico |
| :--- | :--- | :--- |
| \(E_{\mathrm{mitig}} \uparrow \rightarrow x_{\mathrm{phys}} \downarrow\) | Descarbonización europea | Menor tasa de forzamiento propio |
| \(E_{\mathrm{remove}} \uparrow \rightarrow r_{\mathrm{phys}} \uparrow\) | Remoción ingenierizada regional | Mayor tasa de compensación |
| \(\Delta_{\mathrm{phys}} \uparrow \rightarrow D_{\mathrm{reg}} \uparrow \rightarrow \chi \downarrow\) | Deuda persistente | Licencia perdida rápido, recuperación lenta |
| \(E_{\mathrm{digi}} \uparrow \rightarrow D_{\mathrm{ID}} \uparrow \rightarrow E_{\mathrm{digi}}\) | Inercia digital (canal cruzado) | Crecimiento residual aun con χ bajo (fuga institucional) |
| \(T_s \uparrow \rightarrow m(t) \uparrow\) (si \(m_1>0\)) | Solidaridad normativa | Mayor exigencia de compensación ante mundo más caliente |

El bucle virtuoso ahora cierra correctamente: **mitigación + remoción suficientes → \(\Delta=0\) → deuda decae → χ→1 → más crecimiento autorizado.** Y el bucle vicioso: **esfuerzo bajo → \(\Delta>0\) → deuda crece → latch → χ→0 → crecimiento bloqueado.** Existe biestabilidad y una separatriz alcanzable (a diferencia de v2.1.0, donde solo existía la trampa).

---

# 10. Implementación Numérica Reproducible

`scipy.integrate.solve_ivp` (RK45). Constantes físicas fijas; puente en tasas; puerta de responsabilidad.

```python
from dataclasses import dataclass, field
import numpy as np
from scipy.integrate import solve_ivp

SEC_PER_YEAR = 3.155693e7

@dataclass(frozen=True)
class PhysicalConstants:
    S0: float = 1361.0
    albedo: float = 0.30
    epsilon: float = 0.61
    sigma: float = 5.670374419e-8
    C_eff: float = 4.0e8
    T_ref: float = 288.0

@dataclass
class Parameters:
    pc: PhysicalConstants = field(default_factory=PhysicalConstants)

    # --- socio-tecnicos ---
    a=0.05; b=0.08; c=0.04; d=0.01
    gamma_I=0.02; sigma_D=0.1
    eta_mit=0.5; alpha_mit=0.6; beta_mit=0.4; delta_mit=0.03
    eta_rem=0.4; alpha_rem=0.5; beta_rem=0.5; delta_rem=0.02
    eta_dig=0.4; alpha_dig=0.5; beta_dig=0.5; delta_dig=0.03
    kappa_EdigiI=0.02; kappa_DIDE_digi=0.015
    u=1.2; v=0.8; w=1.0; x=-2.5

    # --- contexto fisico global (NIVEL) ---
    Q0_UE=0.18; mu=0.85          # contribucion europea al nivel de forzamiento (W/m2)

    # --- puente regional (TASAS, W/m2/yr) ---  [ILUSTRATIVAS: calibrar con RECCAP2/GCB]
    kappa_rad=0.020              # tasa de forzamiento europea a plena actividad, mitigacion nula
    phi_bio_UE=0.004             # tasa de sumidero biosferico europeo
    k_tech=0.020                 # tasa de remocion ingenierizada europea (potencial)

    # --- puerta (NORMATIVOS) ---
    F_ref=1.0
    rho=0.05                     # zona gris (anclaje en ciclo del carbono)
    theta_on=0.20; theta_off=0.08
    tau_h=2.0; xi=1.5; k_steep=12.0
    m0=0.0; m1=0.0               # margen de solidaridad (normativo)

def smoothstep(z, k): return 1.0/(1.0+np.exp(-k*z))

# ----- Puente en TASAS -----
def x_phys(t, E_mitig, Theta_UE, p):
    """Tasa de forzamiento europea (W/m2/yr)."""
    return p.kappa_rad * Theta_UE(t) * max(0.0, 1.0 - p.mu*E_mitig)

def r_phys(E_remove, p):
    """Tasa de compensacion europea (W/m2/yr)."""
    return p.phi_bio_UE + p.k_tech*E_remove

def solidarity_margin(T_s, p):
    return p.m0 + p.m1*max(0.0, T_s - p.pc.T_ref)

def overshoot(t, E_mitig, E_remove, T_s, Theta_UE, p):
    return max(0.0, x_phys(t,E_mitig,Theta_UE,p) + solidarity_margin(T_s,p) - r_phys(E_remove,p))

def gate(D_reg, h, p):
    return float(np.exp(-D_reg*(1.0+p.xi*h)/p.F_ref))

# ----- Campo vectorial completo (8 estados) -----
def derivatives(t, y, p, inp):
    I_EU, E_mit, E_rem, E_dig, D_ID, T_s, D_reg, h = y
    C=inp["C"](t); Rg=inp["R"](t); A_inst=inp["A_inst"](t)
    U=inp["U"](t); A_ad=inp["A_adopt"](t); S=inp["S"](t)
    Theta_UE=inp["Theta_UE"]; Q_resto=inp["Q_resto"](t)

    chi = gate(D_reg, h, p)

    dI = ((p.a*C+p.b*Rg+p.c*A_inst+p.d)*(1-I_EU)
          + p.kappa_EdigiI*E_dig*(1-I_EU) - p.gamma_I*I_EU)
    base = lambda al,be: (U*A_ad)**al * max(I_EU,0.0)**be
    dEmit = chi*p.eta_mit*base(p.alpha_mit,p.beta_mit)*(1-E_mit) - p.delta_mit*E_mit
    dErem = chi*p.eta_rem*base(p.alpha_rem,p.beta_rem)*(1-E_rem) - p.delta_rem*E_rem
    dEdig = (chi*p.eta_dig*base(p.alpha_dig,p.beta_dig)*(1-E_dig)
             + p.kappa_DIDE_digi*D_ID*(1-E_dig) - p.delta_dig*E_dig)
    z = p.u*I_EU+p.v*S+p.w*E_dig+p.x
    dDID = p.sigma_D*(1.0/(1.0+np.exp(-z)) - D_ID)

    # contexto fisico global (nivel)
    Q_UE = p.Q0_UE*Theta_UE(t)*max(0.0,1.0-p.mu*E_mit)
    Q_anth = Q_resto + Q_UE
    absorbed = p.pc.S0/4.0*(1.0-p.pc.albedo)
    OLR = p.pc.epsilon*p.pc.sigma*T_s**4
    dT = (absorbed - OLR + Q_anth)*SEC_PER_YEAR/p.pc.C_eff

    # deuda regenerativa (acumula la tasa de sobrepaso neto)
    Delta = overshoot(t, E_mit, E_rem, T_s, Theta_UE, p)
    dD_reg = Delta - p.rho*D_reg
    th_eff = p.theta_off + (p.theta_on-p.theta_off)*(1-h)
    dh = (smoothstep(D_reg-th_eff, p.k_steep) - h)/p.tau_h

    return np.array([dI,dEmit,dErem,dEdig,dDID,dT,dD_reg,dh])
```

---

# 11. Escenario Determinista de Simulación

Señales exógenas:

```python
inp = {
    "C":       lambda t: 0.50 + 0.10*np.sin(0.02*t),
    "R":       lambda t: 0.60 + 0.05*t/150.0,
    "A_inst":  lambda t: 0.40 + 0.10*(1-np.exp(-0.02*t)),
    "U":       lambda t: 0.70 + 0.20*(1-np.exp(-0.03*t)),
    "A_adopt": lambda t: 0.50 + 0.15*(1-np.exp(-0.025*t)),
    "S":       lambda t: 0.80,
    "Theta_UE": lambda t: 0.70 + 0.30*(1-np.exp(-0.02*t)),   # actividad europea
    "Q_resto":  lambda t: 1.8 + 0.4*(1-np.exp(-0.03*t)),     # forzamiento resto del mundo -> ~2.2
}
# y0 = [I_EU, E_mitig, E_remove, E_digi, D_ID, T_s, D_reg, h]
y0 = np.array([0.20, 0.10, 0.05, 0.10, 0.10, 287.5, 0.0, 0.0])
```

El escenario **Regenerativo** requiere desplegar mitigación **y** remoción: la mitigación baja \(x_{\mathrm{phys}}\), la remoción sube \(r_{\mathrm{phys}}\), hasta que \(\Delta=0\). La temperatura global sigue dominada por \(Q_{\mathrm{resto}}\); el "doblez térmico" europeo es modesto porque la contribución europea al **nivel** global es pequeña — pero la **licencia** sí responde plenamente al esfuerzo europeo, porque keyea el balance propio.

---

# 12. Calibración e Identificabilidad

- **Núcleo descriptivo (físico/de tasas):** \(\kappa_{\mathrm{rad}}, \varphi_{\mathrm{bio,UE}}, k_{\mathrm{tech}}, Q_{0,\mathrm{UE}}, \mu\) — calibrables con inventarios europeos, RECCAP2, GCB regionalizado (conversión en Apéndice C).
- **Núcleo descriptivo (socio-técnico):** coeficientes de las EDO; **no identificables** sin un modelo de medición con indicadores observables (análisis factorial dinámico; ver hoja de ruta de datos).
- **Capa normativa:** \(F_{\mathrm{ref}}, \theta_{\mathrm{on}}, \theta_{\mathrm{off}}, \xi, \tau_h, m_0, m_1\) — no se estiman; se fijan por deliberación.
- **Zona gris:** \(\rho\) — anclar en el tiempo de ajuste del ciclo del carbono.

La equifinalidad del bloque socio-técnico persiste como limitación central; se requiere identificabilidad estructural/práctica antes de cualquier afirmación de trazabilidad de coeficientes.

---

# 13. Validación por Simulación

> **Las figuras de `v1.1.0` ya no son válidas para `v3.0.0`:** usaban el modelo de niveles, con \(\Phi_{\mathrm{rad}}\), una sola \(E_{\mathrm{clean}}\) y la puerta keyeada distinto. **Toda la validación debe regenerarse bajo esta especificación.** Lo que sigue es la confirmación numérica de la corrección central y las predicciones cualitativas pendientes de re-corrida completa.

### 13.1 Comportamiento esperado (pendiente de re-corrida)

- **Regenerativo:** Europa acelera mitigación y remoción; \(\Delta\to 0\); la deuda decae; χ→1. La temperatura global sigue \(Q_{\mathrm{resto}}\); el doblez térmico es modesto (intencionado: Europa no controla el clima global).
- **Trampa:** esfuerzo de remoción bajo; \(\Delta>0\) persistente; latch activo; χ→0.
- **Recuperación tardía:** tras una crisis, despliegue masivo de remoción; recuperación con el retardo asimétrico característico y el snap por encima de \(\theta_{\mathrm{off}}\).

### 13.2 Confirmación numérica de la corrección de la puerta

| Configuración | Resultado | Veredicto |
| :--- | :--- | :--- |
| **`v2.1.0`** (X global vs R regional), mejor caso \(E_{\mathrm{mitig}}=E_{\mathrm{remove}}=1\) | \(\Delta_{\min}\approx 1.38\,\mathrm{W/m^2}\); \(D_{\mathrm{reg}}^{*}\approx 27.5\,\mathrm{W/m^2}\); \(\chi\approx 1.3\times10^{-30}\) | **Degenerada**: no existe atractor regenerativo |
| **`v3.0.0`** (balance neto europeo), escenario regenerativo | \(D_{\mathrm{reg}}\to 0.000\); \(h\to 0\); \(\chi\to 1.000\) | **No degenerada**: atractor regenerativo alcanzable |
| **`v3.0.0`**, escenario de esfuerzo bajo | \(D_{\mathrm{reg}}\) crece; latch activo; \(\chi\downarrow\) | Trampa alcanzable (biestabilidad) |

Esta tabla es la justificación empírica del cambio arquitectónico de `v3.0.0`.

### 13.3 Modos de diseño de gobernanza (extensión experimental, actividad endógena)

La sección de cuenca se mantiene como extensión experimental, ahora sobre **tres** variables tecnológicas. Modos:

| Modo | Canales cruzados | Actividad bajo χ | Efecto en la separatriz |
| :--- | :--- | :--- | :--- |
| `faithful_v1` | libres | no | Línea base; fuga institucional permite escapes marginales |
| `strict_license` | estrangulados | no | Trampa más profunda; separatriz hacia menor actividad |
| `activity_suppressed_by_chi` | estrangulados | sí | Recuperación por contracción operativa — escenario de gobernanza, no físico |

Salvaguardas: clasificación por atractor (no por foto temporal); la sección 2D es un corte de una cuenca de dimensión superior; condiciones iniciales \(D_{\mathrm{reg},0}=0, h_0=0\).

---

# 14. Condiciones de Validez

1. **Consistencia dimensional** — el puente opera en tasas (W/m²/yr); la deuda es un nivel (W/m²). Nivel y flujo no se confunden.
2. **Separación de capas** — núcleo descriptivo vs capa normativa, en tablas separadas (§7).
3. **Reproducibilidad** — hash de parámetros, entradas y constantes.
4. **Auditabilidad** — fuente, fecha, método, versión y veredicto de identificabilidad por parámetro.
5. **Falsabilidad** — \(\kappa_{\mathrm{rad}}, k_{\mathrm{tech}}, \varphi_{\mathrm{bio,UE}}\) deben poder rechazarse empíricamente.
6. **No externalización irreversible** — codificada por la deuda persistente.
7. **Reducción a modelos estándar** — con \(Q_{\mathrm{anth}}\to 0\), el EBM se reduce al equilibrio radiativo; con \(\chi\to 1\), la dinámica socio-técnica se reduce a difusión estándar.
8. **Separación de escalas físicas** — lo antropogénico no entra en las ecuaciones de campo.
9. **Gobernanza algorítmica** — algoritmos encadenados, explicables, extraíbles, contestables.
10. **Coherencia de escala** — la física es global (contexto); la responsabilidad es regional (lo gobernado). La puerta keyea el **balance neto regional**, no el forzamiento global.
11. **Separación mitigación/remoción** — \(E_{\mathrm{mitig}}\) y \(E_{\mathrm{remove}}\) son capacidades distintas y no co-mueven por construcción.
12. **No degeneración de la puerta** — debe existir un conjunto alcanzable de estados con \(\chi\to 1\) (confirmado §13.2). Una puerta que nunca puede abrirse es inadmisible.

---

# 15. Originalidad y Posicionamiento

La contribución:

1. Una **arquitectura** que separa limpiamente la física descriptiva de los parámetros normativos de gobernanza, con partición is/ought hasta el último parámetro.
2. Un **puente en flujos** dimensionalmente consistente, donde la deuda climática regional emerge como la integral del sobrepaso neto.
3. Una **puerta de responsabilidad** keyeada al balance que el actor controla, no al forzamiento global que no controla — con memoria asimétrica (rápida de perder, lenta de recuperar) y liberación por snap.
4. La **separación explícita** de descarbonización y remoción como canales tecnológicos independientes.
5. La **vulnerabilidad como contexto normativo** (margen de solidaridad), no como compuerta automática — resolviendo la incoherencia de keyear operaciones sobre lo no controlable.

El hallazgo no es "una memoria asimétrica puede emerger" (la histéresis de dos umbrales es de manual), sino la **arquitectura auditable de extremo a extremo cuyas capas descriptiva y normativa se separan limpiamente**, y la demostración de que la elección de qué magnitud acciona la puerta (balance propio vs forzamiento global) es la diferencia entre un modelo viable y uno degenerado.

---

# 16. Implicaciones Operativas

1. **Licencia de operación computable** keyeada a la responsabilidad propia: ¿compensa la región su contribución neta (más el margen elegido)? Evaluable de forma continua contra KPIs reales (inventario de emisiones, sumideros, despliegue de remoción).
2. **Instrumento de deliberación, no predictor.** Los actores fijan \(F_{\mathrm{ref}}\), umbrales y margen de solidaridad \(m_0, m_1\); el modelo proyecta consecuencias sobre la licencia y la dinámica tecnológica. La vulnerabilidad global se delibera como cuánto margen de solidaridad asumir.
3. **Sensibilidad de la separatriz como enunciado de política.** El resultado de mayor valor es cuánto \(k_{\mathrm{tech}}\) (capacidad de remoción) o \(\mu\) (descarbonización) hace falta para desplazar la separatriz y sacar un punto de partida realista de la trampa.

**Límites declarados:** el bloque socio-técnico puede ser irresoluble en identificabilidad al nivel agregado; \(\kappa_{\mathrm{rad}}, k_{\mathrm{tech}}, \varphi_{\mathrm{bio,UE}}\) son marcadores ilustrativos hasta su calibración (RECCAP2/GCB, Apéndice C); la endogenización de la actividad es experimental; la validación por episodios prueba el **mecanismo**, no la aptitud para decidir.

---

# 17. Tesis Consolidada

> **El Ampel Theoretical Framework v3.0.0 modela a una región (Europa) que enfrenta un forzamiento climático global que no controla, pero del que es parcialmente responsable. Su licencia de operación industrial keyea el balance que sí controla: si su tasa de compensación regenerativa (sumideros + remoción) iguala al menos su tasa de forzamiento propio (más un margen de solidaridad elegido), la deuda climática regional no crece y la licencia permanece abierta. Una puerta con deuda e histéresis convierte el déficit acumulado en una restricción asimétrica —rápida de perder, lenta de recuperar—. La física global es el contexto; la vulnerabilidad entra solo como elección normativa de solidaridad; todos los parámetros de valor están separados del núcleo descriptivo. El marco es un instrumento de razonamiento y deliberación, no un predictor validado — y la corrección clave de esta versión es que la puerta debe keyear lo que el actor controla, no lo que padece, so pena de degeneración.**

---

# 18. Fórmula Axial

```text
Contexto fisico global (nivel, exogeno):
  Q_anth = Q_resto(t) + Q_UE(E_mitig)
  dT_s/dt = (solar - OLR + Q_anth) / C_eff

Puente regional EN TASAS (W/m^2/yr):
  x_phys = kappa_rad * Theta_UE * (1 - mu*E_mitig)      # tasa de forzamiento propio
  r_phys = phi_bio_UE + k_tech * E_remove               # tasa de compensacion propia
  Delta  = max(0, x_phys + m(T_s) - r_phys)             # sobrepaso NETO regional

Puerta de responsabilidad:
  dD_reg/dt = Delta - rho*D_reg     # D_reg = forzamiento propio no compensado (W/m^2)
  latch h con umbral movil (snap)
  chi = exp( - D_reg*(1+xi*h) / F_ref )

Normatividad (separada):
  F_ref, theta_on, theta_off, m0, m1  <- elegidos por los actores
  m(T_s) = m0 + m1*max(0, T_s - T_ref)   # vulnerabilidad como solidaridad

Correccion clave v3.0.0:
  La puerta keyea el BALANCE NETO regional (controlable),
  NO el forzamiento global (no controlable).
  v2.1.0: chi ~ 1e-30 siempre (degenerada).
  v3.0.0: chi -> 1 alcanzable (atractor regenerativo existe).
```

---

# Apéndice A — Extensiones Especulativas (No Validadas)

Sin cambios. Acoplamientos cosmológicos o de materia oscura permanecen fuera del modelo operativo. Endogenización de \(\Theta_{\mathrm{UE}}\): requiere una teoría de demanda económica y su estrangulamiento por la licencia, no formalizada.

---

# Apéndice B — Diseño de la Validación por Episodios

Caso canónico: **Protocolo de Montreal / ozono**, físicamente anclado (CFCs medidos → destrucción de ozono → restricción coordinada → recuperación lenta). Distinción explícita de dos mecanismos de memoria, que el test debe separar:

1. **Memoria química** (vida atmosférica de los CFCs) → recuperación lenta, capturada por \(\rho\).
2. **Memoria institucional** (reluctancia a levantar restricciones tras la mejora) → capturada por el latch de histéresis (\(h, \theta_{\mathrm{on}}, \theta_{\mathrm{off}}\)).

El test debe **distinguir** ambas: si el decaimiento químico (\(\rho\)) explica por sí solo la cronología del ozono, el latch institucional no añade poder explicativo **en ese episodio**, y debe descartarse para él. Precauciones obligatorias: precomprometer una métrica (error en fechas de pérdida/recuperación, AIC/BIC) antes de mirar datos; incluir **no-eventos** (carbón, deforestación tropical: externalidad alta sin pérdida de licencia) y una tasa base; encuadre de **análisis de supervivencia** con la externalidad como covariable. Hipótesis esperada: la externalidad física es un **predictor débil** del hazard de pérdida de licencia social — hallazgo que reforzaría la necesidad de un modelo de percepción social separado. No seleccionar episodios por su forma (sesgo sobre la variable dependiente); evitar la coincidencia-de-forma a través de mecanismos distintos.

---

# Apéndice C — Conversión de Flujos (GtCO₂/año → W/m²/año)

Para expresar \(\varphi_{\mathrm{bio,UE}}\) y \(k_{\mathrm{tech}}E_{\mathrm{remove}}\) como tasas de forzamiento (W/m²/año) comparables con \(x_{\mathrm{phys}}\):

1. Emisión/remoción anual en GtCO₂/yr → GtC/yr (÷ 3.664).
2. Fracción aerotransportada para emisiones: AF ≈ 0.45 (la fracción que permanece y altera el forzamiento).
3. Eficacia radiativa marginal del CO₂: \(dF/dC \approx 0.006\ \mathrm{W\,m^{-2}\,GtC^{-1}}\) al nivel actual (\(\approx 420\) ppm), derivada de \(\Delta F = 5.35\,\ln(C/C_0)\).
4. Tasa de forzamiento ≈ (GtC/yr) × AF × \(dF/dC\), en W/m²/yr globales.

**Asimetría emisión/remoción (importante):** retirar 1 GtC **no** reduce el forzamiento tanto como emitir 1 GtC lo aumentó, porque el ciclo del carbono **rellena parcialmente** (desgasificación oceánica y terrestre tras la remoción). La eficacia efectiva de remoción es menor que la de emisión; debe aplicarse un factor de rebote del ciclo del carbono (función de la respuesta impulso del sistema), no la misma eficacia con signo cambiado. Esta asimetría se omitía en `v2.1.0` y es material para \(r_{\mathrm{phys}}\).

> Se descarta la mezcla previa con métricas integradas a 100 años (AGWP), que son una cantidad distinta (W·m⁻²·yr/kg) y no deben combinarse con la eficacia radiativa instantánea. La conversión anterior es aproximada y constituye en sí misma una **nota metodológica**, no un valor cerrado: el mapeo de un flujo de sumidero a W/m²/yr depende de AF y del horizonte, y debe declararse.

---

# Changelog v3.0.0

- **CORRECCIÓN CRÍTICA — puerta degenerada en v2.1.0.** Comparar \(X_{\mathrm{phys}}\) global contra \(R_{\mathrm{phys}}\) regional daba \(\Delta_{\min}\approx 1.38\,\mathrm{W/m^2}\) y \(\chi\approx 1.3\times10^{-30}\) en el mejor caso: no existía atractor regenerativo. **La puerta se re-keyea al balance neto europeo** (responsabilidad propia): \(\Delta=\max(0, x_{\mathrm{phys}}+m-r_{\mathrm{phys}})\). Confirmado \(\chi\to 1\) alcanzable (§13.2).
- **Formulación en flujos.** \(x_{\mathrm{phys}}, r_{\mathrm{phys}}\) son ahora **tasas** (W/m²/yr); \(D_{\mathrm{reg}}\) es el **forzamiento acumulado no compensado** (W/m²) = deuda climática. Corrige el error de categoría nivel-vs-flujo (un sumidero es un flujo, no un nivel de forzamiento).
- **Vulnerabilidad → contexto, no compuerta.** \(Q_{\mathrm{resto}}, T_s\) son contexto exógeno; entran en la puerta solo vía el margen de solidaridad normativo \(m(T_s)=m_0+m_1\max(0,T_s-T_{\mathrm{ref}})\). Se resuelve el bucle perverso de estrangular operaciones por forzamiento no controlable.
- **Margen de solidaridad** \(m_0, m_1\) como parámetros normativos explícitos.
- **Apéndice C reescrito:** conversión GtCO₂/yr → W/m²/yr limpia; añadida la **asimetría emisión/remoción** (rebote del ciclo del carbono); eliminada la mezcla con AGWP.
- **Figuras de v1.1.0 invalidadas** para v3.0.0 (modelo distinto); validación a regenerar.
- **Conservado de v2.x:** separación \(E_{\mathrm{mitig}}/E_{\mathrm{remove}}\); partición is/ought; validación Montreal con distinción química-vs-latch; puerta de memoria asimétrica con snap; honestidad de identificabilidad; GR como marco.
- Nueva condición de validez 12: **no degeneración de la puerta**.

---

> **No more wars. Regeneration now. Industria solo si es sostenible. Competición solo si es regenerativa. Algoritmos solo si rinden cuentas — y la licencia de una región keyea lo que ella controla: la compensación de su propia huella, no el forzamiento del mundo que padece.**

