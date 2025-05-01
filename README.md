# Install Graylog Open in 5* minutes for free!

1. Find hardware or set up a VM with at least 16 GB memory. 4 or more processor 
cores would be nice, too. Our first pilot, which ran for about a year,  was a Dell Optiplex SFF PC with an i5-6500 and 16 GB of memory.

2. [Install Linux](https://ubuntu.com/tutorials/install-ubuntu-server) on it.

3. [Install and configure Graylog Open](https://go2docs.graylog.org/current/downloading_and_installing_graylog/ubuntu_installation.htm) on your new Linux server.

4. [Install NXLog Community Edition](https://docs.nxlog.co/userguide/deploy/windows.html) on your Domain Controllers. Start with installing on one DC and making sure it works well.

5. On your Graylog server, [add a new Graylog Input](https://go2docs.graylog.org/current/getting_in_log_data/setup_an_input.htm?tocpath=Get%20in%20Logs%7CInputs%7C_____1) for port `12201` (you can change this) for your Domain Controller logs.

6. Copy [my nxlog.conf](nxlog.conf) into `C:\Program Files\nxlog\conf`. Open Powershell and run `C:\Program Files\nxlog\nxlog.exe -f` to make sure there are no errors. If it's good, restart the nxlog process.

7. Check Graylog to ensure your logs start appearing. They should start showing up immediately.

\* This is almost certainly a lie.


## Useful Links

- [https://github.com/reighnman/Graylog_Content_Pack_Active_Directory_Auditing](https://github.com/reighnman/Graylog_Content_Pack_Active_Directory_Auditing)
- [https://graylog.org/post/critical-windows-event-ids-to-monitor/](https://graylog.org/post/critical-windows-event-ids-to-monitor/)
- [NSA Event Forwarding Guidance](https://github.com/nsacyber/Event-Forwarding-Guidance)