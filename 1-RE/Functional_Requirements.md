# Functional Requirements — Patient Health Record Consent Management System

## FR-01 Patient Consent Creation
The system shall allow a patient to grant a verified healthcare provider access to a selected medical record or record category.

## FR-02 Consent Duration
The system shall allow the patient to specify the validity period of a consent.

## FR-03 View Active Consent
The system shall allow a patient to view active and existing consent permissions.

## FR-04 Revoke Consent
The system shall allow a patient to revoke previously granted access.

## FR-05 Provider Verification
The system shall verify that a healthcare provider is an authorized/verified provider before granting record access.

## FR-06 Controlled Record Access
The system shall allow a provider to access a medical record only when the provider is verified and a valid consent exists for the requested record.

## FR-07 Consent Enforcement
The system shall enforce consent scope and validity period whenever a provider requests a record.

## FR-08 Auditability
The system shall record relevant consent and record-access activities in an audit log.

## FR-09 Access History
The system shall allow authorized users to view relevant access history/audit information.

## FR-10 Expired Consent
The system shall prevent access when the consent has expired.
