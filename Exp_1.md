# Exprement_1 : Create a forensic image of a storage devise'S using FTK imager 
## Aim and Description
The primary aim of using FTK Imager is to create a forensically sound, bit-for-bit copy of a storage device. This process, known as forensic imaging, is crucial for preserving the original evidence. The resulting image file is a perfect duplicate, including all active files, hidden files, unallocated space, and file slack. This allows investigators to analyze the copy without making any changes to the original media, which is essential for maintaining the integrity of the evidence for legal proceedings. FTK Imager is a free, stand-alone tool developed by AccessData (now Exterro) that is widely respected in the digital forensics community.
![alt text](<screenshorts/Exp_1/WhatsApp Image 2025-09-01 at 22.02.21_322d5d83.jpg>)



## Tools and Equipment
Forensic Workstation: A computer with sufficient storage space to save the forensic image. It should be a dedicated machine for forensic work to avoid contaminating the evidence.

Target Storage Device: The device to be imaged (e.g., hard drive, SSD, USB drive, memory card).

FTK Imager: The software application used to create the image. It can be downloaded for free from the Exterro website.

Write-Blocker: A hardware or software device that prevents any data from being written to the target storage device. This ensures the original evidence remains unaltered during the imaging process.

External Hard Drive: A separate, large-capacity hard drive to store the forensic image file. It should be different from the source drive being imaged.
![alt text](<screenshorts/Exp_1/WhatsApp Image 2025-09-01 at 22.02.20_a1532a3b.jpg>)

Power Supply: A reliable power source for both the workstation and the target device.
![alt text](<screenshorts/Exp_1/WhatsApp Image 2025-09-01 at 22.02.21_e58c28b4.jpg>)
## Procedure
The process involves a series of steps to ensure the integrity of the evidence is maintained.

Connect ![alt text](<screenshorts/Exp_1/WhatsApp Image 2025-09-01 at 22.02.21_e58c28b4.jpg>)the Target Device: Connect the storage device to your forensic workstation using a write-blocker. This is a non-negotiable step to prevent any changes to the original data.
![alt text](<screenshorts/Exp_1/WhatsApp Image 2025-09-01 at 22.02.22_c3996164.jpg>)
Launch FTK Imager: Open the FTK Imager application on your forensic workstation.

Start the Imaging Process: Navigate to the File menu and select Create Disk Image.

Select the Source: Choose the source type you want to image. For a full copy of a physical drive, select Physical Drive.

Identify the Target Drive: From the list of connected physical drives, select the one you want to image. The drive's make, model, and serial number should be used to confirm it's the correct one.
![alt text](<screenshorts/Exp_1/WhatsApp Image 2025-09-01 at 22.02.21_322d5d83.jpg>)
Add Image Destination: Click the Add button to configure the destination for the image file.

Choose Image Type: Select the image file format. Popular formats include Raw (dd) for a simple bit-for-bit copy or E01 (EnCase format) which includes metadata like case information, examiner name, and hash values within the image file itself.

Enter Case Information: If you selected E01, you'll be prompted to enter details such as the case number, evidence number, unique description, and examiner's name. This metadata is critical for maintaining the chain of custody.
![alt text](<screenshorts/Exp_1/WhatsApp Image 2025-09-01 at 22.02.22_c3996164.jpg>)

Specify Destination Path: Choose the location where the image file will be saved. This should be on your separate external hard drive, not on the forensic workstation's C: drive or the source drive.


Start Imaging: Check the "Verify images after they are created" box to automatically generate and compare hash values. Click Start to begin the imaging process.

## Result
Upon completion, FTK Imager will generate a report that documents the imaging process. The key results to check are:

Hash Values: The report will show the MD5 and SHA1 hash values for both the original source drive and the newly created image file. These values must be identical. If they don't match, the image is not a perfe![alt text](<screenshorts/Exp_1/WhatsApp Image 2025-09-01 at 22.02.22_c208a136.jpg>)ct copy, and the process needs to be repeated.

Image Summary: A text file will be created at the destination, summarizing all the details of the imaging process, including the start and end times, the source and destination paths, and the verification status. This log is a vital part of the forensic documentation.
![alt text](<screenshorts/Exp_1/WhatsApp Image 2025-09-01 at 22.02.22_7c110bec.jpg>)
Image File(s): The forensic image file(s) (e.g., evidence.e01 and evidence.e02) will be created at the specified destination. If fragmentation was enabled, the image will be split into multiple files.