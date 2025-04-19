# 1. Show disk usage of all mounted filesystems
df -h

# 2. Show disk usage of current directory
du -sh .

# 3. Show disk usage of all folders in current directory
du -h --max-depth=1

# 4. Find large files over 100MB
find / -type f -size +100M

# 5. Show available inodes
df -i

# 6. Check disk I/O stats
iostat

# 7. Analyze disk usage with ncdu (install if needed)
ncdu /

# 8. Show partition layout
lsblk

# 9. Display disk space using tree view
tree -L 2 -h

# 10. Clean package cache (Debian/Ubuntu)
sudo apt clean

# 11. Clean unused journal logs
sudo journalctl --vacuum-time=3d

# 12. Remove orphaned packages (Debian/Ubuntu)
sudo apt autoremove

# 13. Check mounted filesystems
mount | column -t

# 14. Show disk usage by file type
find . -type f -exec du -Sh {} + | sort -rh | head -n 10

# 15. Check disk usage by user
sudo du -sh /home/*

# 16. Show total size of a folder
du -sh /path/to/folder

# 17. Count number of files in a directory
find /path -type f | wc -l

# 18. Check quota usage (if quotas are enabled)
quota -v

# 19. List deleted open files (can still take up space)
lsof | grep deleted

# 20. Check disk SMART health
sudo smartctl -a /dev/sda
