# Python 3.8.13 in Nox Player

A a statically compiled python 3.8.13 32 bit with instructions to install in Nox Player

To install root must be enabled for the Nox instance.
You will need a terminal app of your choice installed in the Nox instance.

<b>Step 1:</b><i> Need to make filesystem writeable</i><br>
<code>su</code><br>
<code>mount -o rw,remount /system</code><br><br>

<b>Step 2:</b><i> Copy needed files</i><br>
<code>cd /mnt/shared/Other/folder_holding_unzipped_files</code><br>
<code>cp python3 /system/bin</code><br>
<code>chmod 0755 /system/bin/python3</code><br>
<code>cp -r Python.3.8.13.Lib /system/bin</code><br>
<code>cp python.rc /etc</code><br><br>

<b>Step 3:</b><i> Copy mkshrc to windows share</i><br>
<code>cp /etc/mkshrc /mnt/shared/Other</code><br><br>

<b>Step 4:</b><i> Edit mkshrc using notepad++</i> (DO NOT USE WINDOWS NOTEPAD)<br>
<i>Open c:/users/<username>/Nox_share/Download/mkshrc in notepad++</i><br>
<i>Add next two lines to end of file and save the changes</i><br><br>
<code>export PYTHONHOME="/system/bin"</code><br>
<code>export PYTHONPATH="/system/bin/Python.3.8.13.Lib"</code><br><br>

<b>Step 5:</b> <i>Copy edited version back using nox terminal</i><br>
<code>cp /mnt/shared/Other/mkshrc /etc/mkshrc</code><br><br>

Exit terminal and then open it again<br><br>

If you type python3 you should get an interactive python prompt with no warnings.<br><br>
If you get warnings then go back and check step 4

--Enjoy
