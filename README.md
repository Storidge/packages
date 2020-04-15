# Dependent packages for Centos 7 and RHEL 7

This repo collects dependent packages for installing the Storidge CIO software on air gapped systems.


## Download and Install

1. Clone the repo

```
cd /var/tmp
git clone https://github.com/Storidge/packages-c7xl3.git
```

2. Extract Storidge tarball to install directory

```
rm -rf /var/lib/storidge
mkdir -p /var/lib/storidge
tar xf /var/tmp/packages-c7xl3/cio-3222-c7xl3-ee.amd64.txz -C /var/lib/storidge
```

3. Install

```
cd /var/lib/storidge/cio-3222-c7xl3.amd64/
[download r77l3.txz tarball to /var/tmp/packages-c7xl3/]
./install --air-gap /var/tmp/packages-c7xl3/r77l3.txz
```

