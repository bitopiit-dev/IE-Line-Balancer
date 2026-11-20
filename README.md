# Baridhi Garments Limited — IE Line Balancer

**বারিধি গার্মেন্টস লিমিটেড, বিটপী গ্রুপের একটি প্রতিষ্ঠান। ইন্ডাস্ট্রিয়াল ইঞ্জিনিয়ারিং বিভাগ**
S.F.B-07 & 08, Cumilla EPZ, Cumilla, Bangladesh

> লক্ষ্য মোদের একটাই, সেরা হবো আমরাই
> মূল্যবোধ: সততা/ন্যায়পরায়ণতা, বিশ্বাস এবং সম্মান, শৃঙ্খলা, দায়িত্ববোধ

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
| Floor board | Dark indigo hero with the company motto and values, a floor-efficiency gauge and live totals; line tiles with a stitched hour-by-hour seam and achievement bar; **big screen (TV) mode** for the floor display with a clock and automatic floor-by-floor scrolling |
| Floor board (data) | All 36 lines grouped by floor, with output vs target, efficiency, DHU and hour-by-hour status |
| Line balancing | Targets, takt time, bottleneck, balance efficiency, capacity chart, auto-balancing suggestion, manpower needed for target |
| Hourly production | Hourly output, alterations, downtime, variance; problem type, action plan, who and time to solve with status (same as the Production Board sheet); end-of-day forecast; yesterday, MTD and last-month efficiency; run day; quick entry for all lines |
| Quality and audit | DHU against the line's target (default below 5%), today's top 3 defects, lot/audit findings and buyer feedback |
| Operators & skills | Skill matrix (efficiency % per machine); skill-adjusted capacity; best operators for the bottleneck |
| Style / OB library | Save an OB once and put it on any line |
| Reports | Daily table, action tracker for every open problem, 7-day efficiency trend, Excel export (summary, hourly, action tracker, quality), WhatsApp report, print/PDF, backup and restore |

## Advanced IE features

| Feature | What it does |
|---|---|
| Smart alerts | Floor board flags lines with 2+ hours in a row below 85% of target, DHU over target, 20+ min downtime in an hour, overdue problems, end-of-day shortfall and bottleneck below target, grouped per line |
| Yamazumi / pitch diagram | Work content per operator (SAM ÷ MP) against pitch time, takt time and ±15% control limits; balance loss % |
| Learning curve | Simple / medium / complex ramp for a new style; today's target follows the run day automatically |
| Time study | Stopwatch with cycle capture (Space key records a cycle), manual entry, CV%, observations needed (95% confidence, ±5%), rating and allowance → SAM; one tap puts it on the OB, with a check on large changes |
| Order and shipment | Order quantity and ship date per line; made, remaining, average pace, expected finish (Friday off) and late-shipment risk with the daily output needed |
| Downtime Pareto | Minutes lost by problem type across the floor, cumulative %, and estimated cost |
| Costing | Factory cost per minute (CPM); planned and actual sewing cost per piece; cost of today's inefficiency |

## ডিজাইন / Design

Indigo (dye), marigold (thread spool) and teal (thread) palette; Anek Bangla for headings and numbers, Hind Siliguri for text; light, dark and auto (device) theme switch in the header, remembered per device; works on phone, tablet, desktop and TV.

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
