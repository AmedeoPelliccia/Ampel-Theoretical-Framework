---
document_id: AMPEL-THEORETICAL-FRAMEWORK-SICOCA-003
title: "Ampel Theoretical Framework — Capa de Límite Físico, Puente Termodinámico, Gobernanza SICO.CA y Validación por Simulación"
version: "1.1.0"
status: controlled
supersedes: AMPEL-THEORETICAL-FRAMEWORK-SICOCA-002 (v1.0.0)
classification: open-theoretical-framework
author: "Amedeo Pelliccia / AM.PEL — AMPEL Framework"
language: es
architecture_placement:
  taxonomy: Q+ATLANTIDE1000
  informs:
    - "400-499_EPTA — energía, balance térmico, forzamiento antropogénico"
    - "300-399_DTCEC — gemelo digital, registro de evidencia, hilo digital"
    - "900-999_QCSAA — gobernanza algorítmica, agencia, ética"
  rule_compliance: "No-AAA"
domain:
  - theoretical-physics
  - climate-energy-balance
  - socio-technical-governance
  - sustainable-industrial-operations
doctrine:
  - SICO.CA
  - Chained Algorithms
  - "No more wars. Regeneration now."
figures:
  - fig_01_temperature_trajectories.png
  - fig_02_authorization_gate.png
  - fig_03_late_recovery_hysteresis.png
  - fig_04_basin_section.png
data:
  - scenario_A_regenerative.csv
  - scenario_B_unsustainability_trap.csv
  - scenario_C_late_recovery.csv
  - basin_section.csv
---

# Ampel Theoretical Framework
## Capa de Límite Físico, Puente Termodinámico, Gobernanza SICO.CA y Validación por Simulación

El **Ampel Theoretical Framework** define una arquitectura sistémica en la que la física fundamental fija los límites materiales de la civilización, un **modelo de balance energético** traduce esos límites en magnitudes operativas medibles, y la gobernanza socio-técnica determina si las operaciones industriales permanecen dentro de dichos límites.

`v1.1.0` añade, sobre `v1.0.0`, la **validación por simulación** (§14): cuatro figuras y cuatro conjuntos de datos que ejecutan el modelo de la especificación y confirman su comportamiento, más una **corrección cuantificada del mecanismo de liberación histerética** (§6.5).

El marco conecta tres capas:

1. **Capa física** — relatividad general como marco conceptual de conservación; balance energético de orden cero (EBM) como reducción operativa; transferencia radiativa estándar.
2. **Capa de acoplamiento** — un puente termodinámico que define `X_ext` (externalidad) y `R_cap` (capacidad regenerativa) a partir de flujos físicos.
3. **Capa socio-técnica y doctrinal** — un sistema dinámico acotado con una **puerta de autorización `SICO.CA` con retardo e histéresis**.

La tesis central, ahora computable y validada:

> Las operaciones industriales y algorítmicas solo son admisibles si sus externalidades, **medidas como forzamiento físico neto**, permanecen por debajo de una capacidad regenerativa medible, auditable y gobernada.

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
> La sostenibilidad no es una etiqueta descriptiva. Es un límite operativo medible.

## 0.2 Expansión semántica

| Elemento | Significado                                                                                                         |
| :------- | :------------------------------------------------------------------------------------------------------------------ |
| **S**    | `Sustainable`: cero externalización irreversible de daño hacia sistemas, poblaciones o ecosistemas más vulnerables. |
| **I**    | `Industrial`: producción de energía, materiales, logística, manufactura, datos y cadenas de valor.                  |
| **C**    | `Competitive`: mejora sistémica sin guerras, destrucción, heridos, muertes ni colapso ecológico.                    |
| **O**    | `Operations`: ejecución medible en tiempo operacional, validada por métricas y trazabilidad.                        |
| **CA**   | `Chained Algorithms`: algoritmos encadenados, auditables, gobernados, extraíbles y reproducibles.                   |

## 0.3 Línea doctrinal

> **SICO.CA:** industria solo si es sostenible; competición solo si es generativa y regenerativa; algoritmos solo si son rendidores de cuentas.

---

# 1. Arquitectura del Marco y Principios Estructurales

## 1.1 Diagrama de acoplamiento

El flujo de información es **cerrado y bidireccional**:

```text
                ┌─────────────────────────────────────────────┐
                │           CAPA FÍSICA (L1)                   │
                │  GR (marco conceptual) → EBM 0-D (operativo) │
                │  Q_anth(t), T_s(t), forzamiento neto         │
                └───────────────┬─────────────────────────────┘
                                │  flujos físicos (W/m²)
                                ▼
                ┌─────────────────────────────────────────────┐
                │      PUENTE TERMODINÁMICO (L2)               │
                │  X_ext = forzamiento antropogénico / F_ref   │
                │  R_cap = (sumideros + margen radiativo)/F_ref│
                └───────────────┬─────────────────────────────┘
                                │  X_ext, R_cap
                                ▼
                ┌─────────────────────────────────────────────┐
                │   PUERTA SICO.CA con retardo e histéresis    │
                │  deuda regenerativa D_reg + latch h          │
                │  χ(t) ∈ (0, 1]                               │
                └───────────────┬─────────────────────────────┘
                                │  χ(t)
                                ▼
                ┌─────────────────────────────────────────────┐
                │   CAPA SOCIO-TÉCNICA (L3)                    │
                │  I_EU(t), E_tech(t), D_ID(t)  (acotadas)     │
                └───────────────┬─────────────────────────────┘
                                │  E_tech reduce Q_anth (descarbonización)
                                │  E_tech aumenta R_cap (sumideros ingenierizados)
                                └──────────► RETROALIMENTACIÓN a L1/L2
```

La novedad estructural respecto a `v0.2.0`: la flecha de retorno `E_tech → {Q_anth, R_cap}`. La eficacia tecnológica ya no crece en un vacío; **modifica el sistema físico que la autoriza**. La validación de §14 confirma que este bucle es **operativo, no decorativo**.

## 1.2 Principio de separación de escalas (justifica la corrección del tensor)

La potencia primaria antropogénica agregada es del orden de `~2×10¹³ W`. La radiación solar absorbida por el sistema Tierra es `~1.2×10¹⁷ W`. La contribución de cualquiera de las dos a la **curvatura del espacio-tiempo** (`~Gm/c²r`) es despreciable en decenas de órdenes de magnitud.

**Conclusión operativa:** el término antropogénico **no es una fuente de curvatura** y se elimina de las ecuaciones de campo. Donde sí es físicamente real es en el **balance energético atmosférico**, comparado contra el desbalance radiativo (escala `~W/m²`). Allí, y solo allí, entra como `Q_anth`.

## 1.3 Estatuto epistémico de cada bloque

| Bloque                              | Estatuto             | Papel computacional                       |
| :---------------------------------- | :------------------- | :---------------------------------------- |
| Relatividad general (§2)            | Marco conceptual     | Fija la lógica de conservación. No computa directamente. |
| Balance energético 0-D / EBM (§3)   | **Físico riguroso**  | **Carga el cálculo.** Genera `Q_anth`, `T_s`, forzamiento. |
| Transferencia radiativa (§4)        | Físico estándar      | Define la emisividad/absorción del EBM.   |
| Puente termodinámico (§5)           | Definicional         | Convierte flujos físicos en `X_ext`, `R_cap`. |
| Puerta SICO.CA (§6)                 | Doctrinal-dinámico   | Acopla L2 con L3.                          |
| Sistema socio-técnico (§8)          | Dinámica de sistemas | Genera trayectorias institucionales.      |
| Validación por simulación (§14)     | **Empírico-numérico**| **Confirma el comportamiento del modelo.**|
| Apéndice A (acoplamientos cosmológicos / materia oscura) | **Especulativo, no validado** | Fenced. Fuera del modelo operativo. |

---

# 2. Capa Física I — Relatividad General como Marco de Conservación

La relatividad general entra como **marco conceptual de límite físico**, mediante las ecuaciones de campo de Einstein con la constante cosmológica en el lado geométrico:

$$
G_{\mu\nu} + \Lambda g_{\mu\nu} = \frac{8\pi G}{c^4}\, T_{\mu\nu}
$$

