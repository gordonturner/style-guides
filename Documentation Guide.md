Documentation Guide
===================

The following are recommended elements to capture in documentation, wether that is in Word, Markdown or Confluence.


Developer Onboarding
--------------------

What needs to be installed and what steps need to be taken for a new developer to get onboarded.

- Assumptions about OS, MacOS, Windows, Linux
- IDE options, IntelliJ, Xcode, Visual Studio, Sublime
- What tools need to be installed, Java, Node.JS, Python, Brew
- Access to source control, GitHub, GitLab, TeamServer
- Access to databases
- Access to test and development environments


Releases
--------

What are the steps to prepare a release.

- What branch is the release made from?
- What, if any, merging has to happen?
- Are the steps manual or using CI/CD?
- What is the CI/CD job or step to call?
- Where does the release go after the job or step?


Testing
-------

*TODO*


Deployment
----------

*TODO*


Jobs
----

Any scheduled, adhoc or manual jobs should be captured.

- When they run, day, time, condition
- Where they run, server, database
- Monitoring, is there Nagios, Cloudwatch or email notifications

- Who to notify if there was an error?
- How to restart or re-run if there was an error?
