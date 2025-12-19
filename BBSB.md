# **BadeBhaiSaab Product Concept: Pillar 1 Blueprint**
# **User Onboarding & AI Financial Profiling (The Core Engine)**

| Document Version | Date | Status | Prepared By |
| :--- | :--- | :--- | :--- |
| **2.0 (Micro-Detail Blueprint)** | December 19, 2025 | Ready for Engineering & Design | Product Management Office (PMO) |
| **Pillar Scope** | The entire user journey from initial download to final eligibility decision. |

***

# **Table of Contents**

| Section | Title | Page |
| :--- | :--- | :--- |
| **I.** | **Strategic Mandate & Pillar Goals** | 3 |
| 1.1 | Strategic Mandate: The 360° Profile | 3 |
| 1.2 | Success Metrics & KPIs for Pillar 1 | 4 |
| 1.3 | Target User Profile (Initial Pilot Focus) | 5 |
| **II.** | **The Onboarding Funnel: High-Level Flow & Decision Tree** | 6 |
| 2.1 | The 4-Stage Onboarding Flow | 6 |
| 2.2 | Key Decision Point: API vs. Manual Input | 7 |
| 2.3 | Key Decision Point: Eligible vs. Counseling-First | 8 |
| **III.** | **Data Collection Strategy & Technical Specifications** | 9 |
| 3.1 | Strategy A: Account Aggregator (AA) API Data Ingestion | 9 |
| 3.2 | Strategy B: Credit Bureau API Data Ingestion | 11 |
| 3.3 | Strategy C: User-Input Data & Guided Questionnaires | 12 |
| 3.4 | Strategy D: OCR & Document Processing (The Fallback) | 14 |
| 3.5 | Mandatory Data Matrix & Security Requirements | 15 |
| **IV.** | **Screen-by-Screen UX & Content Flow (The Incentivized Journey)** | 16 |
| 4.1 | Stage 1: The Trust & Consent Block | 16 |
| 4.2 | Stage 2: The Core Data Submission (Credit & Cashflow) | 19 |
| 4.3 | Stage 3: Assets, Liabilities, & Behavior Questions | 23 |
| 4.4 | Stage 4: Profile Submission & Reward Allocation | 27 |
| **V.** | **The AI Engine: Alternative Credit Score (ACS) Logic Breakdown** | 29 |
| 5.1 | Model 1: Credit History & Behavior Score (CHBS) | 30 |
| 5.2 | Model 2: Cashflow & Spending Patterns (CSP) | 32 |
| 5.3 | Model 3: Assets & Resilience Score (ARS) | 34 |
| 5.4 | Model 4: Liability Prioritization Engine (LPE) | 36 |
| 5.5 | The Final Alternative Credit Score (ACS) Formula | 38 |
| **VI.** | **The Eligibility Gate: Decision Matrix & Routing** | 40 |
| 6.1 | The Three-Factor Eligibility Rule | 40 |
| 6.2 | Outcome A: Membership-Eligible User Routing | 41 |
| 6.3 | Outcome B: Counseling-First User Routing | 42 |
| **VII.** | **Post-Profiling Outputs & Conclusion** | 44 |
| 7.1 | The Personal Financial Report (PFR) Detail | 44 |
| 7.2 | Final Summary and Key Performance Indicators (KPIs) | 46 |

***
# **I. Strategic Mandate & Pillar Goals**

## **1.1 Strategic Mandate: The 360° Profile**

The strategic mandate of the **User Onboarding & AI Financial Profiling** pillar is to solve the dual problem articulated in the Product Concept Note: **Limited Access to Credit** and **Poor Financial Visibility & Guidance** (P1).

| Strategic Goal | Problem Addressed | Pillar 1 Solution | Core Technology |
| :--- | :--- | :--- | :--- |
| **Credit Inclusion** | The "credit-invisible" lack formal documentation, leading to complete exclusion from formal credit (P4, P5). | **AI-Driven Financial Profiling** (P1): Assesses creditworthiness based on *cash flow* and *asset ownership* (P5). | Alternative Credit Score (ACS) Model |
| **Debt Spiral Prevention** | Late fees, penalties, and high-interest short-term borrowing cause credit score damage (P1, P4). | **Liability Prioritization Engine** (P10): Determines the most damaging liability to clear first with the Short-Term Interest-Free Credit (P2). | Liability Prioritization Engine (LPE) |
| **Behavioral Change** | Nearly 45% of Indians have never checked their credit score. Lack of visibility makes budgeting and debt consolidation hard (P1). | **Personal Financial Report (PFR)** (P11): Provides a simple, visual diagnosis of financial health, setting the stage for advisory. | Cashflow & Spending Patterns Model (CSP) |

### **Goal of User Onboarding**

