---
document_id: AMPEL-THEORETICAL-FRAMEWORK-SICOCA-002
title: "Ampel Theoretical Framework — Capa de Límite Físico, Puente Termodinámico y Gobernanza SICO.CA"
version: "1.0.0"
status: controlled
supersedes: AMPEL-THEORETICAL-FRAMEWORK-SICOCA-GR-FLUIDS-001 (v0.2.0)
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
---

# Ampel Theoretical Framework
## Capa de Límite Físico, Puente Termodinámico y Gobernanza SICO.CA

El **Ampel Theoretical Framework** define una arquitectura sistémica en la que la física fundamental fija los límites materiales de la civilización, un **modelo de balance energético** traduce esos límites en magnitudes operativas medibles, y la gobernanza socio-técnica determina si las operaciones industriales permanecen dentro de dichos límites.

A diferencia de la versión `v0.2.0`, esta versión **acopla las tres capas matemáticamente**: las externalidades y la capacidad regenerativa que gobiernan la doctrina `SICO.CA` ya no son entradas libres, sino que se **derivan del balance energético físico** y **retroalimentan** la dinámica socio-técnica.

El marco conecta tres capas:

1. **Capa física** — relatividad general como marco conceptual de conservación; balance energético de orden cero (EBM) como reducción operativa; transferencia radiativa estándar.
2. **Capa de acoplamiento** — un puente termodinámico que define `X_ext` (externalidad) y `R_cap` (capacidad regenerativa) a partir de flujos físicos.
3. **Capa socio-técnica y doctrinal** — un sistema dinámico acotado con una **puerta de autorización `SICO.CA` con retardo e histéresis**.

La tesis central permanece, ahora computable:

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

A diferencia de la versión anterior, el flujo de información es **cerrado y bidireccional**:

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

La novedad estructural respecto a `v0.2.0`: la flecha de retorno `E_tech → {Q_anth, R_cap}`. La eficacia tecnológica ya no crece en un vacío; **modifica el sistema físico que la autoriza**.

## 1.2 Principio de separación de escalas (justifica la corrección del tensor)

La potencia primaria antropogénica agregada es del orden de `~2×10¹³ W`. La radiación solar absorbida por el sistema Tierra es `~1.2×10¹⁷ W`. La contribución de cualquiera de las dos a la **curvatura del espacio-tiempo** (`~Gm/c²r`) es despreciable en decenas de órdenes de magnitud.

**Conclusión operativa:** el término antropogénico **no es una fuente de curvatura** y se elimina de las ecuaciones de campo (corrección respecto a `v0.2.0`). Donde sí es físicamente real es en el **balance energético atmosférico**, comparado contra el desbalance radiativo (escala `~W/m²`). Allí, y solo allí, entra como `Q_anth`.

## 1.3 Estatuto epistémico de cada bloque

| Bloque                              | Estatuto             | Papel computacional                       |
| :---------------------------------- | :------------------- | :---------------------------------------- |
| Relatividad general (§2)            | Marco conceptual     | Fija la lógica de conservación. No computa directamente. |
| Balance energético 0-D / EBM (§3)   | **Físico riguroso**  | **Carga el cálculo.** Genera `Q_anth`, `T_s`, forzamiento. |
| Transferencia radiativa (§4)        | Físico estándar      | Define la emisividad/absorción del EBM.   |
| Puente termodinámico (§5)           | Definicional         | Convierte flujos físicos en `X_ext`, `R_cap`. |
| Puerta SICO.CA (§6)                 | Doctrinal-dinámico   | Acopla L2 con L3.                          |
| Sistema socio-técnico (§8)          | Dinámica de sistemas | Genera trayectorias institucionales.      |
| Apéndice A (acoplamientos cosmológicos / materia oscura) | **Especulativo, no validado** | Fenced. Fuera del modelo operativo. |

---

# 2. Capa Física I — Relatividad General como Marco de Conservación

La relatividad general entra como **marco conceptual de límite físico**, mediante las ecuaciones de campo de Einstein con la constante cosmológica en el lado geométrico:

$$
G_{\mu\nu} + \Lambda g_{\mu\nu} = \frac{8\pi G}{c^4}\, T_{\mu\nu}
$$

