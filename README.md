# AngularDemoStrict

The purpose of this projects (and its branches) is to show the avantages of strict mode in Angular.  
## Projet  
The most common object every developer may have to deal with is a person.  
Let's define: 
- a person
- a person **may have one to many (0-N)** addresses  
- a person **has at least one (1-N)** role  

Presentation: 
- there should be a page allowing to search for user(s) (form + list)
- there should be a page displaying the detailed info for a selected user and there role(s)

## Branches
### Main
`ng new` avec  
Angular CLI: 13.3.9  
Node: 16.14.2  
Package Manager: npm 8.7.0  

## Test cases
### Function with "Object type" parameter defined as any
- may be an unexpected object type
- may be null
- may be undefined
- may miss a property  
- may not be available _YET_  

> Should not compile using stric mode  

The point is to make sure that, in real life, the final user will be able to react in that case.
If `strict mode` is not posibble, then unit tests should cover this situation.

### Migrate to strict mode
[TODO] 
- create, commit and push one branch and apply the "*old*" configuration
- create, commit and push another branch set in full strict mode and describe steps for this configuration
- create a new local branch base one the "*old*" configuration and add a component implementing proof examples
> Compilation should be successful on this branch, but not when switching to the strict one;
- create a new local branch based on the "strict" one, add the same component adapted to strict mode
> Compilation should be successful.

## FAQ
### Why wouldn't `strict mode` be possible ?

- Because the project was initiated without it. Developers may need to follow the original stratedy to prevent the app from being unusable. To guarantee robustness and prevent regressions, unit tests are much recommanded.  
> Want to see who it would look like with unit testing instead of strict mode? Switch to branch unit-testing

### Why is one (strict mode) or the other (unit testing) important?  

- to guarantee robustness of the application (further to the ability to run restricted operations, the front side of the app is dedicated to the user and to grant them the most possible comfortable experience)
- to help fellow developers make sure the component is still working after their modifications  

