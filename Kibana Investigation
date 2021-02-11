### SSH Barrage
Start by logging into your jump-box.
Run: `ssh username@ip.of.web.vm`

You should receive an error:
 `sysadmin@Jump-Box-Provisioner:~$ ssh sysadmin@10.0.0.5`
 `sysadmin@10.0.0.5: Permission denied (publickey).`

This error was also logged and sent to Kibana.

Run the failed SSH command in a loop to generate failed login log entries.

Search through the logs in Kibana to locate your generated failed login attempts.
![SSH](Images/SSH)
