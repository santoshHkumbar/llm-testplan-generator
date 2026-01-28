---
name: generating-test-plans
description: Helps in generating, verifying, and improving standard test plan documents. Triggered when the user mentions creating or validating a test plan or uploads a test plan file.
---

# Generating Test Plans

## When to use this skill
- When you need to create a new test plan from scratch.
- When you have an existing test plan that needs verification against standards.
- When you want to improve or "make proper" an uploaded test plan.
- When you need to generate a new version of a test plan based on an existing one.

## Workflow

### 1. Identify Input
- Check if the user has provided a document or text.
- If not, ask for details about the project/software to generate a skeleton.

### 2. Validation & Verification
- Use the standard checklist to verify the uploaded document.
- Identify missing sections (e.g., Risks, Environment, Schedule).
- Flag vague or incomplete sections.

### 3. Correction & Improvement
- "Make it proper" by filling in missing sections based on context.
- Improve existing descriptions using professional QA terminology.
- Ensure formatting is consistent.

### 4. Generation
- Generate the final markdown document using the standard template in `resources/test-plan-template.md`.

## Standard Sections Checklist
- [ ] Test Plan Identifier
- [ ] Introduction
- [ ] Test Items
- [ ] Features to be Tested
- [ ] Features Not to be Tested
- [ ] Approach (Strategy)
- [ ] Item Pass/Fail Criteria
- [ ] Suspension & Resumption
- [ ] Test Deliverables
- [ ] Testing Tasks
- [ ] Environmental Needs
- [ ] Responsibilities
- [ ] Staffing & Training
- [ ] Schedule
- [ ] Risks & Contingencies
- [ ] Approvals

## Instructions

- **Verification**: When validating, provide a summary of what is missing or needs improvement.
  - "The section 'Features Not to be Tested' is missing. Would you like me to suggest standard exclusions?"
- **Correction**: If a section is "not proper", expand it.
  - *Improper*: "We will test the login."
  - *Proper*: "The testing approach for the Authentication module will include positive, negative, and boundary value analysis for the login functionality, including multi-factor authentication paths."
- **Generation**: Always use the template in `/resources/test-plan-template.md`.

## Resources
- [Standard Test Plan Template](resources/test-plan-template.md)
