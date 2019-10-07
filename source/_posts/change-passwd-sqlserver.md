---
title: How to change sqlserver password in linux
date: 2019-10-07 10:18:52
tags: [linux,教程,sqlserver]
---

#### 1.stop sql-server

```
sudo systemctl stop mssql-server
```

#### 2. open dir

```
cd /opt/mssql/bin
```

#### 3.check the information

```
./mssql-conf -h
```

#### 4.change the password

```
./mssql-conf set-sa-password
```

#### 5.reboot sql-server

```
sudo systemctl start mssql-server
```

