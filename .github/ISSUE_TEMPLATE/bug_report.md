name: Bug Report
about: Create a report to help us improve
title: "[BUG] "
labels: ["bug"]
assignees: ''

body:
  - type: markdown
    attributes:
      value: |
        Thanks for taking the time to fill out this bug report!

  - type: textarea
    id: what-happened
    attributes:
      label: What happened?
      description: Also tell us, what did you expect to happen?
      placeholder: Tell us what you see!
    validations:
      required: true

  - type: textarea
    id: steps-to-reproduce
    attributes:
      label: Steps to Reproduce
      description: "How can we reproduce the issue?"
      placeholder: |
        1. Go to '...'
        2. Click on '....'
        3. See error
    validations:
      required: true
      
  - type: input
    id: version
    attributes:
      label: Project Version
      description: "What version of our project are you running?"
      placeholder: "e.g., 1.0.0"
    validations:
      required: false

  - type: textarea
    id: logs
    attributes:
      label: Relevant log output
      description: Please copy and paste any relevant log output. This will be automatically formatted into code, so no need for backticks.
      render: shell