To achieve $\mathbf{100\%}$ data integrity and $\mathbf{>65\%}$ conversion rate for the full profile submission through a secure, incentivized, and transparent process, thereby mitigating data scarcity and high acquisition cost risks (P5).

### **Goal of AI Financial Profiling**

To generate an $\mathbf{ACS}$ that is $\mathbf{>15\%}$ more predictive of $\mathbf{90+ DPD}$ default risk for the target cohorts (gig workers, students) than the traditional CIBIL/Experian score alone, by incorporating alternative data.

## **1.2 Success Metrics & KPIs for Pillar 1**

The success of the entire program hinges on the metrics defined below.

| Metric | Definition | Target Goal (Pilot Phase) | Owner |
| :--- | :--- | :--- | :--- |
| **Full Profile Conversion Rate** | (% of users who complete all 4 Stages / % of users who start Stage 1). | **>65%** | PM, UXD |
| **API Adoption Rate** | (% of users who successfully link via AA/Bureau API / Total users). | **>80%** | TL, PM |
| **Document Integrity Score (DIS) Avg.** | Average score from the Document Tampering Algorithm (1.3.4). | **>95/100** | AI/ML, CRA |
| **OCR Accuracy** | Accuracy of parsing key data fields (e.g., transaction amount) from manual uploads. | **>98%** | AI/ML |
| **Non-Credit Cost-to-Serve (CTS) Reduction** | Reduction in human time spent on manual data entry/verification. | **>70%** | Operations Head |
| **ACS Predictive Power** | AUC (Area Under the Curve) score for ACS predicting $\mathbf{90+ DPD}$. | **AUC > 0.75** (on pilot data) | DS, CRA |
| **Counseling-First Engagement Rate** | (% of non-eligible users who complete the first 3 counseling modules). | **>50%** | PM, Operations Head |

## **1.3 Target User Profile (Initial Pilot Focus)**

The entire flow is optimized for the strategic pilot cohorts: **Urban Low-Income Earners (Gig Economy)** and **Young Individuals & Students** (P8).

| Attribute | Urban Low-Income Earners (Gig) | Young Individuals & Students | Onboarding Optimization |
| :--- | :--- | :--- | :--- |
| **Financial Challenge** | Income volatility, irregular/daily/weekly income (P4). | Thin credit file, credit naivety, poor financial habits (P6). | Focus on *Cashflow* data; gamified advice. |
| **Digital Acumen** | High smartphone penetration, reliance on apps (P4). | Highly tech-savvy, digitally native (P6). | **Prioritize API/Digital Acquisition** (Low Acquisition Cost) (P8). |
| **Data Richness** | Alternative Data Rich: Platform earnings, location data (P4). | Thin File Problem (Limited credit history) (P6). | **OCR/Manual Upload** must be robust for non-AA data. |
| **Engagement** | High Churn risk if membership fee/credit is insufficient (P4). | High Engagement potential with AI/Gamification (P6). | **Incentivized Flow & Instant Reward** upon completion (P10). |

***
# **II. The Onboarding Funnel: High-Level Flow & Decision Tree**

The onboarding is a **Non-Linear, Incentivized Guided Journey** designed to secure maximum data at minimum cost while building trust.

## **2.1 The 4-Stage Onboarding Flow**

| Stage | Goal | Key Activity | Output for AI | Incentivization Model |
| :--- | :--- | :--- | :--- | :--- |
| **Stage 1: Trust & Vetting** | Establish trust, confirm target user criteria, secure KYC & Consent. | KYC (PAN/Aadhaar) submission, Target Score Check (<750), Data Privacy Consent. | KYC Data, Initial Score Check. | **Voucher/Bonus** for Consent (e.g., ₹50 mobile recharge voucher). |
| **Stage 2: Core Data Submission** | Ingest the highest-value data (Cashflow & Credit History). | API: Account Aggregator (AA) linking $\mathbf{OR}$ Manual Upload/OCR of Bank Statements (P10). API: Credit Bureau Report Pull (P10). | Raw Transactions (12M), Official Credit Report. | **High Point Allocation** for AA linking/OCR processing (P10). |
| **Stage 3: Profiling Data (Guided Input)** | Collect high-context, low-friction data points on assets, liabilities, and behavior. | Short, guided questions on assets (FD, Property), secondary liabilities (fines, utility bills), and financial behavior. | Assets/Investment Data, Secondary Liability Data, Behavioral Flags. | **Bonus Points** for each completed section. |
| **Stage 4: AI Processing & Decision** | The back-end runs the AI models and generates the final user output. | **User Wait Screen** (5-10 seconds) while 4 models run (P3). **AI Model Run:** OCR, CHBS, CSP, ARS, LPE, ACS. | Alternative Credit Score (ACS), Personal Financial Report (PFR), Eligibility Decision. | **Final Joining Bonus** (can be applied to Membership Fee/First Liability) (P10). |

