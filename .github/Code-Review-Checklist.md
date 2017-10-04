# Code Review Checklist

- [ ] Did you build a [sequence diagram](https://en.wikipedia.org/wiki/Sequence_diagram) of the components (PHP classes, php files, js files) involved in the execution of the functionality (either in your mind or on pen-and-paper)?
- [ ] Were you able to confirm that the code change fixes/addresses the issue?
- [ ] Were you able to ensure that the change did not break anything else?
  - [ ] Do you have a list of classes/functions/files that are changed?
  - [ ] Do you have a list of scenarios to test (based on all the files touched)? Use the Living Spec to list them.
  - [ ] Are any of these used in other code-paths than the one you are used for this issue (e.g., change to a utility method, partial view require us to test the other code-paths that test this.
  - [ ] Do you understand what every single line in the code change does, and why it is necessary. If you are glossing over some lines, don't. 
- [ ] Did you debug the code in the code-path and observe that the values of the variables is correct/expected as you debug through the code? You must always be asking question such as 'what if this value is not passed', 'what if this query does not return any results' etc. ? 
- [ ] Did you merge into release-cocodrie and then test? Ensure the commit has the original author (can be done with the --author flag).
- [ ] If there were any merge conflicts, did you review each file and ensure there are no duplicate lines and such because of an 'auto-merge'.

## Issues Found - Functionality

- [ ] ** List issues found **

## Scenarios and Relevant Test Cases

These are affected scenarios and relevant test cases I checked:

- [ ] Affected Scenario 1
   - [ ] Relevant test case 1
   - [ ] Relevant test case 2
i.e.   
- [FI-001 | Can import users](https://github.com/cellcontrol/web/wiki/Scenario-FI-001)
   - Import A User With **None** of 'Ownership', 'Device Type', 'Deployment Method' and 'Operating System' Attributes Given and Ensure The Phone Shows Up in the Edit User Modal and In the Phone Grid
   - Import A User With Of 'Ownership', 'Device Type', 'Deployment Method' and 'Operating System' Attributes Given and Ensure The Phone Shows Up in the Edit User Modal and In the Phone Grid
