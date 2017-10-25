[//]: # (Created on: October 25, 2017)
[//]: # (Author: Chad Young)
[//]: # (Contact: chad.young@dell.com)


# Readme for iometer snap
This is the same code that is found here: http://www.iometer.org/ except that it
has been "snapified" so that it can be run on Ubuntu Core 16. This snap is meant
to be used as a reference on how-to create snaps for Ubuntu Core 16 and as such
should not be used in a production environment. As with anything you find on the
internet please proceed with caution as you never know when Gremlins, Goblins,
or Trolls will appear.

## How to install
Install the snap using the following command:  
sudo snap install iometer-1.1.0-amd64.snap --devmode  

## How to run
Make sure that you have the following components:  
Windows PC with iometer installed  
Ubuntu Core 16 with this snap installed  
A local network with both the Windows and Linux PCs connected  
-- get their IP addresses  

Run the following command on the UC16 system:  
sudo iometer.dynamo -i (Windows IP address) -m (UC16 IP address) -n (Name)  

The switch -i defines the name of the Windows machine running IOmeter. It
is recommended to start dynamo after IOmeter. The hostname of the system that
should be benchmarked is assigned using the switch -m - that value is used by
IOmeter on the Windows system. If you have problems with DNS you can also
assign the IP. To assign a readable name to the IP inside IOmeter you can
specify a string along with the optional switch -n:  

For questions please email <chad_young@dell.com>

