# Install Graylog Open in 5* minutes for $Ø !

1. Find hardware or set up a VM with at least 16 GB memory. 4 or more processor 
cores would be nice, too. Our first pilot, which ran for about a year,  was a Dell Optiplex SFF PC with an i5-6500 and 16 GB of memory.

2. [Install Linux](https://ubuntu.com/tutorials/install-ubuntu-server) on it.

3. [Install NXLog Community Edition](https://docs.nxlog.co/userguide/deploy/windows.html) on your Domain Controllers. Start with installing on one DC and making sure it works well.

4. Copy [my nxlog.conf](nxlog.conf) into `C:\Program Files\nxlog\conf` and run nxlog.exe -f to make sure there are no errors. If it's good, restart the nxlog process.

5. Check Graylog to ensure your logs start appearing. They should start showing up immediately.

\* Almost certainly a lie.