## **2.2 Key Decision Point: API vs. Manual Input**

This decision point is crucial for the **Digital Accessibility** of the program (P4). The UX must *strongly* guide the user to the API path, while the Manual path must be robust and secure.

| Decision Path | Interaction Flow | Goal | Handoff |
| :--- | :--- | :--- | :--- |
| **API Path (Preferred)** | User selects AA/Bureau $\rightarrow$ Consent Screen $\rightarrow$ OTP/Verification $\rightarrow$ Data fetched seamlessly. | **Efficiency & Data Quality:** Highest quality, structured data immediately. Highest Acquisition Efficiency (P4). | **Raw Transactions (Structured JSON)** to CSP Model. |
| **Manual Path (Fallback)** | User selects Manual $\rightarrow$ Guided Upload Wizard for Bank Statements/Bills/Credit Report (PDF/Image). | **Inclusion & Resilience:** Caters to low digital literacy and non-AA-compliant documents. | **Raw Documents (PDF/Image)** to OCR/Parsing Engine (P10, P12). |

## **2.3 Key Decision Point: Eligible vs. Counseling-First**

This is the final outcome of Pillar 1, powered by the AI Engine.

| Outcome Path | ACS Trigger | Initial Offering | Goal of Routing |
| :--- | :--- | :--- | :--- |
| **Outcome A: Membership-Eligible** | Profile indicates **positive cashflow potential** and **limited/resolvable delinquencies** (P11). | Access to **Liability-Free (0% interest) Credit** and Free/Paid Membership Tiers (P11). | **Credit Graduation:** Start structured repayment and build credit score (P2, P6). |
| **Outcome B: Counseling-First** | Profile indicates **chronic defaults, severe instability, or unsustainable repayment capacity** (P11). | **Human Financial Counseling** and Content Flywheel (P11). **NO Credit** is extended (P11). | **De-risking & Re-engagement:** Stabilize behavior, control expenses, prepare for future eligibility (P11, P12). |

***
# **III. Data Collection Strategy & Technical Specifications**

This section outlines the exact data fields required, their source, and the technical method of collection.

## **3.1 Strategy A: Account Aggregator (AA) API Data Ingestion**

This is the primary data source for **Cashflow & Spending Patterns (CSP)** and must cover a minimum of **12 months** of data (24 months preferred).

### **AA API Specification: `GET /financial-transactions`**

| Field Name | Type | Data Requirement | Purpose in AI Model |
| :--- | :--- | :--- | :--- |
| **`transaction_date`** | Date/Time | $\mathbf{12 M}$ lookback, normalized to UTC. | Income Volatility Index (IVI) calculation (5.2). |
| **`transaction_amount`** | Numeric | Absolute value in INR. Must be separated by Cr/Dr. | Surplus/Deficit Metrics (5.2). |
| **`transaction_type`** | Enum (CREDIT/DEBIT) | Essential for income/expense categorization. | Spending Patterns (Essential vs. Discretionary) (P1). |
| **`transaction_narration`** | String | Bank description (e.g., "NEFT to LENDER\_X"). | **Lender Identification** (Input to LPE) and income source verification. |
| **`account_balance`** | Numeric | End-of-day balance. | **Low Savings Flag** (5.2) and Asset Verification (5.3). |
| **`loan_repayment_flag`** | Boolean (Internal Logic) | Flag transactions matching known EMI amounts/lender names. | **Track Discipline** (Input to CHBS) (5.1). |

## **3.2 Strategy B: Credit Bureau API Data Ingestion**

This is the primary data source for **Credit History & Behavior Score (CHBS)** (P1). Collection is mandatory via API pull (Task 1.3.5) upon user consent.

### **Bureau API Specification: `GET /credit-report`**

| Field Name | Type | Data Requirement | Purpose in AI Model |
| :--- | :--- | :--- | :--- |
| **`credit_score_trad`** | Integer | The traditional CIBIL/Experian score. | Input to ACS Formula (P11), Eligibility Gate (P11). |
| **`total_outstanding_loan`** | Numeric | Total principal amount across all accounts. | Debt-to-Income (DTI) Ratio, LPE (5.4). |
| **`days_past_due_matrix`** | Array | List of DPD flags (30, 60, 90+) for all loans (24M history). | Core of Behavior Score (5.1). |
| **`credit_utilization_ratio`** | Percentage | Ratio of credit used to total limit across all cards/lines. | **High Utilization Risk** flag (P10, 5.1). |
| **`age_of_oldest_account`** | Integer (Months) | Time since the first credit account was opened. | Credit History Depth (5.1). |
| **`enquiry_count_6m`** | Integer | Number of hard inquiries in the last 6 months. | **Credit Hunger** flag (P10, 5.1). |

