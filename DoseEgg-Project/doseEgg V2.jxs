import React, { useMemo, useState } from "react";

export default function DoseEggMobileMockup() {
  const [tab, setTab] = useState("Today");
  const [addType, setAddType] = useState("Medication");
  const [selectedDose, setSelectedDose] = useState("100 mg");
  const [formulation, setFormulation] = useState("IR");

  const timeline = [
    { time: "06:00", category: "med", title: "Sinemet ER", detail: "200 mg · baseline", chip: "ER" },
    { time: "08:20", category: "symptom", title: "Chest tightness", detail: "mild OFF pressure", chip: "OFF" },
    { time: "09:30", category: "med", title: "Sinemet IR", detail: "100 mg · rescue", chip: "IR" },
    { time: "12:00", category: "med", title: "Sinemet IR", detail: "100 mg", chip: "IR" },
    { time: "12:30", category: "meal", title: "Lunch", detail: "low protein", chip: "Meal" },
    { time: "15:00", category: "med", title: "Sinemet IR", detail: "100 mg", chip: "IR" },
    { time: "17:30", category: "med", title: "Sinemet IR", detail: "50 mg · bridge", chip: "Bridge" },
    { time: "21:00", category: "med", title: "Sinemet ER", detail: "100 mg · night", chip: "ER" },
  ];

  const history = [
    { date: "Mar 20", total: "650 mg", note: "stable with bridge dose", mood: "Stable" },
    { date: "Mar 19", total: "650 mg", note: "good daytime function", mood: "Stable" },
    { date: "Mar 18", total: "700 mg", note: "protein effect at dinner", mood: "Watch" },
    { date: "Mar 17", total: "600 mg", note: "more OFF pressure", mood: "OFF" },
  ];

  const patterns = [
    "Functional dose range: 650–700 mg/day",
    "Protein meals reduce medication efficacy",
    "Cognitive load may accelerate OFF episodes",
    "50 mg IR bridge dose helps prevent severe OFF",
  ];

  const screenTitle = useMemo(() => {
    if (tab === "Today") return "Today";
    if (tab === "Add") return "Add Entry";
    if (tab === "History") return "History";
    if (tab === "Reports") return "Reports";
    return "Settings";
  }, [tab]);

  return (
    <div className="min-h-screen bg-neutral-200 p-6 text-neutral-950">
      <div className="mx-auto flex max-w-6xl flex-col items-center gap-6 lg:flex-row lg:items-start lg:justify-center">
        <section className="w-full max-w-[390px] overflow-hidden rounded-[42px] bg-neutral-950 p-3 shadow-2xl">
          <div className="min-h-[844px] overflow-hidden rounded-[34px] bg-neutral-50">
            <StatusBar />
            <AppHeader title={screenTitle} subtitle="DoseEgg" />

            <main className="h-[690px] overflow-hidden px-5 pb-3">
              {tab === "Today" && <TodayScreen timeline={timeline} setTab={setTab} />}
              {tab === "Add" && (
                <AddScreen
                  addType={addType}
                  setAddType={setAddType}
                  selectedDose={selectedDose}
                  setSelectedDose={setSelectedDose}
                  formulation={formulation}
                  setFormulation={setFormulation}
                  setTab={setTab}
                />
              )}
              {tab === "History" && <HistoryScreen history={history} />}
              {tab === "Reports" && <ReportsScreen patterns={patterns} />}
              {tab === "Settings" && <SettingsScreen />}
            </main>

            <TabBar tab={tab} setTab={setTab} />
          </div>
        </section>

        <aside className="w-full max-w-xl rounded-[32px] bg-white p-6 shadow-sm ring-1 ring-black/5">
          <p className="text-sm font-semibold uppercase tracking-[0.24em] text-neutral-500">Developer Notes</p>
          <h1 className="mt-2 text-3xl font-semibold tracking-tight">DoseEgg Mobile App Flow</h1>
          <p className="mt-3 text-neutral-600">
            This mockup is intentionally structured as a mobile app, not a scrolling web dashboard. The core screens are separated by bottom navigation, and the Add Entry screen behaves like a real app task flow.
          </p>
          <div className="mt-6 grid gap-3">
            <SpecCard title="Primary interaction" text="Quick logging through Add Entry: medication, symptom, meal, activity, note." />
            <SpecCard title="Core data model" text="Every log is an event: time, category, medication/dose or context tags, free note, optional severity." />
            <SpecCard title="Clinical output" text="Reports convert daily events into doctor-ready summaries: dose range, OFF windows, protein effects, cognitive load triggers." />
            <SpecCard title="MVP scope" text="Timeline, quick entry, history, report export, inventory. Avoid complex AI in v1." />
          </div>
        </aside>
      </div>
    </div>
  );
}

