# init_dockercompose

## An init.d style script for managing multiple docker compose instances

*Based on the work of samalba:* http://gist.github.com/samalba/8bc1f848b4fa2db6f12e

## Usage:

	# clone the repo to your server
    git clone https://github.com/rafdouglas/init_dockercompose.git init_dockercompose

	# show what you just cloned
    ls -la  init_dockercompose
    
    # copy the init script to /etc/init.d
    sudo cp init_dockercompose/docker_compose /etc/init.d
    
    # create/update the links in /etc/rc[0-5].d
    update-rc.d docker_compose defaults

	# edit the list of compose instances and copy it into the right directory:
    cp init_dockercompose/compose-list.txt_example init_dockercompose/compose-list.txt
    nano init_dockercompose/compose-list.txt
    sudo mkdir -p /etc/docker-compose/
    sudo cp init_dockercompose/compose-list.txt /etc/docker-compose/


## Invoking this script manually:

This will do a clean start/stop/reload/query status of your docker compose instances:

    /etc/init.d/docker_compose start|stop|reload|restart|status