`Λ` aparece **una sola vez**, en el lado geométrico. No se vuelve a contar como término dentro del tensor energía-momento. El doble conteo de la energía oscura queda eliminado.

## 2.1 Descomposición del tensor energía-momento

$$
T_{\mu\nu} = T_{\mu\nu}^{\mathrm{fluid}} + T_{\mu\nu}^{\mathrm{rad}} + T_{\mu\nu}^{\mathrm{dm}}
$$

| Término                       | Descripción                                              |
| :---------------------------- | :------------------------------------------------------- |
| $T_{\mu\nu}^{\mathrm{fluid}}$ | Materia bariónica, fluidos, atmósferas y medios continuos |
| $T_{\mu\nu}^{\mathrm{rad}}$   | Radiación electromagnética y campos radiativos            |
| $T_{\mu\nu}^{\mathrm{dm}}$    | Contribución efectiva de materia oscura                   |

Se elimina $T_{\mu\nu}^{\mathrm{anth}}$ del tensor (separación de escalas, §1.2) y se elimina $T_{\mu\nu}^{\Lambda}$ del tensor (la energía oscura es geométrica, lado izquierdo).

La conservación general se mantiene:

$$
\nabla_{\mu} T^{\mu\nu} = 0, \qquad \nabla_{\mu}\big(\Lambda g^{\mu\nu}\big) = 0
$$

la segunda identidad es trivial porque $\nabla_{\mu} g^{\mu\nu} = 0$.

> Lectura conceptual: la gravedad no lee una masa escalar aislada, sino la configuración tensorial completa del contenido energético. Esta intuición fija el lenguaje de conservación del marco; **el cómputo operativo lo realiza la reducción de balance energético de §3.**

---

# 3. Capa Física II — Modelo de Balance Energético (EBM 0-D)

Esta es la **reducción físicamente rigurosa y computacionalmente activa** del marco. Es un modelo de balance energético global de orden cero, en la tradición Budyko–Sellers, dimensionalmente cerrado.

## 3.1 Ecuación de balance

$$
C_{\mathrm{eff}}\,\frac{dT_s}{dt} = \underbrace{\frac{S_0}{4}\big(1 - A_{\mathrm{alb}}\big)}_{\text{solar absorbido}} \;-\; \underbrace{\epsilon\,\sigma\,T_s^{4}}_{\text{OLR}} \;+\; Q_{\mathrm{anth}}(t)
$$

| Símbolo            | Descripción                                | Valor de referencia                |
| :----------------- | :----------------------------------------- | :--------------------------------- |
| $C_{\mathrm{eff}}$ | Capacidad calorífica efectiva (capa de mezcla) | $\sim 4\times10^{8}\ \mathrm{J\,m^{-2}\,K^{-1}}$ |
| $S_0$              | Constante solar                            | $1361\ \mathrm{W\,m^{-2}}$         |
| $A_{\mathrm{alb}}$ | Albedo planetario                          | $0.30$                             |
| $\epsilon$         | Emisividad efectiva                        | $0.61$ (calibra $T_{eq}\approx 288\ \mathrm{K}$) |
| $\sigma$           | Constante de Stefan–Boltzmann              | $5.670\times10^{-8}\ \mathrm{W\,m^{-2}\,K^{-4}}$ |
| $Q_{\mathrm{anth}}$| Forzamiento antropogénico neto             | $0$–$3.5\ \mathrm{W\,m^{-2}}$      |

**Verificación numérica (§14.5):** con $T_s = 287.5\ \mathrm{K}$, el solar absorbido = $238.175\ \mathrm{W\,m^{-2}}$, la OLR = $236.316\ \mathrm{W\,m^{-2}}$, y para $E_{\mathrm{tech}}=0.15$, $\Theta=0.8$ el flujo neto = $3.953\ \mathrm{W\,m^{-2}}$ con $dT_s/dt = 0.3119\ \mathrm{K/año}$. Coincide con la implementación al cuarto decimal.

**Símbolos previamente huérfanos, ahora activos:** $A_{\mathrm{alb}}$ entra en el solar absorbido; la difusividad térmica $\kappa$ y el factor de escala cosmológico $a_{\mathrm{cosm}}$, $H(t)$ quedan **reservados** (Apéndice A).

## 3.2 Forzamiento antropogénico y su retroacoplamiento

$Q_{\mathrm{anth}}$ está **dominado por el forzamiento de gases de efecto invernadero** (reducción de OLR), con el calor residual directo como término menor:

$$
Q_{\mathrm{anth}}(t) = Q_0\,\Theta(t)\,\big(1 - \mu\, E_{\mathrm{tech}}(t)\big)
$$

| Símbolo      | Descripción                                                    |
| :----------- | :------------------------------------------------------------- |
| $Q_0$        | Forzamiento de referencia a plena actividad y tecnología nula  |
| $\Theta(t)$  | Índice de actividad industrial (exógeno o dinámico)            |
| $\mu$        | Efectividad de descarbonización por eficacia tecnológica       |
| $E_{\mathrm{tech}}$ | Eficacia tecnológica (variable socio-técnica, §8)       |

**Este es el primer canal de retroalimentación:** a mayor eficacia tecnológica, menor forzamiento antropogénico. La figura 1 (§14.1) muestra su efecto observable: la temperatura del escenario regenerativo **se dobla hacia abajo** al crecer $E_{\mathrm{tech}}$.

## 3.3 Linealización y tiempo de respuesta

Alrededor de la temperatura de referencia $T_0$, la OLR se linealiza:

$$
\epsilon\,\sigma\,T_s^{4} \approx F_0 + \lambda_{\mathrm{cl}}\,(T_s - T_0), \qquad \lambda_{\mathrm{cl}} = 4\,\epsilon\,\sigma\,T_0^{3} \approx 3.3\ \mathrm{W\,m^{-2}\,K^{-1}}
$$

La respuesta de equilibrio a un forzamiento $Q_{\mathrm{anth}}$ es $\Delta T_{eq} = Q_{\mathrm{anth}} / \lambda_{\mathrm{cl}}$, con un tiempo característico $\tau = C_{\mathrm{eff}} / \lambda_{\mathrm{cl}} \approx 4$ años — consistente con la capa de mezcla oceánica.

## 3.4 Nota de reducción

La forma usada omite advección (es una reducción **difusiva/global de orden cero**). Una formulación compresible completa llevaría $\rho c_p(\partial_t T + \mathbf{u}\cdot\nabla T)$. La omisión es deliberada y declarada.

---

# 4. Transferencia Radiativa (Formulación Estándar)

La transferencia radiativa fija la emisividad/absorción del EBM. Se usa la forma **estándar**, sin acoplamientos no validados.

## 4.1 Ecuación clásica

$$
\frac{\partial I_{\nu}}{\partial s} = j_{\nu} - \alpha_{\nu}\, I_{\nu}
$$

Se elimina el término $f(F_{\mathrm{cosm}}, \rho_{\mathrm{dm}}, T, p)$. Los fotones no se acoplan directamente a la materia oscura; ese acoplamiento, si se desea explorar, vive **solo** en el Apéndice A.

## 4.2 Generalización relativista (correcta y conservada)

La intensidad invariante y su transporte sobre geodésicas nulas $\lambda$:

$$
\mathcal{I}_{\nu} = \frac{I_{\nu}}{\nu^{3}}, \qquad \frac{d\mathcal{I}_{\nu}}{d\lambda} = \mathcal{J}_{\nu} - \mathcal{A}_{\nu}\,\mathcal{I}_{\nu}
$$

| Símbolo             | Descripción                       |
| :------------------ | :-------------------------------- |
| $\mathcal{I}_{\nu}$ | Intensidad radiativa invariante   |
| $\lambda$           | Parámetro afín de la geodésica    |
| $\mathcal{J}_{\nu}$ | Emisión invariante                |
| $\mathcal{A}_{\nu}$ | Absorción invariante              |

$\mathcal{I}_{\nu} = I_{\nu}/\nu^3$ es el invariante de Liouville apropiado y el transporte geodésico es la generalización correcta en relatividad general.

---

# 5. Puente Termodinámico — Definición de `X_ext` y `R_cap`

Cierra la brecha de acoplamiento: `X_ext` y `R_cap` dejan de ser diales libres y se derivan de flujos físicos del EBM, todo en `W/m²` normalizado por una escala de referencia $F_{\mathrm{ref}}$.