## **3.3 Strategy C: User-Input Data & Guided Questionnaires**

This data is collected via guided, high-context screens (Stage 3) to fill critical gaps not covered by APIs.

### **User-Input Specification: Guided Wizard**

| Question / Input Field | Interaction Type | Data Type | Purpose in AI Model |
| :--- | :--- | :--- | :--- |
| **Employment Type** | Multi-Select/Search | Enum (Gig/Salaried/Self-Employed/Student) | IVI Expectation Setting (5.2). |
| **Platform Earning Verification (Gig)** | Text Input / Platform Login (Optional) | String (Platform name) | Alternative Income Source Check (5.2). |
| **Secondary Liabilities (Unreported)** | Guided List | String/Numeric | Utility bills, credit card minimums, pending fines (LPE Input) (P2, P10). |
| **Asset Ownership: Property** | Yes/No $\rightarrow$ Upload Proof | Boolean/Document | Resilience Score (5.3). |
| **Asset Ownership: Insurance/FD** | Yes/No $\rightarrow$ Upload Proof | Boolean/Document | Resilience Score (5.3). |
| **Financial Literacy Self-Assessment** | 3-Question Quiz (Internal) | Integer Score (1-10) | Behavior Flag for Counseling Path (6.3). |

## **3.4 Strategy D: OCR & Document Processing (The Fallback)**

For the 20% of users who cannot use the AA API, this system converts their manual uploads into the required structured data format (3.1).

### **OCR Extraction Specification: Required Fields (Mandatory for Compliance)**

| Document Type | Mandatory Fields for Extraction | OCR Tooling Required |
| :--- | :--- | :--- |
| **Bank Statements (PDF/Image)** | Account Holder Name, Statement Date Range, **All Transactions (Date, Amount, Narration)**. | Advanced Indian Fintech OCR (Perfios/Glib.ai-level) (P10). |
| **Loan Schedules (PDF/Image)** | Lender Name, Loan Amount, **Monthly EMI Value**, **Next Due Date**. | Advanced Table/Schema-less Parsing. |
| **Identity/KYC Proofs (PAN/Aadhaar)** | Name, Date of Birth, Address, Document ID. | Basic Image-to-Text OCR (for data verification). |

## **3.5 Mandatory Data Matrix & Security Requirements**

| Data Set | Collection Method | Mandatory Field Count | Security Requirement |
| :--- | :--- | :--- | :--- |
| **KYC & Identity** | User Input/OCR | 4 | **Encryption at Rest (AES-256)**, Masking in UAT/Staging. |
| **Credit Report** | Bureau API | 6 | **Tokenized Access**, Regulatory Audit Trail (P10). |
| **Cashflow (12M)** | AA API/OCR | 5 | **Anonymization for Model Training**, Consent Logging (P11). |
| **Assets & Resilience** | User Input/OCR | 3 | **Two-Factor Verification** for sensitive uploads. |

***
# **IV. Screen-by-Screen UX & Content Flow (The Incentivized Journey)**

This section details the exact user interface (UI) and content for the non-linear, 4-Stage Onboarding flow, ensuring a supportive and highly engaging experience (P12, P15).

## **4.1 Stage 1: The Trust & Consent Block (5 Minutes)**

| Screen ID | Screen Title & Goal | User Interaction | Key Content/Tone | Handoff/Next Step |
| :--- | :--- | :--- | :--- | :--- |
| **S1.1** | **Welcome & Value Proposition** **Goal:** Confirm the user is a target cohort and communicate the 360° benefit. | Single Button: "Start My Financial Profile" | **Headline:** "Move Beyond Your Credit Score. Get Rewarded for Your Resilience." **Body:** "If your score is below 750 or you are new to credit, we can help. Our AI builds a 360° profile to find credit you deserve." | S1.2 |
| **S1.2** | **KYC & Identity Verification** **Goal:** Collect mandatory KYC/AML data. | 1. PAN/Aadhaar Upload (Image/PDF). 2. OTP Verification via Aadhaar-linked phone. | **Headline:** "First Step: The Trust Block." **Note:** "This is mandatory for all formal financial services in India." | S1.3 |
| **S1.3** | **Data Consent & Privacy** **Goal:** Secure legal consent for data sharing/processing and build trust. | Checkbox: "I consent to [BadeBhaiSaab] securely processing my financial data..." $\rightarrow$ Button: "I Understand & Consent (Earn ₹50 Bonus!)" | **Headline:** "Why We Need Your Full Picture." **Body:** "We use advanced encryption. Your data is never sold. We only use it to give you the best advice and 0% interest credit." (P11, P15) | Trigger **₹50 Mobile Recharge Voucher**. S2.1 |

