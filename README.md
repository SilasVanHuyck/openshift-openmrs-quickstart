OpenMRS on OpenShift
====================
This git repository helps you get up and running quickly with a OpenMRS Platform 1.10.1 installation on OpenShift.

Create a Do It Yourself (DIY) app on OpenShift
----------------------------------------------
<a href="https://www.openshift.com/">Create an account</a> and install the <a href="https://www.openshift.com/get-started">command-line client tools</a>.

Create a DIY application:
    rhc app create openmrs diy-0.1

Get OpenMRS running
----------------------------
Grab this quickstart project and make it work for you!

    cd openmrs
    git remote add upstream -m master git://github.com/ixWDE4eR/openshift-openmrs-quickstart.git
    git pull -s recursive -X theirs upstream master
    git push

That's it, you can now checkout your openmrs at:
    http://openmrs-$yournamespace.rhcloud.com/openmrs

The default Tomcat managing account is tomcat/openshift; this can be changed by altering the 
openmrs/tomcat/conf/tomcat-users.xml file, committing the change within your secure OpenShift
Git account and issuing another <code>git push</code>.

Forking this Quickstart to use a newer Tomcat version
-----------------------------------------------------
See [here](HowToUpdate.md) for information.

License
-------
This code is dedicated to the public domain to the maximum extent
permitted by applicable law, pursuant to CC0
http://creativecommons.org/publicdomain/zero/1.0/