## 5.1 Externalidad como forzamiento antropogénico normalizado

$$
X_{\mathrm{ext}}(t) = \frac{Q_{\mathrm{anth}}(t)}{F_{\mathrm{ref}}}
$$

donde $F_{\mathrm{ref}}$ es la escala de forzamiento compatible con un objetivo de política. Refinamiento opcional: añadir un término de producción de entropía irreversible $T_0\,\dot\Sigma_{\mathrm{irr}}$ (también en `W/m²`), declarado como extensión.

## 5.2 Capacidad regenerativa como flujo de restauración normalizado

$$
R_{\mathrm{cap}}(t) = \frac{1}{F_{\mathrm{ref}}}\Big[\;\Phi_{\mathrm{bio}}(t) \;+\; \underbrace{k_{\mathrm{tech}}\, E_{\mathrm{tech}}(t)}_{\text{sumideros ingenierizados}} \;+\; \Phi_{\mathrm{rad}}\;\Big]
$$

| Término                  | Descripción                                                       |
| :----------------------- | :---------------------------------------------------------------- |
| $\Phi_{\mathrm{bio}}$    | Flujo de sumidero biosférico/oceánico (forzamiento evitado/tiempo)|
| $k_{\mathrm{tech}}\,E_{\mathrm{tech}}$ | Remoción/eficiencia ingenierizada (CDR, eficiencia)     |
| $\Phi_{\mathrm{rad}}$    | Margen radiativo (capacidad de re-radiar, ligado a OLR y albedo)  |

**Verificación (§14.5):** con $E_{\mathrm{tech}}=0.15$, $\Theta=0.8$: $Q_{\mathrm{anth}}=2.094$, $X_{\mathrm{ext}}=0.698$, $R_{\mathrm{cap}}=0.792$. Coincide al milésimo.

**Segundo canal de retroalimentación:** la capacidad regenerativa **crece con la eficacia tecnológica**. Junto con §3.2 ($Q_{\mathrm{anth}}$ decrece con $E_{\mathrm{tech}}$), el sistema físico y el socio-técnico forman un bucle cerrado:

```text
E_tech ↑  ⇒  Q_anth ↓  y  R_cap ↑  ⇒  (X_ext − R_cap) ↓  ⇒  χ ↑  ⇒  E_tech puede crecer  (bucle virtuoso)
Θ ↑ con E_tech estancada  ⇒  Q_anth ↑  ⇒  deuda ↑  ⇒  χ ↓  ⇒  E_tech ↓  (bucle vicioso, posible trampa)
```

## 5.3 Sobrepaso (overshoot)

$$
\Delta(t) = \max\big(0,\; X_{\mathrm{ext}}(t) - R_{\mathrm{cap}}(t)\big)
$$

es la magnitud físicamente fundamentada que alimenta la puerta SICO.CA.

---

# 6. Función de Autorización SICO.CA — con Retardo e Histéresis

La puerta de `v0.2.0` era instantánea y suponía autocorrección contemporánea (optimista). Las retroalimentaciones reales de insostenibilidad son **retardadas, con umbral y políticamente mediadas**. Esta versión modela explícitamente esa persistencia, validada en §14.3.

## 6.1 Puerta instantánea (línea base, conservada como referencia)

$$
\chi_0(t) = \exp\!\big[-\lambda\,\Delta(t)\big]
$$

## 6.2 Componente con retardo — deuda regenerativa

Se introduce un **estado de deuda regenerativa** $D_{\mathrm{reg}}(t)$ que se acumula rápido bajo sobrepaso y se recupera lento:

$$
\frac{dD_{\mathrm{reg}}}{dt} = \Delta(t) - \rho\,D_{\mathrm{reg}}(t)
$$

con $\rho$ pequeño (recuperación lenta). Captura que el daño **no se corrige en el mismo instante** en que cesa la causa.

## 6.3 Componente con histéresis — latch de régimen

Un estado de régimen $h(t)\in[0,1]$ se enciende cuando la deuda supera $\theta_{\mathrm{on}}$ y solo se libera cuando cae por debajo de un umbral **más estricto** $\theta_{\mathrm{off}} < \theta_{\mathrm{on}}$ (Schmitt-trigger continuo):

$$
\theta_{\mathrm{eff}}(h) = \theta_{\mathrm{off}} + (\theta_{\mathrm{on}} - \theta_{\mathrm{off}})\,(1 - h)
$$

$$
\frac{dh}{dt} = \frac{1}{\tau_h}\Big[\,\varsigma\big(D_{\mathrm{reg}} - \theta_{\mathrm{eff}}(h)\big) - h\,\Big], \qquad \varsigma(z) = \frac{1}{1 + e^{-k\,z}}
$$

## 6.4 Puerta efectiva

$$
\boxed{\;\chi(t) = \exp\!\big[-\lambda\,D_{\mathrm{reg}}(t)\,\big(1 + \xi\,h(t)\big)\big]\;}
$$

| Símbolo               | Descripción                                          |
| :-------------------- | :--------------------------------------------------- |
| $\lambda$             | Fuerza de penalización                               |
| $\rho$                | Tasa de recuperación de la deuda (lenta)             |
| $\theta_{\mathrm{on}}, \theta_{\mathrm{off}}$ | Umbrales de histéresis (encendido/apagado) |
| $\tau_h$              | Escala temporal del latch                            |
| $\xi$                 | Amplificación de la penalización cuando el latch está activo |
| $k$                   | Pendiente del smoothstep                             |

## 6.5 Corrección — el umbral de liberación es dinámico (snap), no $\theta_{\mathrm{off}}$ literal

**Esta es una corrección importante de `v1.1.0`, confirmada por la simulación (§14.3).** Una lectura ingenua diría: «la liberación requiere que $D_{\mathrm{reg}}$ caiga por debajo de $\theta_{\mathrm{off}}$». Los datos lo contradicen.

En el escenario de recuperación tardía, tras la intervención en el año 30:

| Evento                                   | Año     | $D_{\mathrm{reg}}$ en ese punto |
| :--------------------------------------- | :------ | :------------------------------ |
| Latch liberado ($h < 0.5$)               | 73.01   | **0.396**                       |
| Cruce de $\theta_{\mathrm{off}}=0.30$    | 78.56   | 0.300                           |

La liberación **precede** al cruce de $\theta_{\mathrm{off}}$ en ~5.5 años, y ocurre con $D_{\mathrm{reg}}\approx 0.40$, **por encima** de $\theta_{\mathrm{off}}$. La razón es el propio umbral móvil: cuando $h$ empieza a bajar desde 1, $\theta_{\mathrm{eff}}=\theta_{\mathrm{off}}+(\theta_{\mathrm{on}}-\theta_{\mathrm{off}})(1-h)$ **sube**, lo que empuja el target hacia abajo y acelera la caída de $h$. Es una **retroalimentación positiva que hace que la liberación "chasquee"** (snap):

```text
inicio de liberación   : D_reg ≈ 0.68   (h se despega de 1)
media liberación (h=0.5): D_reg ≈ 0.40   (año 73.01)
liberación completa     : D_reg ≈ 0.30   (≈ theta_off, recuperación plena de χ, año 78.56)
```

**Formulación correcta:** la activación ocurre en $D_{\mathrm{reg}}\approx\theta_{\mathrm{on}}$; la liberación es un **proceso de chasquido entre $\theta_{\mathrm{on}}$ y $\theta_{\mathrm{off}}$**, con $\theta_{\mathrm{off}}$ marcando la recuperación **plena** de la licencia, no el instante de liberación. El umbral de liberación efectivo es una cantidad **dinámica** (~0.40–0.68), no $\theta_{\mathrm{off}}$.

> Supuesto declarado: la pérdida de licencia operativa es **persistente, asimétrica y no autocorrectiva en el corto plazo**. La asimetría medida (§14.3): ~6 años para activar el latch; ~43 años desde la intervención para liberarlo. **La licencia SICO.CA es memoria con coste asimétrico.**

---

# 7. Variables Controladas

Para evitar colisiones simbólicas, las variables se separan por capa. **Todas las listadas se usan en alguna ecuación.**

## 7.1 Variables físicas (activas)

