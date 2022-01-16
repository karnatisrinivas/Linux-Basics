**Locations of Access Control Files:**
- /etc/passwd
- /etc/shadow
- /etc/group
<!-- -->
- `sudo adduser [username]` = Create a new user
- `sudo passwd [username]` = Change password of a user
- `su - [username]` = Login as username ('su' = short for substitute or switch user)
- `su -` = Login as root
<!-- -->
- `sudo groupadd [groupname]` = Create new group (System assigns next available GID)
- `sudo adduser [username]` = Switch to Insert Mode

**Note 2 different User/Group commands:**<br />
`adduser`, `addgroup`, `deluser`,  `delgroup` = interactive, more user friendly commands<br />
`useradd`, `groupadd`,  `userdel`,  `groupdel` = low-level utilities, more infos need provided by yourself

- `sudo usermod [OPTIONS] [username]` = Modify a user account
- `sudo usermod -g agile ram` = Assign 'agile' as the primary group for 'ram' user
- `sudo delgroup ram` = Removes group 'tom'
- `groups` = Display groups the current logged in user belongs to
- `groups [username]` = Display groups of the given username
- `sudo useradd -G dev nick` = Create 'nick' user and add nicole to 'dev' group (-G = secondary group, not primary)
- `sudo gpasswd -d nick dev` = Removes user 'nicole' from group 'devops'
