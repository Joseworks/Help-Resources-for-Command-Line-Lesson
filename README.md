# Help-Resources-for-Command-Line-Lesson


   - Please  be extremely careful if you decide to change or follow any of this instructions. Check with an Instructor if you are not sure about what you are doing!

  In Unix-like systems, multiple users can be categorized into groups. POSIX and conventional Unix file system permissions are organized into three classes, user, group, and others. The use of groups allows additional abilities to be delegated in an organized fashion, such as access to disks, printers, and other peripherals. This method, among others, also enables the superuser to delegate some administrative tasks to normal users, similar to the Administrators group on Microsoft Windows NT and its derivatives.

  A Group IDentifier, often abbreviated to GID, is a numeric value used to represent a specific group. The range of values for a GID varies amongst different systems; at the very least, a GID can be between 0 and 32,767, with one restriction: the login group for the superuser must have GID 0. This numeric value is used to refer to groups in the /etc/passwd and /etc/group files or their equivalents. Shadow password files and Network Information Service also refer to numeric GIDs. The group identifier is a necessary component of Unix file systems and processes.


  Supplementary groups
    In Unix systems, every user must be a member of at least one group, the primary group which is identified by the numeric GID of the user's entry in the group database, which can be viewed with the command getent passwd (usually stored in /etc/passwd or LDAP). This group is referred to as the primary group ID. A user may be listed as member of additional groups in the relevant entries in the group database, which can be viewed with getent group (usually stored in /etc/group or LDAP); the IDs of these groups are referred to as supplementary group IDs.


  Reserved ranges
    Many Linux systems reserve the GID number range 0 to 99 for statically allocated groups, and either 100−499 or 100−999 for groups dynamically allocated by the system in post-installation scripts. These ranges are often specified in /etc/login.defs, for useradd, groupadd and similar tools.

    Special values
    0: The superuser normally has a GID of zero (0).

  Personal groups
    Many system administrators allocate for each user also a personal primary group that has the same name as the user's login name, and often also has the same numeric GID as the user's UID. Such personal groups have no other members and make collaboration with other users in shared directories easier, by allowing users to habitually work with umask 0002. This way, newly created files can have by default write permissions enabled for group members, because this will normally only enable write access for members of the personal group, that is only for the file's owner. However, if a file is created in a shared directory that belongs to another group and has the setgid bit set, then the created file will automatically become writable to members of that directory's group as well.


  [How to find group membership in OS X](http://www.macissues.com/2015/11/20/how-to-find-group-membership-in-os-x/)
    Groups in OS X are special account entries that act as umbrellas under which user accounts may exist, allowing single adjustments of access permissions to immediately apply to numerous users. As a result, the use of groups when setting up a multi-user Mac can be exceptionally useful, but then again may also leave open security holes if not done correctly.

    Since groups are technically user account entries in the system’s directory that hold information about other user accounts, groups can be members of other groups, and thus form hierarchies. As a result, there are two types of groups that a user account is associated with in OS X. The first are those that are explicitly defined for a user, and the second are those where the user is given inferred membership based on the hierarchy of the group organization.



Displaying explicit groups
The main directory management utility in OS X is the “dscl” command, which can be used to search for the explicitly assigned groups for users in a couple of ways:

Within the dscl utility:

Open the terminal and enter “dscl”
At the prompt, enter the following command, changing USERNAME accordingly:


``` search /Local/Default/Groups GroupMembership USERNAME ```


Please follow the [link](http://www.macissues.com/2015/11/20/how-to-find-group-membership-in-os-x/) for the full explanation.


 # How to add user to a group from Mac OS X [command line?](http://superuser.com/questions/214004/how-to-add-user-to-a-group-from-mac-os-x-command-line)








# GUI approach
  [OS X El Capitan:Set up users on your Mac](https://support.apple.com/kb/PH21994?locale=en_US)


    # What on Earth is the “wheel” user in OS X?

    Mac OS X has roots in BSD UNIX, a.k.a. the UNIX that came out of UC Berkeley. They had a group of trusted people that could become superuser by using the su command. So they coded their UNIX to only allow people in this specific group to become superuser using su. They chose the groupname 'wheel', supposedly reference to other systems that had WHEEL, possibly a reference to being a "big wheel"

    big wheel
    Word Origin
    noun, Informal.
    1.
    an influential or important person:
    a big wheel in business.