| Símbolo               | Descripción                          |
| :-------------------- | :----------------------------------- |
| $T_s(t)$              | Temperatura superficial (estado EBM) |
| $S_0$                 | Constante solar                      |
| $A_{\mathrm{alb}}$    | Albedo planetario                    |
| $\epsilon$            | Emisividad efectiva                  |
| $\sigma$              | Constante de Stefan–Boltzmann        |
| $C_{\mathrm{eff}}$    | Capacidad calorífica efectiva        |
| $\lambda_{\mathrm{cl}}$ | Retroalimentación de Planck         |
| $Q_{\mathrm{anth}}(t)$| Forzamiento antropogénico neto       |
| $\mathcal{I}_{\nu}$   | Intensidad radiativa invariante      |

## 7.2 Variables del puente termodinámico

| Símbolo               | Descripción                          |
| :-------------------- | :----------------------------------- |
| $X_{\mathrm{ext}}(t)$ | Externalidad normalizada             |
| $R_{\mathrm{cap}}(t)$ | Capacidad regenerativa normalizada   |
| $\Delta(t)$           | Sobrepaso                            |
| $F_{\mathrm{ref}}$    | Escala de forzamiento de referencia  |
| $D_{\mathrm{reg}}(t)$ | Deuda regenerativa acumulada         |
| $h(t)$                | Estado de régimen (histéresis)       |
| $\theta_{\mathrm{eff}}(t)$ | Umbral efectivo (móvil)         |
| $\chi(t)$             | Factor de autorización SICO.CA       |

## 7.3 Variables socio-técnicas (acotadas en $[0,1]$)

| Símbolo                 | Descripción                                  |
| :---------------------- | :------------------------------------------- |
| $I_{\mathrm{EU}}(t)$    | Integración institucional europea            |
| $E_{\mathrm{tech}}(t)$  | Eficacia tecnológica                         |
| $D_{\mathrm{ID}}(t)$    | Adopción de identidad digital                |
| $C(t)$                  | Cooperación bilateral/multilateral           |
| $R(t)$                  | Armonización regulatoria                     |
| $A_{\mathrm{inst}}(t)$  | Apoyo institucional y financiero             |
| $U(t)$                  | Implementación tecnológica                   |
| $A_{\mathrm{adopt}}(t)$ | Adopción base                                |
| $S(t)$                  | Seguridad criptográfica                      |
| $\Theta(t)$             | Actividad industrial (entrada; estado solo en la extensión experimental §14.4) |

## 7.4 Símbolos reservados (no activos en el modelo operativo)

$a_{\mathrm{cosm}}(t)$, $H(t)$, $\Lambda$, $\rho_{\mathrm{dm}}$, $\kappa$ — reservados para extensiones físicas; ver Apéndice A.

---

# 8. Sistema Socio-Técnico Acoplado (Acotado por Construcción)

Las tres variables son **acotadas en $[0,1]$ por construcción** (factores de saturación $(1-x)$ y decaimiento), eliminando la necesidad del recorte `np.clip` que enmascaraba el sobrepaso en `v0.2.0`.

$$
\begin{aligned}
\frac{dI_{\mathrm{EU}}}{dt} &= \big(aC + bR + cA_{\mathrm{inst}} + d\big)\,(1 - I_{\mathrm{EU}}) + \kappa_{EI}\,E_{\mathrm{tech}}\,(1 - I_{\mathrm{EU}}) - \gamma_I\,I_{\mathrm{EU}} \\[8pt]
\frac{dE_{\mathrm{tech}}}{dt} &= \chi(t)\,\eta_E\,\big(U A_{\mathrm{adopt}}\big)^{\alpha}\,I_{\mathrm{EU}}^{\beta}\,(1 - E_{\mathrm{tech}}) + \kappa_{DE}\,D_{\mathrm{ID}}\,(1 - E_{\mathrm{tech}}) - \delta_E\,E_{\mathrm{tech}} \\[8pt]
\frac{dD_{\mathrm{ID}}}{dt} &= \sigma_D\left[\frac{1}{1 + e^{-(u I_{\mathrm{EU}} + v S + w E_{\mathrm{tech}} + x)}} - D_{\mathrm{ID}}\right]
\end{aligned}
$$

| Ecuación                | Lectura                                                                                       |
| :---------------------- | :-------------------------------------------------------------------------------------------- |
| $dI_{\mathrm{EU}}/dt$   | La integración crece con cooperación, regulación, apoyo y eficacia, saturando hacia 1; decae por fricción. |
| $dE_{\mathrm{tech}}/dt$ | La eficacia crece solo si SICO.CA autoriza ($\chi$), satura hacia 1; **reduce $Q_{\mathrm{anth}}$ y eleva $R_{\mathrm{cap}}$ (§3.2, §5.2).** |
| $dD_{\mathrm{ID}}/dt$   | La identidad digital relaja hacia un objetivo logístico acotado en $[0,1]$ por construcción.  |

**Nota de diseño sobre el gate (relevante para §14.4):** $\chi$ multiplica **solo el término de crecimiento primario** de $dE_{\mathrm{tech}}/dt$ y $dI_{\mathrm{EU}}/dt$. Los canales cruzados $\kappa_{DE}\,D_{\mathrm{ID}}$ y $\kappa_{EI}\,E_{\mathrm{tech}}$ **no están estrangulados** por la puerta. En consecuencia, una puerta cerrada ($\chi\approx 0$) no congela del todo a $E_{\mathrm{tech}}$: persiste una "fuga de momento institucional". Es una decisión de diseño legítima (la inercia digital persiste aunque se revoque la licencia primaria) que debe **declararse**, porque afecta a la forma de la separatriz (§14.4).

El **vector de estado del marco integrado** es:

$$
\mathbf{y}(t) = \big[\,I_{\mathrm{EU}},\; E_{\mathrm{tech}},\; D_{\mathrm{ID}},\; T_s,\; D_{\mathrm{reg}},\; h\,\big]
$$

un sistema **físico + socio-técnico genuinamente acoplado**. La extensión experimental de §14.4 añade $\Theta$ como séptimo estado.

---

# 9. Bucles de Retroalimentación (incluyendo físico ↔ social)

| Bucle                                                                       | Mecanismo                                                       | Efecto sistémico                       |
| :-------------------------------------------------------------------------- | :------------------------------------------------------------- | :------------------------------------- |
| $I_{\mathrm{EU}} \leftrightarrow E_{\mathrm{tech}}$                         | Integración habilita innovación; innovación acelera integración | Crecimiento acumulativo o estancamiento |
| $I_{\mathrm{EU}} \rightarrow D_{\mathrm{ID}} \rightarrow E_{\mathrm{tech}}$ | Identidad digital mejora interoperabilidad y despliegue         | Transición hacia adopción masiva       |
| **$E_{\mathrm{tech}} \rightarrow Q_{\mathrm{anth}} \downarrow$**            | **Descarbonización (canal físico, §3.2)**                       | **Reduce externalidad medida**         |
| **$E_{\mathrm{tech}} \rightarrow R_{\mathrm{cap}} \uparrow$**               | **Sumideros ingenierizados (canal físico, §5.2)**               | **Eleva capacidad regenerativa**       |
| **$\Delta \rightarrow D_{\mathrm{reg}} \rightarrow \chi \downarrow$**       | **Deuda regenerativa retardada (§6)**                           | **Pérdida persistente de licencia**    |

Los tres últimos bucles son los que la validación de §14 confirma como **operativos**.

---

# 10. Implementación Numérica Reproducible

Se usa `scipy.integrate.solve_ivp` (RK45, tolerancias explícitas). La deuda y el latch se **integran como estado**. No hay recorte: las variables son acotadas por construcción.

## 10.1 Constantes físicas (FIJAS, no estimadas)