## **4.2 Stage 2: The Core Data Submission (Credit & Cashflow) (8-10 Minutes)**

This is the most critical stage, where $\sim 80\%$ of the AI input data is collected.

| Screen ID | Screen Title & Goal | User Interaction | Key Content/Tone | Handoff/Next Step |
| :--- | :--- | :--- | :--- | :--- |
| **S2.1** | **The Profile Checklist & Reward Preview** **Goal:** Show the user what's left and incentivize the most complex steps. | Progress Bar (30% Complete). Dynamic List with points: **Link Bank (500 pts)**, **Link Credit (300 pts)**, etc. | **Headline:** "Your Road to the Final Offer." **Tip:** "Linking your accounts via API is 5X faster and earns the most rewards!" (P10) | S2.2 |
| **S2.2** | **Credit Report Integration** **Goal:** Get the official Credit History Data (Task 1.3.5). | **Option A (Preferred):** API Login (via partner or OTP). **Option B (Fallback):** Upload CIBIL/Experian PDF. | **Headline:** "Get Credit for Your Past Discipline." **Prompt:** "To understand your credit journey, we pull your official score." | S2.3 (API success $\rightarrow$ S2.4) |
| **S2.3** | **Cashflow Data: API Preference** **Goal:** Strongly encourage AA linking. | **Option A (Preferred):** Button: "Link Bank Accounts Securely (500 Points!)" $\rightarrow$ AA Flow. **Option B (Fallback):** Button: "Upload Bank Statements (PDFs)" | **Headline:** "Your Income & Spending: The True Measure." **Body:** "Traditional scores ignore your cashflow. We need 12-24 months of data to find your true potential." (P1, P11) | S2.4 |
| **S2.4** | **Manual Upload Wizard (If S2.3 Option B)** **Goal:** Reduce friction and capture clean OCR data. | **Wizard:** 1. Select Bank Name. 2. Upload PDF. 3. Confirm Date Range. (Repeat for 2-3 accounts). | **Headline:** "Uploading Documents (Automated Scan)." **Note:** "Our AI will read these documents for you. Please use clear PDF files only." (P10) | S3.1 |

## **4.3 Stage 3: Assets, Liabilities, & Behavior Questions (6-8 Minutes)**

This stage collects high-context data that powers the **Resilience Score** and the **Liability Prioritization Engine**.

| Screen ID | Screen Title & Goal | User Interaction | Key Content/Tone | Handoff/Next Step |
| :--- | :--- | :--- | :--- | :--- |
| **S3.1** | **Financial Resilience: Assets** **Goal:** Collect non-traditional asset data (Task 1.4.3). | **Guided Question Tree:** 1. "Do you have any Fixed Deposits, RDs, or Gold?" (Y/N). 2. "Do you have any Life or Health Insurance policies?" (Y/N). 3. "Do you own property?" (Y/N) $\rightarrow$ If Yes, "Upload Proof (Optional, for higher limit)." | **Headline:** "Show Us Your Safety Net (100 Bonus Points)." **Tip:** "Assets like insurance show financial discipline and can unlock higher limits." (P15) | S3.2 |
| **S3.2** | **Secondary Liabilities & Fines** **Goal:** Capture liabilities *not* reported on the credit bureau (P2, P10). | **Guided Input:** 1. Input: "Pending Electricity/Water Bills." 2. Input: "Unpaid Phone/Internet Bills." 3. Input: "Outstanding Credit Card Minimum Payments." | **Headline:** "Let's Prioritize the Small, Damaging Debts." **Note:** "Fines and late fees quickly damage your score. Tell us the amount so we can clear them first." | S3.3 |
| **S3.3** | **Behavior & Literacy Self-Assessment** **Goal:** Collect a subjective Behavior Flag for counseling/advisory. | **3-Question Quiz:** 1. "How often do you budget?" (Never/Monthly/Weekly). 2. "I know my exact credit card interest rate." (True/False). 3. "Do you frequently use savings for unexpected bills?" (Y/N). | **Headline:** "A Quick Pulse Check on Your Habits." **Note:** "There are no wrong answers! This helps our AI give you the right advice." | S4.1 |

## **4.4 Stage 4: Profile Submission & Reward Allocation (1 Minute)**

