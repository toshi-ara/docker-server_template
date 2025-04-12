# docker-server_template

template of private web server with reverse proxy using docker


## Install

``` bash
git clone https://github.com/toshi-ara/docker-server_template.git
```


## Placement of contents

- Place the contents in html folder

```
.
├── README.md
├── default.conf
├── docker-compose.yml
└── html                  <==
```

## Run

``` bash
cd docker-server_template
docker compose up -d  # start
docker compose down   # stop
```

- access (IP address of host PC) by web browser



## Construction of servers

```
 [Host PC]
  ┌────────────────────────────────────┐
  │  ┌───────────────┐   ┌────────────┐│
--┼->│               │-->│            ││
──┼──┤ reverse proxy ├───┤ web server ││
  │80│    (nginx)    │ 80│  (apache2) ││
  │  └───────────────┘   └────────────┘│
  └────────────────────────────────────┘
```

