# PL/SQL Assignment III: GOTO Statements & Functions

**Student:** Felicien Nshimyumukiza  
**Student ID:** 20251SEN197  
**Course:** Database Programming (PL/SQL)

---

## 📌 Project Overview

This repository contains solutions for PL/SQL Assignment III, focusing on control flow structures (`GOTO`), stored scalar functions, and procedural validation in Oracle Database.

The assignment covers:
1. **Part A — Control Flow with GOTO Statements & Refactoring:** Understanding conditional jumps, syntax rules, limitations, and modern structured alternatives (`IF-THEN-ELSE`).
2. **Part B — PL/SQL Functions:** Designing reusable scalar functions to calculate annual salary, years of service, tax deductions, and department name lookup, integrated directly into SQL queries.
3. **Part C — Payroll Validation Procedure & Reflection:** Creating an audit procedure to detect payroll anomalies (negative/null salaries) and writing a reflective analysis on PL/SQL design patterns.

---

## 📂 Repository Structure

```plaintext
├── 00_setup/
│   └── create_tables.sql            # Table definitions (departments, employees) & initial seed data
├── 01_goto/
│   ├── A1_number_classifier.sql     # Classifies numbers (positive/negative/zero) using GOTO labels
│   ├── A2_salary_review.sql         # Evaluates employee salary thresholds via GOTO branching
│   ├── A3_illegal_goto.sql          # Syntax and compilation error demonstration with GOTO
│   └── A4_rewrite_no_goto.sql       # Clean refactor of salary review using structured IF-THEN logic
├── 02_functions/
│   ├── B1_fn_annual_salary.sql      # Function: annual_salary(monthly_salary)
│   ├── B2_fn_years_of_service.sql   # Function: years_of_service(hire_date)
│   ├── B3_fn_calculate_tax.sql      # Function: calculate_tax(salary) (10% rate)
│   ├── B4_fn_dept_name.sql          # Function: get_department_name(department_id)
│   └── C1_fn_validate_payroll.sql   # Procedure: validate_payroll (audits invalid salaries)
├── 03_tests/
│   ├── B5_functions_in_select.sql   # Comprehensive SELECT combining all functions in one query
│   ├── test_functions.sql           # Automated unit test suite with assertions for functions
│   └── test_validate_payroll.sql    # Verification script for validate_payroll procedure
├── docs/
│   └── REFLECTION.md                # Part C2 reflection report on GOTO vs structured programming
└── screenshots/
    ├── A1-Output.png                # Execution output of A1_number_classifier.sql
    ├── A2-Output.png                # Execution output of A2_salary_review.sql
    ├── A3_error_and_fix.png         # Execution output of A3_illegal_goto.sql
    ├── A4_output.png                # Execution output of A4_rewrite_no_goto.sql
    ├── B5_select_output.png         # Execution output of B5_functions_in_select.sql
    └── C1_output.png                # Execution output of C1_fn_validate_payroll.sql
```

---

## 🚀 Execution Guide

Run the scripts in **Oracle SQL*Plus** or **Oracle SQL Developer** in the following sequence:

### 1. Database Setup
```sql
@00_setup/create_tables.sql
```

### 2. GOTO Demonstrations & Refactoring
```sql
@01_goto/A1_number_classifier.sql
@01_goto/A2_salary_review.sql
@01_goto/A3_illegal_goto.sql
@01_goto/A4_rewrite_no_goto.sql
```

### 3. PL/SQL Stored Functions & Procedure
```sql
@02_functions/B1_fn_annual_salary.sql
@02_functions/B2_fn_years_of_service.sql
@02_functions/B3_fn_calculate_tax.sql
@02_functions/B4_fn_dept_name.sql
@02_functions/C1_fn_validate_payroll.sql
```

### 4. Tests & Verification
```sql
@03_tests/B5_functions_in_select.sql
@03_tests/test_functions.sql
@03_tests/test_validate_payroll.sql
```