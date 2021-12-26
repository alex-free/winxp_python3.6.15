WinXP_Python-3.6 is the latest version of Python 3.6.x (3.6.15 as of 12/24/2021) and is compatible with Windows XP SP3 32-bit systems. 

WinXP_Python-3.6.15 requires the latest Cygwin for Windows XP SP3 to be installed, which is available at http://www.crouchingtigerhiddenfruitbat.org/cygwin/timemachine.html

Install all of the devel packages using the Cygwin Setup, and 'cd' into the winxp_python-3.6 source directory. Then:
	./configure
	make install

After doing so, you need to 'rebaseall' to fix some ugly warnings when using Python3.6.exe. To do so:

In the Cygwin Terminal, do: 
	find /usr/local -type f -name "*.dll" > /tmp/rebase-list

Rxit all cygwin programs and the cygwin terminal. Open cmd.exe and do:
	C:\cygwin\bin\ash.exe C:\cygwin\bin\rebaseall -T C:\cygwin\tmp\rebase-list
	del C:\cygwin\tmp\rebase-list