---
id: page-plugin
title: Qordoba - ftp-ftps integration
header_title: Qordoba - ftp-ftps integration
header_icon: /assets/images/icons/plugins/ftp-ftps-integration.png
breadcrumbs:
  Plugins: /plugins
---

Qordoba can fetch files from an SFTP or FTP server remotely and overwrite the contents of the files with content coming from Qordoba l10n workflow.

In the tables below, you can view which parameters you can use to customize your configuration with this particular system:

```
'Hostname'The fully qualified hostname or IP address of the remote system
'Port'	22	The port that the remote system is listening on for file transfers
'Username'	
'Password' Password for the user account Sensitive Property
'Private Key Path'	The fully qualified path to the Private Key file
'Private Key Passphrase' Password for the private key Sensitive Property
'Remote Path'	The path on the remote system from which to pull or push files
'File Filter Regex'	Provides a Java Regular Expression for filtering Filenames; if a filter is supplied, only files whose names match that Regular Expression will be fetched
'Path Filter Regex'	When Search Recursively is true, then only subdirectories whose path matches the given Regular Expression will be scanned
'Polling Interval'	60 sec	Determines how long to wait between fetching the listing for new files
'Search Recursively'	false	If true, will pull files from arbitrarily nested subdirectories; otherwise, will not traverse subdirectories
'Ignore Dotted Files'	true	If true, files whose names begin with a dot (".") will be ignored
'Delete Original'	true	Determines whether or not the file is deleted from the remote system after it has been successfully transferred
'Connection Timeout'	30 sec	Amount of time to wait before timing out while creating a connection
'Data Timeout'	30 sec	When transferring a file between the local and remote system, this value specifies how long is allowed to elapse without any data being transferred between systems
'Host Key File'	If supplied, the given file will be used as the Host Key; otherwise, no use host key file will be used
'Max Selects'	100	The maximum number of files to pull in a single connection
'Remote Poll Batch Size'	5000	The value specifies how many file paths to find in a given directory on the remote system when doing a file listing. This value in general should not need to be modified but when polling against a remote system with a tremendous number of files this value can be critical. Setting this value too high can result very poor performance and setting it too low can cause the flow to be slower than normal.
'Strict Host Key Checking'	false	Indicates whether or not strict enforcement of hosts keys should be applied
'Send Keep Alive on Timeout'	true	Indicates whether or not to send a single Keep Alive message when SSH socket times out
'Use Compression'	false	Indicates whether or not ZLIB compression should be used when transferring files
'Use Natural Ordering'	false	If true, will pull files in the order in which they are naturally listed; otherwise, the order in which the files will be pulled is not defined
```
