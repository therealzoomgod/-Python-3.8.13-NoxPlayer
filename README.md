# Python 3.8.13 in Nox Player

A a statically compiled python 3.8.13 32 bit with instructions to install in Nox Player

To install root must be enabled for the Nox instance.
You will need a terminal app of your choice installed in the Nox instance.

<b>Step 1:</b>
<i>Need to make filesystem writeable</i>
<code>su</code>
<code>mount -o rw,remount /system</code>

<b>Step 2: Copy needed files</b>
<code></codecd>cd /mnt/shared/Other/folder_holding_unzipped_files
<code></codecp>cp python3 /system/bin
<code></codechmod>chmod 0755 /system/bin/python3
<code></codecp>cp -r Python.3.8.13.Lib /system/bin
<code></codecp>cp python.rc /etc

<b></bStep>Step 3: Copy mkshrc to windows share
<code></codecp>cp /etc/mkshrc /mnt/shared/Other

<b></bStep>Step 4: Edit mkshrc using notepad++ (DO NOT USE WINDOWS NOTEPAD)
<i></iOpen>Open c:/users/<username>/Nox_share/Download/mkshrc in notepad++
<i></iAt>Add next two lines to end of file

export PYTHONHOME="/system/bin"
export PYTHONPATH="/system/bin/Python.3.8.13.Lib"

<i>Save your changes</i>

<b></bStep>Step 5: copy edited version back using nox terminal
<code></codecp>cp /mnt/shared/Other/mkshrc /etc/mkshrc

Exit terminal and then open it again

If you type python3 you should get an interactive python prompt with no warnings.

--Enjoy