# Continuous integration

## Documentation

### Lexicon

CI : Continuous Integration
XP : Extreme Programming
CI/CD : Continuous Integration / Deploymenti

### What is it?

(Quoted from Wikipedia)

In software engineering, continuous integration (CI) is the practice of merging all developer working copies to a shared mainline several times a day.

The main aim of CI is to prevent integration problems, referred to as "integration hell" in early descriptions of XP. In XP, CI was intended to be used in combination with automated unit tests written through the practices of test-driven development. Initially this was conceived of as running and passing all unit tests in the developer's local environment before committing to the mainline. This helps avoid one developer's work-in-progress breaking another developer's copy. Where necessary, partially complete features can be disabled before committing, using feature toggles for instance. 
Later elaborations of the concept introduced build servers, which automatically ran the unit tests periodically or even after every commit and reported the results to the developers.

In the same vein, the practice of continuous delivery further extends CI by making sure the software checked in on the mainline is always in a state that can be deployed to users and makes the deployment process very rapid. 

(Quoted from opensource.com)



## Links and sources

- Wikipedia page : https://en.wikipedia.org/wiki/Continuous_integration
- Best practices for CI/CD found on opensource.com : https://opensource.com/article/18/11/best-practices-cicd
