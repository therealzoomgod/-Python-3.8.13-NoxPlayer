#  Python 3.8.13-NoxPlayer

Statically compiled python 3.8.13 32 bit for Nox Player

Note: To install root must be enabled for Nox instance.

Install using a terminal or your choice and open a console/local connection

Then:
su
mount -o rw,remount /system
cp python3 /system/bin
cp -r Python.3.8.13.Lib /system/bin
cp python.rc /etc

To finish install /etc/mkshrc needs edited 

From terminal in Nox copy to shared folder
cp /etc/mkshrc /mnt/shared/Other

Open c:/users/<username>/Nox_share/Download/mkshrc in notepad++
NOTE:  DO NOT USE WINDOWS NOTEPAD!

At end of file add these two lines:

export PYTHONHOME="/system/bin"
export PYTHONPATH="/system/bin/Python.3.8.13.Lib"

Now copy it back from in nox terminal
cp /mnt/shared/Other/mkshrc /etc/mkshrc

Exit terminal and then open it again

If you type python3 you should get an interactive python prompt with no warnings.

--Enjoy