```python
from __future__ import annotations
import hashlib
import json
from dataclasses import dataclass, asdict, field
from typing import Callable, Dict

import numpy as np
from scipy.integrate import solve_ivp

SEC_PER_YEAR = 3.155693e7  # s/yr (unidad de tiempo del modelo = año)


@dataclass(frozen=True)
class PhysicalConstants:
    """Constantes físicas fijadas desde literatura. NO son parámetros libres."""
    S0: float = 1361.0              # W/m^2  constante solar
    albedo: float = 0.30            # -      albedo planetario
    epsilon: float = 0.61           # -      emisividad efectiva (T_eq ~ 288 K)
    sigma: float = 5.670374419e-8   # W/m^2/K^4  Stefan-Boltzmann
    C_eff: float = 4.0e8            # J/m^2/K   capacidad calorifica (capa de mezcla)
    F_ref: float = 3.0              # W/m^2  escala de forzamiento de referencia
    T_ref: float = 288.0            # K      temperatura de referencia
```

## 10.2 Parámetros del modelo (físicos + socio-técnicos + puerta)

```python
@dataclass
class Parameters:
    pc: PhysicalConstants = field(default_factory=PhysicalConstants)

    # --- socio-tecnicos ---
    a: float = 0.05;  b: float = 0.08;  c: float = 0.04;  d: float = 0.01
    alpha: float = 0.60;  beta: float = 0.40
    u: float = 1.20;  v: float = 0.80;  w: float = 1.00;  x: float = -2.50
    gamma_I: float = 0.02;  delta_E: float = 0.03;  sigma_D: float = 0.10
    kappa_EI: float = 0.02;  kappa_DE: float = 0.015;  eta_E: float = 0.50

    # --- retroacoplamiento fisico ---
    Q0: float = 3.0       # W/m^2  forzamiento a plena actividad, tecnologia nula
    mu: float = 0.85      # -      efectividad de descarbonizacion via E_tech
    k_tech: float = 2.5   # W/m^2  ganancia de flujo regenerativo por E_tech
    Phi_bio: float = 1.5  # W/m^2  sumidero biosferico base
    Phi_rad: float = 0.5  # W/m^2  margen radiativo

    # --- puerta / deuda / histeresis ---
    lam: float = 1.0          # fuerza de penalizacion
    rho: float = 0.05         # tasa de recuperacion de deuda (lenta)
    theta_on: float = 0.80    # umbral de encendido del latch
    theta_off: float = 0.30   # umbral de apagado (histeresis)
    tau_h: float = 2.0        # escala temporal del latch
    xi: float = 1.50          # amplificacion de penalizacion con latch activo
    k_steep: float = 12.0     # pendiente del smoothstep
```

## 10.3 Puente termodinámico y puerta

```python
def smoothstep(z: float, k: float) -> float:
    return 1.0 / (1.0 + np.exp(-k * z))


def anthropogenic_forcing(E_tech: float, activity: float, p: Parameters) -> float:
    """Q_anth(t) = Q0 * actividad * (1 - mu * E_tech), acotado a >= 0."""
    return p.Q0 * activity * max(0.0, 1.0 - p.mu * E_tech)


def externality(E_tech: float, activity: float, p: Parameters) -> float:
    """X_ext = Q_anth / F_ref."""
    return anthropogenic_forcing(E_tech, activity, p) / p.pc.F_ref


def regen_capacity(E_tech: float, p: Parameters) -> float:
    """R_cap = (Phi_bio + k_tech*E_tech + Phi_rad) / F_ref."""
    return (p.Phi_bio + p.k_tech * E_tech + p.Phi_rad) / p.pc.F_ref


def authorization_gate(D_reg: float, h: float, p: Parameters) -> float:
    """chi = exp(-lam * D_reg * (1 + xi*h)). Retardo (D_reg) + histeresis (h)."""
    return float(np.exp(-p.lam * D_reg * (1.0 + p.xi * h)))
```

## 10.4 Campo vectorial del sistema acoplado

```python
def derivatives(t: float, y: np.ndarray, p: Parameters,
                inputs: Dict[str, Callable[[float], float]]) -> np.ndarray:
    """y = [I_EU, E_tech, D_ID, T_s, D_reg, h]."""
    I_EU, E_tech, D_ID, T_s, D_reg, h = y

    C       = inputs["C"](t)
    R       = inputs["R"](t)
    A_inst  = inputs["A_inst"](t)
    U       = inputs["U"](t)
    A_adopt = inputs["A_adopt"](t)
    S       = inputs["S"](t)
    activity = inputs["activity"](t)

    # --- puente termodinamico ---
    X  = externality(E_tech, activity, p)
    Rc = regen_capacity(E_tech, p)
    overshoot = max(0.0, X - Rc)
    chi = authorization_gate(D_reg, h, p)

    # --- socio-tecnico (acotado en [0,1] por construccion) ---
    dI = ((p.a * C + p.b * R + p.c * A_inst + p.d) * (1.0 - I_EU)
          + p.kappa_EI * E_tech * (1.0 - I_EU)
          - p.gamma_I * I_EU)

    base = p.eta_E * (U * A_adopt) ** p.alpha * max(I_EU, 0.0) ** p.beta
    dE = (chi * base * (1.0 - E_tech)
          + p.kappa_DE * D_ID * (1.0 - E_tech)
          - p.delta_E * E_tech)

    z = p.u * I_EU + p.v * S + p.w * E_tech + p.x
    target_D = 1.0 / (1.0 + np.exp(-z))
    dD_ID = p.sigma_D * (target_D - D_ID)

    # --- fisico (EBM 0-D, con conversion a por-anio) ---
    Q_anth = anthropogenic_forcing(E_tech, activity, p)
    absorbed = p.pc.S0 / 4.0 * (1.0 - p.pc.albedo)
    OLR = p.pc.epsilon * p.pc.sigma * T_s ** 4
    dT = (absorbed - OLR + Q_anth) * SEC_PER_YEAR / p.pc.C_eff

    # --- deuda regenerativa (rapida acumulacion, lenta recuperacion) ---
    dD_reg = overshoot - p.rho * D_reg

    # --- latch de histeresis (umbral dependiente del estado) ---
    thr_eff = p.theta_off + (p.theta_on - p.theta_off) * (1.0 - h)
    h_target = smoothstep(D_reg - thr_eff, p.k_steep)
    dh = (h_target - h) / p.tau_h

    return np.array([dI, dE, dD_ID, dT, dD_reg, dh], dtype=float)
```

## 10.5 Integración reproducible

```python
def run(p: Parameters, y0: np.ndarray, t_end: float,
        inputs: Dict[str, Callable[[float], float]], n_eval: int = 1500):
    t_eval = np.linspace(0.0, t_end, n_eval)
    sol = solve_ivp(
        fun=lambda t, y: derivatives(t, y, p, inputs),
        t_span=(0.0, t_end),
        y0=y0,
        method="RK45",
        t_eval=t_eval,
        rtol=1e-8,
        atol=1e-10,
        dense_output=True,
    )
    return sol
```

---

# 11. Escenario Determinista de Simulación

```python
inputs = {
    "C":       lambda t: 0.50 + 0.10 * np.sin(0.02 * t),
    "R":       lambda t: 0.60 + 0.05 * t / 150.0,
    "A_inst":  lambda t: 0.40 + 0.10 * (1.0 - np.exp(-0.02 * t)),
    "U":       lambda t: 0.70 + 0.20 * (1.0 - np.exp(-0.03 * t)),
    "A_adopt": lambda t: 0.50 + 0.15 * (1.0 - np.exp(-0.025 * t)),
    "S":       lambda t: 0.80,
    "activity": lambda t: 0.80 + 0.20 * (1.0 - np.exp(-0.02 * t)),
}

p = Parameters()
y0 = np.array([0.20, 0.15, 0.10, 287.5, 0.0, 0.0])  # [I_EU, E_tech, D_ID, T_s, D_reg, h]
sol = run(p, y0, t_end=150.0, inputs=inputs)
I_EU, E_tech, D_ID, T_s, D_reg, h = sol.y
```

---

# 12. Calibración e Identificabilidad

Con ~20 parámetros y solo tres trayectorias agregadas observables, el sistema socio-técnico es **prácticamente no identificable** sin restricciones. Esta sección lo aborda de frente.

## 12.1 Jerarquía de fijación de parámetros

