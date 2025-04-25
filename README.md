# Analysis-of-the-Disk-Structure-using-Sleuth-Kit
### NAME : G LEKASRI
### REGISTER NUMBER : 212223100025
## AIM:
To analyze the disk structure of a given disk image using Sleuth Kit tools in Kali Linux.

## DESIGN STEPS:
### Step 1:
Obtain or create a disk image file (e.g., disk.dd) to analyze. Open the terminal in Kali Linux.

### Step 2:
Use Sleuth Kit tools like mmls, fsstat, and fls to examine the partition layout, file system details, and file listing.

### Step 3:
Interpret the output of the tools to understand the disk structure, including partitions, sectors, and files.

## PROGRAM:
Sleuth Kit Disk Analysis Commands

✅ Option 1: Create a Sample Disk Image (for Testing)

Let’s create a 10MB blank disk image and simulate file system activity:

```bash
cd ~/Downloads

# Step 1: Create an empty disk image
dd if=/dev/zero of=disk.dd bs=1M count=10

# Step 2: Format it with a file system (like FAT32)
mkfs.vfat disk.dd
```

## OUTPUT:
![dd1](https://github.com/user-attachments/assets/f0df8e81-c8e2-4320-8b1a-085b87a87c5b)

### Create Disk
![dd2](https://github.com/user-attachments/assets/382d0ca1-9490-43c7-9751-4472ca19ab00)

### mmls 
```bash
mmls disk.dd
```
### fls
```bash
fls -f fat -o 0 disk.dd
```
![dd3](https://github.com/user-attachments/assets/ad2a7b87-e216-4080-803b-44cf976e02c6)

![dd4](https://github.com/user-attachments/assets/7c866076-0671-476f-bbab-9837247581c0)

![dd5](https://github.com/user-attachments/assets/6f3e688b-1904-4f45-a127-a5b116100f60)

![dd6](https://github.com/user-attachments/assets/c63ab497-dcac-48d4-b816-6726e7e2dbf9)

## RESULT:
The analysis was performed successfully using Sleuth Kit, and the disk structure was understood in detail.
