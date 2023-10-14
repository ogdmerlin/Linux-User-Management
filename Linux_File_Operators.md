**_`# Basic File Operators In Bash Scripting`_**

`-a`, --access: Checks if the file exists and is accessible.

    if [[ -a my_file ]]; then
     echo "The file my_file exists and is readable."
    else
     echo "The file my_file does not exist or is not readable."
    fi

#

`-b`, --block-special: Checks if the file is a block special file.

    if [[ -b /dev/sda ]]; then
       echo "The file /dev/sda is a block special file."
    else
       echo "The file /dev/sda is not a block special file."
    fi

#

`-c`, --character-special: Checks if the file is a character special file.

    if [[ -c /dev/tty ]]; then
      echo "The file /dev/tty is a character special file."
    else
      echo "The file /dev/tty is not a character special file."
    fi

#

`-d`, --directory: Checks if the file is a directory.

    if [ -d mydirectory ]; then
      echo "mydirectory exists and is a directory"
    fi

#

`-e`, --exists: Checks if the file exists.

    if [ -e myfile.txt ]; then
      echo "myfile.txt exists"
    else
      echo "myfile.txt does not exist."
    fi

#

`-f`, --regular: Checks if the file is a regular file.

    if [[ -f my_file ]]; then
        echo "The file my_file is a regular file."
    else
        echo "The file my_file is not a regular file."
    fi

#

`-g`, --group-writable: Checks if the file is writable by the group.

    if [[ -g my_file ]]; then
        echo "The file my_file is writable by the group."
    else
        echo "The file my_file is not writable by the group."
    fi

#

`-k`, --sticky: Checks if the file has the sticky bit set.

    if [[ -k my_file ]]; then
        echo "The file my_file has the sticky bit set."
    else
        echo "The file my_file does not have the sticky bit set."
    fi

#

`-h` AND `-L`: Checks if the given file is a symbolic link.

    if [ -h /path/to/file ]; then
        echo "$(readlink /path/to/file)"
    fi

`-L`: Also Checks if the given file is a symbolic link.(same as `-h`)

    if [[ -L my_link ]]; then
        echo "The file my_link is a symbolic link."
    else
        echo "The file my_link is not a symbolic link."
    fi

#
