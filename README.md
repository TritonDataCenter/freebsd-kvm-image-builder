# freebsd-kvm-image-builder

This repo creates a custom FreeBSD install ISO and a KVM image for use in SmartOS and Triton.

**WARNING** This repo is a work in progress and most likely contains various bugs and issues.

## Requirements

This must be run on a FreeBSD machine or VirtualMachine.

## Setup

The following packages are required:

```
pkg install -y bash rsync cdrtools
```

## Usage

To build a custom ISO, run the `create-iso` script:


```
./create-iso -r <RELEASE> -m <MIRROR> -p <MIRROR_PATH> -i <ISO> -c <ISO_CHECKSUM> -d <ISO_DIR> -M <MOUNT_POINT> -l <ISO_LAYOUT> -f <ISO_FILENAME>
```

see `./create-iso -h` for usage

This will download an ISO, created a customized layout with installerconfig, install the Triton guesttools then build the custom ISO.

To build the FreeBSD KVM image run the `create-image` script:

```
./create-image -i <ISO> -n <IMAGE_NAME> -d <DESC> -u <HOMEPAGE> -o <OWNER_UUID> -p <IP> -m NETMASK -g <GATEWAY> -v <VLAN_ID> -U <NETWORK_UUID>
```

see `./create-image -h` for usage
