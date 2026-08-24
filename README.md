# Integrated Business Planning & Financial Model in Excel

An integrated business planning model built entirely in Microsoft Excel, connecting commercial planning, operations, expenses, workforce planning, working capital, financing, and projected financial statements within a single workbook.

The objective of this project was to model how decisions made in one area of a business propagate through the rest of the organization.

For example:

```text
Sales assumptions
       ↓
Marketing & demand plan
       ↓
Production requirements
       ↓
Materials, labor & operating costs
       ↓
Inventory / receivables / payables
       ↓
Cash requirements & financing
       ↓
Income Statement
Balance Sheet
Cash Flow Statement
```

This was developed as a university business-planning project and is intended as a **planning and financial modeling system**, rather than a replacement for transactional ERP platforms such as SAP or Microsoft Dynamics 365.

---

## View the Model

### Browser Preview

The workbook is also available through Google Sheets for easier browser-based inspection:

**[Open the complete model in Google Sheets](PASTE_MAIN_GOOGLE_SHEETS_URL_HERE)**

> **Note:** The original Microsoft Excel `.xlsx` file included in this repository should be considered the reference version of the model. Conversion to Google Sheets may cause differences in formula compatibility, formatting, or other Excel-specific behavior.

### Downloadable Excel Model

The complete workbook is available in this repository:

```text
Business Planning Full Flow.xlsx
```

Opening the `.xlsx` file in Microsoft Excel is recommended when reviewing formulas and cross-sheet dependencies.

---

# Project Objective

The project models a hypothetical company's planning process across multiple business functions over a multi-period planning horizon.

Rather than developing each plan independently, the workbook connects the major planning areas so that changes in assumptions can flow through downstream calculations.

The model covers:

* business and financial assumptions;
* sales and marketing planning;
* operations and production planning;
* product and material requirements;
* operating expenses;
* workforce and salary planning;
* payment schedules;
* accounts receivable and delayed collections;
* capital expenditure;
* depreciation;
* financing and loan repayment;
* projected Income Statement;
* projected Balance Sheet;
* projected Cash Flow Statement.

The workbook contains **19 interconnected worksheets**, including both primary planning modules and supporting calculation schedules.

---

# Model Architecture

At a high level, the workbook follows the following structure:

```text
                         PARAMETERS
                             │
          ┌──────────────────┼──────────────────┐
          │                  │                  │
          ▼                  ▼                  ▼
     MARKETING          OPERATIONS        WORKFORCE
        PLAN               PLAN             PLANNING
          │                  │                  │
          │          ┌───────┴───────┐          │
          │          ▼               ▼          │
          │      PRODUCTION       MATERIALS     │
          │      REQUIREMENTS      & COSTS      │
          │          │               │          │
          └──────────┴───────┬───────┴──────────┘
                             │
                             ▼
                         EXPENSES
                             │
              ┌──────────────┼──────────────┐
              │              │              │
              ▼              ▼              ▼
         RECEIVABLES     PAYABLES       PAYROLL
              │              │              │
              └──────────────┼──────────────┘
                             │
                             ▼
                    CASH REQUIREMENTS
                             │
                 ┌───────────┴───────────┐
                 ▼                       ▼
              EQUITY                  LOANS
                                         │
                                         ▼
                                  REPAYMENT PLAN
                             │
                             ▼
                  FINANCIAL STATEMENTS
                             │
              ┌──────────────┼──────────────┐
              ▼              ▼              ▼
           INCOME         BALANCE          CASH
          STATEMENT        SHEET           FLOW
```

The purpose of this structure is to make the financial statements the **output of operational assumptions**, rather than manually prepared standalone statements.

---

# Key Capabilities

## Centralized Business Assumptions

The `Parameter` worksheet acts as a central input area for assumptions used throughout the model.

These assumptions include areas such as:

* sales and pricing;
* production;
* material requirements;
* operating costs;
* working capital;
* cash requirements;
* inventory;
* receivable and payable timing;
* financing;
* taxation;
* rent and utilities;
* workforce-related costs.

Changing an input in the parameter model can therefore affect multiple downstream schedules.

**[Open Parameter sheet](PASTE_PARAMETER_SHEET_URL_HERE)**

---

# Workbook Navigation

The complete workbook currently consists of the following worksheets.

Direct Google Sheets links can be added to this table later.

