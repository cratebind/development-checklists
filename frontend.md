# Junior

### Does all code comply with best practices?
- [ ] Is code easy to read?
- [ ] Is the code easy to understand?
    - [ ] If you removed all the business logic from this file, and left only the component and function names, would you be able to tell what this file does?
- [ ] Are all functions or classes an acceptable size?
    - [ ] Can you describe what this class/function does in one sentence?
    - [ ] Does each method have a single responsibility?
- [ ] Is code properly DRY?
   - [ ] Can duplicated code be refactored into a module without overcomplicating?
- [ ] Are comments added where context is unclear and helpful?
    - [ ] Its helpful to add comments about why, not what

### Is each AC fully implemented?
- [ ] Have you run this code in different browsers (plus mobile browsers) & view sizes?
- [ ] Does it match the design in all viewports / device
- [ ] Is this commit complete or will we need to come back and finish this feature *OR* Are there any dependencies that are needed to make this feature work as intended? Ie: front end, back end, third party, etc.
    - [ ] if so, is there sufficient comments/notes about what is needed?

### Is authentication handled properly?
- [ ] If this code accesses a restricted resource, is it protected from unauthorized users?
- [ ] Have you tested this feature from accounts with differing levels of permissions to test?
- [ ] Does this commit impact any other parts of the project that needs to be handled?
- [ ] Are all error states gracefully handled?
  - [ ] APIs down or returning errors
  - [ ] Database servers down or returning errors
  - [ ] Unauthorized access attempted (Should redirect back or to a login screen if login is required)
  - [ ] Users taking unexpected actions
  - [ ] Results are incomplete [insufficient or empty data]

### Data Fetching
- [ ] Are loading states handled?
- [ ] Are "empty states" or error states handled when fetching data?

### End User Impact
- [ ] Do all interactive elements follow accessibility best practices?
  - [ ] [W3C / WAI-ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) guidelines
  - [ ] [Maybe add Accessibe auditing here if we end up using it]
  - [ ] Make sure to use accessibility-focused libraries ([Minerva UI](https://minerva-ui.js.org/), [Reach UI](https://reach.tech/), [Headless UI](https://headlessui.dev/))

# Mobile
- [ ] Have you run this code on both iOS & Android devices and on differing sizes devices?

# Senior
- [ ] Are exceptions gracefully handled?
- [ ] Is the caching strategy properly implemented?
- [ ] Is image optimization handled properly?
- [ ] Are security standards met?
- [ ] Are accessibility standards met?
- [ ] Are unit tests written?
- [ ] Are e2e tests written?
