Getting Started
===============

 0. Ask Chuck Norris and his brother for permission.

 1. Get a login on http://github.com/

 1. Fork http://github.com/davedf/cuke4ninja and you will now have a url like this:
  * http://github.com/your-login-name/cuke4ninja

 1. Clone your fork to create a local repository on your machine and go into the cloned directory.
  * git clone https://your-login-name@github.com/your-login-name/cuke4ninja.git
  * cd cuke4ninja

 1. Add davedf's branch as a remote (this will be the effective trunk).
  * git remote add davedf git://github.com/davedf/cuke4ninja.git

 1. Watch davedf's branch on http://github.com/davedf/cuke4ninja.
    This means you will get pull requests.

 1. Get Xalan software at http://xml.apache.org/xalan-j/downloads.html and install it in (default) /opt/javalib directory and "xalan".

 1. Get XEP (personal edition) at http://www.renderx.com and install it in (default) /opt/XEP diretory. Xep appears to work on both MAC OS/X and PC.
  * Remember to run the setup jar inside XEP's readme.txt file to install and activate the license key file. The license key file will come to you in separate email from company.
  * Note that the license key file should be roughly 11 lines.

 1. Copy resources/environment.template to resources/environment.local and change XEP and XALAN paths if you did not use the following defaults:
  * XALANHOME=/opt/java-lib/xalan
  * XEPHOME=/opt/XEP

 1. Get docbook-xsl from http://sourceforge.net/projects/docbook/files/ and unpack it to resources/xsl (so that there is a folder resources/xsl/fo).

 1. Run **checksetup.sh** in the resources folder to check your configuration.

 1. Go to ../plainbook

 1. Run **"make docbook"**
  * May have to install GNU gawk if you do not have it already. I used "brew install gawk" on Mac.
  * May need to patch xep.xml file (after STAMP_PNG) with these 2 lines if you get "cannot have a value" errors.

        &lt;option name="VALIDATE" value="true"/><br>
        &lt;option name="DISCARD_IF_NOT_VALID" value="false"/>


 1. Open docbook.pdf.

When you get a pull request
===========================

 1. Check the status of your clone
  * git status

 1. Add/or checkout until your clone is clean

 1. Pull changes from davedf's branch
  * git pull davedf master

 1. Push the changes to your fork on github
  * git push origin master


When you want to get your changes back to GitHub
================================================

 1. Get the current status
  * git status

 1. Add any new files to the change list
  * git add file-name ...

 1. Add any changed files to the change list and commit
  * git add file-name

    ...

    git commit -m"message"

    or

    commit -a -m"message"

    to commit all changed files

 1. Push the changes to your fork on github
  * git push origin master

If you want the changes to be pulled, send a pull request on github.

Chuck Norris does not need to request a pull, you already have his changes, as he types.