| Clase                       | Parámetros                                              | Tratamiento                                  |
| :-------------------------- | :------------------------------------------------------ | :------------------------------------------- |
| **Constantes físicas**      | $S_0, \sigma, \epsilon, A_{\mathrm{alb}}, C_{\mathrm{eff}}, \lambda_{\mathrm{cl}}$ | **Fijas** desde literatura. No se estiman.  |
| **Magnitudes de forzamiento/sumidero** | $Q_0, \Phi_{\mathrm{bio}}, \Phi_{\mathrm{rad}}, F_{\mathrm{ref}}$ | Fijas desde datasets observacionales (GCB, IPCC AR6). |
| **Acoplamientos físico-sociales** | $\mu, k_{\mathrm{tech}}$                          | Estimables con prior fuerte.                 |
| **Coeficientes socio-técnicos** | $a,b,c,d,\alpha,\beta,\gamma_I,\delta_E,\eta_E,\kappa_{EI},\kappa_{DE}$ | Conjunto reducido estimable; el resto fijo desde prior. |
| **Logística de identidad**  | $u,v,w,x,\sigma_D$                                      | Estimables (curva de adopción observable).   |
| **Puerta**                  | $\lambda,\rho,\theta_{\mathrm{on}},\theta_{\mathrm{off}},\tau_h,\xi$ | Fijados por elicitación de política + análisis de sensibilidad. |

## 12.2 Riesgo de equifinalidad

Múltiples combinaciones de coeficientes socio-técnicos producen trayectorias indistinguibles. **No se debe prometer "todo coeficiente trazable" sin antes demostrar que es recuperable.** Estrategia mínima:

1. **Identificabilidad estructural** — qué combinaciones aparecen solo como producto (p. ej. $\eta_E$ y las elasticidades).
2. **Identificabilidad práctica** — perfil de verosimilitud por parámetro.
3. **Sensibilidad global** — índices de Sobol.
4. **Inferencia bayesiana** — priors informativos + comprobaciones predictivas posteriores.
5. **Veredicto por parámetro** — `identificable`, `débilmente identificable` o `fijado-desde-prior` en el registro de auditoría.

## 12.3 Registro de auditoría

```python
def audit_record(p: Parameters, y0: np.ndarray, t_end: float,
                 inputs: Dict[str, Callable[[float], float]]) -> dict:
    param_blob = json.dumps(asdict(p), sort_keys=True).encode()
    input_grid = np.linspace(0.0, t_end, 1500)
    input_blob = json.dumps(
        {k: [float(f(t)) for t in input_grid] for k, f in inputs.items()},
        sort_keys=True,
    ).encode()
    return {
        "model_id": "AMPEL-SICOCA-COUPLED-003",
        "version": "1.1.0",
        "integrator": "scipy.solve_ivp / RK45",
        "rtol": 1e-8, "atol": 1e-10,
        "time_span": [0.0, t_end],
        "state_vars": ["I_EU", "E_tech", "D_ID", "T_s", "D_reg", "h"],
        "y0": [float(v) for v in y0],
        "parameter_set_sha256": hashlib.sha256(param_blob).hexdigest(),
        "input_series_sha256": hashlib.sha256(input_blob).hexdigest(),
        "physical_constants_sha256":
            hashlib.sha256(json.dumps(asdict(p.pc), sort_keys=True).encode()).hexdigest(),
        "identifiability_verdicts": "see §12.2 — per-parameter table required",
    }
```

---

# 13. Escenarios de Simulación (Catálogo)

| Escenario                    | Mecanismo                                            | Resultado esperado                                 |
| :--------------------------- | :--------------------------------------------------- | :------------------------------------------------- |
| Baseline                     | Continuidad de tendencias                            | Crecimiento moderado, deuda regenerativa contenida |
| Regenerativo                 | $E_{\mathrm{tech}}$ alta temprano                    | $Q_{\mathrm{anth}}\downarrow$, $R_{\mathrm{cap}}\uparrow$, $\chi\approx 1$, bucle virtuoso |
| Trampa de insostenibilidad   | Actividad alta + tecnología estancada                | Deuda supera $\theta_{\mathrm{on}}$, latch activo, $\chi\downarrow$, **bloqueo persistente** |
| Estrés energético            | $Q_0$ elevado                                        | Penalización con retardo; recuperación lenta       |
| Ciberataque                  | Caída abrupta de $S(t)$                              | Caída de $D_{\mathrm{ID}}$ y de eficacia           |
| Fragmentación regulatoria    | $R(t), C(t)\downarrow$                               | Estancamiento de integración                       |
| Recuperación tardía          | Tecnología mejora tras activar el latch              | **Histéresis:** liberación tardía, asimétrica      |

Los escenarios Regenerativo, Trampa y Recuperación tardía se ejecutan y validan en §14.

---

# 14. Validación por Simulación

Esta sección presenta las simulaciones que ejecutan el modelo de la especificación y confirman su comportamiento. Las figuras y los datos acompañan a este documento.

**Aclaración metodológica.** Los tres escenarios (A regenerativo, B trampa, C recuperación tardía) usan el **modelo reducido** (estados $T_s$, $D_{\mathrm{reg}}$, $h$) con $E_{\mathrm{tech}}(t)$ y $\Theta(t)$ **prescritas** como funciones de escenario, para aislar la capa física + puerta. La sección de cuenca (§14.4) usa el **sistema completo con actividad endógena** (extensión experimental). Las verificaciones base (§14.5) reproducen los valores de la especificación al tercer–cuarto decimal.

## 14.1 Trayectorias térmicas — el bucle cerrado es observable

<img width="640" height="480" alt="fig_01_temperature_trajectories" src="https://github.com/user-attachments/assets/52ab74dd-c4b8-4af8-bf86-ddcdf3d68427" />


*Figura 1. Temperatura superficial $T_s$ (EBM 0-D) para los escenarios regenerativo, trampa de insostenibilidad y recuperación tardía.*

Lectura:

- **Regenerativo (azul):** $T_s$ sube hasta un **pico de 288.62 K en el año 16.3** y luego **se dobla hacia abajo** hasta 288.44 K. Ese doblez es la **firma empírica del bucle cerrado**: al crecer $E_{\mathrm{tech}}$ (0.15 → 0.69), $Q_{\mathrm{anth}}$ cae y baja el equilibrio térmico. La curva que se dobla **emerge de la dinámica; no está impuesta**.
- **Trampa (naranja):** subida monótona hasta una meseta de 289.27 K — el forzamiento nunca se alivia porque la tecnología queda estancada.
- **Recuperación tardía (verde):** sigue la trampa hasta la intervención en el año 30, y luego **cae abruptamente** hacia ~288.24 K.

> Salvaguarda de interpretación: los valores absolutos de $T_s$ (287–289 K) provienen de un EBM global de orden cero con $\epsilon$ ajustada. **La señal con sentido es el $\Delta T$ y la forma** (el doblez en regenerativo, la meseta en trampa), no el valor absoluto.

## 14.2 Puerta de autorización — colapso vs recuperación tardía

<img width="640" height="480" alt="fig_02_authorization_gate" src="https://github.com/user-attachments/assets/f13b92e8-f7c2-4f48-8fa3-fe65a00c19fc" />


*Figura 2. Factor de autorización $\chi(t)$ de la puerta SICO.CA.*

Lectura:

- **Regenerativo (azul):** $\chi = 1$ durante toda la corrida. El sobrepaso $\Delta$ es nulo en todo momento: la operación se mantiene **dentro de la capacidad regenerativa** y la licencia nunca muerde.
- **Trampa (naranja):** $\chi$ **colapsa a ~0 hacia el año 12** y queda bloqueado (valor final $\sim 5\times10^{-13}$).
- **Recuperación tardía (verde):** $\chi$ colapsa junto con la trampa, permanece cerca de 0 hasta ~año 60, y luego **se recupera (snap)** cruzando 0.5 en el año 73 y alcanzando 0.99 hacia el año 150.

## 14.3 Liberación histerética — la asimetría medida

<img width="640" height="480" alt="fig_03_late_recovery_hysteresis" src="https://github.com/user-attachments/assets/40773f47-cc65-4b6b-baf6-fb47c64d4661" />


*Figura 3. Recuperación tardía: deuda regenerativa $D_{\mathrm{reg}}$, latch $h$ y umbral efectivo $\theta_{\mathrm{eff}}$.*

Lectura:

