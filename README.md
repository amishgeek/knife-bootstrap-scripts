# Knife Bootstrap Scripts

Miscellaneous scripts for use with knife to bootstrap remote servers & instances with chef-client

## About

This repository is where I store my scripts which I use to bootstrap remote servers with knife.  These are customized scripts to handle cases that the default knife bootstrap scripts cannot handle.


## Using these scripts

- Place the script you wish to use inside your .chef/bootstrap/ folder
- Call the script when using the "knife bootstrap" command, using the -d flag
-- Example: "knife bootstrap <SERVER IP> -d <SCRIPTNAME>"


# Script Details

## centos5-amazon-rvm.erb

*USE:* knife bootstrap <SERVER IP> -d centos5-amazon-rvm

This script installs ruby 1.8.7 and chef via RVM.  It follows the standards RVM installation methods outlined http://beginrescueend.com/rvm/install/

It does not rely on any .rpm's other than the EPEL .rpm which is required for git and a couple other dependencies.  Since it uses RVM for ruby and chef and does not require prepackaged files for chef, it *should* continue to work with future versions/releases of the OS.

### Supported (Tested) Distros

- Centos 5.x
- Amazon Linux