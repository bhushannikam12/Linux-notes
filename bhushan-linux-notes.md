# Bhushan Linux Notes

1. pwd --> It shows the present working directory of the user

2. ls --> It shows the list of the folders in home directory.
    umount

3. clear --> It doesn't delete but clears the screen.
    e2fsck -f /dev/vg/bh → lvm path

4. lsusb --> It shows the information related to the usb.
    resize2fs /lvm path + Size you want in lv

5. lscpu --> It shows the whole cpu information.
    lvreduce -L 500M /lvm path
    Note: if after using mount command error found use
    resize2fs /lvm path.

6. lspci --> It shows the peripheral component connected to system example- ethernet cable.

7. free --> It shows the memory status ie how much is occupied how much is free in numerical format but with no unit. So free -h is the other option to use this command and it will show human readable format.

8. man --> It is used to see detail of any other command. Suppose if you forget the free -h command you can type "man free" then it will show you a detailed note on free command along with options.

9. info --> Its just same as man command but the data is unstructured.

10. date --> It shows date along with day and time as per your region.
    NOTE : If you want a detail info for any command just use man in front of the specific command.

11. tty --> It shows the terminal type: Terminal start from 0

12. whoami --> It shows the name of current user who is logged in.

13. whatis --> If you don't know what a particular command is for you can simply use whatis "command you want to know about".

14. who --> It shows the login information of all the user using machine/terminal along with time.

15. w --> It shows who is logged in and what they are doing. It also shows load average of the machine.

16. uname --> It shows which kernel is in used.

17. shutdown --> It is used to shutdown your machine although it can be cancelled within a minute by using shutdown -c.

18. history --> It shows all the command used after

19. ls -a --> It shows all the hidden files.

20. touch --> Creates and new empty file eg: touch "filename".

21. touch filename --> Creates an hidden empty file.

22. ls -la --> Shows all the files including hidden files.
    
23. ls -ltr --> shows folder name of file/directory
    Syntax --> is -ltd <directory name>


24. rm --> Used for removing files or directories eg: rm "filename"

25. touch filename {1 . .10} --> Used to create files as per the number in the brackets. also updates timestamp.

26. rm -f --> Used for removing file forcefully, it avoids the warning & deletes the file directly

27. rm -vf --> Used for showing "removed file" in the di mode

28. dmidecode --> Shows Bios information, Serial no etc. root user can handle this command.

29. | -> pipe command --> It is very useful in di mode as the mouse is not working, there also we can't scroll by up/downs key so to overcome this pipe command came into picture mostly used along with "cat + file name + I + Read operations (less, more etc.)"

30. echo --> Before this command whatever you write in " " is printed on next line.

31. hostname --> Used to print or change the hostname for current login session (Temporarily)
    Note - To change your hostname permanently you can use "hostnamectl set-hostname "Name"

32. "bash" -> To apply changes / update changes.

33. mv → Used to move and rename file
    Syntax: mv (filename) (destination)
    ex: mv file.txt /home/ → move file
    mv file.txt /home/new.txt → rename file

34. cp → Used to copy a file from one directory to other
    ex: cp (filename) (destination)
    cp new.txt /root

35. mkdir → Used to create a new directory
    ex: mkdir (directory name)

36. rmdir → Used to remove a created directory /
    rm-rf(directory name) should be empty

37. mkdir -p → ex: mkdir -p P5/P6/P7
    Here this command is creating a sub directory whose parent is P5.
    User administration (root user)

38. chage -m+days+username → To change the minimum day to change password again

39. chage -l+username → Shows information regarding current user in the prompt.

40. chage -M+days+username → To change the maximum day to change password

41. chage -R + username chage +
    chage -R + days + username → Sets expiration warning
    days to change password.

42. chage -I + days + username →

43. chage -E + "11th July 2023" + username → used to expire
    a local user login.

44. chage -d + "date" + username → changes last password
    changed date.

45. useradd -u → Set wid for user

46. useradd -g → sets gid for user

47. useradd -c → sets comment for user

48. useradd -d → set deletes user, sets directory for user

49. useradd -e → sets expiry date for user

50. useradd -s → sets shell to the user.
    Note: useradd command doesn't modify previous user info.
    it can set to new/creating user info.

51. userdel + username → deletes user but not home directory.

