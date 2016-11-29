# init_dockercompose
/etc/init.d/docker_compose start/stop with multiple composes

based on the work of samalba:
gist.github.com/samalba/8bc1f848b4fa2db6f12e

Usage:
git clone rafdouglas/init_dockercompose init_dockercompose

cd init_dockercompose
sudo cp docker_compose /etc/init.d

update-rc.d docker_compose


invoking this script manually:
/etc/init.d/docker_compose start|stop|reload|restart
