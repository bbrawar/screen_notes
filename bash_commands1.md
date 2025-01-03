# Bash Notes

## System and Disk Operations
```bash
cp -r * ./misc/                # Copy all files and directories to the misc/ directory recursively.
cp -r *.py ./misc/             # Copy all Python files to the misc/ directory recursively.
cp * ./misc/                   # Copy all files to the misc/ directory (non-recursive).
df -h                          # Display disk space usage in human-readable format.
du -h --max-depth=1 ~/ | grep -E '^[0-9.]+[KMG]?\s+[^/]+' > directory_structure.txt  # Save directory size summary to a text file.
du -h ./ > septentrio_disk.txt  # Save disk usage of current directory to a file.
du -h ./ > sumanjit_backup.txt  # Save disk usage to a backup file.
du -h ./ septentrio_disk.txt    # Print disk usage of current directory and content from septentrio_disk.txt.
find . -type d -empty           # Find empty directories.
find . -type d -empty -delete   # Find and delete empty directories.
```
---
## Workspace
```bash
gsettings set org.gnome.shell.extensions.dash-to-dock isolate-workspaces true   #To isolate workspace
gsettings reset org.gnome.shell.extensions.dash-to-dock isolate-workspaces      #Revert effect
```
---
## File Search Operations
```bash
find ./ -name "*.ipynb" -exec grep -l "%store IPP_GPS" {} +  # Search Jupyter notebooks for a specific stored variable.
find ./ -name "*.m" -exec grep -l "ROT (dTEC/dt)" {} +       # Search MATLAB files for ROT-related calculations.
find ./ -name "*.m" -exec grep -l "S_{4_C}" {} +             # Search MATLAB files for specific S4 content.
grep -rIl 'NavIC_S4c2020_2022.csv'                           # Find files containing 'NavIC_S4c2020_2022.csv'.
grep -rnw ./ -e 'scinti_S4c2020_2022.csv'                    # Search recursively for 'scinti_S4c2020_2022.csv' with line numbers.
```
---
## Git and GitHub Operations
```bash
find ./ -name "*.ipynb" -exec grep -l "%store IPP_GPS" {} +  # Search Jupyter notebooks for a specific stored variable.
find ./ -name "*.m" -exec grep -l "ROT (dTEC/dt)" {} +       # Search MATLAB files for ROT-related calculations.
find ./ -name "*.m" -exec grep -l "S_{4_C}" {} +             # Search MATLAB files for specific S4 content.
grep -rIl 'NavIC_S4c2020_2022.csv'                           # Find files containing 'NavIC_S4c2020_2022.csv'.
grep -rnw ./ -e 'scinti_S4c2020_2022.csv'                    # Search recursively for 'scinti_S4c2020_2022.csv' with line numbers.
```
---
## Git and GitHub Operations
```bash
gh auth login                  # Authenticate GitHub CLI.
gh add .                       # Stage all changes.
gh clone misc                  # Clone the 'misc' repository.
gh repo create misc --private  # Create a private repository named 'misc'.
gh repo misc --clone           # Clone the 'misc' repository.
git --version                  # Check the Git version.
git add *                      # Stage all changes.
git commit -m 'files added'    # Commit staged changes with a message.
git config --global user.email "bbrawar@gmail.com"  # Configure Git user email.
git config --global user.name "Bhuvnesh Brawar"     # Configure Git user name.
git push -u origin main        # Push commits to the main branch and set upstream.
git clone https://github.com/bbrawar/ionex_reader.git  # Clone the ionex_reader repository.
git branch -M main             # Rename the current branch to 'main'.
```
---
## SSH Operations
```bash
ssh-keygen                           # Generate a new SSH key pair.
ssh-keygen -R 10.205.2.175           # Remove old SSH key from known hosts.
ssh-keygen -t rsa -C "LabPC_bhuvi"   # Generate an RSA SSH key with a comment.
ssh git@github.com:bbrawar/ismr_processor.git  # Test SSH connection to GitHub.
```
---
## Python and Jupyter Operations
```bash
python3 -m georinex.read sndl1260.21d.Z  # Use georinex module to read a compressed RINEX file.
python3 -m pytest                        # Run tests using pytest.
jupyter-nbconvert --to script IPP_NavIC.ipynb  # Convert a Jupyter notebook to a Python script.
```
---
## File Compression and Backup
```bash
tar xvfz hplip-3.22.6.tar.gz  # Extract a tar.gz archive.
split -b 3G 2024_btech_lab_demo.zip  # Split a large zip file into 3GB parts.
unzip RTKLIB-master.zip       # Extract a zip file.
```
---
## Bluetooth and Sound Settings
```bash
pactl load-module module-bluetooth-discover  # Enable Bluetooth discovery module.
pactl unload-module module-bluetooth-discover  # Disable Bluetooth discovery module.
```
---
## System Configuration and Management
```bash
sudo blkid                                # List block devices and their UUIDs.
sudo chown -R $USER /DATA/                # Change ownership of /DATA/ directory to the current user.
sudo find / -name dwagent -type f         # Search for 'dwagent' files.
sudo systemctl restart dwagent.service    # Restart the dwagent service.
sudo vi /etc/fstab                        # Edit the fstab file for mounting configuration.
systemctl restart bluetooth.*             # Restart Bluetooth services.
```
---
## Repository Structure and Tree Commands
```bash
tree -h --du -o septentrio_disk.txt ./  # Generate a directory tree with disk usage in a file.
tree -H ./ > septentrio_disk.html       # Generate an HTML version of the directory tree.
mkdir -p ismr_processor/ismr_processor/ tests  # Create nested directories.
```
---
## Miscellaneous Commands
```bash
make                                     # Run make utility to build targets specified in Makefile.
mv python_programs gnss_school/          # Move python_programs directory to gnss_school/.
touch downloader.py                      # Create an empty Python file.
touch setup.py README.md .gitignore      # Create multiple empty files.
wget --ftp-user anonymous --ftp-password bbrawar -r ftps://gdc.cddis.eosdis.nasa.gov/vlbi/ivsdata/ngs/2023  # Download data from an FTP server.
winecfg                                  # Open Wine configuration tool.
```
---
## LaTeX to Word Conversion
```bash
pandoc -o ./../out.docx -t docx main.tex  # Convert LaTeX to Word document.
pandoc main.tex -o book.docx              # Generate a Word document from LaTeX.
```
---
## Gnome Utilities
```bash
gnome-control-center  # Open the GNOME control center.
```
