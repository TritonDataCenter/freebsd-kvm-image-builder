# freebsd-kvm-image-builder

This repo creates a custom FreeBSD install ISO and a KVM image for use in SmartOS and Triton.

## Requirements

This must be run on a FreeBSD machine or VirtualMachine.

## Setup

The following packages are required:

```
pkg install -y bash rsync cdrtools git
```

## Usage

To build a custom ISO, run the `create-iso` script:


```
./create-iso -r <RELEASE> -m <MIRROR> -p <MIRROR_PATH> -i <ISO> -c <ISO_CHECKSUM> -d <ISO_DIR> -M <MOUNT_POINT> -l <ISO_LAYOUT> -f <ISO_FILENAME>
```

This will download an ISO, created a customized layout with installerconfig, install the Triton guesttools then build the custom ISO.
