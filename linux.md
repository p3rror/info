# Linux

  ## file processing:

ls –> directory listing
ls -al –> formatted listing with hidden files
cd <DIR> -> change directory to dir
cd –> change to home
pwd –> show current directory
mkdir <DIR> –> create a directory dir
rm <FILE> – delete file
rm -r <DIR> –> delete directory dir
rm -f <FILE> –> force remove file
rm -rf <DIR> –> force remove directory dir *
cp <FILE1> <FILE2> –> copy file1 to file2
cp -r <DIR1> <DIR2> –> copy dir1 to dir2; create dir2 if it doesn't exist
mv <FILE1> <FILE2> –> rename or move file1 to file2 if file2 is an existing directory, moves file1 into directory file2
ln -s <FILE> <LINK> –> create symbolic link link to file
touch <FILE> –> create or update file
cat > <FILE> –> places standard input into file
more <FILE> –> output the contents of file
head <FILE> –> output the first 10 lines of file
tail <FILE> –> output the last 10 lines of file
tail -f <FILE> –> output the contents of file as it grows, starting with the last 10 lines

  ## process management:

ps –> display your currently active processes
top –> display all running processes
kill <PID> –> kill process id pid
killall proc –> kill all processes named proc *
bg –> lists stopped or background jobs; resume a stopped job in the background
fg –> brings the most recent job to foreground
fg n –> brings job n to the foreground

  ## file permissions:

chmod octal file –> change the permissions of file to octal, which can be found separately for user, group, and world by adding:
4 – read (r)
2 – write (w)
1 – execute (x)
  
    ### examples:

    chmod 777 – read, write, execute for all
    chmod 755 – rwx for owner, rx for group and world

  ## ssh:

ssh <USER>@<HOST> –> connect to host as user
ssh -p <PORT> <USER>@<HOST> –> connect to host on port port as user
ssh-copy-id <USER>@<HOST> –> add your key to host for user to enable a keyed or passwordless login

  ## searching:

grep pattern files –> search for pattern in files
grep -r pattern dir –> search recursively for pattern in dir
command | grep pattern –> search for pattern in the output of command
locate file –> find all instances of file

  ## system info:

date –> show the current date and time
cal –> show this month's calendar
uptime –> show current uptime
w –> display who is online
whoami –> who you are logged in as
finger user –> display information about user
uname -a –> show kernel information
cat /proc/cpuinfo –> cpu information
cat /proc/meminfo –> memory information
man command –> show the manual for command
df –> show disk usage
du –> show directory space usage
free –> show memory and swap usage
whereis app –> show possible locations of app
which app –> show which app will be run by default

  ## compression:

tar cf file.tar files –> create a tar named file.tar containing files
tar xf file.tar –> extract the files from file.tar
tar czf file.tar.gz files –> create a tar with Gzip compression
tar xzf file.tar.gz –> extract a tar using Gzip
tar cjf file.tar.bz2 –> create a tar with Bzip2 compression
tar xjf file.tar.bz2 –> extract a tar using Bzip2
gzip file –> compresses file and renames it to file.gz
gzip -d file.gz –> decompresses file.gz back to file

  ## network:

ping host –> ping host and output results
whois domain –> get whois information for domain
dig domain –> get DNS information for domain
dig -x host –> reverse lookup host
wget file –> download file
wget -c file –> continue a stopped download

  ## installation:

dpkg -i pkg.deb –> install a package (Debian)
rpm -Uvh pkg.rpm –> install a package (RPM)

  ## install from source:

./configure
make
make install

  ## shortcuts:

Ctrl+C –> halts the current command
Ctrl+Z –> stops the current command, resume with
fg in the foreground or bg in the background
Ctrl+D –> log out of current session, similar to exit
Ctrl+W –> erases one word in the current line
Ctrl+U –> erases the whole line
Ctrl+R –> type to bring up a recent command
!! - repeats the last command
exit – log out of current session
