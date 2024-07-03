# removeMetadataCli
example on how to automate metadata removal without error/warning 


Add the following files in your workspace/git

manifest/destruct.xml
manifest/destructiveChanges.xml


In the destructiveChanges, list all the metadata that should be removed during deployment (BE CAREFUL)

Launch the following command prior to deployment of your metadata if needed :

sf project deploy start --manifest manifest/destruct.xml --pre-destructive-changes manifest/destructiveChanges.xml -r -g

-r -g : prevent the script to fail if the metadata is already deleted in the org
