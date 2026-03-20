export default function DoseEggMockup() {
  const timeline = [
    { time: '06:00', type: 'med', label: 'Sinemet ER', meta: '200 mg', tag: 'baseline' },
    { time: '08:20', type: 'symptom', label: 'Chest tightness', meta: 'mild OFF pressure', tag: 'symptom' },
    { time: '09:30', type: 'med', label: 'Sinemet IR', meta: '100 mg', tag: 'rescue' },
    { time: '12:00', type: 'med', label: 'Sinemet IR', meta: '100 mg', tag: 'daytime' },
    { time: '12:30', type: 'meal', label: 'Lunch', meta: 'low protein', tag: 'meal' },
    { time: '15:00', type: 'med', label: 'Sinemet IR', meta: '100 mg', tag: 'daytime' },
    { time: '17:30', type: 'med', label: 'Sinemet IR', meta: '50 mg', tag: 'bridge' },
    { time: '18:00', type: 'activity', label: 'Walk + study', meta: '30 min / math', tag: 'activity' },
    { time: '21:00', type: 'med', label: 'Sinemet ER', meta: '100 mg', tag: 'night' },
  ];

  const history = [
    { date: 'Mar 19', total: '650 mg', note: 'stable', state: 'good' },
    { date: 'Mar 18', total: '700 mg', note: 'protein effect', state: 'warn' },
    { date: 'Mar 17', total: '600 mg', note: 'OFF periods', state: 'bad' },
  ];

  const reportBullets = [
    'Functional range appears to be 650–700 mg/day',
    'Protein meals reduce medication efficacy',
    'Cognitive load may accelerate OFF episodes',
    '50 mg IR bridge doses help prevent severe OFF periods',
  ];

  const tagStyle = {
    med: 'bg-blue-50 text-blue-700 border-blue-200',
    symptom: 'bg-red-50 text-red-700 border-red-200',
    meal: 'bg-amber-50 text-amber-700 border-amber-200',
    activity: 'bg-emerald-50 text-emerald-700 border-emerald-200',
  };

  const statusDot = {
    good: 'bg-emerald-500',
    warn: 'bg-amber-500',
    bad: 'bg-red-500',
  };

  return (
    <div className="min-h-screen bg-neutral-100 p-6 text-neutral-900">
      <div className="mx-auto max-w-7xl">
        <div className="mb-6 flex items-center justify-between">
          <div>
            <p className="text-sm font-medium uppercase tracking-[0.24em] text-neutral-500">DoseEgg</p>
            <h1 className="text-3xl font-semibold tracking-tight">Visual MVP Mockup</h1>
            <p className="mt-1 text-neutral-500">A developer-ready UI direction for the medication + context intelligence app.</p>
          </div>
          <div className="rounded-2xl bg-white px-5 py-3 shadow-sm ring-1 ring-black/5">
            <div className="text-sm text-neutral-500">Today</div>
            <div className="text-xl font-semibold">Mar 20</div>
          </div>
        </div>

        <div className="grid gap-6 lg:grid-cols-[1.1fr_0.9fr]">
          <section className="rounded-[28px] bg-white p-6 shadow-sm ring-1 ring-black/5">
            <div className="mb-5 flex items-start justify-between">
              <div>
                <h2 className="text-2xl font-semibold">Today</h2>
                <p className="mt-1 text-neutral-500">Timeline-first logging with medication, symptoms, meals, and activity.</p>
              </div>
              <div className="rounded-2xl bg-neutral-900 px-4 py-3 text-white shadow-sm">
                <div className="text-xs uppercase tracking-[0.24em] text-neutral-300">Total</div>
                <div className="text-2xl font-semibold">650 mg</div>
                <div className="mt-1 text-sm text-neutral-300">ER 300 · IR 350</div>
              </div>
            </div>

            <div className="mb-5 grid grid-cols-2 gap-3 md:grid-cols-4">
              {[
                ['+ Medication', 'Quick med entry'],
                ['+ Symptom', 'Tag + severity'],
                ['+ Meal', 'Protein level'],
                ['+ Activity', 'Walk / math / exercise'],
              ].map(([title, sub]) => (
                <button
                  key={title}
                  className="rounded-2xl border border-neutral-200 bg-neutral-50 p-4 text-left transition hover:bg-neutral-100"
                >
                  <div className="font-medium">{title}</div>
                  <div className="mt-1 text-sm text-neutral-500">{sub}</div>
                </button>
              ))}
            </div>

            <div className="relative">
              <div className="absolute left-[59px] top-2 bottom-2 w-px bg-neutral-200" />
              <div className="space-y-4">
                {timeline.map((item, idx) => (
                  <div key={idx} className="grid grid-cols-[48px_24px_1fr] items-start gap-3">
                    <div className="pt-4 text-right text-sm font-medium text-neutral-500">{item.time}</div>
                    <div className="relative flex justify-center pt-4">
                      <div className={`h-3 w-3 rounded-full ${item.type === 'med' ? 'bg-blue-500' : item.type === 'symptom' ? 'bg-red-500' : item.type === 'meal' ? 'bg-amber-500' : 'bg-emerald-500'}`} />
                    </div>
                    <div className="rounded-2xl border border-neutral-200 bg-white p-4 shadow-sm">
                      <div className="flex flex-wrap items-center justify-between gap-3">
                        <div>
                          <div className="font-semibold">{item.label}</div>
                          <div className="mt-1 text-sm text-neutral-500">{item.meta}</div>
                        </div>
                        <span className={`rounded-full border px-3 py-1 text-xs font-medium capitalize ${tagStyle[item.type]}`}>
                          {item.tag}
                        </span>
                      </div>
                    </div>
                  </div>
                ))}
              </div>
            </div>
          </section>

          <div className="grid gap-6">
            <section className="rounded-[28px] bg-white p-6 shadow-sm ring-1 ring-black/5">
              <div className="mb-4 flex items-center justify-between">
                <div>
                  <h2 className="text-xl font-semibold">Quick Add</h2>
                  <p className="mt-1 text-sm text-neutral-500">Bottom-sheet style input for fast logging.</p>
                </div>
                <div className="rounded-full bg-neutral-100 px-3 py-1 text-xs font-medium text-neutral-600">Medication</div>
              </div>

              <div className="space-y-4">
                <div>
                  <label className="mb-2 block text-sm font-medium text-neutral-700">Medication</label>
                  <div className="rounded-2xl border border-neutral-200 px-4 py-3">Sinemet</div>
                </div>
                <div className="grid grid-cols-3 gap-3">
                  {['IR', 'ER', 'ODT'].map((x, i) => (
                    <button
                      key={x}
                      className={`rounded-2xl border px-4 py-3 text-sm font-medium ${i === 0 ? 'border-blue-500 bg-blue-50 text-blue-700' : 'border-neutral-200 bg-white text-neutral-700'}`}
                    >
                      {x}
                    </button>
                  ))}
                </div>
                <div>
                  <label className="mb-2 block text-sm font-medium text-neutral-700">Dose</label>
                  <div className="grid grid-cols-3 gap-3">
                    {['50 mg', '100 mg', '150 mg'].map((x, i) => (
                      <button
                        key={x}
                        className={`rounded-2xl border px-4 py-3 text-sm font-medium ${i === 1 ? 'border-blue-500 bg-blue-50 text-blue-700' : 'border-neutral-200 bg-white text-neutral-700'}`}
                      >
                        {x}
                      </button>
                    ))}
                  </div>
                </div>
                <div className="grid grid-cols-2 gap-3">
                  <div className="rounded-2xl border border-neutral-200 px-4 py-3">
                    <div className="text-xs uppercase tracking-wide text-neutral-500">Time</div>
                    <div className="mt-1 font-medium">Auto now · 09:30</div>
                  </div>
                  <div className="flex items-center justify-between rounded-2xl border border-neutral-200 px-4 py-3">
                    <div>
                      <div className="text-xs uppercase tracking-wide text-neutral-500">Rescue</div>
                      <div className="mt-1 font-medium">Bridge dose</div>
                    </div>
                    <div className="h-6 w-11 rounded-full bg-blue-600 p-1">
                      <div className="ml-auto h-4 w-4 rounded-full bg-white" />
                    </div>
                  </div>
                </div>
                <button className="w-full rounded-2xl bg-neutral-900 px-4 py-3 font-medium text-white">Save Entry</button>
              </div>
            </section>

            <section className="rounded-[28px] bg-white p-6 shadow-sm ring-1 ring-black/5">
              <div className="mb-4">
                <h2 className="text-xl font-semibold">History</h2>
                <p className="mt-1 text-sm text-neutral-500">Recent days with simple clinical signal summaries.</p>
              </div>
              <div className="space-y-3">
                {history.map((item) => (
                  <div key={item.date} className="flex items-center justify-between rounded-2xl border border-neutral-200 p-4">
                    <div className="flex items-center gap-3">
                      <span className={`h-2.5 w-2.5 rounded-full ${statusDot[item.state]}`} />
                      <div>
                        <div className="font-medium">{item.date}</div>
                        <div className="text-sm text-neutral-500">{item.note}</div>
                      </div>
                    </div>
                    <div className="text-sm font-medium text-neutral-700">{item.total}</div>
                  </div>
                ))}
              </div>
            </section>

            <section className="rounded-[28px] bg-white p-6 shadow-sm ring-1 ring-black/5">
              <div className="mb-4 flex items-center justify-between">
                <div>
                  <h2 className="text-xl font-semibold">Report Preview</h2>
                  <p className="mt-1 text-sm text-neutral-500">Doctor-ready summary output.</p>
                </div>
                <button className="rounded-2xl border border-neutral-200 px-4 py-2 text-sm font-medium">Export PDF</button>
              </div>
              <div className="rounded-2xl bg-neutral-50 p-4">
                <div className="mb-3 text-sm font-medium text-neutral-700">Clinical Patterns</div>
                <ul className="space-y-2 text-sm text-neutral-600">
                  {reportBullets.map((x) => (
                    <li key={x} className="flex gap-2"><span>•</span><span>{x}</span></li>
                  ))}
                </ul>
              </div>
            </section>
          </div>
        </div>

        <div className="mt-6 rounded-[28px] bg-white p-4 shadow-sm ring-1 ring-black/5">
          <div className="flex flex-wrap items-center justify-between gap-3">
            <div>
              <div className="text-sm font-medium">Bottom Navigation</div>
              <div className="text-sm text-neutral-500">Today · History · Reports · Settings</div>
            </div>
            <div className="flex items-center gap-2 rounded-full bg-neutral-100 p-1">
              {['Today', 'History', 'Reports', 'Settings'].map((tab, i) => (
                <div
                  key={tab}
                  className={`rounded-full px-4 py-2 text-sm font-medium ${i === 0 ? 'bg-white shadow-sm text-neutral-900' : 'text-neutral-500'}`}
                >
                  {tab}
                </div>
              ))}
            </div>
          </div>
        </div>
      </div>
    </div>
  );
}
