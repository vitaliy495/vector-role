Vector role
=========

This role install [vector](https://vector.dev/docs/)

Role Variables
--------------

| Variable name | Default | Description |
|-----------------------|----------|-------------------------|
| vector_version  | "0.30.0" | Параметр, который определяет какой версии vector будет установлен |
| clickhouse_host  | 127.0.0.1 | Эмулятор хоста ClickHouse |


Dependencies
------------

В `inventory` должен быть хост `clickhouse-01`
```yaml
для тестирования на с реальным хостом поднятым хостом в playbook раскоментируем endpoint: http://{{ hostvars['clickhouse-01'].ansible_host }}:8123
для эмуляции хоста создана переменная clickhouse_host: 127.0.0.1
```


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - vector-role

License
-------

MIT

Author Information
------------------

Vitaliy Nekrasov
