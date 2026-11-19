# How Efficient Are Nepal's Banks? (DEA Project)

This project checks **how well 20 commercial banks in Nepal use what they have** (money, staff and costs) **to produce results** (loans, interest income and profit).

It uses a method called **Data Envelopment Analysis (DEA)**, built in **Excel with Solver and VBA macros**.

It was my final project for the **OIE 548 Performance Analytics** course at Worcester Polytechnic Institute (WPI).

---

## Why this matters

Nepal is a small country, but it has a lot of banks. The central bank, **Nepal Rastra Bank**, wants weaker banks to merge so the system becomes stronger and safer.

This project asks a simple question: **Which banks are doing well, and which ones could gain the most from a merger?**

---

## What is DEA? (in plain words)

Think of each bank as a machine:

- **What goes in (inputs):** money spent, people hired, deposits collected
- **What comes out (outputs):** loans given, interest earned, profit made

DEA compares all the banks with each other. It finds the banks that get the **most output from the least input**. Those banks get a score of **1 (fully efficient)** or higher. Banks below 1 are wasting some resources compared to the best ones.

| Inputs (what the bank uses) | Outputs (what the bank produces) |
|---|---|
| Operating Expenses | Total Loans and Advances |
| Number of Employees | Interest Income |
| Total Deposits | Net Profit After Tax |

---

## The three models I used

1. **Balanced Benchmarking**: every input and output counts equally. A simple first check.
2. **Super-Efficiency (CRS)**: assumes bigger banks should get proportionally bigger results ("constant returns to scale"). It lets efficient banks score **above 1**, so we can rank even the best banks.
3. **Super-Efficiency (VRS)**: allows for the fact that size can help or hurt ("variable returns to scale").

Small **VBA macros** run Excel Solver for every bank automatically, so you don't have to run it by hand 20 times.

---

## Main results

- **Fully efficient (score = 1) in Balanced Benchmarking:** Nabil, Everest, Standard Chartered, Himalayan, NMB and Prime Commercial Bank.
- **Top banks in CRS Super-Efficiency:** Standard Chartered (**2.11**), Prime Commercial (**1.31**), Nabil (**1.14**).
- **Top banks in VRS Super-Efficiency:** Standard Chartered (**2.29**), Prime Commercial (**1.32**), Himalayan (**1.09**).
- **Lowest score in both CRS and VRS:** Rastriya Banijya Bank.
- **Average VRS score:** about **0.69**, so many banks are working well below their potential.
- **Nabil and Global IME** could not be scored in the VRS model ("infeasible"). This usually means they are already at the top and there is nobody better to compare them with.

**Bottom line:** only a few banks are truly efficient. This supports Nepal Rastra Bank's push for mergers between weaker and stronger banks.

---

## What's in this repo

| File | What it is |
|---|---|
| `BBBidhanAdhikari_Final Project_ Performance Analytics.pdf` | The full written report (15 pages) |
| `BidhanAdhikari_FinalProject_ExcelFile-1.xlsm` | The Excel model with data, Solver setup and VBA macros |
| `FinalprojectPresentation_PerformanceAnalytics_Bidhan Adhikari-1.pptx` | The presentation slides (11 slides) |

### Sheets inside the Excel file

| Sheet | What it does |
|---|---|
| `Data Collection` | The raw numbers for each bank (inputs and outputs) |
| `Balanced Benchmarking` | Model 1: equal weights |
| `SuperEfficiency(CRS)` | Model 2: constant returns to scale |
| `SuperEfficiency(vrs)` | Model 3: variable returns to scale |

---

## How to open and run it

1. Download or clone this repo.
2. Open the `.xlsm` file in **Microsoft Excel** (Windows works best).
3. When Excel asks, click **Enable Content** so the macros can run.
4. Turn on **Solver**: go to **File > Options > Add-ins > Manage: Excel Add-ins > Go**, tick **Solver Add-in**, then click OK.
5. Go to any model sheet and run the macro to recalculate the scores.

> Macros only run if you trust the file. These are simple macros that run Solver. Nothing else.

---

## Where the data came from

- Bank annual reports (official numbers)
- [ShareSansar](https://www.sharesansar.com/) and SmartWealth Pro (financial data websites)
- Bank staff, contacted directly when the number of employees was missing

When website numbers didn't match the annual reports, I used the annual report numbers.

---

## Limits

- Only 3 inputs and 3 outputs, so some parts of bank performance are not covered.
- Only **one year** of data. Results can change from year to year.

## Ideas for the future

- Add more inputs and outputs (for example, bad loans or number of branches).
- Use several years of data to see trends.
- Compare Nepal's banks with banks in other countries of similar size.

---

## Tools used

Excel · Solver (linear programming) · VBA · PowerPoint

## Author

**Bidhan Adhikari**, MS Business Analytics, Worcester Polytechnic Institute
[LinkedIn](https://www.linkedin.com/in/bidhan-adhikari-a67582269)
