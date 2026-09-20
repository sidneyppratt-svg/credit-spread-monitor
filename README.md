# Credit Spread Monitor
### Fixed Income Credit Research Tool | Sidney Pratt

---

## Overview
This model tracks the credit spread between High Yield bonds (HYG)
and Investment Grade bonds (LQD) to detect building stress in credit
markets. The spread is converted into a stress score from 1 to 5
using 16 years of real daily data from 2010 to 2026.

When investors flee from risky High Yield bonds toward safer Investment
Grade bonds the spread widens — one of the earliest and most reliable
warning signals of financial stress. This model detects that widening
in real time and classifies it against historical context.

---

## Key Features
- Live High Yield and Investment Grade bond data downloaded on every run
- Credit stress score from 1 (very calm) to 5 (high stress)
- Percentile ranking against full history since 2010
- 21-day rolling spread smoothing to filter daily noise
- Key stress period identification and annotation
- Two chart visualization — raw spread and stress score over time
- Dynamic signal and interpretation that updates with every run

---

## Why It Matters
Credit spreads are one of the most important leading indicators in
fixed income markets. When High Yield bonds underperform Investment
Grade bonds it signals that investors are pulling back from risk —
often weeks or months before stress shows up in equity markets.

- **Credit traders** watch spread widening as an early warning signal
- **Rates traders** use credit stress to anticipate Fed policy response
- **Portfolio managers** reduce risk exposure when spreads widen sharply
- **Risk managers** use spread levels to size positions and hedges

The 2008 financial crisis, 2011 European debt crisis, 2016 oil crash,
2020 COVID crash, and 2022 Fed rate hike cycle all showed up first
in credit spreads before hitting equity markets.

---

## Methodology
The model downloads daily price data for HYG (High Yield) and LQD
(Investment Grade). It calculates 21-day rolling mean returns for
each — smoothing daily noise to reveal trends.

The credit spread is calculated as LQD returns minus HYG returns
multiplied by 10,000 to convert to basis points. A wider spread
means High Yield is underperforming Investment Grade — a stress signal.

The spread is ranked as a percentile against all historical readings
in the selected date range and converted into a stress score from 1
to 5 using equal quintile bins.

**This methodology does not change regardless of the date range selected.**

---

## Stress Score Classification

| Score | Label | Interpretation |
|-------|-------|----------------|
| 1 | Very Calm | Credit markets extremely relaxed |
| 2 | Calm | Normal credit conditions |
| 3 | Moderate | Some caution warranted |
| 4 | Elevated | Credit stress building — watch closely |
| 5 | High Stress | Significant credit risk — reduce exposure |

---

## Asset Classes Covered

| Asset | Ticker | What It Represents |
|-------|--------|--------------------|
| High Yield Bonds | HYG | Loans to riskier companies — junk bonds |
| Investment Grade Bonds | LQD | Loans to safer, higher quality companies |
| US Equities | SPY | S&P 500 — used for context and comparison |

---

## Dynamic Results
*The following update every time the model is run based on selected dates.*

**Signal** — Current stress score from 1 to 5 based on the latest
spread reading relative to the full history in the selected date range.

**Strategy Signal** — Plain language guidance based on current stress
score — from very calm to high stress.

**Results** — Current spread in basis points, stress score, and
percentile rank versus full history since 2010.

**Summary & Key Findings** — Plain language explanation of what the
current credit spread level means for markets.

**What to Watch** — Specific indicators to monitor given the current
stress level including spread direction, equity correlation, and
Fed policy signals.

**Historical Context** — Key stress periods identified including
2011 EU Crisis, 2016 Oil Crash, 2020 COVID, and 2022 Fed hikes.

**Charts** — Two charts: credit spread over time with high and low
stress zones highlighted, and stress score over time with color
coded severity bands.

---

## Tools & Technologies
- **Python** — core programming language
- **yfinance** — live bond and equity price data
- **pandas & numpy** — data processing and calculations
- **matplotlib** — chart generation
- **Streamlit** — live interactive web application
- **Google Colab** — development environment

---

## Full Research Notebook
View the complete Credit Spread Monitor including all code, charts,
stress score analysis, and historical period breakdown:

github.com/sidneyppratt-svg/credit-spread-monitor

---

## About
Sidney Pratt is a Finance and Economics student at Western Michigan
University and an ACHA D1 hockey player building a quantitative
research portfolio targeted at fixed income trading internships.

sidneyppratt.com | github.com/sidneyppratt-svg
