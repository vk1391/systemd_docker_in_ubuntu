Рабочий ubuntu c systemd
 - собрать докерфайл со следующими ключами:
`docker build -t ubuntu/systemd . `
 - запустить собранный образ со следущими ключами:
`docker run -d --name=systemd --security-opt seccomp=unconfined --tmpfs /tmp --tmpfs /run --tmpfs /run/lock -v /sys/fs/cgroup:/sys/fs/cgroup:ro <container_id>`