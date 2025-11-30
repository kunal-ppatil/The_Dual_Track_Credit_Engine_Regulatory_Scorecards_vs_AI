# The_Dual_Track_Credit_Engine_Regulatory_Scorecards_vs_AI
Dual-track credit decision engine comparing a regulatory-compliant Logistic Regression (using Weight of Evidence/OptBinning) against an AI Challenger (XGBoost) with alternative data. Includes a Strategy Layer that optimizes approval thresholds for financial profit rather than just accuracy.

# 🏦 Dual-Track Credit Decision Engine: AI vs. Regulatory Scorecards

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![Library](https://img.shields.io/badge/OptBinning-Credit%20Scoring-orange)
![Model](https://img.shields.io/badge/XGBoost-Challenger-green)
![Status](https://img.shields.io/badge/Strategy-Profit%20Optimized-red)

A comprehensive simulation of a modern banking credit risk pipeline. This project compares **Track A (The Banker)**, a regulatory-compliant Logistic Regression model using Weight of Evidence (WoE) binning, against **Track B (The Challenger)**, an XGBoost model leveraging Alternative Data.

Most importantly, it evaluates performance not just on AUC, but on **Net Profit ($)**, demonstrating the tangible business value of AI adoption.

We built the code, and GPT helped polish it for clarity.

## 📖 About The Project

**The Problem:** Traditional banks often reject "Thin-File" borrowers—young people or immigrants who are financially responsible but lack a long credit history. Banks rely on rigid metrics like Debt-to-Income ratio, missing out on millions of reliable customers ("Invisible Primes").

**The Solution:** This project builds a **Dual-Track Credit Engine** to demonstrate how AI and Alternative Data can solve this inefficiency without ignoring regulatory requirements.

It simulates a "Challenger Bank" environment where two models compete:
1.  **The Banker (Track A):** A traditional, regulatory-compliant Scorecard using **Logistic Regression** and **Weight of Evidence (WoE)** binning. It is safe, interpretable, and standard in the industry.
2.  **The Challenger (Track B):** An AI-driven **XGBoost** model that incorporates **Alternative Data** (e.g., utility payment consistency, digital footprint). It captures complex, non-linear patterns that linear models miss.

**The Goal:** To prove that by using AI to analyze alternative data, we can approve more borrowers, maintain low default rates, and significantly increase the **Net Portfolio Profit**.

## 🏗️ The Architecture

### 1. Data Simulation (Traditional vs. Alternative)
We simulate a realistic "Thin-File" borrower scenario:
* **Traditional Data:** Age, Income, Debt-to-Income Ratio.
* **Alternative Data:** Utility Payment Consistency, App Usage behaviors.
* *Hypothesis:* Traditional metrics unfairly penalize young/low-income borrowers who are actually reliable (high utility consistency).

### 2. Track A: The Banker (Regulatory Standard)
This track builds a **Credit Scorecard** strictly adhering to banking regulations (e.g., Basel III).
* **Library:** `optbinning` (Industry standard for monotonic binning).
* **Method:** Weight of Evidence (WoE) transformation $\rightarrow$ Logistic Regression.
* **Why:** This ensures the model is interpretable and linear (Risk must strictly increase as credit score drops).

### 3. Track B: The Challenger (AI Innovation)
This track uses modern Machine Learning to find non-linear risk patterns.
* **Model:** XGBoost Classifier.
* **Features:** Uses ALL data, including Alternative Data.
* **Why:** To capture complex relationships (e.g., low income is fine *if* utility payments are perfect).

### 4. Strategy Layer: Financial Optimization
We move beyond accuracy metrics (AUC) to financial metrics (Profit).
* **Loan Economics:** Average Loan $10k, Interest 18%.
* **Optimization:** We calculate the Net Profit curve across all approval thresholds to find the "Sweet Spot" for lending.

---

## 🚀 Installation & Usage

1.  **Install dependencies:**
    ```bash
    pip install optbinning xgboost scikit-learn pandas matplotlib
    ```

2.  **Run the analysis:**
    ```bash
    python main.py
    ```

---

## 📊 Key Results

The simulation consistently demonstrates:
* **AUC Uplift:** The AI model typically outperforms the traditional model by 10-15% in AUC.
* **Revenue Increase:** By identifying good customers that the traditional model rejected ("Swap-Ins"), the AI strategy typically yields a **15-20% increase in Net Portfolio Profit**.
* **Swap Set Analysis:** The AI successfully identifies "Invisible Primes"—borrowers with thin credit files but high repayment reliability.

---

## ⚠️ Disclaimer
This project uses synthetic data for educational purposes. `optbinning` is a powerful tool used in real production environments; please refer to the official documentation for advanced constraints and monotonicity enforcement.
