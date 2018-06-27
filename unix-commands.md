- Disable a service which starts automatically `sudo update-rc.d -f nginx disable`

- Space investigation:

	- Find top biggest directories under particular partition: `du -a /home/xxx | sort -n -r | head -n 5`

	- To display the above result in human readable format: `du -Sh /home/xxx | sort -rh | head -5`

	- Find Top File Sizes Only `find /home/xxx -type f -exec du -Sh {} + | sort -rh | head -n 5`

- Delete files older than x days `find ./$BK_FOLDER -mtime $KEEPING_DAYS -type f -delete`

- Find all find have modified time greater than date in `backup_date.txt` `find /mnt/disks/backup/dot_net/ftp/id_card/ -type f -newer backup_date.txt`

- Run composer with particular PHP version: `/opt/plesk/php/7.0/bin/php /usr/lib/plesk-9.0/composer.phar xxx`

- Alter files/folder permission:

	- `find /specific/directory -type [f|d] -exec setfacl -Rm u:unix_account:rwx {} \;`
	- `find /specific/directory -type [f|d] -exec chmod 644 {} \;`
