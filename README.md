Test assignment
We are looking for Automation Engineers that have the mindset "only the sky is the limit" and "automation doesn't stop at testing, it's just a beginning!" ;)
The purpose of this test assignment is to assess the applicant's automation skills, allowing him/her to show the best they can do and how fast they can learn.
It is an open assignment. There is no the right answer and there is no end goal other than proving yourself. Surprise us!
Make sure that you give detailed comments or descriptions of your tests.
When the assignment is complete, please push your solution to Github(Gitlab) and send us the link
If you have any questions, please contact us back.
Good luck.
PS. We don't expect you to spend weeks (and sleepless nights) on doing it. Lets see how far you can get in 6-10 hours. We want to see how you approach and solve problems.
PSPS. Please use mobile native tools. (Tests written on Java are accepted too)

Kiran findings
old version of java 11  
"Note: I encountered a build failure due to deprecated JCenter dependencies (Detekt).
I resolved this by updating the repository configuration to MavenCentral
and bypassing legacy linting tools to prioritize the automation suite delivery.

Note: Encountered NoSuchMethodException during test execution due to Espresso 3.1.0 compatibility issues with Android API 30+. Resolved by upgrading Espresso to 3.5.1 to ensure stable event injection on modern emulators."
"Updated Target SDK from legacy version to API 34 to comply with modern Android security standards and ensure Espresso 3.5.1 compatibility.

I noticed the project included a Jenkinsfile but lacked the Ruby dependencies. I have introduced a Fastlane configuration to bridge the gap between local development and CI/CD.
Why Fastlane? It abstracts the Gradle commands, making the build process platform-independent.
Why Jenkins? I have updated the Jenkinsfile logic to trigger the Fastlane verify_pull_request lane, ensuring that every push is automatically built and tested before it reaches the main branch.

GitHub Structure should look like this:
app/ (Your code and tests)

fastlane/ (Your automation "Surprise")

gradle/ (The wrapper)

build.gradle (The configuration)

README.md (Your strategy and scenarios)

Gemfile

Jenkinsfile
