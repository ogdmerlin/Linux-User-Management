# ALTSCHOOL(CLOUD ENGINEERING)

# Linux User/Group Assignment:

### Step 1: Create a user in your name:

Use(d) the command `useradd` to create a user. Then proceed(s) to use `useradd ogdmerlin`, to create a user in my name with the help of `sudo` command, an example is shown below:👇🏽

<img src=useradd.png>

### **Step 2**: Set an expiry of 2week for the user:

To set an expiry for the user `ogdmerlin` use `sudo usermod -e 2023-08-30 ogdmerlin`, this command set the expiry date for the user `ogdmerlin`. An example is shown below:👇🏽

<img src=expiry.png>

### Step 3: Prompt the user to change there password on every login:

To prompt the user to change their password on login, you can use the `passwd` command with the `-e` flag. The `-e` flag will expire the user's current password and force them to change it on the next login. For example, to prompt the user `ogdmerlin` to change their password on the next login, you would use the following command: 👇🏽

<img src=prompt.png>

### Step 4: Attach the user to a group called altschool:

_Meanwhile; If the group `'altschool'` does not exist on the system. You cannot add the user `ogdmerlin` to a group that does not exist. To fix this, you can do this using the `groupadd` command. For example, to create the group `altschool`, you would use the following command:_

<img src=group_add.png>

Once the group `altschool` has been created, you can then add the user `ogdmerlin` to the group. To attach the user `ogdmerlin` to a group called altschool, you can use the `usermod` command with the `-G` flag. Below is an example:👇🏽

<img src=group_mod.png>

This command will add the user `ogdmerlin` to the group `altschool`. The user will now have the same permissions as other users in the group `altschool`.

### Step 5: Allow altschool group to be able to run only cat command on `/etc/`:

To allow the altschool group to be able to run only the cat command on `/etc/`, you need to edit the `/etc/group file`. The `/etc/group` file is a text file that contains a list of all the _groups_ on the system, along with the members of each group and their permissions.

To edit the /etc/group file, you need to open it with a text editor. For example, to edit the `/etc/group` file using Vim/Vi, Using the below command:

<img src=cat_command.png>

Once the /etc/group file is open, you need to find the line that contains the group `altschool`, to allow the `altschool` group to be able to run only the `cat` command on `/etc/` you need to change the permissions for the group to only allow the cat command. You can do this by adding the following line to the end of the line.. an example is shown below: 👇🏽
<img src=Untitled.png>

### Step 6: Create another user so that this user doesn't have a home directory:

We can create a user without a home directory by using the `useradd` command we practiced from our first step then with the _`-M`_ flag. The -M flag tells the `useradd` command not to create a home directory for the user. For example, to create a user named _`"anon"`_ without a home directory, you would use the following command:

`sudo useradd -M anon`

<img src=anon.png>

This command will create a user named _"anon"_ without a home directory. The user will not be able to log in to the system, unless you specifically grant them permission to do so.
