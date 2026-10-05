# Design discussion

## Scheduling

A proposed schedule is a candidate decision. Approval must validate the relevant availability and constraints again. Repeated submissions should not create duplicate operations. Concurrent edits should either serialize or produce an explicit conflict. A UI success state should follow a committed backend result.

## Document lifecycle

An upload, replacement, review, and deletion share identity and authorization concerns. A replacement must not leave old evidence active while presenting the new document as approved. A permission change during retrieval must be respected before publication. Lock order should be consistent across every caller that touches the same resources.

## Retrieval and answers

Retrieval returns candidates, not truth. The system needs to preserve entity boundaries, requested fields, uncertainty, and source references. When a source does not answer a question, a refusal or clarification is more useful than a related but unsupported answer. Evaluation denominators should include failures and unavailable cases.

## Voice interaction

Microphone permission and provider connection are separate asynchronous operations. A cancellation can arrive while either operation is pending. Session identity should prevent late callbacks from overwriting the current UI. Text fallback should remain usable without microphone permission. Listening acceptance must include actual audio, interruptions and device behavior.

## Production direction

Production work would require operational monitoring, explicit retention and privacy controls, authenticated voice sessions, verified tenant boundaries, tested recovery procedures, a maintained provider contract suite, and a clearly owned support process. These are improvement areas rather than claims of completed controls in this case study.