**Corrección respecto a `v0.2.0`:** `Λ` aparece **una sola vez**, en el lado geométrico. No se vuelve a contar como término dentro del tensor energía-momento. El doble conteo de la energía oscura queda eliminado.

## 2.1 Descomposición del tensor energía-momento

$$
T_{\mu\nu} = T_{\mu\nu}^{\mathrm{fluid}} + T_{\mu\nu}^{\mathrm{rad}} + T_{\mu\nu}^{\mathrm{dm}}
$$

| Término                       | Descripción                                              |
| :---------------------------- | :------------------------------------------------------- |
| $T_{\mu\nu}^{\mathrm{fluid}}$ | Materia bariónica, fluidos, atmósferas y medios continuos |
| $T_{\mu\nu}^{\mathrm{rad}}$   | Radiación electromagnética y campos radiativos            |
| $T_{\mu\nu}^{\mathrm{dm}}$    | Contribución efectiva de materia oscura                   |

**Corrección respecto a `v0.2.0`:** se elimina $T_{\mu\nu}^{\mathrm{anth}}$ del tensor (separación de escalas, §1.2) y se elimina $T_{\mu\nu}^{\Lambda}$ del tensor (la energía oscura es geométrica, lado izquierdo).

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

**Símbolos previamente huérfanos, ahora activos:** $A_{\mathrm{alb}}$ entra en el solar absorbido; la difusividad térmica $\kappa$ y el factor de escala cosmológico $a_{\mathrm{cosm}}$, $H(t)$ quedan **reservados** y marcados como tales (Apéndice A), no listados como si fueran maquinaria activa.

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

**Este es el primer canal de retroalimentación:** a mayor eficacia tecnológica, menor forzamiento antropogénico.

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

**Corrección respecto a `v0.2.0`:** se elimina el término $f(F_{\mathrm{cosm}}, \rho_{\mathrm{dm}}, T, p)$. Los fotones no se acoplan directamente a la materia oscura; ese acoplamiento, si se desea explorar, vive **solo** en el Apéndice A como extensión especulativa.

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

Esta parte se conserva de `v0.2.0` por ser correcta: $\mathcal{I}_{\nu} = I_{\nu}/\nu^3$ es el invariante de Liouville apropiado y el transporte geodésico es la generalización correcta en relatividad general.

---

# 5. Puente Termodinámico — Definición de `X_ext` y `R_cap`

**Esta sección es la novedad central de `v1.0.0`.** Cierra la brecha de acoplamiento: `X_ext` y `R_cap` dejan de ser diales libres y se derivan de flujos físicos del EBM, todo en unidades de `W/m²` normalizadas por una escala de referencia $F_{\mathrm{ref}}$.

## 5.1 Externalidad como forzamiento antropogénico normalizado

$$
X_{\mathrm{ext}}(t) = \frac{Q_{\mathrm{anth}}(t)}{F_{\mathrm{ref}}}
$$

donde $F_{\mathrm{ref}}$ es la escala de forzamiento compatible con un objetivo de política (p. ej. el forzamiento asociado a un objetivo térmico). Refinamiento opcional: añadir un término de producción de entropía irreversible $T_0\,\dot\Sigma_{\mathrm{irr}}$ (también en `W/m²`), declarado como extensión.

## 5.2 Capacidad regenerativa como flujo de restauración normalizado

$$
R_{\mathrm{cap}}(t) = \frac{1}{F_{\mathrm{ref}}}\Big[\;\Phi_{\mathrm{bio}}(t) \;+\; \underbrace{k_{\mathrm{tech}}\, E_{\mathrm{tech}}(t)}_{\text{sumideros ingenierizados}} \;+\; \Phi_{\mathrm{rad}}\;\Big]
$$

| Término                  | Descripción                                                       |
| :----------------------- | :---------------------------------------------------------------- |
| $\Phi_{\mathrm{bio}}$    | Flujo de sumidero biosférico/oceánico (forzamiento evitado/tiempo)|
| $k_{\mathrm{tech}}\,E_{\mathrm{tech}}$ | Remoción/eficiencia ingenierizada (CDR, eficiencia)     |
| $\Phi_{\mathrm{rad}}$    | Margen radiativo (capacidad de re-radiar, ligado a OLR y albedo)  |

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

