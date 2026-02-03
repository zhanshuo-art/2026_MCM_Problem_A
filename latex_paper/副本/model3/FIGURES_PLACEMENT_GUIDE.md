# Model III Figures Placement Guide

## 📋 Overview

This document provides guidance on where to insert each figure from the `figures/` folder into the Model III paper sections.

**Total Figures:** 7 (each available in PDF and PNG formats)

---

## 🗂️ Figure-to-Section Mapping

| Figure | Filename | Paper Section | Recommended Location |
|--------|----------|---------------|----------------------|
| Fig 1 | `fig1_state_space` | §6.1.2 | After State Space Definition table |
| Fig 2 | `fig2_circadian_gate` | §6.2.3 | After gating function equation |
| Fig 3 | `fig3_current_distributions` | §6.3.3 | Before/after parameter table |
| Fig 4 | `fig4_sample_trajectory` | §6.4.1 | After hybrid system description |
| Fig 5 | `fig5_profile_comparison` | §6.4.1 or §6.5 | In results/validation section |
| Fig 6 | `fig6_generator_matrix` | §6.1.4 | After Q matrix equation |
| Fig 7 | `fig7_circadian_modulation` | §6.2.4 | After modulation explanation |

---

## 📍 Detailed Placement Instructions

### Figure 1: State Space Diagram
**File:** `fig1_state_space.pdf`

**Content:** 4-state CTMC showing $S_1$ (Idle), $S_2$ (Light), $S_3$ (Video), $S_4$ (Gaming) with transition arrows.

**Insert Location:** 
- **Section 6.1.2** "State Space Definition"
- Place immediately after the state definition table
- Before Section 6.1.3

**LaTeX Code:**
```latex
\begin{figure}[htbp]
    \centering
    \includegraphics[width=0.6\textwidth]{figures/fig1_state_space.pdf}
    \caption{State transition diagram of the 4-state CTMC. Arrows indicate possible transitions with rates $q_{ij}$.}
    \label{fig:state_space}
\end{figure}
```

**Caption (EN):** "State transition diagram of the Continuous-Time Markov Chain with four user activity states: Idle ($S_1$), Light ($S_2$), Video ($S_3$), and Gaming ($S_4$). Arrow thickness represents relative transition rates."

**Caption (CN):** "连续时间马尔可夫链的状态转移图，包含四种用户活动状态：待机（$S_1$）、轻度（$S_2$）、视频（$S_3$）和游戏（$S_4$）。箭头粗细表示相对转移率。"

---

### Figure 2: Circadian Gating Function
**File:** `fig2_circadian_gate.pdf`

**Content:** 24-hour activity curve $\gamma(t)$ showing noon and evening peaks with sleep suppression.

**Insert Location:**
- **Section 6.2.3** "Gating Function Formulation"
- Place after the double-Gaussian equation
- After the activity level table

**LaTeX Code:**
```latex
\begin{figure}[htbp]
    \centering
    \includegraphics[width=0.7\textwidth]{figures/fig2_circadian_gate.pdf}
    \caption{Circadian gating function $\gamma(t)$ over a 24-hour period.}
    \label{fig:circadian_gate}
\end{figure}
```

**Caption (EN):** "Circadian gating function $\gamma(t)$ showing dual peaks at noon (12:30) and evening (21:00), with sleep suppression during 01:00–05:00. The shaded region indicates the sleep period."

**Caption (CN):** "昼夜节律门控函数 $\gamma(t)$，显示中午（12:30）和晚间（21:00）的双峰，以及01:00–05:00期间的睡眠抑制。阴影区域表示睡眠时段。"

---

### Figure 3: Current Distributions
**File:** `fig3_current_distributions.pdf`

**Content:** Probability density functions of discharge current for each of the 4 states.

**Insert Location:**
- **Section 6.3.3** "Calibrated Current Parameters"
- Place before or after the parameter table (Table 2)
- Provides visual validation of state separation

