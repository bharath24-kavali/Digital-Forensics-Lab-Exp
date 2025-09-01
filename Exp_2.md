# Exprement_2: Recover deleted or damaged files from a storage device using Test Disk  
## Aim and Description
The primary aim of TestDisk is to address structural damage to a storage device. This includes repairing corrupted partition tables, restoring deleted partitions, and making non-booting disks bootable again. While it has an "undelete" function for specific file systems, its strength lies in fixing the underlying file system structure, which can, in turn, make lost files accessible again.
![alt text](<screenshorts/Screenshot (2).png>)

## Tools and Equipment
Computer: A functioning computer to run the TestDisk software.
![alt text](<screenshorts/Screenshot (9).png>)
Target Storage Device: The hard drive, USB drive, or memory card that has the lost or damaged data.

TestDisk: The free, open-source software, available for multiple operating systems like Windows, Linux, and macOS.

Wri![alt text](<screenshorts/Screenshot (5).png>)te-blocker (Optional but Recommended): A hardware or software write-blocker to prevent any accidental writes to the target device during the recovery process. This is crucial for forensic or sensitive data recovery.

External Storage Device: A separate drive with enough free space to save the recovered files. Never save recovered files to the same drive you are recovering from, as this can overwrite the data you are trying to restore.

## Procedure
The TestDisk process is text-based and requires careful navigation using arrow keys.

Launch TestDisk: Run the testdisk_win.exe (on Windows) or testdisk (on Linux/macOS) as an administrator.
![alt text](<screenshorts/Screenshot (11).png>)
Create Log File: Choose "Create" to create a log file of the recovery process. This is important for documentation and troubleshooting.
![alt text](<screenshorts/Screenshot (6).png>)
Select the Disk: From the list of connected storage devices, select the one you want to recover data from. Use the disk size and model to ensure you've picked the correct one. Press Proceed.

Choose Partition Table Type: TestDisk will try to auto-detect the partition table type (e.g., Intel/PC, EFI GPT). The default option is usually the correct one. Press Enter.

Analyze the Partition Structure: Select the Analyze option and press Enter to check the current partition structure.

Quick Search: Choose Quick Search to have TestDisk scan for lost or deleted partitions. If the lost partition is found, it will be listed. You can highlight it and press P to view the files within it to confirm it's the correct partition.
![alt text](<screenshorts/Screenshot (10).png>)

Deeper Search: If the Quick Search doesn't find the partition, select Deeper Search for a more thorough scan of the entire disk.
![alt text](<screenshorts/Screenshot (10).png>)
Undelete Files: Once the correct partition is selected, you can often navigate to the Undelete option. TestDisk will list recoverable files, often marked in red.


Copy Recovered Files: Use the arrow keys and the C key to select and copy the deleted files to your separate, external storage device.

## Result
Upon completion, you will have the recovered files on your destination drive. The success of the recovery depends on whether the original data has been overwritten since its deletion. Key results to note are:
![alt text](<screenshorts/Screenshot (10).png>)
File Recovery: Successfully recovered files will be copied to the specified destination.

Log File: A log file is created detailing the entire process, including the steps taken and any errors encountered. This is essential for documenting the recovery.
![alt text](<screenshorts/Screenshot (7).png>)
Repaired Partition: If you chose to repair a damaged partition, the partition table will be rewritten, making the disk accessible again.