| Worksheet                        | Purpose                                    | Direct Link                              |
| -------------------------------- | ------------------------------------------ | ---------------------------------------- |
| `Parameter`                      | Central business and financial assumptions | [Open](PASTE_PARAMETER_SHEET_URL_HERE)   |
| `Marketing plan`                 | Commercial and sales planning              | [Open](PASTE_MARKETING_PLAN_URL_HERE)    |
| `Operations plan`                | Main operational and production planning   | [Open](PASTE_OPERATIONS_PLAN_URL_HERE)   |
| `Expenses`                       | Operating expense calculations             | [Open](PASTE_EXPENSES_URL_HERE)          |
| `Item list`                      | Product/item-level supporting data         | [Open](PASTE_ITEM_LIST_URL_HERE)         |
| `Salaries and wages`             | Workforce compensation planning            | [Open](PASTE_SALARIES_URL_HERE)          |
| `Paycheck schedule`              | Timing of payroll-related payments         | [Open](PASTE_PAYCHECK_SCHEDULE_URL_HERE) |
| `Delayed payment`                | Delayed collection/payment calculations    | [Open](PASTE_DELAYED_PAYMENT_URL_HERE)   |
| `INCOME STATEMENT`               | Projected profitability                    | [Open](PASTE_INCOME_STATEMENT_URL_HERE)  |
| `BALANCE SHEET`                  | Projected financial position               | [Open](PASTE_BALANCE_SHEET_URL_HERE)     |
| `CASH FLOW STATEMENT`            | Projected cash movements and balance       | [Open](PASTE_CASH_FLOW_URL_HERE)         |
| `Loan repay {supplement}`        | Supporting debt repayment schedule         | [Open](PASTE_LOAN_REPAYMENT_URL_HERE)    |
| `Spending {supplement}`          | Supporting capital-spending schedule       | [Open](PASTE_SPENDING_URL_HERE)          |
| `Dep. plan monthly {supplement}` | Supporting monthly depreciation schedule   | [Open](PASTE_DEPRECIATION_URL_HERE)      |
| `M&S`                            | Supporting/internal model worksheet        | [Open](PASTE_MS_URL_HERE)                |
| `OP`                             | Supporting/internal model worksheet        | [Open](PASTE_OP_URL_HERE)                |
| `MAN`                            | Supporting/internal model worksheet        | [Open](PASTE_MAN_URL_HERE)               |
| `FINAL BACKUP OPs PLAN`          | Development/backup operational model       | [Open](PASTE_BACKUP_OPS_URL_HERE)        |
| `Functions`                      | Supporting workbook functions/calculations | [Open](PASTE_FUNCTIONS_URL_HERE)         |

---

# Recommended Review Path

For someone reviewing the project for the first time, I recommend following the model in this order:

### 1. Parameters

Start with the assumptions driving the model.

**[Parameter](PASTE_PARAMETER_SHEET_URL_HERE)**

↓

### 2. Marketing Plan

See how commercial assumptions are translated into planned sales.

**[Marketing Plan](PASTE_MARKETING_PLAN_URL_HERE)**

↓

### 3. Operations Plan

Follow how demand becomes operational and production requirements.

**[Operations Plan](PASTE_OPERATIONS_PLAN_URL_HERE)**

↓

### 4. Expenses and Workforce

Review how operating activity generates costs.

**[Expenses](PASTE_EXPENSES_URL_HERE)**
**[Salaries and Wages](PASTE_SALARIES_URL_HERE)**

↓

### 5. Financial Statements

Review how all previous planning modules ultimately affect company financial performance.

**[Income Statement](PASTE_INCOME_STATEMENT_URL_HERE)**
**[Balance Sheet](PASTE_BALANCE_SHEET_URL_HERE)**
**[Cash Flow Statement](PASTE_CASH_FLOW_URL_HERE)**

For a detailed inspection of formulas and cross-sheet references, download the original Excel workbook from the repository.

---

# Tools Used

The project was developed entirely in **Microsoft Excel**.

The workbook relies primarily on:

* spreadsheet formulas;
* cross-sheet references;
* financial modeling logic;
* linked planning schedules;
* structured business assumptions;
* accounting relationships.

No dedicated ERP or enterprise planning software was used to construct the model.

---

# Project Scope and Limitations

This project is an academic-scale integrated business planning model.

It is **not intended to replicate a commercial ERP system** such as SAP S/4HANA or Microsoft Dynamics 365.

Enterprise systems provide capabilities outside the scope of this project, including:

* transactional databases;
* concurrent multi-user access;
* role-based permissions;
* audit trails;
* real-time inventory transactions;
* procurement workflows;
* production execution;
* API integrations;
* enterprise master-data management.

Instead, this project focuses on the **planning logic connecting business functions and financial outcomes**.

The workbook demonstrates how an integrated planning model can be constructed using spreadsheet tools without requiring a dedicated enterprise software platform.

---

# What I Learned

The most important part of this project was not individual Excel formulas, but understanding how different business functions depend on each other.

The project required connecting concepts from:

* marketing;
* operations management;
* production planning;
* inventory management;
* human resources;
* managerial accounting;
* corporate finance;
* working-capital management;
* financial reporting.

Building the workbook made it possible to see how a decision made in one part of a company can create operational and financial consequences elsewhere in the business.
