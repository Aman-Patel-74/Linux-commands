A-Logical-Volume-Manager-(LVM).md

A Logical Volume Manager (LVM) is a system of managing logical volumes, or filesystems, in a more flexible manner than traditional partitioning schemes. It allows for dynamic resizing, snapshotting, and combining of storage devices.

## Key Concepts of LVM:

1. **Physical Volumes (PVs)**: These are the actual storage devices (e.g., hard drives, SSDs).
2. **Volume Groups (VGs)**: These are pools of storage created by combining multiple PVs.
3. **Logical Volumes (LVs)**: These are the partitions created from the storage pool (VGs) and can be resized or moved without affecting the underlying physical storage.
4. **Physical Extents (PEs)**: Smallest allocation unit in a Physical Volume.
5. **Logical Extents (LEs)**: Smallest allocation unit in a Logical Volume, mapped to a Physical Extent.

## Using LVM:

1. **Install LVM Tools**

   Ensure you have the LVM tools installed on your system:

    sudo apt-get install lvm2  # For Debian-based systems
   sudo yum install lvm2      # For Red Hat-based systems

2. **Create Physical Volumes**

    sudo pvcreate /dev/sda1 /dev/sdb1

3. **Create a Volume Group**

    sudo vgcreate my_volume_group /dev/sda1 /dev/sdb1

4. **Create Logical Volumes**

    sudo lvcreate -n my_logical_volume -L 10G my_volume_group

5. **Format and Mount the Logical Volume**

    sudo mkfs.ext4 /dev/my_volume_group/my_logical_volume
   sudo mount /dev/my_volume_group/my_logical_volume /mnt

## LVM Commands in Linux

### 1. Physical Volume (PV) Commands

- **Create a Physical Volume:**

  pvcreate /dev/sdX


- **Display Physical Volumes:**

  pvs
  pvdisplay


- **Remove a Physical Volume:**

  pvremove /dev/sdX


### 2. Volume Group (VG) Commands

- **Create a Volume Group:**

  vgcreate vg_name /dev/sdX /dev/sdY


- **Display Volume Groups:**

  vgs
  vgdisplay


- **Extend a Volume Group:**

  vgextend vg_name /dev/sdZ


- **Reduce a Volume Group:**

  vgreduce vg_name /dev/sdX


- **Remove a Volume Group:**

  vgremove vg_name


### 3. Logical Volume (LV) Commands

- **Create a Logical Volume:**

  lvcreate -L 10G -n lv_name vg_name


- **Display Logical Volumes:**

  lvs
  lvdisplay


- **Extend a Logical Volume:**

  lvextend -L +5G /dev/vg_name/lv_name
  resize2fs /dev/vg_name/lv_name


- **Reduce a Logical Volume:**

  resize2fs /dev/vg_name/lv_name 15G
  lvreduce -L -5G /dev/vg_name/lv_name


- **Remove a Logical Volume:**

  lvremove /dev/vg_name/lv_name


### 4. Snapshot Commands

- **Create a Snapshot:**

  lvcreate --size 1G --snapshot --name snap_name /dev/vg_name/lv_name


- **Remove a Snapshot:**

  lvremove /dev/vg_name/snap_name


### 5. Miscellaneous Commands

- **Scan for LVM Components:**

  vgscan
  pvscan
  lvscan


- **Activate/Deactivate a Volume Group:**

  vgchange -a y vg_name  # Activate
  vgchange -a n vg_name  # Deactivate


- **Rename a Volume Group:**

  vgrename old_vg_name new_vg_name


- **Rename a Logical Volume:**

  lvrename /dev/vg_name/old_lv_name /dev/vg_name/new_lv_name


## Checking LVM Status and Partitions

- **Show all Physical Volumes:**

  pvdisplay
  pvs


- **Show all Volume Groups:**

  vgdisplay
  vgs


- **Show all Logical Volumes:**

  lvdisplay
  lvs


- **List all LVM Partitions:**

  lsblk
  blkid
  fdisk -l


- **Detailed LVM Tree:**

  lvmdiskscan
  lvm vgscan
  lvm lvscan


## Managing Multiple Disks (LVM & RAID)

- **List All Block Devices:**

  lsblk -f
  lsblk -o NAME,FSTYPE,SIZE,MOUNTPOINT


- **Check Mounted Partitions:**

  df -hT
  mount | column -t


### RAID Commands (mdadm - Multiple Disk Management)

- **Check RAID Status:**

  cat /proc/mdstat
  mdadm --detail --scan
  mdadm --detail /dev/md0  # Replace with RAID device


- **List RAID Devices:**

  mdadm --examine --scan


- **Check Disks in RAID:**

  mdadm --detail /dev/mdX  # Replace with the RAID device name


- **Verify RAID Disk Partitions:**

  fdisk -l /dev/sdX


- **Check if RAID is Degraded:**

  cat /proc/mdstat


LVM provides a powerful way to manage storage in Linux, allowing for dynamic resizing and efficient use of disk space. Always back up data before performing critical operations like resizing or reducing logical volumes.
