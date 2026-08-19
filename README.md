# Bank Transfer QA Project

## 3MTT Software Testing Portfolio Project

A comprehensive Quality Assurance project for a **simulated mobile banking application's Bank Transfer feature**. The project demonstrates practical QA activities including test planning, test case design, requirements traceability, defect identification, simulated test execution, API testing, and test reporting.

---

## Project Overview

The objective of this project was to verify that users can perform bank transfers **accurately, securely and reliably**, while ensuring that the application handles invalid inputs, authentication failures, network interruptions, duplicate requests and other edge cases safely.

The project uses fictional test data and a simulated banking environment. No real financial transactions or production banking credentials are involved.

---

## Testing Objectives

The testing activities were designed to:

* Verify successful fund transfers.
* Validate beneficiary and account information.
* Validate transfer amounts, transaction limits and fees.
* Verify PIN and OTP authentication.
* Ensure failed transactions do not result in unintended debits.
* Verify receipts and transaction history.
* Test cancellation and safe navigation.
* Evaluate network and transaction-state error handling.
* Assess duplicate-transaction prevention.
* Identify defects that could affect transaction integrity and release readiness.

---

## Scope

### In Scope

* Login and session handling
* Beneficiary validation
* Account number validation
* Transfer amount validation
* Transaction fees
* Transaction narration
* PIN/OTP authentication
* Transfer confirmation
* Transfer cancellation
* Receipts
* Transaction history
* Network and error handling
* Duplicate transaction prevention
* API request and response validation

### Out of Scope

* Airtime
* Bill payments
* Card management
* Loans
* Investments
* Production banking infrastructure
* Real customer accounts
* Real financial transactions

---

## Test Strategy

The project applies a combination of:

* Functional Testing
* Smoke Testing
* Regression Testing
* Negative Testing
* Boundary-Value Testing
* Exploratory Testing
* Security-Focused Validation
* Usability Testing
* API Testing

The approach focuses particularly on financial-integrity risks, authentication, transaction state management and failure conditions.

---

## Test Environment

| Item             | Description                |
| ---------------- | -------------------------- |
| Application      | Simulated Banking MVP      |
| Device           | Android phone              |
| Operating System | Android 12+                |
| Browser          | Chrome for web version     |
| Connectivity     | Wi-Fi / 4G                 |
| Test Data        | Fictional / Dummy Accounts |

All test data used in the project is fictional.

---

## Test Coverage

A total of **40 test cases** were designed to cover positive, negative and edge-case scenarios.

Examples include:

* Successful transfer
* Invalid account number
* Invalid beneficiary
* Insufficient balance
* Zero transfer amount
* Negative transfer amount
* Transaction-limit validation
* Fee calculation
* Incorrect PIN
* Expired OTP
* Network interruption
* Duplicate transfer attempt
* Receipt generation
* Transaction-history verification
* Session protection

The Requirements Traceability Matrix maps the requirements to their corresponding test cases.

---

## Test Execution Results

The simulated execution produced the following results:

| Metric             | Result |
| ------------------ | -----: |
| Total Test Cases   |     40 |
| Passed             |     31 |
| Failed             |      7 |
| Blocked            |      2 |
| Pass Rate          |  77.5% |
| Exit Criterion     |    95% |
| Exit Criterion Met |     No |

The 77.5% pass rate did not meet the defined 95% release criterion.

### Defect Summary

| Severity | Count |
| -------- | ----: |
| Critical |     3 |
| High     |     4 |
| Medium   |     2 |
| Low      |     1 |

### Major Findings

The simulated testing identified several important risks:

* Duplicate transaction processing when confirmation is rapidly repeated.
* Unsafe transaction-state handling during connectivity interruptions.
* Expired OTP codes requiring stronger validation.
* Transfer fee and transaction-limit validation requiring improvement.
* Receipt and transaction-history information requiring consistency with the processed transaction.

### Release Recommendation

**NOT RECOMMENDED FOR PRODUCTION**

The simulated build did not meet the 95% pass-rate exit criterion, and critical defects affecting transaction integrity and authentication remained unresolved.

---

## API Testing

The project includes a simulated API collection stored in the `api/` directory.

API testing focuses on:

* Request payload validation
* Response structure
* HTTP status behaviour
* Transaction outcomes
* Error handling
* Repeatable API execution

The API collection provides an additional layer of testing beyond the application interface.

---

## Project Deliverables

| Folder/File                                               | Description                                            |
| --------------------------------------------------------- | ------------------------------------------------------ |
| `README.md`                                               | Project overview and documentation                     |
| `documentation/Bank_Transfer_Test_Plan.docx`              | Detailed QA test plan                                  |
| `documentation/Bank_Transfer_Test_Summary_Report.docx`    | Simulated execution results and release recommendation |
| `test-artifacts/Bank_Transfer_QA_Test_Artifacts.xlsx`     | Test cases, traceability, defects and test summary     |
| `api/Bank_Transfer_Simulated_Postman_Collection.json`     | Simulated API testing collection                       |
| `presentation/Bank_Transfer_QA_Project_Presentation.pptx` | Project presentation                                   |

---

## Requirements Traceability

The project includes traceability between requirements and test cases.

Examples include:

* `REQ-001` — User can transfer money
* `REQ-002` — Account number must be validated
* `REQ-003` — Transfer amount must be valid
* `REQ-004` — Transfer fees must be calculated
* `REQ-005` — User must authenticate the transaction
* `REQ-007` — Network failures are handled safely
* `REQ-008` — Duplicate transactions are prevented
* `REQ-009` — Successful transactions generate receipts
* `REQ-010` — Transactions appear in history
* `REQ-011` — Sessions are protected

These requirements are mapped to the appropriate test cases in the test-artifact workbook.

---

## Retest & Regression Plan

Following defect fixes, the recommended QA activities are:

1. Retest all failed test cases.
2. Execute regression testing against previously passed transaction flows.
3. Repeat network interruption scenarios.
4. Repeat duplicate-request scenarios.
5. Verify OTP expiration and invalid-code handling.
6. Confirm that no Critical or High financial-integrity defects remain.
7. Update the final test summary with post-fix results.

---

## Key QA Skills Demonstrated

This project demonstrates practical experience in:

* Test Planning
* Test Case Design
* Functional Testing
* Negative Testing
* Boundary-Value Analysis
* Requirements Traceability
* API Testing
* Defect Management
* Risk-Based Testing
* Test Execution
* Test Reporting
* Release Readiness Assessment
* Regression Testing

---

## Project Structure

```text
bank-transfer-QA-project-3MTT/
│
├── index.html
├── README.md
│
├── api/
│   └── Bank_Transfer_Simulated_Postman_Collection.json
│
├── documentation/
│   ├── .gitkeep
│   ├── Bank_Transfer_Test_Plan.docx
│   └── Bank_Transfer_Test_Summary_Report.docx
│
├── test-artifacts/
│   ├── .gitkeep
│   └── Bank_Transfer_QA_Test_Artifacts.xlsx
│
└── presentation/
    ├── .gitkeep
    └── Bank_Transfer_QA_Project_Presentation.pptx
```

---

## Conclusion

This project demonstrates a structured QA approach to a financial transaction workflow, combining functional, negative, boundary, security-focused and API testing techniques.

The simulated execution identified significant transaction-integrity and authentication risks, demonstrating the importance of testing not only successful workflows but also failure conditions and edge cases.

The release should remain on hold until the identified Critical and High-severity issues are resolved and successful retesting and regression testing are completed.
