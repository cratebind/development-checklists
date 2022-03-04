## Junior

- [ ] Is each AC fully implemented?
- [ ] Does all code comply with best practices?
    - [ ] Is the code easy to understand?
        - [ ] If you removed all the business logic from this file, and left only the
        def method_names and class Names, would you be able to tell what this file does?
    - [ ] Does each class have a single responsibility?
    - [ ] Does each method have a single responsibility?
    - [ ] Are style guidelines followed?
        - [ ] rubocop configured correctly?
    - [ ] Is code properly DRY?
        - [ ] can duplicated code be refactored into a module or inherited?
    - [ ] Are comments added where context is unclear and helpful?
        - [ ] It’s helpful to add comments about why, not what
- [ ] Is authentication handled properly?
    - [ ] Was the gem README followed? Were there any points of confusion?
- [ ] Is authorization handled properly?
    - [ ] Was the gem README followed? Were there any points of confusion?
- [ ] Are exceptions gracefully handled?
    - [ ] Be sure not to swallow exceptions
- [ ] Are unit tests written?
    - [ ] Is there value by testing this feature?
- [ ] Are e2e tests written?
    - [ ] Is there value by testing this feature?
- [ ] Was the Ability.rb filed updated to the user role authenticated resources?

**Your methods should NOT be bigger than 3-4 lines per method. If so, you probably should refactor that method logic to make if much more modular.**

Try to avoid having a **huge block of code** logic in a single point of your runtime.

### ActiveRecord:
If your application loads any kind of data from ActiveRecord:

If loading multiple records:
- [ ] Are those records being **paginated**? Never do `.all` in your entire life.
- [ ] Did you **sideload relations** on those records to optimize the loading time required?

If loading a single record:
- [ ] Did you made sure that the record is scoped to the user role authorization?

**Example:**

```ruby
def show
  current_user.profile
end
```

### Graphql:

- Do your functions have authorization properly implemented?
- Did separated sensitive information for user types between `user_type.rb` and `user_public_type.rb`  ?

## Senior

- [ ] Is each AC fully implemented?
    - [ ] Any decision we make in advance of an explicit requirement is just a guess
- [ ] Does all code comply with best practices?
    - [ ] Is code easy to read?
    - [ ] Are naming conventions followed?
        - [ ] Methods/Classes/Modules/Files
    - [ ] Is the code easy to understand?
        - [ ] If you removed all the business logic from this file, and left only the
        def method_names and class Names, would you be able to tell what this file does?
        - [ ] Are files names thoughtfully created?
          ```ruby
          include MemberValidations

          # vs

          include Vals
          ```
        - [ ] Does the code ‘read well’? 
          ```ruby
          reject_application unless fully_qualified

          # vs

          reject unless !errors?
          ```
    - [ ] Are all functions or classes an acceptable size?
        - [ ] Can you describe what this class/function does in one sentence?
    - [ ] Does each class have a single responsibility?
    - [ ] Does each method have a single responsibility?
    - [ ] Public interface definitions
        - [ ] Has a public interface been defined?
        - [ ] Has the public interface changed? Why?
        - [ ] Is there an opportunity for a polymorphic interface?
    - [ ] What does our dependency risk look like?
        - [ ] Method argument order
        - [ ] Use of class names within other classes
        - [ ] Messages being sent to explicitly defined classes
            - [ ] Can we use Dependency Injection?
        - [ ] Are third party libs wrapped by a class we created?
    - [ ] Are style guidelines followed?
        - [ ] rubocop configured correctly?
    - [ ] Is code properly DRY?
        - [ ] can duplicated code be refactored into a module or inherited?
    - [ ] Are comments added where context is unclear and helpful?
        - [ ] Its helpful to add comments about why, not what
- [ ] Is authentication handled properly?
    - [ ] Was the gem README followed? Were there any points of confusion?
    - [ ] Is the auth lib tested and trusted?
    - [ ] Is any custom authentication implemented only as a last resort
        - [ ] Thoughtful, comprehensive testing in place?
- [ ] Is authorization handled properly?
    - [ ] Was the gem README followed? Were there any points of confusion?
    - [ ] Is the auth lib tested and trusted?
    - [ ] Is any custom authorization implemented only as a last resort
        - [ ] Thoughtful, comprehensive testing in place?
- [ ] Are exceptions gracefully handled?
    - [ ] Be sure not to swallow exceptions
- [ ] Are unit tests written?
    - [ ] Is there value by testing this feature?
- [ ] Are e2e tests written?
    - [ ] Is there value by testing this feature?
- [ ] Project should have at least 90% percent testing coverage
- [ ] Project should have at least 90% percent documentation coverage
