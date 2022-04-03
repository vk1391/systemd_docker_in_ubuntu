Рабочий centos c systemd
 - собрать докерфайл со следующими ключами:
`docker build --rm -t local/c7-systemd . `
 - запустить собранный образ со следущими ключами:
`docker run -ti -v /sys/fs/cgroup:/sys/fs/cgroup:ro -v /tmp/$(mktemp -d):/run -p 80:80 local/c7-systemd `