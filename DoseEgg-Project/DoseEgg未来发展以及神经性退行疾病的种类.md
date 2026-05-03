# 🧠 DoseEgg – Medication & Symptom Intelligence App

> **"Fragile, yet whole. The future is still unfolding."**

Not a pill tracker.  
A medication + context intelligence system.

---

## 📌 Overview

DoseEgg is a health logging system designed to track medication, symptoms, meals, and activity in a unified timeline. 

This project is inspired by real-world Parkinson’s Disease management, where:
- Medication timing is critical.
- Food (especially protein) affects absorption.
- Cognitive load (e.g., studying math/Python) impacts symptoms.
- Daily patterns matter more than isolated events.

---

## 🚨 Problem

Existing apps focus on:
- Simple pill reminders.
- Generic medication logs.

**Real-world management requires understanding:**
- *When* medication works (Kick-in time).
- *Why* symptoms fluctuate (Context).
- *How* food and activity interfere (Interactions).
- *Where* OFF periods occur (Patterns).

---

## 💡 Solution

DoseEgg provides:
1. **Unified Timeline**: Combining med, symptoms, meals, and activity.
2. **Low-Friction Logging**: Fast entry for daily variables.
3. **Smart Context Tags**: Protein intake, cognitive load, hydration, etc.
4. **n-of-1 Trial Logic**: High-resolution data for personalized optimization.
5. **Doctor-Ready Export**: Structured clinical summaries.

---

## ✨ Core Features (MVP)

### 1️⃣ Daily Timeline
A single timeline merging medication, symptoms, meals, and activity.
- *Example:* 17:30 | IR 50 mg | **Bridge dose** | Stable.

### 2️⃣ Quick Logging
Minimal input, fast entry:
- **Medication**: Name, Formulation (IR/ER/ODT), Dose, Rescue toggle.
- **Symptom**: Tag-based (e.g., dystonia, tremor) + Severity (1-5).
- **Meal**: Protein level (Low/Medium/High).
- **Activity**: Walk, Exercise, **Cognitive Load (Math, Study)**.

### 3️⃣ Clinical Insights (The "Kick-in" Timer)
Automatically calculates the **Lead Time** between medication and symptom relief to map the patient's unique efficacy curve.

---

## 🆚 Differentiation

| Feature | Existing Apps | DoseEgg |
| :--- | :---: | :---: |
| Pill Reminder | ✅ | ❌ (Not core) |
| Medication Log | ✅ | ✅ |
| Context Tagging | ❌ | ✅ |
| Protein Interaction | ❌ | ✅ |
| Cognitive Load Tracking | ❌ | ✅ |
| n-of-1 Analysis | ❌ | ✅ |
| Doctor Export | ❌ | ✅ |

---

## 🚀 Expansion Roadmap (The "DoseEgg" Spectrum)

DoseEgg is evolving from a Parkinson's tool into a multi-modal neurology intelligence system.


| 凶险等级 | 疾病名称 | 核心病理机制 | 难点与挑战 |
| :--- | :--- | :--- | :--- |
| **SSS (地狱级)** | **ALS (渐冻症)** | 上、下运动神经元全线凋亡 | 进展极快，无有效阻断药物，呼吸衰竭是致命伤。 |
| **SS (极端级)** | **PSP / MSA (多系统萎缩)** | 蛋白异常沉积累及多系统 | 属于“帕金森叠加”，对多巴胺药物不敏感，平衡与自主神经极速瓦解。容易被误诊为简单的PD |
| **S (高危级)** | **MG (重症肌无力)** | 神经-肌肉接头受体受免疫攻击 | 具“波动性”，最怕“危象”，但有药可控。 |
| **A (慢性级)** | **PD (帕金森病)** | 黑质多巴胺神经元丢失 | 漫长持久战，药物敏感度高，重点在于稳态管理。 |
| **B (功能级)** | **ET (特发性震颤)** | 丘脑-皮层环路节律异常 | 精细动作受阻，不影响寿命，重点在于功能评估。 |

---

## 🧪 Real-World Insight

This system validates that:
- Strong levodopa responsiveness is the baseline.
- **Protein interaction** effects are consistent and measurable.
- **Cognitive load (math/study)** directly triggers OFF episodes.
- **Bridge dosing (50 mg IR)** is essential for maintaining the functional range (650–700 mg/day).

---

## 🚧 Roadmap
- [x] Define Data Model
- [x] Build React Mockup (V2)
- [ ] Implement n-of-1 Logic (Python/Pandas)
- [ ] Pattern Detection (SMC/Statistical Models)
- [ ] PDF Export for Clinicians

---

## 🧠 Philosophy

> **"Fragile, yet whole. The future is still unfolding."**

This project explores how structured self-tracking can improve clinical understanding and patient quality of life.

---

## 📄 License
Distributed under the **MIT License**. See `LICENSE` for more information.

Copyright (c) 2026 Ludan Lai.