**Corrección respecto a `v0.2.0`:** la puerta anterior era instantánea y suponía autocorrección contemporánea (optimista). Las retroalimentaciones reales de insostenibilidad son **retardadas, con umbral y políticamente mediadas**. Esta versión modela explícitamente esa persistencia.

## 6.1 Puerta instantánea (línea base, conservada como referencia)

$$
\chi_0(t) = \exp\!\big[-\lambda\,\Delta(t)\big]
$$

## 6.2 Componente con retardo — deuda regenerativa

Se introduce un **estado de deuda regenerativa** $D_{\mathrm{reg}}(t)$ que se acumula rápido bajo sobrepaso y se recupera lento:

$$
\frac{dD_{\mathrm{reg}}}{dt} = \Delta(t) - \rho\,D_{\mathrm{reg}}(t)
$$

con $\rho$ pequeño (recuperación lenta). Esto captura que el daño **no se corrige en el mismo instante** en que cesa la causa.

## 6.3 Componente con histéresis — latch de régimen

Un estado de régimen $h(t)\in[0,1]$ se enciende cuando la deuda supera $\theta_{\mathrm{on}}$ y solo se libera cuando cae por debajo de un umbral **más estricto** $\theta_{\mathrm{off}} < \theta_{\mathrm{on}}$ (Schmitt-trigger continuo):

$$
\theta_{\mathrm{eff}}(h) = \theta_{\mathrm{off}} + (\theta_{\mathrm{on}} - \theta_{\mathrm{off}})\,(1 - h)
$$

$$
\frac{dh}{dt} = \frac{1}{\tau_h}\Big[\,\varsigma\big(D_{\mathrm{reg}} - \theta_{\mathrm{eff}}(h)\big) - h\,\Big], \qquad \varsigma(z) = \frac{1}{1 + e^{-k\,z}}
$$

La dependencia de $\theta_{\mathrm{eff}}$ de $h$ es lo que produce la **histéresis** (la recuperación exige sobre-corregir por debajo de un umbral más bajo).

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

> Supuesto declarado explícitamente: este modelo asume que la pérdida de licencia operativa es **persistente y no autocorrectiva en el corto plazo**. Es una postura más conservadora —y más realista— que la puerta instantánea de `v0.2.0`.

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

## 7.4 Símbolos reservados (no activos en el modelo operativo)

$a_{\mathrm{cosm}}(t)$, $H(t)$, $\Lambda$, $\rho_{\mathrm{dm}}$, $\kappa$ — reservados para extensiones físicas; ver Apéndice A. **No se usan en el cómputo de §10.**

---

# 8. Sistema Socio-Técnico Acoplado (Acotado por Construcción)

**Corrección respecto a `v0.2.0`:** las tres variables son ahora **acotadas en $[0,1]$ por construcción** (factores de saturación $(1-x)$ y decaimiento), eliminando la necesidad del recorte `np.clip` que enmascaraba el sobrepaso.

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

El **vector de estado completo** del marco integrado es:

$$
\mathbf{y}(t) = \big[\,I_{\mathrm{EU}},\; E_{\mathrm{tech}},\; D_{\mathrm{ID}},\; T_s,\; D_{\mathrm{reg}},\; h\,\big]
$$

un sistema **físico + socio-técnico genuinamente acoplado**, no dos modelos yuxtapuestos.

---

# 9. Bucles de Retroalimentación (incluyendo físico ↔ social)

| Bucle                                                                       | Mecanismo                                                       | Efecto sistémico                       |
| :-------------------------------------------------------------------------- | :------------------------------------------------------------- | :------------------------------------- |
| $I_{\mathrm{EU}} \leftrightarrow E_{\mathrm{tech}}$                         | Integración habilita innovación; innovación acelera integración | Crecimiento acumulativo o estancamiento |
| $I_{\mathrm{EU}} \rightarrow D_{\mathrm{ID}} \rightarrow E_{\mathrm{tech}}$ | Identidad digital mejora interoperabilidad y despliegue         | Transición hacia adopción masiva       |
| **$E_{\mathrm{tech}} \rightarrow Q_{\mathrm{anth}} \downarrow$**            | **Descarbonización (canal físico, §3.2)**                       | **Reduce externalidad medida**         |
| **$E_{\mathrm{tech}} \rightarrow R_{\mathrm{cap}} \uparrow$**               | **Sumideros ingenierizados (canal físico, §5.2)**               | **Eleva capacidad regenerativa**       |
| **$\Delta \rightarrow D_{\mathrm{reg}} \rightarrow \chi \downarrow$**       | **Deuda regenerativa retardada (§6)**                           | **Pérdida persistente de licencia**    |

