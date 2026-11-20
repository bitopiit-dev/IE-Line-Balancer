# IE Line Balancer — Baridhi Garments Limited

৩৬ লাইনের সুইং ফ্লোরের জন্য IE ও লাইন ব্যালেন্সিং অ্যাপ। বাংলা ও ইংরেজি দুই ভাষাতেই চলে।
An IE and line-balancing app for a 36-line sewing floor, in Bangla and English.

## চালানোর নিয়ম / How to run

`index.html` ব্রাউজারে খুলুন। কোনো সার্ভার বা ইনস্টল লাগবে না।
Open `index.html` in a browser. No server or install is needed.

- Opened as a file, data is saved in that browser only. Use **Reports → Download backup** to move it to another computer.
- Published as a claude.ai artifact, the data is shared live: share it as **Editor** with the IE team (setup, OB, operators), **Contributor** with supervisors (hourly entry), and **Viewer** with management.

## যা আছে / Features

| অংশ / Section | কাজ / What it does |
|---|---|
| Floor board | All 36 lines grouped by floor, with output vs target, efficiency, DHU and hour-by-hour status |
| Line balancing | Targets, takt time, bottleneck, balance efficiency, capacity chart, auto-balancing suggestion, manpower needed for target |
| Hourly production | Hourly output, alterations, downtime and reasons; end-of-day forecast; quick entry for all lines at once |
| Operators & skills | Skill matrix (efficiency % per machine); skill-adjusted capacity; best operators for the bottleneck |
| Style / OB library | Save an OB once and put it on any line |
| Reports | Daily table, 7-day efficiency trend, Excel export, WhatsApp report, print/PDF, backup and restore |

## হিসাবের সূত্র / Formulas

- Active manpower = (operators + helpers) × (1 − absenteeism)
- Daily target = active MP × hours × 60 ÷ SMV × target efficiency
- Operation capacity/hr = 60 ÷ SAM × MP (skill-adjusted when operators are assigned)
- Balance efficiency = ΣSAM × bottleneck capacity ÷ (ΣMP × 60)
- Line efficiency = output × SMV ÷ (active MP × (logged minutes − downtime))
- DHU = defects ÷ output × 100

## Excel টেমপ্লেট / Excel templates

- `OB_import_template.xlsx` — columns: Operation, Machine, SAM, MP
- `Operator_import_template.xlsx` — columns: Card, Name, Line, then one column per machine