- $D_{\mathrm{reg}}$ (azul) **alcanza su pico de 3.40 en la intervención** (año 30) y luego decae exponencialmente.
- El latch $h$ (naranja) **se activa ($h\to 1$) hacia el año 6** y se mantiene hasta ~año 73.
- El umbral efectivo $\theta_{\mathrm{eff}}$ (verde) baja de 0.8 a 0.3 cuando $h=1$, y **chasquea de vuelta a 0.8** en la liberación.

**Eventos exactos (de los datos):**

| Evento                                | Año     |
| :------------------------------------ | :------ |
| Latch activado ($h \ge 0.5$)          | 6.23    |
| Intervención (actividad → 0.35)       | 30.02   |
| Latch liberado ($h < 0.5$)            | 73.01   |
| Cruce de $\theta_{\mathrm{off}}=0.30$ | 78.56   |

**Asimetría:** ~6 años para perder la licencia; ~43 años desde la intervención para recuperarla. La liberación (año 73, $D_{\mathrm{reg}}\approx 0.40$) **precede** al cruce de $\theta_{\mathrm{off}}$ (año 78.56), confirmando la corrección de §6.5: $\theta_{\mathrm{off}}$ marca la recuperación plena, no el instante de liberación. **La licencia SICO.CA es memoria con coste asimétrico.**

## 14.4 Sección de cuenca de atracción — la separatriz

![Figura 4 — Sección de cuenca en el plano de actividad inicial y E_tech inicial, clasificada en regenerativo, marginal y trampa](fig_04_basin_section.png)

*Figura 4. Sección 2D de la cuenca de atracción en el plano $(\Theta_0, E_{\mathrm{tech},0})$, clasificada por atractor: R = regenerativo, M = marginal, T = trampa.*

Lectura: la separatriz separa **baja actividad + suficiente $E_{\mathrm{tech}}$ → R** de **alta actividad + baja $E_{\mathrm{tech}}$ → T**.

**Declaraciones de diseño obligatorias:**

1. **Actividad endógena = extensión experimental.** Para esta sección, $\Theta$ se promueve a **séptimo estado** con una ley de evolución propia. Esto **no es núcleo `v1.0.0`**, donde $\Theta(t)$ era una señal de entrada. Marcado explícitamente como experimental.
2. **Sección, no cuenca completa.** La figura es una **sección 2D de una cuenca de dimensión superior**, tomada en $D_{\mathrm{reg},0}=0$, $h_0=0$. La misma pareja $(\Theta_0, E_{\mathrm{tech},0})$ puede caer en cuencas distintas según la **historia** de $D_{\mathrm{reg}}$ y $h$.
3. **Clasificación por atractor, no por foto.** Se integra largo y se etiqueta el destino (R: $\chi\to 1$, $D_{\mathrm{reg}}$ baja, $h\to 0$; T: $\chi\to 0$, $h\to 1$), no por un corte temporal que clasificaría mal trayectorias marginales lentas.
4. **Modo `faithful_v1`.** Se computó con `activity_gate_suppression = 0` y `gate_cross_channels = False`: la actividad no es suprimida por $\chi$, y los canales cruzados $\kappa_{DE},\kappa_{EI}$ no están estrangulados (§8). La fuga de momento institucional resultante puede dejar escapar trayectorias incluso con $\chi\approx 0$, y por tanto **modela la forma de la separatriz**.

**Modos de diseño de gobernanza (análisis de sensibilidad estructural):**

| Modo                          | Canales cruzados | Actividad bajo $\chi$ | Efecto esperado en la separatriz                          |
| :---------------------------- | :--------------- | :-------------------- | :-------------------------------------------------------- |
| `faithful_v1`                 | libres           | no                    | Línea base; fuga institucional permite escapes marginales |
| `strict_license`              | estrangulados    | no                    | Trampa más profunda; menos escapes; separatriz se desplaza hacia menor actividad |
| `activity_suppressed_by_chi`  | estrangulados    | sí                    | "Recuperación por contracción operativa"; muchas trampas se vuelven recuperables — **escenario de gobernanza, no físico** |

## 14.5 Datos y reproducibilidad

Conjuntos de datos adjuntos: `scenario_A_regenerative.csv`, `scenario_B_unsustainability_trap.csv`, `scenario_C_late_recovery.csv`, `basin_section.csv`.

**Verificaciones base (coinciden con la especificación):**

| Magnitud                    | Valor      | Esperado    |
| :-------------------------- | :--------- | :---------- |
| $Q_{\mathrm{anth}}$ (E=0.15, Θ=0.8) | 2.094 | 2.0940 |
| $X_{\mathrm{ext}}$          | 0.698      | 0.6980      |
| $R_{\mathrm{cap}}$          | 0.792      | 0.7917      |
| Solar absorbido             | 238.175    | 238.1750    |
| OLR ($T_s=287.5$)           | 236.316    | 236.3159    |
| Flujo neto                  | 3.953      | 3.9531      |
| $dT_s/dt$                   | 0.31187    | 0.311868    |

Cada corrida debe registrar el `audit_record` de §12.3 (hash de parámetros, entradas y constantes físicas).

---

# 15. Condiciones de Validez

1. **Consistencia dimensional** — todos los términos físicos en `W/m²`; el puente normaliza por $F_{\mathrm{ref}}$.
2. **Separación de capas** — variables físicas, de puente y socio-técnicas no se confunden.
3. **Reproducibilidad** — toda simulación repetible vía hash de parámetros, entradas y constantes.
4. **Auditabilidad** — cada parámetro con fuente, fecha, método, versión **y veredicto de identificabilidad**.
5. **Falsabilidad** — los coeficientes de acoplamiento físico-social ($\mu, k_{\mathrm{tech}}$) deben poder rechazarse empíricamente.
6. **No externalización irreversible** — ninguna operación transfiere daño no regenerable; codificado por la deuda persistente.
7. **Reducción a modelos estándar** — con $Q_{\mathrm{anth}}\to 0$, el EBM se reduce al balance radiativo de equilibrio; con $\chi\to 1$, el sistema socio-técnico se reduce a dinámica de difusión estándar.
8. **Separación de escalas** — lo antropogénico no entra en las ecuaciones de campo; solo en el balance energético.
9. **Gobernanza algorítmica** — algoritmos encadenados, explicables, extraíbles y contestables.

---

# 16. Originalidad y Posicionamiento (Declaración Honesta)

## 16.1 Componentes estándar (no nuevos)

| Componente                          | Linaje                                                  |
| :---------------------------------- | :------------------------------------------------------ |
| Ecuaciones de campo de Einstein     | Relatividad general clásica                             |
| Balance energético 0-D (EBM)        | Tradición Budyko–Sellers                                |
| Difusión logística de adopción      | Modelo de Bass / difusión de innovaciones               |
| Penalización exponencial de un lado | Métodos de barrera/penalización en optimización         |
| Histéresis de dos umbrales          | Schmitt-trigger / modelos de relé en sistemas dinámicos |
| Dinámica de sistemas acoplada       | Tradición Forrester                                     |

## 16.2 La contribución (dónde vive lo propio)

1. **Puerta de admisibilidad multiplicativa, físicamente fundamentada.** Sostenibilidad como **condición dinámica de admisibilidad** $\chi(t)$, con `X_ext` y `R_cap` **derivadas de un balance energético**, no postuladas.
2. **Bucle físico ↔ socio-técnico cerrado.** La eficacia tecnológica modifica el sistema físico que la autoriza — **validado** por el doblez térmico de la figura 1.
3. **Persistencia no autocorrectiva con liberación asimétrica.** Retardo (deuda) + histéresis (latch con umbral móvil) — **validado** por la asimetría 6 vs 43 años (§14.3).
4. **Provenance como ciudadano de primera clase.** Hashing de parámetros, entradas y constantes; veredictos de identificabilidad.

La doctrina `SICO.CA` da identidad coherente al conjunto. El posicionamiento correcto **antepone el núcleo de gobernanza-dinámica** y trata la relatividad general como marco conceptual.

---

# 17. Implicaciones Operativas

