---
name: Custom issue template
about: Describe this issue template's purpose here.
title: Firewall
labels: ''
assignees: ''

---

name: Firewall Change Request
description: Submit a change request for firewall changes
title: "[Firewall Change Request]"
labels: "[firewall]"

body:
  - type: markdown
    attributes:
      value: |
        This issue is used to request a firewall change.
  - type: input
    id: contact
    attributes:
      label: Contact Details
      description: How can we get in touch if we need more info?
      placeholder: ex. email@example.com"
    validations:
      required: false
  - type: textarea
    id: firewall-request-desc
    attributes:
      label: Firewall change description
      description: What is the purpose of the firewall change?
  - type: dropdown
    id: environment
    attributes:
      label: Environment
      Description: What environment are you requesting a change for?
      multiple: true
      options:
        - Dev
        - Test
        - Prod
  - type: checkboxes
    id: consent
    attributes:
      label: Verification
      description: By submitting this issue, you confirm that you have only requested the necessary firewall openings
      options:
        - label: I have only requested the necessary firewall openings.
          required: true
