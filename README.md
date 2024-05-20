# splunk_add_on_pkg
This repository contains Splunk Apps/Add-on packages

# Installing and configuring Splunk Add-on
1. Download the Splunk Add-on locally from the repo using the link below:
https://github.com/threatworx/splunk_packages/blob/master/packages/add_on/TA-threatworx-add-on-1.0.0.spl
Note that Splunk package files have an ".spl" extension but are ".tgz" files. One can rename the file to change the extension and unzip the file.
3. Install the Splunk Add-on from "Apps --> Manage --> Install app from file"
4. Create an index for ThreatWorx data from "Settings --> Indexes"
5. Open the "ThreatWorx Add-on"
6. Configure the Add-on by navigating to "Configuration --> Add-on Settings"
7. Configure a new input by navigating to "Inputs --> Create New Input"
You are all set.
