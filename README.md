# AzureSpotWorker - Folding@Home

This is an ARM (Azure Resource Manager) template to deploy an Azure Spot VM instance specifically for the Folding@home client.

You will need to update the parameters JSON file to reflect your own Azure subscription and resources.

Spot instances are currently available in Preview in the US East and South Central US Azure regions. South Central has more availability and is cheaper for Spot VMs currently.

As of April 2020, each VM deployment costs about $0.40/day once all disk, computer, and network resources are factored in. This is subject to change with Spot VM demand.

After VM deployment, you will need to download and configure the Folding@Home client here: https://foldingathome.org/start-folding/

Install the AMD GPU drivers for your worker VM here: https://docs.microsoft.com/en-us/azure/virtual-machines/windows/n-series-amd-driver-setup

To enable automatic logon and folding on your worker client at boot, use the Sysinternal Autologon tool: https://docs.microsoft.com/en-us/sysinternals/downloads/autologon

Use the StartAzureV2Vm Automation Runbook to automatically start your folding worker VMs if they are evicted due to demand: https://gallery.technet.microsoft.com/scriptcenter/Start-Azure-ARM-VMs-66fb875d

Please reach out to me if I can help with your setup: info@covid19folding.org or @josh_heffner on Twitter. More info on this project can be found on my site: https://joshheffner.com/how-to-run-foldinghome-on-azure-spot-vms/
