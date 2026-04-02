name: "🐛 Bug Report"
description: If something isn't working as expected 🤔
labels: ["bug"]
body:
  - type: markdown
    attributes:
      value: |
        ## Bug Report
        Please provide as much detail as possible so we can squash this bug!

  - type: textarea
    id: steps-to-reproduce
    attributes:
      label: Steps to Reproduce
      description: Provide a clear list of steps to reproduce the behavior.
      placeholder: |
        1. Go to '...'
        2. Click on '....'
        3. Scroll down to '....'
        4. See error
    validations:
      required: true

  - type: textarea
    id: expected-result
    attributes:
      label: Expected Result
      description: A clear and concise description of what you expected to happen.
      placeholder: "I expected the system to..."
    validations:
      required: true

  - type: textarea
    id: actual-result
    attributes:
      label: Actual Result
      description: |
        What actually happened? Please include full exceptions (entire stack traces), log entries, or screenshots.
      placeholder: "The application crashed with the following error: ..."
    validations:
      required: true

  - type: textarea
    id: environment
    attributes:
      label: Environment
      description: Versions, OS, Runtime, etc.
      placeholder: |
        Project Version/Build:
        OS:
        Runtime:
        Environment (e.g. Docker, VirtualBox):
    validations:
      required: true

  - type: textarea
    id: additional-context
    attributes:
      label: Additional Context
      description: Add any other context or screenshots about the problem here.
    validations:
      required: false