function StatusBar() {
  return (
    <div className="flex items-center justify-between px-7 pb-2 pt-4 text-xs font-semibold text-neutral-900">
      <span>9:41</span>
      <div className="flex items-center gap-1">
        <span className="h-2 w-4 rounded-sm border border-neutral-900" />
        <span className="h-2 w-2 rounded-full bg-neutral-900" />
      </div>
    </div>
  );
}

function AppHeader({ title, subtitle }) {
  return (
    <header className="px-5 pb-3 pt-2">
      <div className="flex items-center justify-between">
        <div>
          <p className="text-xs font-semibold uppercase tracking-[0.22em] text-neutral-400">{subtitle}</p>
          <h2 className="mt-1 text-3xl font-semibold tracking-tight">{title}</h2>
        </div>
        <div className="flex h-11 w-11 items-center justify-center rounded-full bg-white shadow-sm ring-1 ring-black/5">
          🥚
        </div>
      </div>
    </header>
  );
}

function TodayScreen({ timeline, setTab }) {
  return (
    <div className="flex h-full flex-col gap-4">
      <section className="rounded-[28px] bg-neutral-950 p-5 text-white shadow-sm">
        <div className="flex items-start justify-between">
          <div>
            <p className="text-sm text-neutral-300">Current functional range</p>
            <div className="mt-1 text-4xl font-semibold">650 mg</div>
          </div>
          <span className="rounded-full bg-emerald-400/15 px-3 py-1 text-sm font-medium text-emerald-200">Stable</span>
        </div>
        <div className="mt-5 grid grid-cols-3 gap-2 text-center text-sm">
          <Metric label="ER" value="300" />
          <Metric label="IR" value="350" />
          <Metric label="Steps" value="4.3k" />
        </div>
      </section>

      <section className="grid grid-cols-2 gap-3">
        <button onClick={() => setTab("Add")} className="rounded-[24px] bg-white p-4 text-left shadow-sm ring-1 ring-black/5">
          <div className="text-2xl">＋</div>
          <div className="mt-2 font-semibold">Quick Log</div>
          <div className="mt-1 text-sm text-neutral-500">Medication, symptom, meal</div>
        </button>
        <button onClick={() => setTab("Reports")} className="rounded-[24px] bg-white p-4 text-left shadow-sm ring-1 ring-black/5">
          <div className="text-2xl">📄</div>
          <div className="mt-2 font-semibold">Report</div>
          <div className="mt-1 text-sm text-neutral-500">Doctor-ready summary</div>
        </button>
      </section>

      <section className="min-h-0 flex-1 rounded-[28px] bg-white p-4 shadow-sm ring-1 ring-black/5">
        <div className="mb-3 flex items-center justify-between">
          <h3 className="font-semibold">Today Timeline</h3>
          <span className="text-sm text-neutral-400">8 events</span>
        </div>
        <div className="h-[350px] overflow-y-auto pr-1">
          <div className="space-y-3">
            {timeline.map((item, idx) => (
              <TimelineItem key={idx} item={item} compact={idx > 4} />
            ))}
          </div>
        </div>
      </section>
    </div>
  );
}