Los tres últimos bucles **no existían en `v0.2.0`** como acoplamiento computacional.

---

# 10. Implementación Numérica Reproducible

**Corrección respecto a `v0.2.0`:** se sustituye el integrador de Euler explícito (primer orden, condicionalmente estable, con recorte que distorsionaba la dinámica) por `scipy.integrate.solve_ivp` (RK45, tolerancias explícitas). La deuda y las violaciones se **integran como estado**, no se registran en un bucle con error off-by-one. No hay recorte: las variables son acotadas por construcción.

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
# Señales exógenas (deterministas y auditables)
inputs = {
    "C":       lambda t: 0.50 + 0.10 * np.sin(0.02 * t),
    "R":       lambda t: 0.60 + 0.05 * t / 150.0,
    "A_inst":  lambda t: 0.40 + 0.10 * (1.0 - np.exp(-0.02 * t)),
    "U":       lambda t: 0.70 + 0.20 * (1.0 - np.exp(-0.03 * t)),
    "A_adopt": lambda t: 0.50 + 0.15 * (1.0 - np.exp(-0.025 * t)),
    "S":       lambda t: 0.80,
    # actividad industrial: crece y luego se estabiliza
    "activity": lambda t: 0.80 + 0.20 * (1.0 - np.exp(-0.02 * t)),
}

p = Parameters()
# Estado inicial: [I_EU, E_tech, D_ID, T_s, D_reg, h]
y0 = np.array([0.20, 0.15, 0.10, 287.5, 0.0, 0.0])

