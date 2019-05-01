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


Onboarding
----------

Anyone who is not a developer, how are they onboarded.

- Account onboarding
- Project Management onboarding
- QA onboarding
- BA onboarding
- Client onboarding
- Partner onboarding


Releases
--------

What are the steps to prepare a release.

- What branch is the release made from?
- What, if any, merging has to happen?
- Are the steps manual or using CI/CD?
- What is the CI/CD job or step to call?
- Where does the release go after the job or step?
- What are the release notes?
- How are people notified of releases?


Testing
-------

What testing does the project have.

- What unit testing is setup?
- What integration testing is setup?  What platforms, desktop, mobile etc
- Are any of the tests part of the release or CI/CD?
- How are people notified of test failures?


Deployment
----------

How does a deployment happen.

- How do the releases get deployed?
- What environments are available for deployment?
- How are things not in the release deployed?  Creative content, configuration, db updates
- How are people notified of deployments


Jobs
----

Any scheduled, adhoc or manual jobs should be captured.

- When they run, day, time, condition
- Where they run, server, database
- Monitoring, is there Nagios, Cloudwatch or email notifications

- Who to notify if there was an error?
- How to restart or re-run if there was an error?


Monitoring
----------

What is being monitored and by who.

- What are the SLAs?
- Who are the points of contact and escalation path?

- What servers are being monitored?  
- What is being monitored?
- Things to consider:
  - Disk space
  - CPU load
  - Network traffic
  - Errors
- How are they being monitored?  Nagios, NewRelic, Splunk
- What third party tools?  Pingdom, GTMetrix
- Are any of the integration tests used to monitor the site in production?