| Screen ID | Screen Title & Goal | User Interaction | Key Content/Tone | Handoff/Next Step |
| :--- | :--- | :--- | :--- | :--- |
| **S4.1** | **Final Submission & Review** **Goal:** Confirm all data, start AI processing, and manage the user's wait time. | Button: "Submit My Full Profile & Get My Offer" | **Headline:** "Submission Complete. Your AI Profile is Building..." **Wait Screen:** *Animated graphic* showing data points converging into a 360° profile. (Max 10-second wait time). | S4.2 (Decision) |
| **S4.2** | **Reward Allocation & Next Step** **Goal:** Pay the final bonus and route the user to the appropriate outcome (A or B). | Dynamic Text $\rightarrow$ Button: "View My Personal Financial Report" | **Success Banner:** "Congratulations! You earned $\mathbf{1,200}$ Reward Points. Your initial offer is ready." **Dynamic Content:** *Content shifts based on the Eligibility Gate (VI).* | Outcome A $\rightarrow$ Membership Offer/PFR. Outcome B $\rightarrow$ Counseling Offer/PFR. |

***
# **V. The AI Engine: Alternative Credit Score (ACS) Logic Breakdown**

The ACS is a proprietary, weighted score (hypothetical range 100-1000) that is the core output of Pillar 1. It is the sole determinant of credit size and membership tier.

### **ACS Core Principle**

The ACS integrates four key models to overcome the "Thin File" and "Income Volatility" challenges of the target market (P4, P6).

$$\mathbf{ACS} = f(\mathbf{CHBS}, \mathbf{CSP}, \mathbf{ARS}, \mathbf{LPE})$$

## **5.1 Model 1: Credit History & Behavior Score (CHBS)**

**Model Goal:** Quantify the user's reliability and past financial discipline (P10).

### **CHBS Sub-Score Formula & Inputs**

| CHBS Component | Data Source | Weight (%) | Risk Threshold (Flag) | Output Score Range |
| :--- | :--- | :--- | :--- | :--- |
| **Days Past Due (DPD)** | Bureau API (3.2) | 40% | $\mathbf{>90 DPD}$ in last 12M $\rightarrow$ **High Risk Flag** | 100-300 |
| **Credit Utilization** | Bureau API (3.2) | 30% | $\mathbf{>75\%}$ Utilization $\rightarrow$ **Behavior Warning** | 100-300 |
| **Credit History Depth** | Bureau API (3.2) | 15% | $\mathbf{<24}$ Months History $\rightarrow$ **Thin File Flag** | 100-150 |
| **Recent Enquiries** | Bureau API (3.2) | 15% | $\mathbf{>4}$ Hard Inquiries in 6M $\rightarrow$ **Credit Hunger Flag** | 100-150 |
| **Total CHBS Score** | | **100%** | | **400-900** |

## **5.2 Model 2: Cashflow & Spending Patterns (CSP)**

**Model Goal:** Assess current income stability, *ability to pay*, and capacity for a short-term liability (P1, P10).

### **CSP Sub-Score Formula & Inputs**

| CSP Component | Data Source | Calculation Logic | Risk Threshold (Flag) | Output Score Range |
| :--- | :--- | :--- | :--- | :--- |
| **Income Volatility Index (IVI)** | AA/OCR (3.1) | $\mathbf{StDev(Monthly Income) / Avg(Monthly Income)}$. | $\mathbf{IVI > 0.6}$ (High Volatility) $\rightarrow$ **Pilot Risk Flag** | 100-300 |
| **Monthly Cashflow Surplus** | AA/OCR (3.1) | $\mathbf{Avg(Income) - Avg(Essential Expenses + Existing EMIs)}$. | $\mathbf{Surplus < 2 \times}$ Avg. Monthly Penalty $\rightarrow$ **Repayment Strain** (P11) | 100-300 |
| **Discretionary Spending Ratio** | AA/OCR (3.1) | $\mathbf{Total Discretionary Spending / Total Income}$. | $\mathbf{Ratio > 35\%}$ $\rightarrow$ **Advisory Trigger** (P1) | 100-150 |
| **Low Savings/Balance Flag** | AA/OCR (3.1) | Count of days in 12M where balance was $\mathbf{< \mathbf{₹}500}$. | $\mathbf{>50\%}$ of days $\rightarrow$ **Liquidity Crunch Flag** (P1) | 100-150 |
| **Total CSP Score** | | **100%** | | **400-900** |

## **5.3 Model 3: Assets & Resilience Score (ARS)**

**Model Goal:** Provide a compensating factor for credit-invisible users who demonstrate financial maturity through savings, investments, or assets (P1, P5).

### **ARS Sub-Score Formula & Inputs**

| ARS Component | Data Source | Calculation Logic | Weight (%) | Output Score Range |
| :--- | :--- | :--- | :--- | :--- |
| **Savings/FD Track Record** | AA/OCR/User Input (3.1, 3.3) | $\mathbf{Count}$ of recurring FD/RD transactions (inflow > 6M). | 40% | 100-300 |
| **Insurance Premium Payments** | AA/OCR/User Input (3.1, 3.3) | $\mathbf{Count}$ of recurring Life/Health premium debits (over 12M). | 35% | 100-300 |
| **Property Ownership Flag** | User Input/Document (3.3) | $\mathbf{Verified}$ Flag for self-owned property (even if mortgaged). | 25% | 100-300 |
| **Total ARS Score** | | **100%** | | **300-900** |