1. **Licencia de operación computable.** La puerta $\chi$ como criterio formal de admisibilidad, cableada a KPIs reales: `X_ext` desde contabilidad de emisiones/energía, `R_cap` desde métricas de regeneración. La validación muestra que es una **licencia con memoria**: revocarla es rápido; reganarla, lento.
2. **Enlace con ESG/CSRD.** El puente conecta con la maquinaria de reporte existente; más concreto que la mayoría de "marcos de sostenibilidad" porque es **una función con umbral**, no un eslogan.
3. **Mapa de cuencas como instrumento de política.** El resultado de mayor valor no es la separatriz en sí, sino **su sensibilidad paramétrica**: cuánta capacidad regenerativa ingenierizada ($k_{\mathrm{tech}}$) o descarbonización ($\mu$) hace falta para desplazar la separatriz de modo que un punto de partida realista deje de caer en la trampa. **Ese es el enunciado de política computable** que persigue el marco.

**Límites declarados:** la capa física, si se sobreextiende, invita al rechazo (de ahí el Apéndice A separado); la calibración puede ser irresoluble al nivel agregado; la actividad endógena de §14.4 es experimental; y los valores de $\epsilon, F_{\mathrm{ref}}, Q_0, \Phi_{\mathrm{bio}}, k_{\mathrm{tech}}$ son **marcadores plausibles, no datos**, hasta su fijación contra AR6 / Global Carbon Budget (§12.1).

---

# 18. Tesis Consolidada

## 18.1 Español

> **El Ampel Theoretical Framework define un espacio de estados físico y socio-técnico genuinamente acoplado, en el que las operaciones industriales solo son admisibles cuando sus externalidades —medidas como forzamiento físico neto sobre el balance energético— permanecen por debajo de una capacidad regenerativa medible. La simulación confirma que el acoplamiento es operativo: la eficacia tecnológica dobla la trayectoria térmica, y la licencia de autorización exhibe memoria asimétrica —rápida de perder, lenta de recuperar—. Un balance energético de orden cero proporciona la capa de límite físico operativa; la relatividad general fija el marco conceptual de conservación; un puente termodinámico convierte flujos físicos en externalidad y capacidad regenerativa; y una puerta con retardo e histéresis gobierna, de forma persistente y no autocorrectiva, la dinámica tecnológica, institucional e identitaria.**

## 18.2 English

> **The Ampel Theoretical Framework defines a genuinely coupled physical and socio-technical state-space in which industrial operations are admissible only when their externalities — measured as net physical forcing on the energy budget — remain below measurable regenerative capacity. Simulation confirms the coupling is operative: technological efficacy bends the thermal trajectory, and the authorization license exhibits asymmetric memory — fast to lose, slow to regain. A zero-dimensional energy-balance model provides the operational physical boundary layer; general relativity sets the conceptual conservation frame; a thermodynamic bridge converts physical fluxes into externality and regenerative capacity; and a lagged, hysteretic gate governs technological, institutional, and identity-system dynamics in a persistent, non-self-correcting manner.**

---

# 19. Fórmula Axial

```text
Physical boundary (operational):
  Zero-dimensional Energy Balance Model
  C_eff dT_s/dt = absorbed_solar - OLR + Q_anth

Conceptual frame:
  General Relativity — gravity sources from total stress-energy
  (anthropogenic energy is NOT a curvature source: scale separation)

Bridge:
  X_ext = Q_anth / F_ref
  R_cap = (Phi_bio + k_tech * E_tech + Phi_rad) / F_ref

Operational doctrine:
  SICO.CA = Sustainable Industrial Competitive Operations
            through Chained Algorithms

Governance rule (persistent, non-self-correcting, asymmetric):
  Regenerative debt accumulates fast, recovers slow;
  authorization latch releases via a moving threshold (snap),
  with full recovery only at theta_off.
  Measured asymmetry: ~6 yr to lose license, ~43 yr to regain.

Closed loop (validated):
  E_tech reduces Q_anth and raises R_cap -> bends the thermal trajectory.

Audit layer:
  Every coefficient, input, constant, scenario and figure
  is traceable, reproducible, contestable — with identifiability verdicts.
```

---

# Apéndice A — Extensiones Especulativas (No Validadas, Fuera del Modelo Operativo)

> **Advertencia:** este apéndice contiene acoplamientos físicos **no validados empíricamente**. Están separados deliberadamente para que su carácter especulativo no contamine el modelo operativo (§3–§10, §14), que es físicamente estándar.

A.1 **Acoplamiento cosmológico atmosférico.** Un término $Q_{\mathrm{cosm}}$ en el balance, con la condición de consistencia $Q_{\mathrm{cosm}}\to 0$ reduciéndose al EBM estándar. Variables reservadas: $a_{\mathrm{cosm}}(t), H(t), \Lambda$.

A.2 **Acoplamiento radiación–materia oscura.** Un término $\mathcal{F}_{\mathrm{coupling}}(\rho_{\mathrm{dm}}, g_{\mu\nu})$ en el transporte radiativo. Sin evidencia de acoplamiento directo fotón–materia oscura; hipótesis falsable.

A.3 **Producción de entropía irreversible.** Refinamiento de `X_ext` con $T_0\,\dot\Sigma_{\mathrm{irr}}$. Físicamente motivado pero requiere instrumentación específica.

A.4 **Actividad industrial endógena.** La ley dinámica de $\Theta$ usada en §14.4 es ilustrativa. Una versión defendible requiere una teoría de la demanda económica y de su estrangulamiento por la licencia, todavía no formalizada.

Cualquier promoción de A.1–A.4 al modelo operativo exige superar las condiciones de validez de §15.

---

# Changelog

## v1.1.0 (supersede v1.0.0)

- **NUEVO §14 — Validación por Simulación** con cuatro figuras (trayectorias térmicas, puerta de autorización, liberación histerética, sección de cuenca) y cuatro conjuntos de datos.
- **§6.5 — corrección del umbral de liberación dinámico (snap):** $\theta_{\mathrm{off}}$ no es el instante de liberación sino el umbral de **recuperación plena**; la liberación chasquea entre $\theta_{\mathrm{on}}$ y $\theta_{\mathrm{off}}$ por el umbral móvil $\theta_{\mathrm{eff}}(h)$. Confirmado: liberación en el año 73.01 con $D_{\mathrm{reg}}=0.396 > \theta_{\mathrm{off}}$.
- **Asimetría cuantificada:** ~6 años para activar el latch; ~43 años desde la intervención para liberarlo.
- **§14.4 — sección de cuenca documentada como extensión experimental** (actividad como séptimo estado endógeno); declaradas las salvaguardas de sección-2D-de-cuenca-superior y clasificación-por-atractor.
- **§14.4 — modos de diseño de gobernanza** (`faithful_v1` / `strict_license` / `activity_suppressed_by_chi`) como primer análisis de sensibilidad estructural.
- **§8 — declarada la nota de gate de canales cruzados** (fuga de momento institucional; canales $\kappa_{DE},\kappa_{EI}$ no estrangulados).
- **Verificaciones base confirmadas** al tercer–cuarto decimal contra la especificación.
- Renumeración: Validez §14→§15, Originalidad §15→§16, Implicaciones §16→§17, Tesis §17→§18, Axial §18→§19.

## v1.0.0 (supersede v0.2.0)

- Eliminado el doble conteo de $\Lambda$ (geométrico, lado izquierdo).
- Eliminado $T_{\mu\nu}^{\mathrm{anth}}$ de las ecuaciones de campo; añadido el principio de separación de escalas.
- Eliminado el acoplamiento radiación–materia oscura del transporte radiativo; especulativos al Apéndice A.
- Añadido el EBM de orden cero como reducción física operativa.
- Añadido el puente termodinámico que deriva `X_ext` y `R_cap` de flujos físicos.
- Añadido retroacoplamiento $E_{\mathrm{tech}}\to Q_{\mathrm{anth}}$ y $E_{\mathrm{tech}}\to R_{\mathrm{cap}}$.
- Puerta con retardo (deuda) e histéresis (dos umbrales) en lugar de la puerta instantánea.
- Dinámica socio-técnica acotada por construcción; eliminado el recorte `np.clip`.
- Euler explícito sustituido por `solve_ivp` (RK45); corregido el error off-by-one.
- Símbolos huérfanos activados; símbolos reservados etiquetados.
- Añadidas las secciones de identificabilidad y de originalidad.

---

# Línea Final

> **No more wars. Regeneration now. Industria solo si es sostenible. Competición solo si es regenerativa. Algoritmos solo si rinden cuentas — y la sostenibilidad, medida, no declarada.**
