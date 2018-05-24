# PT-KILL
Show process PT-KILL :    ps aux | grep pt-kill\
Start PT-kill:            pt-kill

#The following command intends to kill queries which have execute time greater than 30s and save terminated queries to database.\
pt-kill --host=localhost --user=root --password=root \
--busy-time=30 --interval=5s \
--log-dsn=h=localhost,D=pt_kill,t=kill_log,P=3306,u=root,p=root \
--kill --daemonize --ignore-user=backup


# Mail commands
Show all current connection:\
dove who\
Reload service to stop connection:\
dove reload