52. userdel -r + username → deletes user with home directory.

53. usermod -s → To change the shell of the particular user
    ex: usermod -s + new shell + username

54. usermod -e → To modify the expiry date of a particular user
    ex: usermod -e + date in " " + username

55. usermod -L → To lock a particular user from logging in
    ex: usermod -L + username

56. usermod -U → To unlock a particular user
    ex: usermod -U + username

57. groupadd → To add new group without user
    ex: groupadd + groupname

58. groupadd -g → To give gid of your own will
    ex: groupadd -g + gid + groupname

59. groupadd -n → To give new name to a created group
    ex: groupadd -n + new name + existing name

60. groupdel → To delete the group
    ex: groupdel + groupname

61. gpasswd → To set password to a group
    ex: gpasswd + groupname

62. gpasswd -a → Add a single user to group
    ex: gpasswd -a + username + groupname

63. gpasswd -d -> delete user from a group
    ex: gpasswd -d + username + groupname.

64. gpasswd -M -> Add multiple user to a group but the previous member should also be added again or else they get replaced.
    ex: gpasswd -M username, username, username + groupname.

65. gpasswd -A -> sets admin to a group
    ex: gpasswd -A + username + groupname.

66. gpasswd -A" -> Remove admin & of a group...
    ex: gpasswd -A" + groupname.

67. pwd pwuncony -> Give this command, after checking lotelshan. It is used for hiding the shadow file.

68. pwconv -> Used for unhiding the shadow file.

69. grpconv -> hides gshadow file

70. grpconv -> Unhides gshadow file

71. alias -> give's alternate command name to same command (modify's command name for temporarily)
    ex: alias newname = command name.

72. passwd -k -> Used to disable user password, since user can't login after then (inactivate's password)
    ex: passwd -k + username.

73. passwd -u → Set's the password back to active
    for the user
    ex: passwd -u + username.

74. In → Creates a hard link of a file which is
    like a copy but it makes changes in runtime.
    ex: ln + filename + new name of hard link.

75. ls -s → Creates soft link of a particular file,
    changes are replicated in both the files but if
    original file is deleted soft link won't work
    ex: ls -s + filename + username for soft link.

76. ls -l → Shows metadata of all the data in your
    home directory. (Inode number)

78. chown → Used for changing the ownership of a
    file or directory
    ex: chown + ownername:groupname + filename

79. wc → Show 1) No. of lines 2) No. of words 3) No
    of characters in a particular text file
    ex: wc + filename.

80. tee → Shows content on Terminal as well as save
    into a new file.
    ex: Command whose data you want to save + "|" + tee
    + new file name.
    Commands In Linux

81. umask → Temporary changes the umask value
    ex: umask + value

82. chmod → Modify the permission, given to file or directory (root user only)
    ex: chmod ugo + permission (s,w,x) + filename or directory name.
    Note → Here u→ user, g→ group, o→ other and the "+" sign is mandatory to add permission also using the same way you can remove permission just switch "-" with "-".eq+ chmod ugo- permission + filename.
    The "=" sign & here remove the previous permission and give the mentioned permission only.
    ex chmod u=x (removes other permission and gives * permission).

83. chmod u+s + path of command → gives user/ local user the access of privileged commands also known as suid bit

84. chmod g+s + path of directory → If group have permissions to execute. It will show small s if not shows Big 'S'.

85. chmod o+t + path of directory → Sticky Bit only. owner have access to delete or rename a particular file. Show capital T in other's place when other's can't have execution permission.

86. getfacl + Filename or directory name → shows the file, owner, group name along with all permission those are given to a particular file.

87. setfacl -m + u:username:permission + filename/dir.
    → Gives a particular user, a specific permission
    to the file mentioned.

88. setfacl -x u:username /directory or filename
    → Removes the user of which we gave access
    in above command.

89. setfacl -b + /filename or directory
    → Remove all user's who were granted permission
    by ACL

90. setfacl -m g:groupname /file or directory
    → To give ACL access to group.
    ex: setfacl -m g:groupname +permission + filename

91. grep → Searches for a string in a particular files
    works similar to "ctrl+F" as in windows.
    ex: grep "string to find" /filename.

92. grep -i → Work almost same as grep but ignores
    case sensitive words.

