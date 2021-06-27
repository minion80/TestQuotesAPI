# QUOTES Base API Tests

## Command line maven parameters  (Default used if no value provided.)
### Required Properties
runType - Set for the TestRail sync

            options- [LOCALKARATE, GITLABKARATE]
            default- LOCALKARATE
            usage- -DrunType=option on command line, i.e. -DrunType="LOCALKARATE"
                   -Dtest=RunnerJavaFile on command line, i.e. -Dtest=RegressionTestRunner/TestRunner

### Framework Structure
1. Has a set of Unit Test Feature of each GET parameter type with a positive scenario inside below directory-
   src/test/java/com/quotes/features/QuotesMS/UnitTests
2. Has a set of Dynamic Test Feature of each GET parameter type with all regression scenarios inside below directory-
   src/test/java/com/quotes/features/QuotesMS/DynamicTests
3. Has a set of Dynamic Test cases written with dynamic data on a test data csv file inside below directory-
   src/test/java/com/quotes/testData/QuotesMS
4. Has a naming similarity between Dynamic Test Feature and Dynamic Test data files   
5. Has some global variable set at karate-config.js file
6. Has some additional set of customized assertions available under utils/AssertionUtilClass
7. Has some common feature which could be imported in other functional Test feature

## Updating results to TestData folder
1. Creates a TestData folder with all test run results and all different types of reports

## Reporting through Jenkins using Cucumber Report plugin
1. Make sure users have Cucumber reports plugin installed on Jenkins
2. Provide Jenkins the Json report placed under below directory to display with Jenkins job-
   target/surefire-reports
