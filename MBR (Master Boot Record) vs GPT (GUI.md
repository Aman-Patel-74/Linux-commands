### MBR (Master Boot Record) vs GPT (GUID Partition Table)

#### MBR (Master Boot Record)
- **Description**: An older partitioning scheme used by BIOS-based systems.
- **Partition Limit**: Supports up to 4 primary partitions. To create more partitions, one primary partition can be converted into an extended partition, which can contain multiple logical partitions.
- **Disk Size Limit**: Supports disks up to 2 TB in size.
- **Boot Data Location**: Stores boot data in the first sector of the disk.
- **Compatibility**: Widely supported by older systems and operating systems.

#### GPT (GUID Partition Table)
- **Description**: A newer partitioning scheme used by UEFI-based systems.
- **Partition Limit**: Supports up to 128 primary partitions (without the need for extended or logical partitions).
- **Disk Size Limit**: Supports disks larger than 2 TB (up to 9.4 ZB).
- **Boot Data Location**: Stores multiple copies of boot data across the disk for redundancy and recovery.
- **Compatibility**: Required for UEFI systems and supported by modern operating systems. Provides better data integrity and recovery options.

### Key Differences
- **Partition Limit**: MBR supports up to 4 primary partitions, while GPT supports up to 128 primary partitions.
- **Disk Size Limit**: MBR supports disks up to 2 TB, while GPT supports disks larger than 2 TB.
- **Boot Data**: MBR stores boot data in a single location, while GPT stores multiple copies for redundancy.
- **Compatibility**: MBR is compatible with older BIOS systems, while GPT is required for UEFI systems.

### Example Commands in Linux
- **Viewing Partition Table**:
  ```sh
  sudo fdisk -l /dev/sdX
  sudo parted /dev/sdX print
  ```

- **Converting MBR to GPT** (using `gdisk`):
  ```sh
  sudo gdisk /dev/sdX
  ```

These differences highlight the advantages of GPT over MBR, especially for modern systems with larger disks and UEFI firmware.