93. grep -E → If user want to search+2 or more
    word then he can use pipe command between
    two words
    ex grep "string 1 | string 2" filename.

94. grep -nE → show the number of the line from file on which the string matched.
    grep -cE → Shows Number of lines in the output

95. locate → Help to serach file path but you should know the file name correctly.
    ex: locate filename
    du -sh → Shows the file size of a directory in human readable format.
    ex: du -sh /directory name.

96. find → Helps to search a specific file returns the file of same name like if you search for file1 it will return only files name with file1 and not file12. This the difference between locate & find.
    ex: find /-name filename.
    tar → Helps to create a zip file, of a directory or a file into another directory
    ex: tar -crf /path/new filename.tar & /directory name.

97. tar -tvf /bgmi/insta.tar → To see files in tar.
    tar filename

98. tar -xvf /bgmi/insta.tar -C/bgmi → To entract tar file.
    directory to store tar

99. tail -f /var/log/cron → Shows logs for all the crons which are executing in backend by cron.

100. ls -i → Shows inode number of all files and directories in current directory.

101. wget url -> for downloading packages

102. curl-0 -> for downloading packages

103. rpm -q + package name -> To check weather pkg
    is installed or not

104. rpm -qa -> Shows all the packages present in the system.

105. rpm -ivh + full package name -> for installing downloaded packages.

106. rpm -evh + package name -> for uninstalling the downloaded package.

107. rpm -qi + packagename -> gives detailed information of a particular command/package.

108. rpm -qip + full packagename with version
    -> Shows detailed information of a package which is downloaded in the system but is not installed yet.

109. rpm -ql + package name -> Shows the list of files and directories installed by specific rpm package.

110. rpm -qip -> Gives detail info of packages which are
    not installed or are not downloaded yet, you just
    need a Binary Package link of particular command.

111. yumdownloader + Package Name - For downloading pages.

112. yum install + Package Name - For installing pkg through
    yum ie high level tool of red hat family.

113. yum remove + Package Name - Remove downloaded package
    from system.

114. yum list installed -> Shows the list of packages which
    are already installed.

115. yum provides + command name -> To check package
    name of a particular command.

116. yum reinstall + package name -> For reinstalling missing
    commands.

117. yum update -> Updates each and every packages on
    your system also fines previous bug if any.

118. yum autoremove + command name -> Removes package
    along with it's dependencies:

119. yum repolist -> Show all the enabled repository list
    on your system

120. yum repolist all -> Show disabled as well as enabled
    repolists on your system

121. yum clean all -> Used to free up disk space by
    removing unnecessary cached files.

122. df -hT -> Shops all the mounted partition in your
    System.

123. mount /dev/sdb1 -> mounts you partition to a
    specific directory temporarily.
    ex: mount /dev/sdb1 /mnt -> mounted on /mnt

124. umount +, directory name -> unmounts the directory
    from partition.

125. mkfs. + Tab -> Used for making file systems.
    type mkfs. and Tab multiple options will
    be shown select the file type insert it after
    mkfs. and enter.

126. partprobe -> Run this command after editing
    an saving partition to refresh your system.

127. lsblk -> Used to list information about block devices,
    including partition and disks

128. blkid -> Used to display information about block device
    and their associated file system attributes.

129. pvcreate -> Creates a physical volume of partitions mention
    ex: pvcreate /dev/sdb1 /dev/sdb3

130. pvs -> Shows the physical volume data/information.

131. vgcreate -> Used for merging two or more physical
    volume
    ex: vgcreate <groupname> /dev/sdb1 /dev/sdb3
    physical volume

132. vgs -> shows the combined storage information.

133. lvcreate -> Used for creating a logical volume inside
    a volume group.
    ex: lvcreate -L <size> -n <name> <volume groupname>
    lvcreate -L +1G -n lv1 vg

134. lvs -> Shows, information about logical volume
    which is created in volume group.

135. lvremove -> Used to delete the logical volume inside
    volume group.
    ex: lvremove /dev/vg/lv

136. vgremove → deletes the volume group.
    ex: vgremove + group name

137. pvremove → deletes parti physical volumes which were created to merge and create a vg group.
    ex: pvremove + physical volume + physical volume
    ex: pvremove /dev/sdb1 /dev/sdb3

