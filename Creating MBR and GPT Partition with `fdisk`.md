### Creating MBR Partition with `fdisk`

1. **Open `fdisk`**:
    ```sh
    sudo fdisk /dev/sdX
    ```
    Replace `/dev/sdX` with your actual disk identifier (e.g., `/dev/sda`).

2. **Create a new partition**:
    - Type `n` to create a new partition.
    - Follow the prompts to set the partition type, size, etc.

3. **Write changes**:
    - Type `w` to write the changes and exit `fdisk`.

### Creating GPT Partition with `gdisk`

1. **Open `gdisk`**:
    ```sh
    sudo gdisk /dev/sdX
    ```
    Replace `/dev/sdX` with your actual disk identifier (e.g., `/dev/sda`).

2. **Create a new partition**:
    - Type `n` to create a new partition.
    - Follow the prompts to set the partition type, size, etc.

3. **Write changes**:
    - Type `w` to write the changes and exit `gdisk`.

### Formatting the Partition

After creating the partition, you need to format it with a filesystem (e.g., ext4).

1. **Format the partition**:
    ```sh
    sudo mkfs.ext4 /dev/sdX1
    ```
    Replace `/dev/sdX1` with your partition identifier.

### Permanently Mounting a Partition

1. **Create a mount point**:
    ```sh
    sudo mkdir /mnt/my_partition
    ```

2. **Edit `/etc/fstab`**:
    Open `/etc/fstab` in a text editor:
    ```sh
    sudo nano /etc/fstab
    ```

3. **Add an entry for the partition**:
    ```plaintext
    /dev/sdX1  /mnt/my_partition  ext4  defaults  0  2
    ```
    Replace `/dev/sdX1` with your partition identifier and `ext4` with your filesystem type.

4. **Mount all filesystems**:
    ```sh
    sudo mount -a
    ```

### Unmounting a Partition

1. **Unmount the partition**:
    ```sh
    sudo umount /mnt/my_partition
    ```

2. **Remove the entry from `/etc/fstab`** if you no longer want it to be mounted automatically.

### Example `/etc/fstab` Entry

Here is an example of what an `/etc/fstab` entry might look like:

```plaintext
# <file system> <mount point> <type> <options> <dump> <pass>
/dev/sda1  /mnt/my_partition  ext4  defaults  0  2
```

### Summary

- Use `fdisk` for MBR and `gdisk` for GPT partitioning.
- Format the partition with a filesystem like `ext4`.
- Create a mount point and add an entry to `/etc/fstab` for permanent mounting.
- Use `mount -a` to mount all filesystems listed in `/etc/fstab`.
- Use `umount` to unmount partitions and remove entries from `/etc/fstab` if needed.

This should cover the basics of creating partitions and managing mounts in Linux.