# Perintah cli Mysql

#### Membuat user, contoh user root dengan password 'secret' dan bisa diakses disemua client
```mysql
  CREATE USER 'root'@'%'IDENTIFIED BY 'secret';
```

#### Memberikan hak akses ke semua database terhadap user root
```mysql
  GRANT ALL PRIVILEGES ON *.* TO 'root'@'%';
  FLUSH PRIVILEGES;
```

#### Membuat user, contoh user contoh dengan password 'secret'
```mysql
  CREATE USER contoh IDENTIFIED BY 'secret';
```

#### Memberikan hak akses database db_contoh terhadap user contoh dengan password 'secret' dan bisa diakses disemua client
```mysql
  GRANT ALL PRIVILEGES ON db_contoh.* TO 'contoh'@'%' IDENTIFIED BY 'secret';
  FLUSH PRIVILEGES;
```

#### Format perintah untuk export database
```mysql
  mysqldump -u [username] -p [nama-database] > [nama-file.sql]
  mysqldump -u root -p kampus > 08-01-2020-kampus.sql
```

#### Format perintah untuk import database
```mysql
  mysql -u [username] -p [nama-database] < [nama-file.sql]
  mysql -u root -p kampus_baru < data-kampus-lama.sql
```
