Welcome to the OpenMRS Concept Proposal Module!
===============================================

Intro
-----

[OpenMRS](http://openmrs.org) is an open source medical records system
actively developed by volunteers worldwide to support healthcare delivery in
developing nations.

The Concept Proposal Module is intended to be used by local administrators
who have created new concepts they wish to propose for inclusion in the central
dictionary database.  There are 2 parts to this module: The proposal and the review.

To find out more information, visit our [wiki](https://wiki.openmrs.org/display/projects/Melbourne+Hack+Night+-+Concept+Proposal+Module)

How to Contribute
-----------------

We are looking for volunteers to help!  Please contact us via the [mailing list](http://groups.google.com/d/forum/openmrs-australia)
or through the [meetup](http://www.meetup.com/melbourne-hack-nights) based in Melbourne, Australia.

If you're new to web or Java development, or are just curious to see what we're working with, have a look at
the [summary of technologies used](https://github.com/OpenMRS-Australia/openmrs-cpm/wiki/Resources).

We ask that contributors please submit contributions in the form of [pull
requests](https://help.github.com/articles/using-pull-requests) in order for a
member of our team to review the code appropriately as any commits to master
are picked up by our continuous deployment server.

Quickstart
----------

1. [Download](http://openmrs.org/download/) the OpenMRS standalone distribution and login as the administrator
2. Clone the concept proposal module source code onto your local drive:
    * `git clone https://github.com/OpenMRS-Australia/openmrs-cpm.git`
3. Build the module:
    * `mvn -DskipTests=true package`
4. Locate the module file:
    * `omod/target/cpm-1.0-SNAPSHOT-<build-id>.omod`
5. Install the module into OpenMRS by uploading the OMOD file within administration section:
    * Administration -> Manage Modules -> Add or upgrade module -> Add module
   
   Alternatively you can use `publish-vagrant.sh` script

The [notes on setting up a dev environment](https://github.com/OpenMRS-Australia/openmrs-cpm/wiki/HowTo) and the [list of gotchas](https://github.com/OpenMRS-Australia/openmrs-cpm/wiki/Gotchas) may also be useful.

Sample workflow
---------------

    git checkout -b 92-github-move

    while not done:
        hack
        run(tests)
        refactor
        run(tests)
        git add .
        git commit -m 'Somthing meaningful'

    git push origin 92-github-move
    open https://github.com/OpenMRS-Australia/openmrs-cpm
    Click the Pull Request button
    Verify your changes
    Send pull request

Ideally somebody else should merge your code into `master` (which will trigger
a build) and delete the short-lived branch. Occasionally, you may need to do
this yourself.

And then you're done. More information on how to use Git to synchronize changes to/from your fork here: https://www.openshift.com/wiki/github-workflow-for-submitting-pull-requests

Links
-----

Mailing list: http://groups.google.com/d/forum/openmrs-australia

Meetup: http://www.meetup.com/melbourne-hack-nights

OpenMRS core source: https://github.com/openmrs/openmrs-core

Concept Proposal Module Documentation:
http://wiki.openmrs.org/display/projects/Concept+Proposal+Module+Documentation

CI server: http://ec2-50-112-42-202.us-west-2.compute.amazonaws.com:8153/go/

Mingle: https://minglehosting.thoughtworks.com/unicef/profile/login?project_id=openmrs_oz

CI environment (admin, OpenMRS1): http://ec2-54-245-143-28.us-west-2.compute.amazonaws.com:8080/openmrs

QA environment (admin, OpenMRS1): http://ec2-54-245-1-154.us-west-2.compute.amazonaws.com:8080/openmrs
