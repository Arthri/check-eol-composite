# check-eol-composite
A composite action for linting end-of-line sequences.

## Installation
Open the workflow(s) to add the composite action to, then add the step below to the desired jobs.
```yml
jobs:
  job:
    - name: Check End-of-Line Sequences
      uses: Arthri/check-eol-composite@v1
```

## Usage

### Default End-of-Line Sequence
The workflow enforces `LF` for all files in the index. `autocrlf=true` modifies files in the working tree rather than the index and thus does not affect the composite action. The following example configures the workflow to enforce `CRLF` instead.
```yml
jobs:
  job:
    - name: Check End-of-Line Sequences
      uses: Arthri/check-eol-composite@v1
      with:
        default-eol: crlf
```