**LaTeX Code:**
```latex
\begin{figure}[htbp]
    \centering
    \includegraphics[width=0.7\textwidth]{figures/fig3_current_distributions.pdf}
    \caption{Current probability distributions for each user activity state.}
    \label{fig:current_dist}
\end{figure}
```

**Caption (EN):** "Probability density functions of discharge current $I$ for each activity state, derived from K-Means clustering on 36,000 samples. Clear separation validates the 4-state model design."

**Caption (CN):** "各活动状态放电电流 $I$ 的概率密度函数，通过对36,000个样本进行K-Means聚类得到。明显的分离验证了4状态模型设计的合理性。"

---

### Figure 4: Sample Trajectory
**File:** `fig4_sample_trajectory.pdf`

**Content:** A realization of CGSL showing state trajectory $X(t)$ and corresponding current $I(t)$ over 12 hours.

**Insert Location:**
- **Section 6.4.1** "The Complete CGSL-ECM Framework"
- Or after Algorithm 1 in **Section 6.4.2**
- Demonstrates the model output

**LaTeX Code:**
```latex
\begin{figure}[htbp]
    \centering
    \includegraphics[width=0.85\textwidth]{figures/fig4_sample_trajectory.pdf}
    \caption{Sample CGSL trajectory: (a) User state $X(t)$; (b) Stochastic current $I(t)$.}
    \label{fig:sample_trajectory}
\end{figure}
```

**Caption (EN):** "Sample CGSL trajectory over 12 hours starting at 8:00 AM. Top: User activity state $X(t)$ showing transitions between Idle, Light, Video, and Gaming. Bottom: Corresponding stochastic discharge current $I(t)$ in mA."

**Caption (CN):** "从上午8:00开始的12小时CGSL样本轨迹。上图：用户活动状态 $X(t)$，显示待机、轻度、视频和游戏之间的转换。下图：对应的随机放电电流 $I(t)$（单位：mA）。"

---

### Figure 5: User Profile Comparison
**File:** `fig5_profile_comparison.pdf`

**Content:** Bar chart comparing mean current across different user profiles (light/moderate/heavy/office).

**Insert Location:**
- **Section 6.4.1** after describing user profiles
- Or **Section 6.5** "Model III Summary" as validation
- Shows practical application of the model

**LaTeX Code:**
```latex
\begin{figure}[htbp]
    \centering
    \includegraphics[width=0.6\textwidth]{figures/fig5_profile_comparison.pdf}
    \caption{Mean discharge current comparison across user profiles.}
    \label{fig:profile_comparison}
\end{figure}
```

**Caption (EN):** "Mean discharge current (with standard deviation) across four user profiles: Light, Moderate, Heavy, and Office. Values computed from 30 simulated 4-hour trajectories per profile."

**Caption (CN):** "四种用户配置文件的平均放电电流（含标准差）：轻度、中度、重度和办公。数值由每种配置30次4小时模拟轨迹计算得出。"

---

### Figure 6: Generator Matrix Heatmap
**File:** `fig6_generator_matrix.pdf`

**Content:** Heatmap visualization of the transition rate matrix $\mathbf{Q}$.

**Insert Location:**
- **Section 6.1.4** "Transition Rate Calibration"
- Place after the numerical Q matrix
- Provides visual intuition for transition rates

**LaTeX Code:**
```latex
\begin{figure}[htbp]
    \centering
    \includegraphics[width=0.5\textwidth]{figures/fig6_generator_matrix.pdf}
    \caption{Heatmap of the CTMC generator matrix $\mathbf{Q}$.}
    \label{fig:generator_matrix}
\end{figure}
```

**Caption (EN):** "Heatmap visualization of the generator matrix $\mathbf{Q}$ (rates in h$^{-1}$). Diagonal elements (negative) represent total departure rates; off-diagonal elements represent transition rates between states."