sol = run(p, y0, t_end=150.0, inputs=inputs)
I_EU, E_tech, D_ID, T_s, D_reg, h = sol.y
```

---

# 12. Calibración e Identificabilidad

**Corrección respecto a `v0.2.0`:** el protocolo anterior listaba fuentes de datos pero ninguna estrategia de identificación. Con ~20 parámetros y solo tres trayectorias agregadas observables, el sistema socio-técnico es **prácticamente no identificable** sin restricciones. Esta sección lo aborda de frente.

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

Múltiples combinaciones de coeficientes socio-técnicos producen trayectorias indistinguibles (el problema clásico de la dinámica de sistemas). **No se debe prometer "todo coeficiente trazable" sin antes demostrar que es recuperable.** Estrategia mínima:

1. **Identificabilidad estructural** — análisis de qué combinaciones de parámetros aparecen solo como producto (p. ej. $\eta_E$ y las elasticidades), reduciendo el espacio efectivo.
2. **Identificabilidad práctica** — perfil de verosimilitud (profile likelihood) por parámetro; los planos indican no identificabilidad práctica.
3. **Sensibilidad global** — índices de Sobol para ordenar parámetros por influencia sobre las salidas.
4. **Inferencia bayesiana** — priors informativos + comprobaciones predictivas posteriores; reportar intervalos creíbles, no solo puntos.
5. **Veredicto por parámetro** — cada coeficiente se etiqueta como `identificable`, `débilmente identificable` o `fijado-desde-prior` en el registro de auditoría.

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
        "model_id": "AMPEL-SICOCA-COUPLED-002",
        "version": "1.0.0",
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

# 13. Escenarios de Simulación

| Escenario                    | Mecanismo                                            | Resultado esperado                                 |
| :--------------------------- | :--------------------------------------------------- | :------------------------------------------------- |
| Baseline                     | Continuidad de tendencias                            | Crecimiento moderado, deuda regenerativa contenida |
| Regenerativo                 | $E_{\mathrm{tech}}$ alta temprano                    | $Q_{\mathrm{anth}}\downarrow$, $R_{\mathrm{cap}}\uparrow$, $\chi\approx 1$, bucle virtuoso |
| Trampa de insostenibilidad   | Actividad alta + tecnología estancada                | Deuda supera $\theta_{\mathrm{on}}$, latch activo, $\chi\downarrow$, **bloqueo persistente** |
| Estrés energético            | $Q_0$ elevado                                        | Penalización con retardo; recuperación lenta       |
| Ciberataque                  | Caída abrupta de $S(t)$                              | Caída de $D_{\mathrm{ID}}$ y de eficacia           |
| Fragmentación regulatoria    | $R(t), C(t)\downarrow$                               | Estancamiento de integración                       |
| Recuperación tardía          | Tecnología mejora tras activar el latch              | **Histéresis:** se exige $D_{\mathrm{reg}}<\theta_{\mathrm{off}}$ antes de recuperar licencia |

El escenario "Recuperación tardía" es el que **distingue `v1.0.0`**: demuestra que el modelo ya no supone autocorrección instantánea.

---

# 14. Condiciones de Validez

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

# 15. Originalidad y Posicionamiento (Declaración Honesta)

Esta sección distingue lo estándar de lo propio, porque la credibilidad del marco depende de no reclamar autoridad prestada.

## 15.1 Componentes estándar (no nuevos)

| Componente                          | Linaje                                                  |
| :---------------------------------- | :------------------------------------------------------ |
| Ecuaciones de campo de Einstein     | Relatividad general clásica                             |
| Balance energético 0-D (EBM)        | Tradición Budyko–Sellers                                |
| Difusión logística de adopción      | Modelo de Bass / difusión de innovaciones               |
| Penalización exponencial de un lado | Métodos de barrera/penalización en optimización         |
| Histéresis de dos umbrales          | Schmitt-trigger / modelos de relé en sistemas dinámicos |
| Dinámica de sistemas acoplada       | Tradición Forrester                                     |

## 15.2 La contribución (dónde vive lo propio)

1. **Puerta de admisibilidad multiplicativa, físicamente fundamentada.** Tratar la sostenibilidad no como término de la función objetivo sino como **condición dinámica de admisibilidad** $\chi(t)$, con `X_ext` y `R_cap` **derivadas de un balance energético** y no postuladas.
2. **Bucle físico ↔ socio-técnico cerrado.** La eficacia tecnológica modifica el sistema físico que la autoriza ($E_{\mathrm{tech}}\to Q_{\mathrm{anth}}, R_{\mathrm{cap}}$).
3. **Persistencia no autocorrectiva.** Retardo (deuda) + histéresis (latch) como postura modeladora explícita y conservadora.
4. **Provenance como ciudadano de primera clase.** Hashing de parámetros, entradas y constantes; veredictos de identificabilidad — práctica ausente en la mayoría del modelado de política.

La doctrina `SICO.CA` da identidad coherente al conjunto. El posicionamiento correcto **antepone el núcleo de gobernanza-dinámica** y trata la relatividad general como marco conceptual, no como fuente de autoridad física sobre operaciones industriales.

---

# 16. Implicaciones Operativas

1. **Licencia de operación computable.** La puerta $\chi$ como criterio formal de admisibilidad, cableada a KPIs reales: `X_ext` desde contabilidad de emisiones/energía, `R_cap` desde métricas de regeneración. Evaluable de forma continua por una organización o un regulador.
2. **Enlace con ESG/CSRD.** El puente conecta con la maquinaria de reporte existente; más concreto que la mayoría de "marcos de sostenibilidad" porque es **una función con umbral**, no un eslogan.
3. **Capa de auditoría como contribución independiente.** Registros de simulación reproducibles y anclados por hash son valiosos por sí mismos.

**Límites declarados:** la capa física, si se sobreextiende, invita al rechazo (de ahí el Apéndice A separado); la calibración puede ser irresoluble al nivel agregado; la puerta codifica supuestos de retroalimentación que deben validarse empíricamente.

---

# 17. Tesis Consolidada

## 17.1 Español

> **El Ampel Theoretical Framework define un espacio de estados físico y socio-técnico genuinamente acoplado, en el que las operaciones industriales solo son admisibles cuando sus externalidades —medidas como forzamiento físico neto sobre el balance energético— permanecen por debajo de una capacidad regenerativa medible. Un balance energético de orden cero proporciona la capa de límite físico operativa; la relatividad general fija el marco conceptual de conservación; un puente termodinámico convierte flujos físicos en externalidad y capacidad regenerativa; y una puerta de autorización con retardo e histéresis gobierna, de forma persistente y no autocorrectiva, la dinámica tecnológica, institucional e identitaria.**

## 17.2 English

> **The Ampel Theoretical Framework defines a genuinely coupled physical and socio-technical state-space in which industrial operations are admissible only when their externalities — measured as net physical forcing on the energy budget — remain below measurable regenerative capacity. A zero-dimensional energy-balance model provides the operational physical boundary layer; general relativity sets the conceptual conservation frame; a thermodynamic bridge converts physical fluxes into externality and regenerative capacity; and a lagged, hysteretic authorization gate governs technological, institutional, and identity-system dynamics in a persistent, non-self-correcting manner.**

---

# 18. Fórmula Axial

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

Governance rule (persistent, non-self-correcting):
  Regenerative debt accumulates fast, recovers slow;
  authorization latch releases only below a stricter threshold.

Closed loop:
  E_tech reduces Q_anth and raises R_cap -> modifies the physics that authorizes it.

Audit layer:
  Every coefficient, input, constant and scenario
  is traceable, reproducible, contestable — with identifiability verdicts.
```