138. vgentend → Used to extend volume group with the help of physical volume
    ex: vgcreate + groupname + physical volume path.

139. lvextend → Used to extend logical volume inside volume group.
    ex: lvextend -l +500M /dev/vg/bh
    ex: lvextend -l +size + lvm path.
    After running the above command the data is not updated in df-hT command for that you will need to run "resize2fs + /lvm path" then it will tell you to first run "e2fsk -f + lvm path" and then run resize command again. New the data is updated in df-hT, this process is for entry file type only. Different file type have different process.

140. lvreduce → Used to reduce logical volume disk size &
    ex: steps: 1) take backup
               2)umount    
               3)e2fsck -f /dev/vg/bh --> lvm path
               4)resize2fs /lvm path + size you want in lv
               5)lvreduce -L -500M /lvm path
Note:If after using mount command error found use resize2fs /lvm path               
               
141. Ivrename → Used for changing the name of logical
    volume ex: Ivrename + lvm path + newname.

142. vgreduce → Used to reduce physical volume from volume group, remove only unused physical volume
    ex: vgreduce + groupname + physical volu path.
    Note: Basic commands that we use regularly are already
    installed with their respective package. Still there are
    many more command which pre not pre-installed, for that
    we need package management. The word "package
    name" used in commands 101 to 109 is actully the
    command name.

143. vgrename → Used for changing volume group name.
    ex: vgrename + current group name + new group name.

144. find / -inum + inode number → shows the file path of
    specific inode number.

145. yum --enablerepo= (repoid) + install + packagename.
    Downloads the packages from yum repository of
    its packages are downloaded in it.

146. nmtui → Used for editing a new network connection(ip)

147. Firewall-cmd --list-services → shows enabled services
    in your systems firewall

148. Firewall-cmd --add-service=service name --permanent
    adds a service mentioned to firewall

149. Firewall-cmd --reload → Refreshes / updates the list of
    services.

150. firewall-cmd --remove-service = service name --permanent
    → Used for removing a selected service from firewall
    list

151. firewall-cmd --add-port=8080/tcp --permanent
    → Used for adding a changed port number to
    firewall list

152. firewall-cmd --add-forward-port=port=80:proto=tcp:
    toport=8080 --permanent.
    → Used for forwarding the port number

153. top → Shows live running processers and
    also refreshes it every 3 seconds automatic

154. pkill + process name → kills the process.

155. ifconfig → Shows all the networks and their ip.

156. getenforce → shows status/mode of selinux

157. setenforce → Used for setting/changing
    selinux modes. temporary.
    eg. setenforce permissive

158. chcon -t + content name + directory name
    → Used for changing the content name of
    a directory temporary.
    
    Commands Related to package management

159. restorecon -vFR + directory name
    → Used for restoring, the content name/type
    which was changed using chcon -t...

160. semanage fcontent -a -t httpd-sys_content_t /demo
    Syntax : semanage fcontent -a -t + content type + "/demo (/).?""
    Note: In place of /demo you will write directory name.
    This command is used for permanently chang-
    ing the content name/type. Also after running
    this command, the changes doesn't appear immediately.
    user will need to run "restorecon -vFR /demo"
    command to apply the changes.

161. semanage port -a -t http-cache_port_t -p tcp 2020
    Used for adding a port permanently in.
    httpd service.

162. rm * -> deletes all files in your present
    directory except hidden files.

163. rm .* -> Removes all hidden files

164. filename* -> all files are removed with mentioned
    filename

165. *.txt -> removes all files ending with .txt
    (suffix can be anything after *.)

166. echo "data" -> Inserts data in the file written in "".
    Syntax: echo "data" > filename
 
167. chown <username>:<groupname> <filename/dirname>
    to change user and group using single command
    eg: chown atul:grow file1

167. chown -R <username>:<groupname> <file/dirname>
    to change the permission for dir/sub-dir/files
    eg: chown -R atul:dexops demo(dir)
168. chown <username> <file/dir_name>
    to change owner of the file/dir
    eg: chown atul file1
169. chgrp <group-name> <file/dir_name>
    eg: chgrp aws file1

170. ls -ltd --> Shows foldername of file/directory
     eg: ls -ltd <directory name>

171. ls -lhr --> Shows all files in ascending order, newly created files will be shown at the bottom.