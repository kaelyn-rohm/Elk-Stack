### SSH Barrage
Start by logging into your jump-box.
Run: `ssh username@ip.of.web.vm`

You should receive an error:
 ```sysadmin@Jump-Box-Provisioner:~$ ssh sysadmin@10.0.0.5```
 ```sysadmin@10.0.0.5: Permission denied (publickey).```

This error was also logged and sent to Kibana.

Run the failed SSH command in a loop to generate failed login log entries.

Search through the logs in Kibana to locate your generated failed login attempts.
![SSH](Images/SSH_Barrage.png)

### Linux Stress
From your jump box, start up your Ansible container and attach to it.
SSH from your Ansible container to one of your WebVM's.

Run `sudo apt install stress` to install the stress program.
Run `sudo stress --cpu 1` and allow stress to run for a few minutes.

View the Metrics page for that VM in Kibana. 
![Stress CPU](Images/Stress_CPU.png)
![Stress Load](Images/Stress_Load.png)