---

# Apéndice A — Extensiones Especulativas (No Validadas, Fuera del Modelo Operativo)

> **Advertencia:** este apéndice contiene acoplamientos físicos **no validados empíricamente**. Están separados deliberadamente para que su carácter especulativo no contamine el modelo operativo (§3–§10), que es físicamente estándar.

A.1 **Acoplamiento cosmológico atmosférico.** Un término $Q_{\mathrm{cosm}}$ en el balance, con la condición de consistencia $Q_{\mathrm{cosm}}\to 0$ reduciéndose al EBM estándar. Variables reservadas: $a_{\mathrm{cosm}}(t), H(t), \Lambda$.

A.2 **Acoplamiento radiación–materia oscura.** Un término $\mathcal{F}_{\mathrm{coupling}}(\rho_{\mathrm{dm}}, g_{\mu\nu})$ en el transporte radiativo. Sin evidencia de acoplamiento directo fotón–materia oscura; se mantiene aquí solo como hipótesis falsable.

A.3 **Producción de entropía irreversible.** Refinamiento de `X_ext` con $T_0\,\dot\Sigma_{\mathrm{irr}}$. Físicamente motivado pero requiere instrumentación específica.

Cualquier promoción de A.1–A.3 al modelo operativo exige superar las condiciones de validez de §14 (falsabilidad, reducción a modelos estándar).

---

# Changelog — v1.0.0 (supersede v0.2.0)

- **Eliminado** el doble conteo de $\Lambda$: ahora geométrico (lado izquierdo) únicamente.
- **Eliminado** $T_{\mu\nu}^{\mathrm{anth}}$ de las ecuaciones de campo; añadido **principio de separación de escalas** (§1.2).
- **Eliminado** el acoplamiento radiación–materia oscura del transporte radiativo; transporte estándar retenido; acoplamientos especulativos movidos al **Apéndice A**.
- **Añadido** el **EBM de orden cero** (§3) como reducción física operativa que carga el cálculo.
- **NUEVO: puente termodinámico** (§5) que deriva `X_ext` y `R_cap` de flujos físicos — cierra la brecha de acoplamiento.
- **Añadido** retroacoplamiento $E_{\mathrm{tech}}\to Q_{\mathrm{anth}}$ (descarbonización) y $E_{\mathrm{tech}}\to R_{\mathrm{cap}}$ (sumideros ingenierizados).
- **Sustituida** la puerta binaria/instantánea por una puerta **con retardo (deuda regenerativa) e histéresis (dos umbrales)** (§6); supuesto de persistencia declarado.
- **Dinámica socio-técnica acotada por construcción** (§8); eliminado el recorte `np.clip` que enmascaraba el sobrepaso.
- **Sustituido** Euler explícito por `solve_ivp` (RK45); deuda/violaciones **integradas como estado**; corregido el error off-by-one.
- **Todos los símbolos previamente huérfanos** ($A_{\mathrm{alb}}$, etc.) ahora activos; símbolos reservados etiquetados (§7.4).
- **Añadida** sección de **identificabilidad y equifinalidad** (§12).
- **Añadida** sección honesta de **originalidad y posicionamiento** (§15).

---

# Línea Final

> **No more wars. Regeneration now. Industria solo si es sostenible. Competición solo si es regenerativa. Algoritmos solo si rinden cuentas — y la sostenibilidad, medida, no declarada.**
