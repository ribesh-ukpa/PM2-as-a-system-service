# PM2-as-a-system-service


1. Generate a startup script
      ```bash
      pm2 startup
      ```

2. Run the output of the command(sample)

     ```bash
     #sample
     sudo env PATH=$PATH:/usr/bin /usr/lib/node_modules/pm2/bin/pm2 startup systemd -u CMSRentalBux --hp /home/CMSRentalBux
     ```

3. Save the current process list
      ```bash
     pm2 save
      ```

4. Kill the existing PM2 Daemon:
     ```bash
     pm2 kill
     ```

5. Rest the failed systemd servie:
     ```bash
     sudo systemctl reset-failed pm2-$(whoami)
     ```

7. Start
     ```bash
     sudo systemctl  start pm2-$(whoami)
     ```

8. Status
      ```bash
      sudo systemctl status pm2-$(whoami)
      ```





