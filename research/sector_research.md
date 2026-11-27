# Sector Research – ClearPath

## 1. Sector and company size

**Sector:** Everyday-life advice and support services in Germany

**Client:** Chleo, CEO of a medium-sized everyday-support company in Berlin (about 80 employees).

**What the company does today:** Consultants help people with any everyday problem in Germany – official letters, documents, registration, insurance, work, health, school, legal questions, emergencies and more – one by one, in person or by phone.

**Why company size matters:**
- **Why AI helps Chleo:** Her consultants spend much of their day answering the same simple questions (for example "How do I register my address?" or "What does this letter mean?"). ClearPath answers these instantly, so consultants have more time for difficult cases where a human is really needed.
- **Why a medium company is the right fit:** It has enough budget and possibly one IT person to introduce a small AI tool, but it is still flexible enough to try something new quickly.
- **Why not small or large:** A small company (under 50 people) usually lacks the money and IT staff. A large company (over 250 people) has many existing systems and strict rules, so introducing a new tool takes much longer.

**Who ClearPath serves:** Everyone living in Germany – Germans and non-Germans – who needs help with any everyday problem.

## 2. The problem

Everyday problems in Germany often mean dealing with authorities, official letters and forms – and many people find this hard. Official data shows it clearly:

**Dealing with authorities is complicated for many people**
- 39% of citizens found their contacts with authorities complicated (very, rather or partly). [1]
- The lowest-rated factors (scale –2 to +2) are: understandable law (0.5), online services (0.6), opening hours (0.7) and waiting time (0.7). Understandable forms (0.8) and official letters (0.9) are also below average (1.0). [1]
- 58% of citizens still communicate with authorities only on paper, while 95% use digital devices in their private life. [1]

**Some life situations are especially hard**
- The lowest-rated life situations are: court cases (0.5), divorce (0.6), tax return, unemployment, financial problems and old-age poverty (each 0.8). [1]
- These are exactly the stressful moments when people need clear guidance quickly.

**Many people also face a language barrier**
- About 14.07 million foreign citizens lived in Germany at the end of 2025. [2]
- This group is growing – for example, the number of Indian citizens rose from 124,095 (2018) to 311,130 (2025). [2]

**The market is everyone in Germany**
- 83.5 million people lived in Germany at the end of 2025 – all of them deal with authorities at some point. [3]

### Sources
[1] Destatis – Lebenslagenbefragung 2023, Bürgerinnen und Bürger (results report). Latest published edition; no 2025 edition was available at the time of research (November 2026). File: `data/life_events_survey_2023_report.pdf`
[2] Destatis – Foreign population by selected citizenships and years (Central Register of Foreigners, as at 31 Dec 2025; page as at 2 April 2026). https://www.destatis.de/EN/Themes/Society-Environment/Population/Migration-Integration/Tables/foreigner-citizenship-time-serie.html
[3] Destatis – press release "Bevölkerung Deutschlands sinkt im Jahr 2025 um 0,1 %" (June 2026). https://www.destatis.de/DE/Presse/Pressemitteilungen/2026/06/PD26_203_124.html

## 3. The data we use

The rule for this project: public or synthetic data only – no real company data and no real personal data.

| Dataset | Source | What it shows | Why it fits |
|---|---|---|---|
| `data/life_events_satisfaction_2023.csv` | Destatis, Lebenslagenbefragung 2023, Table 1 [1] | Satisfaction (–2 to +2) for 23 life situations × 17 factors (e.g. waiting time, understandable forms, online services) | Shows where people struggle most with authorities – the core problem ClearPath solves |
| `data/foreign_population_by_citizenship_2018_2025.csv` | Destatis, Central Register of Foreigners [2] | Foreign residents in Germany by citizenship, 2018–2025 | Shows the size and growth of a key user group facing a language barrier |
| Total population (83.5 million, end of 2025) | Destatis press release [3] | All people living in Germany | Shows the full market: everyone deals with authorities |

**How the data was checked**
- Both CSV files were converted directly from the official Destatis sources.
- Values were checked by hand against the original PDF and web page (3 sample values each – all matched).
- Destatis rounds foreign population numbers to multiples of 5 for privacy, so totals can differ by up to 5 from the sum of the parts.
- Cells marked "/" in the survey (too few answers) are left empty – no values were invented.

**Four checks before choosing the data** (from the course brief)
- **Fits the company?** Yes – it describes the everyday problems Chleo's consultants handle.
- **Big and clean enough?** Yes – official national statistics (7,573 survey respondents; full population register).
- **Has the columns we need?** Yes – life situations, problem factors, scores, citizenship and years.
- **Allowed to use it?** Yes – public data; Destatis allows reuse with the source named.

## 4. Why AI fits this problem

The data shows people struggle most with **understanding** (law, forms, official letters), **finding information online** and **waiting** for help. These are exactly the things modern AI does well:

| Problem (from the data) | How AI helps |
|---|---|
| Understandable law (0.5), forms (0.8) and official letters (0.9) score low | AI explains complex official language in simple words – and can read a photo of a letter |
| Online services score low (0.6) | One simple app where people ask any question, instead of searching many websites |
| Waiting time and opening hours score low (0.7) | AI answers 24/7, in seconds |
| Many residents don't speak German well | AI understands and answers in 10 languages, by voice and text |
| Hard life situations (job loss, divorce, court) | AI gives a clear step-by-step plan and says when a human expert is needed |

**What AI does NOT do (by design)**
- It does not make decisions about people (no visa, benefit or legal decisions).
- It does not give medical or legal advice – only general guidance and the right contact.
- In emergencies it always says "Call 112 / 110" first.
- Every answer shows its official source, so people can check it.

**Why this matters for Chleo:** Chleo fears AI is a black box. ClearPath is the opposite: every answer is based on official sources, shows where it comes from, and hands complex cases to her human consultants.