# Perintah cli Mysql

#### Membuat user, contoh user root dengan password 'secret' dan bisa diakses disemua client
```mysql
  CREATE USER 'root'@'%'IDENTIFIED BY 'secret';
```

#### Memberikan hak akses ke semua database terhadap user root
```mysql
  GRANT ALL PRIVILEGES ON *.* TO 'root'@'%';
```