**Caption (CN):** "生成矩阵 $\mathbf{Q}$ 的热力图可视化（速率单位：h$^{-1}$）。对角元素（负值）表示总离开速率；非对角元素表示状态间的转移速率。"

---

### Figure 7: Circadian State Modulation
**File:** `fig7_circadian_modulation.pdf`

**Content:** Two-panel figure: (a) Time-modulated transition rates; (b) State occupation fraction vs time of day.

**Insert Location:**
- **Section 6.2.4** "Modulated Generator Matrix"
- After the probability conservation discussion
- Demonstrates the effect of circadian gating

**LaTeX Code:**
```latex
\begin{figure}[htbp]
    \centering
    \includegraphics[width=0.9\textwidth]{figures/fig7_circadian_modulation.pdf}
    \caption{Effect of circadian gating on state transitions and occupation.}
    \label{fig:circadian_modulation}
\end{figure}
```

**Caption (EN):** "Effect of circadian gating. (a) Time-modulated transition rates from Idle to Video ($q_{13}$) and Gaming ($q_{14}$) over 24 hours. (b) Stacked area plot showing average state occupation fraction vs. time of day, computed from 50 simulated trajectories."

**Caption (CN):** "昼夜节律门控的效果。(a) 从待机到视频（$q_{13}$）和游戏（$q_{14}$）的时变转移率在24小时内的变化。(b) 堆叠面积图显示平均状态占比与一天中时间的关系，由50条模拟轨迹计算得出。"

---

## 📐 Recommended Figure Order in Paper

Based on the logical flow of the paper, figures should appear in this order:

```
Section 6.1: State Space Construction and CTMC Framework
    ├── §6.1.2: [Figure 1] State Space Diagram
    └── §6.1.4: [Figure 6] Generator Matrix Heatmap

Section 6.2: Circadian-Gated Transition Mechanism
    ├── §6.2.3: [Figure 2] Circadian Gating Function
    └── §6.2.4: [Figure 7] Circadian State Modulation

Section 6.3: Data-Driven Load Mapping Interface
    └── §6.3.3: [Figure 3] Current Distributions

Section 6.4: Hybrid System Integration and Simulation
    ├── §6.4.1: [Figure 4] Sample Trajectory
    └── §6.4.1: [Figure 5] User Profile Comparison
```

---

## 🎨 Format Recommendations

### For LaTeX/PDF Submission:
- Use **PDF** format for vector quality
- Width recommendations:
  - Single-column: `width=0.7\textwidth` to `0.85\textwidth`
  - Two-panel figures: `width=0.9\textwidth`
  - Square figures: `width=0.5\textwidth`

### For Word Submission:
- Use **PNG** format (300 DPI)
- Insert using "Insert > Picture"
- Set text wrapping to "Top and Bottom"

### Caption Style (MCM/ICM):
- Start with figure content description
- Include technical details (sample size, method)
- Keep under 3 sentences

---

## 📎 Quick Reference Table

| Fig # | Section | After Text Starting With... | Key Purpose |
|-------|---------|----------------------------|-------------|
| 1 | 6.1.2 | "...users and researchers can identify" | Visualize state space |
| 6 | 6.1.4 | "Calibrated Generator Matrix" | Show Q matrix values |
| 2 | 6.2.3 | "sleep suppression factor" | Show γ(t) curve |
| 7 | 6.2.4 | "Numerical Example" | Show modulation effect |
| 3 | 6.3.3 | Table 2 (parameter table) | Validate state separation |
| 4 | 6.4.1 | "continuous component" description | Demo model output |
| 5 | 6.4.1 | After Figure 4 | Compare user profiles |

---

## ✅ Checklist Before Submission

- [ ] All 7 figures inserted in correct locations
- [ ] Figure numbers match paper references
- [ ] Captions are bilingual (if required)
- [ ] PDF format used for vector quality
- [ ] Figure references updated (`\ref{fig:...}`)
- [ ] No orphaned figures (each referenced in text)

---

*Generated for MCM 2026 Model III (CGSL) Paper*
