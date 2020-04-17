# Dependent packages for Centos 7 and RHEL 7

This repo collects dependent packages for installing the Storidge CIO software on air gapped systems.

Follow the steps below to download the dependent packages, extract the Storidge software, and install on a node. Repeat the steps for all nodes that will be added to the cluster. 

After the initial git clone operation, the local repo can be updated by running `git pull`. This checks the master repo for changes and downloads any updates to the local repo. 

## Download and Install

1. Clone the repo to download dependent packages

```
cd /var/tmp
git clone https://github.com/Storidge/packages-c7xl3.git
```

2. Extract Storidge tarball to install directory

```
rm -rf /var/lib/storidge
mkdir -p /var/lib/storidge
tar xf /var/tmp/packages-c7xl3/cio-3225-c7xl3-ee.amd64.txz -C /var/lib/storidge
```

3. Install software in air gap mode

```
cd /var/lib/storidge/cio-3225-c7xl3.amd64/
./install --air-gap /var/tmp/packages-c7xl3/r77l3
```

## Initialize cluster

After installing softare on all nodes, create and initialize the cluster for operation. Run:

```
cioctl create
```

Follow the directions in the generated command strings, to add additional nodes and start cluster initizliation. 