## **5.4 Model 4: Liability Prioritization Engine (LPE)**

**Model Goal:** Identify *what* liability the interest-free credit should tackle first (P10). This is a *Prioritization Index* rather than a score.

### **LPE Index & Output**

| LPE Component | Data Source | Weight Factor | Prioritization Logic | Output |
| :--- | :--- | :--- | :--- | :--- |
| **Credit Score Damage Index** | Bureau (3.2) & User Input (3.3) | **3X** | Highest weight to liabilities leading to $\mathbf{>30 DPD}$ or collection calls (P12). | **Priority 1 Liability (P1)** |
| **Late Fee/Penalty Multiplier** | Bureau (3.2) & User Input (3.3) | **2X** | Prioritize liabilities with $\mathbf{>5\%}$ late fee penalties (P2). | **Priority 2 Liability (P2)** |
| **Repayment Capacity Fit** | CSP (5.2) | **1X** | Liability amount must be $\mathbf{\le 80\%}$ of 90-day Cashflow Surplus (P12). | **Recommended Credit Allocation** (₹5k - ₹20k) (P12) |

## **5.5 The Final Alternative Credit Score (ACS) Formula**

The final ACS combines the three sub-scores using the strategic weighting model, where **Cashflow** is the dominant factor for the target cohort.

### **ACS Calculation (Weighted Average)**

$$\mathbf{ACS} = (\mathbf{CHBS} \times 0.35) + (\mathbf{CSP} \times 0.50) + (\mathbf{ARS} \times 0.15)$$

| Component | Strategic Weighting | Rationale |
| :--- | :--- | :--- |
| **Cashflow & Spending Patterns (CSP)** | **50%** | Highest weight to counter *income volatility* and assess *current capacity* (P4). |
| **Credit History & Behavior Score (CHBS)** | 35% | Traditional risk is important but secondary to current cashflow health. |
| **Assets & Resilience Score (ARS)** | 15% | Compensates for thin files and credits non-traditional savings discipline (P6). |

### **ACS Action Matrix**

| ACS Range (Hypothetical) | Eligibility Path | Initial Credit Line (LPE Output) |
| :--- | :--- | :--- |
| **< 400** | **Counseling-First (High Risk)** (VI.3) | $\mathbf{₹0}$ (No credit extended) (P11) |
| **400 - 550** | **Eligible - Silver Tier** (VI.2) | $\mathbf{₹5,000} - \mathbf{₹10,000}$ (Modest amount) (P12) |
| **> 550** | **Eligible - Gold Tier** (VI.2) | $\mathbf{₹10,000} - \mathbf{₹20,000}$ (Higher amount) (P12) |

***
# **VI. The Eligibility Gate: Decision Matrix & Routing**

This is the final logic step (Task 1.5.3) that routes the user to the appropriate program track based on the AI's final assessment.

## **6.1 The Three-Factor Eligibility Rule**

The system does *not* rely on the ACS alone. A user must pass three simultaneous risk checks to qualify for credit.

| Factor | AI Input Model | Threshold for Eligibility | Rationale |
| :--- | :--- | :--- | :--- |
| **Factor 1: Credit Potential** | Final ACS (5.5) | **ACS $\ge \mathbf{400}$** | Core measure of overall creditworthiness and discipline. |
| **Factor 2: Repayment Strain** | CSP (5.2) $\rightarrow$ Surplus Metric | **Cashflow Surplus $\ge \mathbf{2 \times}$ Avg. Monthly Penalty** | Must demonstrate *positive cashflow potential* (P11) for repayment. |
| **Factor 3: Behavioral Risk** | CHBS (5.1) $\rightarrow$ DPD Flag | **NO $\mathbf{>90 DPD}$ in the last 6 months** | Filters out *chronic defaulters* who require intensive, non-credit-based counseling (P11). |

$$\mathbf{Membership\ Eligible} \iff (\mathbf{Factor 1: True}) \land (\mathbf{Factor 2: True}) \land (\mathbf{Factor 3: True})$$

## **6.2 Outcome A: Membership-Eligible User Routing**

**Targeted User:** Demonstrates a path to solvency; needs short-term relief and behavioral guidance.

