# splunk_add_on_pkg
This repository contains Splunk Apps/Add-on packages

# Installing and configuring Splunk Add-on
1. Download the Splunk Add-on locally from the repo using the link below:
https://github.com/threatworx/splunk_packages/blob/master/packages/add_on/TA-threatworx-add-on-1.0.0.spl
<br/><b>Note</b> that Splunk package files have a ".spl" extension but are ".tgz" files. You can rename the file to change the extension and unzip the file.
3. Install the Splunk Add-on from <i>"Apps --> Manage --> Install app from file"</i>
4. Create an index for ThreatWorx data from <i>"Settings --> Indexes"</i>
5. Open the <i>"ThreatWorx Add-on"</i>
6. Configure the Add-on by navigating to <i>"Configuration --> Add-on Settings"</i>
7. Configure a new input by navigating to <i>"Inputs --> Create New Input"</i>

<p>You are all set.</p>

<b>Note</b> if you have a distributed Splunk environment (comprising of multiple Splunk Indexers, Splunk Heavy Forwarders, Splunk Search Head Clusters) you will want to update props.conf on the Splunk Search Head to avoid double JSON extraction at search time as below:<br>
<pre>
$ cat $SPLUNK_HOME/etc/apps/my_TA_threatworx/local/props.conf
[threatworx:vulnerability:impact]
KV_MODE = none
AUTO_KV_JSON = false
</pre>
