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
