# Bank Transfer QA Demonstration Environment

This is a local, fictional banking-transfer demo created for a QA portfolio exercise.

## How to use
1. Open `index.html` in a modern browser.
2. Use only the dummy data shown below.
3. Valid beneficiary: `0000000002`
4. Valid OTP: `123456`
5. Starting balance: NGN 100,000
6. Suggested valid transfer: NGN 10,000

## Suggested demonstrations
- TC001: valid account + NGN 10,000 + OTP 123456
- TC004: enter an invalid account number
- TC018: enter more than NGN 100,000
- TC029: enter an incorrect OTP
- TC036: click Confirm Transfer repeatedly; the demo blocks duplicate processing

## Important
This is not connected to any bank, payment provider, API, or real account. It contains no real financial credentials.