| Routing Action | System Trigger | Product Handoff (Pillar 2) |
| :--- | :--- | :--- |
| **Tiering Decision** | ACS score automatically assigns Silver/Gold tier (5.5). | **Fee Structure:** Present free/paid membership tiers (P11). |
| **Credit Offer Generation** | LPE output is used to generate the offer. | $\mathbf{90-Day\ Interest-Free\ Credit\ Line}$ offered, linked to the P1 liability (P2, P12). |
| **PFR Presentation** | PFR (7.1) focuses on *potential* and *next steps* (P11). | **Conversion Logic:** Clearly explains **why** they qualify and **what improves** with membership (P11). |

**Messaging Tone (PFR Summary Screen):**
> *“**Great News!** Based on your cashflow stability, you are **Eligible** for the BadeBhaiSaab program. We found a small gap in your savings, but your income is stable. Your **₹8,000 Interest-Free Credit Line** is ready to immediately clear your most damaging overdue fees and stop the collection calls.”*

## **6.3 Outcome B: Counseling-First User Routing**

**Targeted User:** High-risk, chronic defaulters, or users with unsustainably high Debt-to-Income (DTI) ratios. **NO Credit is Extended.**

| Routing Action | System Trigger | Product Handoff (Pillar 3) |
| :--- | :--- | :--- |
| **Credit Lock** | The system $\mathbf{does\ not\ push\ membership\ or\ credit}$ (P11). | **Human Financial Counseling (1:1/Small Group)** is offered as the **ONLY** immediate solution (P11). |
| **PFR Presentation** | PFR (7.1) focuses on *severity* and *urgent actions*. | **Content Flywheel:** Offer free access to the Education & Gamification modules (P11, P14). |
| **Re-evaluation Path** | System sets a **90-day cooling-off period** (P12). | **Action Plan:** User is prompted to complete specific modules and upload a 90-day *new* bank statement for re-evaluation (P12). |

**Messaging Tone (PFR Summary Screen):**
> *“**We're Here to Help.** Our analysis shows you currently have **Unsustainable Repayment Capacity**. We cannot offer you credit right now, as it would worsen your debt. However, you are **Eligible for FREE Human Financial Counseling** to restructure your debts and begin your path to eligibility. Your 90-Day Action Plan is ready.”* (P11, P12)

***
# **VII. Post-Profiling Outputs & Conclusion**

## **7.1 The Personal Financial Report (PFR) Detail**

The PFR (Task 1.5.1) is the core user-facing artifact, translating AI complexity into simplicity.

| PFR Section | AI Data Source | Visual Representation | Sample Output/Advice (P13) |
| :--- | :--- | :--- | :--- |
| **1. Overall Status** | ACS (5.5) / CHBS (5.1) | Score Dial / Status Color (Red/Amber/Green) | "Your score is 580 (Poor). You are flagged as **Medium Discipline**." |
| **2. Urgent Liabilities** | LPE (5.4) | Bar Chart: $\mathbf{P1} > \mathbf{P2} > \mathbf{P3}$ | "You have $\mathbf{₹10,000}$ in pending penalties/EMIs. Your 60-day overdue EMI is the most damaging." (P10) |
| **3. Cashflow Health** | CSP (5.2) | Line Graph: Income Fluctuation / Pie Chart: Spending Mix | "Your monthly cashflow surplus is only $\mathbf{₹500}$ (P11). Your IVI is High, suggesting irregular income." |
| **4. Behavioral Insight** | CSP (5.2) | Highlighted Transaction | "You spent $\mathbf{₹2000}$ on dining out last month, which is $\mathbf{10\%}$ of your income - consider cutting back to save for your EMI." (P13) |
| **5. Next Steps/Call to Action** | Eligibility Gate (6.1) | Single Button | **If Eligible:** "Claim your Interest-Free Credit Offer." **If Counseling:** "Book Your Free 1:1 Counseling Session." (P11) |

## **7.2 Final Summary and Key Performance Indicators (KPIs)**

The execution of Pillar 1 must be rigorously measured against the KPIs defined in Section 1.2. The primary metric for all engineering and data science teams is the **Full Profile Conversion Rate ($\ge 65\%$ target)**, as a failure here renders the AI model useless.

| Key Milestone | Deliverable | Success Criteria | Timeframe |
| :--- | :--- | :--- | :--- |
| **Data Readiness** | All AA, Bureau, and OCR pipelines integrated and tested. | $\mathbf{>98\%}$ OCR Accuracy; AA Adoption $\mathbf{>80\%}$. | Week 11 |
| **ACS Validation** | Final ACS v1.0 Model Deployed in Production. | $\mathbf{ACS\ AUC > 0.75}$ on Test Data. | Week 18 |
| **Go-Live** | Full End-to-End Onboarding Funnel (S1.1 $\rightarrow$ S4.2) Deployed. | $\mathbf{Full\ Profile\ Conversion\ Rate \ge 50\%}$ (Initial). | Week 19 |

***
*This document contains proprietary information and is intended for internal use only.*
***
