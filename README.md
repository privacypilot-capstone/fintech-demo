# fintech-demo
# LoanEasy India — Synthetic Fintech Benchmark

## Purpose

This repository is a synthetic fintech application used to evaluate
PrivacyPilot's detection of code–privacy-policy mismatches.

It is intentionally designed with several planted test cases.
The presence of a finding in this repository is not, by itself,
proof of a legal violation in a real application.

## Intended positive cases

- PAN is collected but is not disclosed in the privacy policy.
- Bank account number and IFSC are collected but are not disclosed
  in the privacy policy.
- Aadhaar is collected but is not disclosed in the privacy policy.
- Personal and financial data are transmitted to Segment, although
  the policy says personal information is not shared with third parties
  except as required by law.

## Negative controls

Some comments mention sensitive identifiers or third-party SDKs
for testing whether the scanner mistakes comments for executable
data processing.

These comment-only references should not independently produce
findings for collection, storage, or transmission.

## Evaluation notes

Record expected positive and negative cases in the benchmark
ground-truth manifest before running PrivacyPilot.

Treat source-code findings as technical evidence. Whether consent
was valid, a processor contract exists, or a legal violation occurred
may require evidence beyond the source code and privacy policy.