function Metric({ label, value }) {
  return (
    <div className="rounded-2xl bg-white/10 px-3 py-2">
      <div className="text-xs text-neutral-300">{label}</div>
      <div className="text-lg font-semibold">{value}</div>
    </div>
  );
}

function TimelineItem({ item }) {
  const dot = {
    med: "bg-blue-500",
    symptom: "bg-red-500",
    meal: "bg-amber-500",
    activity: "bg-emerald-500",
  }[item.category];

  const chip = {
    med: "bg-blue-50 text-blue-700",
    symptom: "bg-red-50 text-red-700",
    meal: "bg-amber-50 text-amber-700",
    activity: "bg-emerald-50 text-emerald-700",
  }[item.category];

  return (
    <div className="flex items-center gap-3 rounded-2xl border border-neutral-100 bg-neutral-50 p-3">
      <div className="w-11 text-sm font-medium text-neutral-500">{item.time}</div>
      <div className={`h-3 w-3 rounded-full ${dot}`} />
      <div className="min-w-0 flex-1">
        <div className="truncate font-semibold">{item.title}</div>
        <div className="truncate text-sm text-neutral-500">{item.detail}</div>
      </div>
      <span className={`rounded-full px-2.5 py-1 text-xs font-medium ${chip}`}>{item.chip}</span>
    </div>
  );
}

function AddScreen({ addType, setAddType, selectedDose, setSelectedDose, formulation, setFormulation, setTab }) {
  const types = ["Medication", "Symptom", "Meal", "Activity", "Note"];

  return (
    <div className="flex h-full flex-col gap-4">
      <section className="rounded-[28px] bg-white p-4 shadow-sm ring-1 ring-black/5">
        <div className="grid grid-cols-3 gap-2">
          {types.map((type) => (
            <button
              key={type}
              onClick={() => setAddType(type)}
              className={`rounded-2xl px-3 py-3 text-sm font-semibold transition ${addType === type ? "bg-neutral-950 text-white" : "bg-neutral-100 text-neutral-600"}`}
            >
              {type}
            </button>
          ))}
        </div>
      </section>

      <section className="min-h-0 flex-1 rounded-[28px] bg-white p-5 shadow-sm ring-1 ring-black/5">
        {addType === "Medication" && (
          <div className="space-y-5">
            <FieldLabel title="Medication" />
            <div className="rounded-2xl border border-neutral-200 bg-neutral-50 px-4 py-4 font-semibold">Sinemet</div>

            <FieldLabel title="Formulation" />
            <Segmented options={["IR", "ER", "ODT"]} value={formulation} setValue={setFormulation} />

            <FieldLabel title="Dose" />
            <Segmented options={["50 mg", "100 mg", "150 mg"]} value={selectedDose} setValue={setSelectedDose} />

            <div className="grid grid-cols-2 gap-3">
              <InfoBox label="Time" value="Auto now · 09:41" />
              <InfoBox label="Rescue" value="Bridge dose" active />
            </div>
          </div>
        )}

        {addType === "Symptom" && <TagEntry title="Select symptoms" tags={["Chest tightness", "Dystonia", "Tremor", "Typing slow", "Fatigue", "Mood drop"]} />}
        {addType === "Meal" && <TagEntry title="Protein level" tags={["Low protein", "Medium protein", "High protein", "Snack", "Dinner"]} />}
        {addType === "Activity" && <TagEntry title="Activity" tags={["Walk", "Exercise", "Math", "Study", "Language class", "Stretching"]} />}
        {addType === "Note" && (
          <div className="space-y-4">
            <FieldLabel title="Free note" />
            <div className="h-40 rounded-2xl border border-neutral-200 bg-neutral-50 p-4 text-neutral-400">Type observation...</div>
          </div>
        )}
      </section>

      <button onClick={() => setTab("Today")} className="rounded-[22px] bg-neutral-950 px-5 py-4 font-semibold text-white shadow-sm">
        Save Entry
      </button>
    </div>
  );
}

