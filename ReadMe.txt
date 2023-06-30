I finaly find the solution.
the configuraton is located on cd /etc/systemd/system/
then open sudo nano frontail.service
on the line

ExecStart=/usr/bin/frontail --ui-highlight --ui-highlight-preset ./preset/openhab.json -t openhab -l 2000 -n 200 /var/log/openhab2/openhab.log /var/log/open$
you can edit all settings, the full list is here 331
but beware of using to much lines, it slow down the Browser and the Raspberry Pi.
In my Case i edit the -n 200 to -n 2000