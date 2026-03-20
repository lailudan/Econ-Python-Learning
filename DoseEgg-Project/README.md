### 🧠 DoseEgg – Medication & Symptom Intelligence App

Not a pill tracker.
A medication + context intelligence system.

📌 Overview

DoseEgg is a health logging system designed to track medication, symptoms, meals, and activity in a unified timeline.

This project is inspired by real-world Parkinson’s Disease medication management, where:

medication timing is critical

food (especially protein) affects absorption

cognitive load impacts symptoms

daily patterns matter more than isolated events

DoseEgg aims to transform raw logs into clinically meaningful insights.

🚨 Problem

Existing apps focus on:

pill reminders

simple medication logs

But real-world management requires understanding:

when medication works

why symptoms fluctuate

how food and activity interfere

where OFF periods occur

👉 Current tools do not capture context.

💡 Solution

DoseEgg provides:

a unified timeline-based logging system

low-friction quick entry

structured context tagging

automatic daily summaries

exportable doctor-ready reports

✨ Core Features (MVP)
1️⃣ Daily Timeline

A single timeline combining:

medication

symptoms

meals

activity

06:00 ER 200 mg

09:30 IR 100 mg

12:00 IR 100 mg

14:30 symptom: chest tightness

17:30 IR 50 mg (rescue)

21:00 ER 100 mg

2️⃣ Quick Logging (Low Friction)

Minimal input, fast logging:

Medication

name

IR / ER / ODT

dose

auto timestamp

rescue toggle

Symptom

tag-based (e.g. dystonia, tremor)

optional severity

short note

Meal

low / medium / high protein

Activity

walk / exercise / cognitive load (math, study)

3️⃣ Smart Context Tags (Key Differentiator)

Predefined tags:

protein meal

cognitive load

exercise

hydration

sleep quality

OFF symptoms

👉 Enables pattern detection without heavy typing.

4️⃣ Daily Auto Summary

Automatically generated:

Total dose: 650 mg  
Structure: ER 200 + IR 100 + IR 100 + IR 100 + IR 50 + ER 100  

Likely OFF windows:
- morning before 09:30
- late afternoon ~17:00  

Protein interaction observed at dinner.  

Right foot dystonia noted once.  

Overall functional status: stable.
5️⃣ History & Filtering

view by day / week

filter by:

symptom

protein intake

medication pattern

OFF episodes

6️⃣ Doctor-Ready Export

Two modes:

Full Log → raw timeline

Clinical Summary → structured report

7️⃣ Medication Inventory

Auto-tracked:

ER / IR / ODT pills

patch count

remaining supply

🧪 Real-World Insight (Core Value)

This system is based on actual medication tracking showing:

strong levodopa responsiveness

consistent protein interaction effects

cognitive load (math/study) triggers OFF

need for bridge dosing (50 mg IR)

stable functional range: 650–700 mg/day

👉 Highlights the need for multi-variable tracking, not simple logs.

🆚 Differentiation
Feature	Existing Apps	DoseEgg
Pill reminder	✅	❌ (not core)
Medication log	✅	✅
Symptom tracking	⚠️ basic	✅ structured
Food interaction	❌	✅
Cognitive load tracking	❌	✅
Auto summary	❌	✅
Doctor export	❌	✅
🚧 MVP Scope
Build first:

timeline logging

quick entry

daily summary

export

Not in v1:

AI prediction

complex charts

wearable integration

🔭 Future Directions

pattern detection (AI)

OFF prediction

wearable integration

clinician dashboard

research dataset potential

📄 Product Brief

👉 View Product Brief (PDF)

✏️ Initial Concept Sketch

👉 (optional – add your image here)

![Sketch](./docs/sketch.jpg)
🧭 Roadmap
[ ] Define data model
[ ] Build timeline UI
[ ] Implement quick logging
[ ] Generate daily summary
[ ] Add PDF export
[ ] Pattern detection (future)
🧠 Philosophy

This project explores:

How structured self-tracking can improve
clinical understanding, medication adjustment,
and patient quality of life.

