# 1. Create a new user
sudo adduser orderbook

# 2. Set the user's password
echo 'orderbook:Konstantinos1' | sudo chpasswd

# 3. Expire the password
sudo passwd --expire orderbook
# Output: passwd: password changed.

# 4. Edit sudoers file
sudo visudo
# No output (sudoers file opened)

sudo EDITOR=vim visudo
# No output (sudoers file opened in vim)

# 5. Switch to the new user and change the password
su orderbook
# Output: You are required to change your password immediately (administrator enforced).
# Changing password for orderbook.
# Current password:
# New password:
# Retype new password:

# 6. Create a directory as the new user
mkdir /home/test
# Output: mkdir: cannot create directory ‘/home/test’: Permission denied

sudo mkdir /home/test
# No output (directory created successfully)

# 7. List directory contents
ls -l /home
# Output:
# total 12
# drwxr-x--- 18 konstantinos-varelis konstantinos-varelis 4096 Aug  9 09:30 konstantinos-varelis
# drwxr-x---  2 orderbook            orderbook            4096 Aug  8 15:09 orderbook
# drwxr-xr-x  2 root                 root                 4096 Aug  9 09:30 test

# 8. Add orderbook to admins group
sudo groupadd admins
# No output (group created successfully)

sudo usermod -a -G admins orderbook
# No output (user added to group successfully)

groups orderbook
# Output: orderbook : orderbook users admins

# 9. Switch to the new user and attempt to create a file
su orderbook
# No output (switched user)

touch /home/test/test.txt
# Output: touch: cannot touch '/home/test/test.txt': Permission denied

sudo chgrp -R admins /home/test
# No output (group ownership changed successfully)

sudo chmod 771 /home/test
# No output (permissions changed successfully)

sudo chmod g+w /home/test
# No output (group write permissions added successfully)

# 10. Create the file again
touch /home/test/test.txt
# No output (file created successfully)

ls -l /home/test
# Output:
# total 0
# -rw-rw-r-- 1 orderbook orderbook 0 Aug  9 09:34 test.txt

# 11. Change ownership of the directory
sudo chown -R orderbook /home/test
# No output (ownership changed successfully)

ls -l /home/test
# Output:
# total 0
# -rw-rw-r-- 1 orderbook orderbook 0 Aug  9 09:34 test.txt

# 12. Create a script in the directory
cat << EOF > /home/test/orderbook.sh
echo "welcome to orderbook"
echo "Anyone can execute this script!!!"
echo "But not everyone can edit it"
EOF
# No output (script created successfully)

# 13. Change script permissions
chmod a+x+r /home/test/orderbook.sh
# No output (permissions changed successfully)

chmod o+x+r /home/test/orderbook.sh
# No output (permissions changed successfully)

chmod 755 /home/test/orderbook.sh
# No output (permissions changed successfully)

# 14. Edit and execute the script
vi /home/test/orderbook.sh
# No output (file opened in vi)

bash /home/test/orderbook.sh
# Output:
# welcome to orderbook
# Anyone can execute this script!!!
# But not everyone can edit it
