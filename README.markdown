# Overview

This module manages the Unofficial prosvc yum repository configuration on an
Enterprise Linux host.  This repository is primary used for development and
testing, particularly with Vagrant.  This Puppet module makes it quick and easy
to work with software contained in the ProSvc repository.

# Quick Start

This will point yum to a copy of the prosvc repository running on your laptop
when using Vagrant.

    node default {
      $prosvc_repo_url="http://10.0.2.2/yum/prosvc"
      include prosvc_repo
    }

# Tips

The ProSvc repository may be easily cloned.

    cd /Library/WebServer/Documents/yum
    rsync -avxHP --delete rsync://yum.puppetlabs.com/packages/yum/prosvc/ \
      prosvc/