function FieldLabel({ title }) {
  return <div className="text-sm font-semibold text-neutral-600">{title}</div>;
}

function Segmented({ options, value, setValue }) {
  return (
    <div className="grid grid-cols-3 gap-2">
      {options.map((option) => (
        <button
          key={option}
          onClick={() => setValue(option)}
          className={`rounded-2xl px-3 py-3 text-sm font-semibold ${value === option ? "bg-blue-600 text-white" : "bg-neutral-100 text-neutral-600"}`}
        >
          {option}
        </button>
      ))}
    </div>
  );
}

function InfoBox({ label, value, active }) {
  return (
    <div className={`rounded-2xl border p-4 ${active ? "border-blue-200 bg-blue-50" : "border-neutral-200 bg-neutral-50"}`}>
      <div className="text-xs uppercase tracking-wide text-neutral-400">{label}</div>
      <div className="mt-1 text-sm font-semibold">{value}</div>
    </div>
  );
}

function TagEntry({ title, tags }) {
  return (
    <div className="space-y-4">
      <FieldLabel title={title} />
      <div className="flex flex-wrap gap-2">
        {tags.map((tag, idx) => (
          <button key={tag} className={`rounded-full px-4 py-2 text-sm font-semibold ${idx < 2 ? "bg-neutral-950 text-white" : "bg-neutral-100 text-neutral-600"}`}>
            {tag}
          </button>
        ))}
      </div>
      <FieldLabel title="Severity" />
      <div className="grid grid-cols-5 gap-2">
        {[1, 2, 3, 4, 5].map((n) => (
          <button key={n} className={`rounded-2xl py-3 text-sm font-semibold ${n === 2 ? "bg-blue-600 text-white" : "bg-neutral-100 text-neutral-600"}`}>{n}</button>
        ))}
      </div>
      <FieldLabel title="Note" />
      <div className="h-28 rounded-2xl border border-neutral-200 bg-neutral-50 p-4 text-sm text-neutral-400">Optional note...</div>
    </div>
  );
}

function HistoryScreen({ history }) {
  return (
    <div className="flex h-full flex-col gap-4">
      <section className="rounded-[28px] bg-white p-4 shadow-sm ring-1 ring-black/5">
        <div className="grid grid-cols-3 gap-2 text-sm font-semibold">
          <button className="rounded-2xl bg-neutral-950 px-3 py-3 text-white">7 Days</button>
          <button className="rounded-2xl bg-neutral-100 px-3 py-3 text-neutral-600">Month</button>
          <button className="rounded-2xl bg-neutral-100 px-3 py-3 text-neutral-600">Custom</button>
        </div>
      </section>
      <section className="min-h-0 flex-1 overflow-y-auto rounded-[28px] bg-white p-4 shadow-sm ring-1 ring-black/5">
        <div className="space-y-3">
          {history.map((day) => (
            <div key={day.date} className="rounded-2xl border border-neutral-100 bg-neutral-50 p-4">
              <div className="flex items-center justify-between">
                <div>
                  <div className="font-semibold">{day.date}</div>
                  <div className="mt-1 text-sm text-neutral-500">{day.note}</div>
                </div>
                <div className="text-right">
                  <div className="font-semibold">{day.total}</div>
                  <div className="mt-1 text-sm text-neutral-500">{day.mood}</div>
                </div>
              </div>
            </div>
          ))}
        </div>
      </section>
    </div>
  );
}

function ReportsScreen({ patterns }) {
  return (
    <div className="flex h-full flex-col gap-4">
      <section className="rounded-[28px] bg-neutral-950 p-5 text-white shadow-sm">
        <p className="text-sm text-neutral-300">Appointment Summary</p>
        <h3 className="mt-2 text-2xl font-semibold">Doctor-ready PDF</h3>
        <button className="mt-5 rounded-2xl bg-white px-4 py-3 font-semibold text-neutral-950">Export PDF</button>
      </section>
      <section className="rounded-[28px] bg-white p-5 shadow-sm ring-1 ring-black/5">
        <h3 className="font-semibold">Clinical Patterns</h3>
        <div className="mt-4 space-y-3">
          {patterns.map((p) => (
            <div key={p} className="rounded-2xl bg-neutral-50 p-3 text-sm text-neutral-700">• {p}</div>
          ))}
        </div>
      </section>
      <section className="rounded-[28px] bg-white p-5 shadow-sm ring-1 ring-black/5">
        <h3 className="font-semibold">Suggested Report Sections</h3>
        <div className="mt-3 grid grid-cols-2 gap-2 text-sm font-medium text-neutral-600">
          <div className="rounded-2xl bg-neutral-100 p-3">Dose range</div>
          <div className="rounded-2xl bg-neutral-100 p-3">OFF windows</div>
          <div className="rounded-2xl bg-neutral-100 p-3">Protein effect</div>
          <div className="rounded-2xl bg-neutral-100 p-3">Inventory</div>
        </div>
      </section>
    </div>
  );
}

function SettingsScreen() {
  const meds = ["Sinemet ER 200", "Sinemet ER 100", "Sinemet IR 100", "Neupro Patch"];
  return (
    <div className="flex h-full flex-col gap-4">
      <section className="rounded-[28px] bg-white p-5 shadow-sm ring-1 ring-black/5">
        <h3 className="font-semibold">Default Schedule</h3>
        <div className="mt-4 space-y-2 text-sm text-neutral-600">
          <div>06:00 · ER 200</div>
          <div>09:30 · IR 100</div>
          <div>12:00 · IR 100</div>
          <div>15:00 · IR 100</div>
          <div>17:30 · IR 50–100</div>
          <div>21:00 · ER 100</div>
        </div>
        <button className="mt-4 rounded-2xl bg-neutral-950 px-4 py-3 text-sm font-semibold text-white">Copy to Today</button>
      </section>
      <section className="rounded-[28px] bg-white p-5 shadow-sm ring-1 ring-black/5">
        <h3 className="font-semibold">Inventory</h3>
        <div className="mt-4 space-y-3">
          {meds.map((med, idx) => (
            <div key={med} className="flex items-center justify-between rounded-2xl bg-neutral-50 p-3">
              <span className="text-sm font-medium">{med}</span>
              <span className="text-sm text-neutral-500">{[62, 45, 133, 21][idx]}</span>
            </div>
          ))}
        </div>
      </section>
    </div>
  );
}

function TabBar({ tab, setTab }) {
  const tabs = [
    { name: "Today", icon: "◎" },
    { name: "Add", icon: "+" },
    { name: "History", icon: "◷" },
    { name: "Reports", icon: "▤" },
    { name: "Settings", icon: "⚙" },
  ];

  return (
    <nav className="mx-4 mb-4 rounded-[28px] bg-white p-2 shadow-lg shadow-neutral-200/80 ring-1 ring-black/5">
      <div className="grid grid-cols-5 gap-1">
        {tabs.map((item) => (
          <button
            key={item.name}
            onClick={() => setTab(item.name)}
            className={`rounded-2xl px-1 py-2 text-center text-xs font-semibold transition ${tab === item.name ? "bg-neutral-950 text-white" : "text-neutral-400"}`}
          >
            <div className="text-base leading-none">{item.icon}</div>
            <div className="mt-1 truncate">{item.name}</div>
          </button>
        ))}
      </div>
    </nav>
  );
}

function SpecCard({ title, text }) {
  return (
    <div className="rounded-2xl border border-neutral-200 bg-neutral-50 p-4">
      <div className="font-semibold">{title}</div>
      <p className="mt-1 text-sm leading-6 text-neutral-600">{text}</p>
    </div>
  );
}
